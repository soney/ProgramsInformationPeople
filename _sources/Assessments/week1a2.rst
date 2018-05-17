..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

Week 1 Assessment 2
-------------------

**Check your understanding**

.. activecode:: ps_01_02
    :include: addl_functions
    :language: python
    :autograde: unittest
    :topics: SimplePythonData/FunctionCalls

    **2.** There is a function we are providing in for you in this problem set called ``square``. It takes one integer and returns the square of that integer value. Write code to assign a variable called ``xyz`` the value ``5*5`` (five squared). Use the square function, rather than just multiplying with ``*``.
    ~~~~
    xyz = ""

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
            self.assertEqual(type(xyz), type(3), "Checking type of xyz")
            self.assertEqual(xyz, 25, "Checking if xyz is 25")
            self.assertIn('square', self.getEditorText(), "Testing that 'square' is in your code. (Don't worry about Actual and Expected Values.)")

    myTests().main()

.. activecode:: ps_01_01
    :language: python
    :autograde: unittest
    :practice: T
    :topics: Sequences/SplitandJoin

    **1.** Write code to assign the number of *characters* in the string ``rv`` to a variable ``num_chars``.
    ~~~~
    rv = """Once upon a midnight dreary, while I pondered, weak and weary,
        Over many a quaint and curious volume of forgotten lore,
        While I nodded, nearly napping, suddenly there came a tapping,
        As of some one gently rapping, rapping at my chamber door.
        'Tis some visitor, I muttered, tapping at my chamber door;
        Only this and nothing more."""

    # Write your code here!

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
           self.assertEqual(num_chars, len(rv), "Testing that num_chars has been set to the length of rv")

    myTests().main()


.. mchoice:: question1_1_1_3
   :answer_a: a = len("hello worldwelcome!")
   :answer_b: a = 19
   :answer_c: a = 11 + 8
   :answer_d: a = len(z) + len(y)
   :answer_e: a = len("hello world") + len("welcome!")
   :answer_f: none of the above are hardcoding.
   :feedback_a: Though we are using the ``len`` function here, we are hardcoding what len should return the length of. We are not referencing ``z`` or ``y``
   :feedback_b: This is hardcoding, we are writing in the value without referencing ``z`` or ``y``
   :feedback_c: This is hardcoding, we are writing in the value without referencing ``z`` or ``y``
   :feedback_d: 
   :feedback_e: Though we are using the ``len`` function here, we are hardcoding what len should return the length of each time we call ``len``. We are not referencing ``z`` or ``y``
   :feedback_f: Incorrect, at least one of these solutions is considered hardcoding. Take another look.
   :correct: a,b,c,e
   :practice: T
   :topics: 

   The code below initializes two variables, ``z`` and ``y``. We want assign the number of characters in ``z`` and in ``y`` to the variable ``a``. Which of the following solutions, if any, would be considered hard coding?
   
   .. sourcecode:: python

    z = "hello world"
    y = "welcome!"


.. activecode:: addl_functions
    :language: python
    :nopre:
    :hidecode:

    (This is not a problem set question) The code below defines functions used by several questions. Do not modify them, but feel free to take a look.

    ~~~~

    def square(num):
        return num**2

