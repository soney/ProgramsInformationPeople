..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

Week 3 Assessment 2
-------------------

**Check your understanding**

.. mchoice:: question3_2_1_1
   :answer_a: string
   :answer_b: integer
   :answer_c: float
   :answer_d: list
   :feedback_a: not quite, is it slicing or accessing an element?
   :feedback_b: what is happening in the assigment statement for ``m``?
   :feedback_c: what is happening in the assigment statement for ``m``?
   :feedback_d: correct, a slice returns a list no matter how large the slice.
   :correct: d
   :practice: T
   :topics: 

   What is the type of ``m``?
   .. sourcecode::python

   l = ['w', '7', 0, 9]
   m = l[1:2]

.. mchoice:: question3_2_1_2
   :answer_a: string
   :answer_b: integer
   :answer_c: float
   :answer_d: list
   :feedback_a: yes, the quotes around the number mean that this is a string.
   :feedback_b: not quite, look again at what is being extracted.
   :feedback_c: not quite, look again at what is being extracted.
   :feedback_d: not quite, is it slicing or accessing an element?
   :correct: a
   :practice: T
   :topics: 

   What is the type of ``m``?
   .. sourcecode::python

   l = ['w', '7', 0, 9]
   m = l[1]

.. mchoice:: question3_2_1_3
   :answer_a: string
   :answer_b: integer
   :answer_c: float
   :answer_d: list
   :feedback_a: not quite, think about what the result of .split() is.
   :feedback_b: not quite, look again at what types are present and what the result of .split() is.
   :feedback_c: not quite, look again at what types are present and what the result of .split() is.
   :feedback_d: yes, the .split() method returns a list.
   :correct: d
   :practice: T
   :topics: 

   What is the type of ``x``?
   .. sourcecode::python

   b = "My, what a lovely day"
   x = b.split(',')

.. mchoice:: question3_2_1_3
   :answer_a: string
   :answer_b: integer
   :answer_c: float
   :answer_d: list
   :feedback_a: yes, the string is split into a list, then joined back into a string, then split again, and finally joined back into a string.
   :feedback_b: not quite, look again at what types are present and what the result of .split() is.
   :feedback_c: not quite, look again at what types are present and what the result of .split() is.
   :feedback_d: not quite, think about what .split() and .join() return.
   :correct: a
   :practice: T
   :topics: 

   What is the type of ``a``?
   .. sourcecode::python

   b = "My, what a lovely day"
   x = b.split(',')
   z = "".join(x)
   y = z.split()
   a = "".join(y)


.. mchoice:: question3_2_1_4
   :answer_a: 
   :answer_b: 
   :answer_c: 
   :answer_d: 
   :feedback_a: 
   :feedback_b: 
   :feedback_c: 
   :feedback_d: 
   :correct: 
   :practice: T
   :topics: 

   Which of these is a correct reference diagram following an execution?

.. mchoice:: question3_2_1_2
   :answer_a: .pop()
   :answer_b: .insert()
   :answer_c: .count()
   :answer_d: .index()
   :feedback_a: pop removes and returns items (default is to remove and return the last item in the list) 
   :feedback_b: insert will add an item at whatever position is specified.
   :feedback_c: count returns the number of times something occurs in a list
   :feedback_d: yes, index will return the position of the first occurance of an item.
   :correct: d
   :practice: T
   :topics: 

   Which method would you use to figure out the position of an item in a list?

.. mchoice:: question3_2_1_2
   :answer_a: .insert()
   :answer_b: .pop()
   :answer_c: .append()
   :answer_d: .remove()
   :feedback_a: while you can use insert, it is not the best method to use because you need to specify that you want to stick the new item at the end.
   :feedback_b: pop removes an item from a list
   :feedback_c: yes, though you can use insert to do the same thing, you don't need to provide the position.
   :feedback_d: remove gets rid of the first occurance of any item that it is told, not add.
   :correct: c
   :practice: T
   :topics: 

   Which method best to use when adding an item to the end of a list?

.. activecode:: a_03_02_01
    :language: python
    :topics: Sequences/ListSlices

    **8.** Write code to add 'horse back riding' to the third position (english third) in the list ``sports``.
    ~~~~
    sports = ['cricket', 'football', 'volleyball', 'baseball', 'softball', 'track and field', 'curling', 'ping pong', 'hockey']


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

      def test_output(self):
        self.assertEqual(sports, ['cricket', 'football', 'horse back riding', 'volleyball', 'baseball', 'softball', 'track and field', 'curling', 'ping pong', 'hockey'], "Testing that sports is set correctly (Don't worry about actual and expected values).")

.. activecode:: a_03_02_02
    :language: python
    :topics: Sequences/ListSlices

    **9.** Write code to take 'London' out of the list ``trav_dest``.
    ~~~~
    trav_dest = ['Beirut', 'Milan', 'Pittsburgh', 'Buenos Aires', 'Nairobi', 'Kathmandu', 'Osaka', 'London', 'Melbourne']


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

      def test_output(self):
        self.assertEqual(trav_dest, ['Beirut', 'Milan', 'Pittsburgh', 'Buenos Aires', 'Nairobi', 'Kathmandu', 'Osaka', 'Melbourne'], "Testing that trav_dest is set correctly (Don't worry about actual and expected values).")


.. activecode:: a_03_02_03
    :language: python
    :topics: Sequences/ListSlices

    **10.** Write code to add 'Guadalajara' to the end of the list ``trav_dest`` using a list method.
    ~~~~
    trav_dest = ['Beirut', 'Milan', 'Pittsburgh', 'Buenos Aires', 'Nairobi', 'Kathmandu', 'Osaka', 'Melbourne']


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

      def test_output(self):
        self.assertEqual(trav_dest, ['Beirut', 'Milan', 'Pittsburgh', 'Buenos Aires', 'Nairobi', 'Kathmandu', 'Osaka', 'Melbourne', 'Guadalajara'], "Testing that trav_dest is set correctly (Don't worry about actual and expected values).")
        self.assertNotIn('+', self.getEditorText(), "Testing your code (Don't worry about actual and expected values).")

.. activecode:: a_03_02_04
    :language: python
    :topics: Sequences/ListSlices

    **11.** Write code to find the postion of the string "Tony" in the list ``awards`` and save that information in the variable ``pos``.
    ~~~~
    awards = ['Emmy', 'Tony', 'Academy', 'Grammy']


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

      def test_output(self):
        self.assertEqual(pos, 1, "Testing that pos is set correctly (Don't worry about actual and expected values).")

.. activecode:: a_03_02_05
    :language: python
    :topics: Sequences/ListSlices

    **12.** Write code to rearrage the strings in the list ``winners`` so that they are in alphabetical order from A to Z.
    ~~~~
    winners = ['Kazuo Ishiguro', 'Rainer Weiss', 'Youyou Tu', 'Malala Yousafzai', 'Alice Munro', 'Alvin E. Roth']


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

      def test_output(self):
        self.assertEqual(winners, ['Alice Munro', 'Alvin E. Roth', 'Kazuo Ishiguro', 'Malala Yousafzai', 'Rainer Weiss', 'Youyou Tu'], "Testing that winners is set correctly (Don't worry about actual and expected values).")       

.. activecode:: a_03_02_06
    :language: python
    :topics: Sequences/ListSlices

    **13.** Write code to switch the order of the ``winners`` list so that it is now Z to A. Assign this list to the variable ``z_winners``. 
    ~~~~
    winners = ['Alice Munro', 'Alvin E. Roth', 'Kazuo Ishiguro', 'Malala Yousafzai', 'Rainer Weiss', 'Youyou Tu']


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

      def test_output(self):
        self.assertEqual(z_winners, ['Youyou Tu','Rainer Weiss', 'Malala Yousafzai','Kazuo Ishiguro', 'Alvin E. Roth', 'Alice Munro'], "Testing that z_winners is set correctly (Don't worry about actual and expected values).")

.. activecode:: a_03_02_07
    :language: python
    :topics: Sequences/ListSlices

    **14.** Write code to determine how many 9's are in the list ``nums`` and assign that value to the variable ``how_many``. 
    ~~~~
    nums = [4, 2, 23.4, 9, 545, 9, 01, 234.001, 5, 49, 8, 9 , 34, 52, 1, -2, 9.0, 4]


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

      def test_output(self):
        self.assertEqual(how_many, 3, "Testing that how_many is set correctly (Don't worry about actual and expected values).")


.. activecode:: a_03_02_07
    :language: python
    :topics: Sequences/ListSlices

    **14.** Write code to get rid of the the second 8 so that here are only two 8's in the list nums. 
    ~~~~
    nums = [4, 2, 8, 23.4, 8, 9, 545, 9, 01, 234.001, 5, 49, 8, 9 , 34, 52, 1, -2, 9.0, 4]


    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

      def test_output(self):
        self.assertEqual(nums, [4, 2, 8, 23.4, 9, 545, 9, 01, 234.001, 5, 49, 8, 9 , 34, 52, 1, -2, 9.0, 4], "Testing that nums is set correctly (Don't worry about actual and expected values).")