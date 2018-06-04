..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

The Range Function
==================

Sometimes we want to iterate for a certain number of times, not just to iterate through a string. 
For example, say that you want to print out "Hello, friend!" eight different times. 
Sure, you can write ``print("Hello, friend!")`` on eight different lines, but that's tedious. 
Imagine you had to do that for each of your friends. 
Maybe you don't find it a bother because it's for your friends, but that might end up being a lot of work. 
Thankfully, there's a handy function in python to solve this kind of problem.

The ``range`` function is a built-in python function, much like ``print``. The ``range`` function takes at least one input - which should be an integer - and returns a list as long as your input.
While you can provide two inputs, we will focus on using range with just one input. With one input, range will start at zero and go up to - but not include - the input.

One important thing to know about the range function in python3 is that if we want to use it outside of iteration, we have to cast it as a list using ``list()``. Inside the textbook you'll notice that ``range`` works with or without casting it as a list but it is best for you to try and get into the habit of casting it as a list.

Below we can see how ``range`` is used in different circumstances. 
The safest way to use the range function is to always cast it as a list, though it is not necessary in every case. 
Try changing the code to see what it's like to use range!


.. activecode:: chap_09_range_01

   z = range(3)
   print(list(z))

   for n in z:
       print(n)
       # this is what happens when we don't cast the range function as a list.
       print(z)


Now with the range function we can greet our eight friends!

.. activecode:: chap_09_range_02

   for _ in range(8):
       print("Hello, friend!")








