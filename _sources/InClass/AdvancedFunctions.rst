Advanced Functions Discussion Section
=====================================

.. activecode:: advanced_functions_1
    :language: python
    :autograde: unittest
    :hidecode:

    Define a function called ``double`` that accepts a list and returns a list where every item is.
    ~~~~
    def double(L):
        pass

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
            L = [1,2,3]
            self.assertEqual(double(L), [2,4,6], "Testing double with [1,2,3]")
            self.assertEqual(L, [1,2,3], "Testing that the original list was not mutated")
            self.assertEqual(double([]), [], "Testing double with an empty list")

    myTests().main()

.. activecode:: advanced_functions_2
    :language: python
    :autograde: unittest
    :hidecode:

    Define a function called ``mutating_double`` that accepts a list and **mutates** that list to double every item. (hint: iterate through every index using `range()` and assign each individual index). Your function should return ``None``

    ~~~~
    def mutating_double(L):
        pass

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
            L = [1,2,3]
            self.assertEqual(mutating_double(L), None, "Testing double with [1,2,3]")
            self.assertEqual(L, [2,4,6], "Testing that the original list was mutated")
            L2 = []
            self.assertEqual(mutating_double(L2), None, "Testing double with an empty list")
            self.assertEqual(L2, [], "Testing double with an empty list")

    myTests().main()

.. activecode:: advanced_functions_3
    :language: python
    :autograde: unittest
    :hidecode:

    Define a function called ``add_values`` whose input is two integers, whose default parameter values are the integers ``1`` and ``2`` . The function’s return value should be the two input integers added together.

    ~~~~

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
            self.assertEqual(add_values(3,5), 8, "3+5 == 8")
            self.assertEqual(add_values(-1,2), 1, "-1+2 == 1")
            self.assertEqual(add_values(), 3, "defaults are 1+2 == 3")
            self.assertEqual(add_values(10), 12, "testing with only second default used (10+2)")

    myTests().main()

.. activecode:: advanced_functions_4
    :language: python
    :autograde: unittest
    :hidecode:

    Define a function called ``smallest`` that takes a list of integers as input and returns the integer with the lowest value. Your code should have an optional argument named ``default`` that is returned if the list of integers is empty. If default is not specified, it should be ``0``

    ~~~~

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
            self.assertEqual(smallest([1,2,-10]), -10)
            self.assertEqual(smallest([]), 0)
            self.assertEqual(smallest([], True), True)
            self.assertEqual(smallest([], default=106), 106)
            self.assertEqual(smallest([5], default=106), 5)

    myTests().main()


.. activecode:: advanced_functions_5
    :language: python
    :autograde: unittest
    :hidecode:

    Use a ``lambda`` function to define ``myLambdaFunc`` to do the same thing as ``myFunc``.
    ~~~~

    def myFunc(x,y):
        return 2*x + y

    myLambdaFunc = # fill this in with a lambda function

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
            self.assertEqual(myLamdaFunc(2,3), myFunc(2,3))
			self.assertIn('lambda', self.getEditorText(), "Testing that you're using a lamda function")

    myTests().main()

.. activecode:: advanced_functions_6
    :language: python
    :autograde: unittest
    :hidecode:

    Define a function ``apply`` that accepts two arguments. The first argument is an integer and the second argument is a function. When called, ``apply`` should return the value of that function applied to that integer.
    ~~~~
    def apply(inp, func):
        pass

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
            self.assertEqual(apply(2, lambda x: x+1), 2+1)
            self.assertEqual(apply(2, lambda x: 199), 199)
            self.assertEqual(apply("hello", lambda x: x+"o"), "helloo")

    myTests().main()

.. activecode:: advanced_functions_7
    :language: python
    :autograde: unittest
    :hidecode:

    Define a function ``mean_mode`` that returns a three-item tuple for any list of integers:

    - the mean (arithmetic average) as a float
    - the mode (the most common value)

    You may use any strategy for writing your ``mean_mode`` function, including writing out two separate functions to compute the mean and mode individually.

    **Bonus**:
    Add the median to your code from above:

    - the median (the “middle” value of a sorted list)
        - if there’s an even number of items, average the middle two
        - if there’s an odd number of items, the one in the middle

    You can sort the list ``L`` by calling ``sorted(L)``
    ~~~~

    =====

    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):

        def testOne(self):
            self.assertEqual(mean_mode([1,2,2,3]), (2.0,2))
            self.assertEqual(mean_mode([0,3,3]), (2.0,3))

    myTests().main()
