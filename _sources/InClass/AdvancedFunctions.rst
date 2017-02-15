Advanced Sequences Discussion Section
=====================================

.. activecode:: advanced_sequences_1
    :language: python
    :autograde: unittest
    :hidecode:

    Define a function called ``topThree`` that accepts a list of integers (``L``) and returns the three largest integers in that list sorted in descending order.
    ~~~~
    

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
            self.assertEqual(topThree([1,6,4,3,8]), [8,6,4], "Testing with [1,6,4,3,8]")
            self.assertEqual(topThree([1]), [1], "Testing with [1]")

    myTests().main()

.. activecode:: advanced_sequences_2
    :language: python
    :autograde: unittest
    :hidecode:

    Define a function called ``topThreeLen`` that accepts a list of strings (``S``) and returns the three longest strings, sorted from longest to shortest.

    ~~~~
    

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
            self.assertEqual(topThreeLen(["4", "first", "3r", "2nd"]), ["first","2nd","3r"], 'Testing with ["4", "first", "3r", "2nd"]')
            self.assertEqual(topThreeLen(["ABC"]), ["ABC"], "Testing with a one-element list")

    myTests().main()