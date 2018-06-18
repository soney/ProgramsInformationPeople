..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

Week 3 Assessment 1
-------------------

**Check your understanding**

.. mchoice:: question3_1_1_1
   :answer_a: I.
   :answer_b: II.
   :answer_c: Neither is the correct reference diagram.
   :feedback_a: Yes, when we are using the remove method, we are just editing the existing list, not making a new copy.
   :feedback_b: When we use the remove method, we just edit the existing list. We do not make a new copy that does not include the removed object.
   :feedback_c: One of the diagrams is correct - look again at what is happening to lst.
   :correct: a
   :practice: T
   :topics: 

   Which of these is a correct reference diagram following the execution of the following code?

   .. sourcecode:: python
   
    lst = ['mercury', 'venus', 'earth', 'mars', 'jupiter', 'saturn', 'uranus', 'neptune', 'pluto']
    lst.remove('pluto')
    first_three = lst[:2]

   I. 

   .. image:: Figures/week3a1_1.png
      :alt: First Potential Solution

   II. 

   .. image:: Figures/week3a1_2.png
      :alt: Second Potential Solution

.. mchoice:: question3_1_1_2
   :answer_a: ['travel', 'lights', 'moon']
   :answer_b: ['world', 'travel', 'lights']
   :answer_c: ['travel', 'lights']
   :answer_d: ['world', 'travel']
   :feedback_a: When we take a slice of something, it is inclusive of the first number and exclusive of the second.
   :feedback_b: When we take a slice of something, it is inclusive of the first number and exclusive of the second. Additionally, Python is a zero-index based language.
   :feedback_c: Yes, python is a zero-index based language and slices are inclusive of the first number and exclusive of the second.
   :feedback_d: Python is a zero-index based language.
   :correct: c 
   :practice: T
   :topics: 

   What will the output be for the following code?
   
   .. sourcecode:: python
   
    ls = ['run', 'world', 'travel', 'lights', 'moon', 'baseball', 'sea']
    new = ls[2:4]
    print(new)

.. mchoice:: question3_1_1_3
   :answer_a: zpzpzpzpzp
   :answer_b: zzzzzppppp
   :answer_c: pzpzpzpzpz
   :answer_d: pppppzzzzz
   :answer_e: None of the above, an error will occur.
   :feedback_a: The order of concatenation matters.
   :feedback_b: Think about the order that the program is executed in, what occurs first?
   :feedback_c: Yes, because let_two was put before let, c has "pz" and then that is repeated five times.
   :feedback_d: Think about the order that the program is executed in, what occurs first?
   :feedback_e: This is correct syntax and no errors will occur.
   :correct: c
   :practice: T
   :topics: 

   What will the output be for the following code?
  
   .. sourcecode:: python

    let = "z"
    let_two = "p"
    c = let_two + let
    m = c*5
    print(m)

.. activecode:: a_03_01_01
    :language: python
    :topics: Sequences/ListSlices

    **4.** Write a program that extracts the last three items in the list ``sports`` and assigns it to the variable ``last``. Make sure to write your code so that it works no matter how many items are in the list.
    ~~~~
    sports = ['cricket', 'football', 'volleyball', 'baseball', 'softball', 'track and field', 'curling', 'ping pong', 'hockey']


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

      def test_output(self):
        self.assertEqual(last, ['curling', 'ping pong', 'hockey'], "Testing that the value of last is the last three items in sports.")
        self.assertNotIn("[6:]", self.getEditorText(), "Testing that your code would work no matter how many items. (Don't worry about actual and expected values).")
        

    myTests().main()

.. activecode:: a_03_01_02
    :language: python
    :topics: 

    **5.** Write code that combines the following variables so that the sentence "You are doing a great job, keep it up!" is assigned to the variable ``message``. Do not edit the values assigned to ``by``, ``az``, ``io``, or ``qy``.
    ~~~~
    by = "You are"
    az = "doing a great "
    io = "job"
    qy = "keep it up!"


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

      def test_output(self):
        self.assertEqual(by, 'You are', "Testing original variables.")
        self.assertEqual(az, 'doing a great ', "Testing original variables.")
        self.assertEqual(io, 'job', "Testing original variables.")
        self.assertEqual(qy, 'keep it up!', "Testing original variables.")
        self.assertEqual(message, 'You are doing a great job, keep it up!', "Testing that the value of message is what was expected.")
        self.assertNotIn("You are doing a great job, keep it up!", self.getEditorText(), "Testing for hardcoding (Don't worry about actual and expected values).")
        

    myTests().main()