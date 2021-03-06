..  Copyright (C)  Paul Resnick.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

Generating Request URLs
=======================

In a REST API, the client or application program-- the kind of program you will be writing-- makes an HTTP request 
that includes information about what kind of request it is making. Web sites are free to define whatever format 
they want for how the request should be formatted. This chapter covers a particularly common and particularly 
simple format, where the request information is encoded right in the URL. This is convenient, because if something 
goes wrong, we can debug by copying the URL into a browser and see what happens when it tries to visit that URL.

In this format, the URL has a standard structure:

* the base URL
* a ``?`` character
* one or more key-value pairs, formatted as ``key=value`` pairs and separated by the ``&`` character.

For example, consider the URL ``https://itunes.apple.com/search?term=Ann+Arbor&entity=podcast``. 
Try copying that URL into a browser. It data about podcasts posted from Ann Arbor, MI. Depending on your browser, 
it may put the contents into a file attachment that you have to open up to see the contents.

Let's pull apart that URL. In this case, the FAA uses a slight variation on the basic structure described above.

* the base URL is ``https://itunes.apple.com/search``
* a ``?`` character
* key=value pairs. In this case, there are two pairs. The keys are ``term`` and ``entity``.
   
.. image:: Figures/parameterformat.png

All those parts are concatenated together to form the full URL.

.. image:: Figures/urlstructure.png

Note that in the search term Ann Arbor, the space had to be "encoded" as ``+``. More on that below.

Encoding URL Parameters
-----------------------
      
Here's another URL that has a similar format. ``https://www.google.com/search?q=%22violins+and+guitars%22&tbm=isch``. It's a search on Google for images that match the string "violins and guitars". It's not actually based on a REST 
API, because the contents that come back are meant to be displayed in a browser. But the URL has the same structure 
we have been exploring above and introduces the idea of "encoding" URL parameters.

* The base URL is ``https://www.google.com/search``
* ``?``
* Two key=value parameters, separated by ``&``
   * ``q=%22violins+and+guitars%22`` says that the query to search for is "violins and guitars".
   *  ``tbm=isch`` says to go to the tab for image search

Now why is ``"violins and guitars"`` represented in the URL as ``%22violins+and+guitars%22``? The answer is that 
some characters are not safe to include, as is, in URLs. For example, a URL path is not allowed to include the double
-quote character. It also can't include a : or / or a space. Whenever we want to include one of those characters in 
a URL, we have to *encode* them with other characters. A space is encoded as ``+``. ``"`` is encoded as ``%22``. 
``:`` would be encoded as ``%3A``. And so on.  

Using requests.get to encode URL parameters
-------------------------------------------

Fortunately, when you want to pass information as a URL parameter value, you don't have to remember all the 
substitutions that are required to encode special characters. Instead, that capability is built into the requests 
module.

The get function in the requests module takes an optional parameter called ``params``. If a value is specified for 
that parameter, it should be a dictionary. The keys and values in that dictionary are used to append something to 
the URL that is requested from the remote site. 

For example, in the following, the base url is https://google.com/search. A dictionary with two parameters is 
passed. Thus, the whole url is that base url, plus a question mark, "?", plus a "q=..." and a "tbm=..." separated 
by an "&". In other words, the final url that is visited is ``https://www.google.com/search?q=%22violins+and+guitars%22&tbm=isch``. Actually, because dictionary keys are unordered in python, the 
final url might sometimes have the encoded key-value pairs in the other order: ``https://www.google.com/search?tbm=isch&q=%22violins+and+guitars%22``. Fortunately, most websites that accept URL parameters in this 
form will accept the key-value pairs in any order.

.. sourcecode:: python

    d = {'q': 'violins and guitars', 'tbm': 'isch'}
    results = requests.get("https://google.com/search", params=d)
    print(results.url)

Below are more examples of urls, outlining the base part of the url - which would be the first argument when 
calling ``request.get()`` - and the parameters - which would be written as a dictionary and passed into the params 
argument when calling ``request.get()``.

.. image:: Figures/urlexamples.png

.. note:: 

    If you're ever unsure exactly what url has been produced when calling requests.get and passing a value for params, you can access the .url attribute of the object that is returned. This will be a helpful debugging strategy. You can take that url and plug it into a browser and see what results come back! We will talk about this more in the next section, on debugging calls to ``requests.get()`` when they don't do exactly what you expect.

**Check your understanding**

.. mchoice:: restapis_1
   :practice: T
   :topics: RESTAPIs/RequestURLs
   :answer_a: requests.get("http://bar.com/goodstuff", '?", {'greet': 'hi there'}, '&', {'frosted':'no'})
   :answer_b: requests.get("http://bar.com/", params = {'goodstuff':'?', 'greet':'hi there', 'frosted':'no'})
   :answer_c: requests.get("http://bar.com/goodstuff", params = ['greet', 'hi', 'there', 'frosted', 'no'])
   :answer_d: requests.get("http://bar.com/goodstuff", params = {'greet': 'hi there', 'frosted':'no'})
   :feedback_a: The ? and the & are added automatically.
   :feedback_b: goodstuff is part of the base url, not the query params
   :feedback_c: The value of params should be a dictionary, not a list
   :feedback_d: The ? and & are added automatically, and the space in hi there is automatically encoded as %3A.
   :correct: d

   How would you request the URL ``http://bar.com/goodstuff?greet=hi+there&frosted=no`` using the requests module?
