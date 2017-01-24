:orphan:

Problem Set 4 (due midnight Feb 5)
==================================

..  Copyright (C) Paul Resnick.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".


.. assignment::
  :name: PS4
  :assignment_type: problem_set
  :questions: ps_4_1 5, ps_4_2 5, ps_4_3 5, ps_4_4 5, ps_4_5 5, ps_3_6 5, ps_4_7 5, ps_4_8 5, ps_4_9 5, ps_4_10 5
  :deadline: 2017-02-06 04:00
  :points: 50
  :autograde: unittest

  .. activecode:: ps_4_1
         :language: python

         **1.** Below is an empty dictionary saved in the variable ``nums``, and a list saved in the variable ``num_words``. Use iteration and dictionary mechanics to add each element of ``num_words`` as a key in the dictionary ``nums``. Each key should have the value ``0``. The dictionary should end up looking something like this when you print it out (remember, you can't be sure of the order): ``{"two":0,"three":0,"four":0,"eight":0,"seventeen":0,"not_a_number":0}``
         ~~~~
         nums = {}
         num_words = ["two","three","four","seventeen","eight","not_a_number"]
         # Write your code here.

         =====

         from unittest.gui import TestCaseGui

         class myTests(TestCaseGui):

            def testOne(self):
               self.assertEqual(nums["two"], 0, "Testing that the key 'two' has been assigned the value of 0.")
               self.assertEqual(type(nums["seventeen"]), type(3), "Testing that the key 'seventeen' has been assigned a value whose type is an integer.")
               self.assertEqual(sorted(nums), sorted({"two": 0, "three": 0, "four": 0, "eight": 0, "seventeen": 0, "not_a_number": 0}), "Testing that the contents of nums is accurate.")

            def testOneA(self):
               self.assertIn('for', self.getEditorText(), "Testing your code (Don't worry about actual and expected values).")

         myTests().main()

  .. activecode:: ps_4_2
         :language: python

         **2.** Given the string ``s`` in the code below, write code to figure out what the most common LETTER in the string is and assign that to the variable ``common_letter``. (Do not hard-code the right answer.) Hint: dictionary mechanics will be useful here.
         ~~~~
         s = """
           Peter Piper picked a peck of pickled peppers;
          A peck of pickled peppers Peter Piper picked;
          If Peter Piper picked a peck of pickled peppers,
          Where's the peck of pickled peppers Peter Piper picked?
          """

         # Write your code here.

         =====

         from unittest.gui import TestCaseGui

         class myTests(TestCaseGui):

            def testOne(self):
               self.assertEqual(common_letter, 'p', "testing whether common_letter is set correctly")

            def testOneA(self):
               self.assertIn('for', self.getEditorText(), "Testing your code (Don't worry about actual and expected values).")

         myTests().main()

  .. activecode:: ps_4_3
         :language: python

         **3.** Given the string ``s`` in the code below, write code to figure out what the most common WORD in the string is and assign that to the variable ``abc``. (Do not hard-code the right answer.) Hint: dictionary mechanics will be useful here.
         ~~~~
         s = "Number of slams in an old screen door depends upon how loud you shut it, the count of slices in a bread depends how thin you cut it, and amount 'o good inside a day depends on how well you live 'em. All depends, all depends, all depends on what's around ya."

         # Write your code here.

         =====

         from unittest.gui import TestCaseGui

         class myTests(TestCaseGui):

            def testOne(self):
               self.assertEqual(abc, 'depends', "testing whether abc is set correctly")

            def testOneA(self):
               self.assertIn('for', self.getEditorText(), "Testing your code (Don't worry about actual and expected values).")

         myTests().main()

  .. activecode:: ps_4_4
         :language: python

         **4.** Given the string ``sentence`` in the code below, write code to figure out what the longest word is and assign that to the variable ``longest_word``. (Do not hard-code the right answer.)
         ~~~~
         sentence = "singing in the rain and playing in the rain are two entirely different situations but both can be fun"

         # Write your code here.

         =====

         from unittest.gui import TestCaseGui

         class myTests(TestCaseGui):

            def testOne(self):
               self.assertEqual(longest_word, 'situations', "testing whether longest_word is set correctly")

            def testOneA(self):
               self.assertIn('for', self.getEditorText(), "Testing your code (Don't worry about actual and expected values).")

         myTests().main()

  .. activecode:: ps_4_5
         :language: python

         **5.** Like the above problem, you are given the string ``sentence`` in the code below. However, this time, find the longest word THAT DOES NOT CONTAIN the letter "i" and set ``longest_no_vowels`` to that word. (Do not hard-code the right answer.)
         ~~~~
         sentence = "singing in the rain and playing in the rain are two entirely different situations but both can be fun"

         # Write your code here.

         =====

         from unittest.gui import TestCaseGui

         class myTests(TestCaseGui):

            def testOne(self):
               self.assertEqual(longest_no_vowels, 'both', "testing whether longest_no_vowels is set correctly")

            def testOneA(self):
               self.assertIn('for', self.getEditorText(), "Testing your code (Don't worry about actual and expected values).")

         myTests().main()

  .. activecode:: ps_4_6
         :language: python

         **6.** Write code that will count the number of vowels in the sentence ``s`` and assign the result to the variable ``num_vowels``. For this problem, vowels are only a, e, i, o, and u. Hint: use the ``in`` operator with ``vowels``.
         ~~~~
         s = "singing in the rain and playing in the rain are two entirely different situations but both can be fun"
         vowels = ['a','e','i','o','u']

         # Write your code here.

         =====

         from unittest.gui import TestCaseGui

         class myTests(TestCaseGui):

            def testOne(self):
               self.assertEqual(num_vowels, 'both', "testing whether longest_word is set correctly")

            def testOneA(self):
               self.assertIn('for', self.getEditorText(), "Testing your code (Don't worry about actual and expected values).")

         myTests().main()

  .. activecode:: ps_4_7
         :language: python

         **7.** Write code that will determine the most common vowel in ``s`` is and assign the result to the variable ``common_vowel``. Use dictionary accumulation and do not hard code the answer.
         ~~~~
         s = "singing in the rain and playing in the rain are two entirely different situations but both can be fun"
         vowels = ['a','e','i','o','u']

         # Write your code here.

         =====

         from unittest.gui import TestCaseGui

         class myTests(TestCaseGui):

            def testOne(self):
               self.assertEqual(num_vowels, 'both', "testing whether longest_word is set correctly")

            def testOneA(self):
               self.assertIn('for', self.getEditorText(), "Testing your code (Don't worry about actual and expected values).")

         myTests().main()

  .. activecode:: ps_4_8
         :language: python

         **8.** Write code that will create two dictionaries that map years to temperatures. In both dictionaries, the keys should be integers dictionary where the keys are years and  Write code that will determine the most common vowel in ``s`` is and assign the result to the variable ``common_vowel``. Use dictionary accumulation and do not hard code the answer.
         ~~~~
        # COLUMNS:
        # 0: year
        # 1: lowest temperature  (F)
        # 2: highest temperature (F)
         temp_data = """
            2016,   6, 51
            2015,  -3, 41
            2014, -14, 43
            2013,  -3, 60
            2012,   2, 55
            2011,   1, 52
            2010,   3, 47
            2009, -10, 39
            2008,   3, 62
            2007,   5, 50
            2006,  18, 53
            2005,  -3, 56
            2004,  -6, 55
            2003,  -5, 47
            2002,  11, 55
            2001,   1, 43
            2000,  -2, 56
            """
         s = "singing in the rain and playing in the rain are two entirely different situations but both can be fun"
         vowels = ['a','e','i','o','u']

         # Write your code here.

         =====

         from unittest.gui import TestCaseGui

         class myTests(TestCaseGui):

            def testOne(self):
               self.assertEqual(num_vowels, 'both', "testing whether longest_word is set correctly")

            def testOneA(self):
               self.assertIn('for', self.getEditorText(), "Testing your code (Don't worry about actual and expected values).")

         myTests().main()

  .. activecode:: ps_4_9
         :language: python

         **9.** Write code that will find the year that has the highest total precipitation PLUS snowfall. Do not hard code your answer.
         ~~~~
        # COLUMNS:
        # 0: year
        # 1: lowest temperature  (F)
        # 2: highest temperature (F)
         temp_data = """
            2016,   6, 51
            2015,  -3, 41
            2014, -14, 43
            2013,  -3, 60
            2012,   2, 55
            2011,   1, 52
            2010,   3, 47
            2009, -10, 39
            2008,   3, 62
            2007,   5, 50
            2006,  18, 53
            2005,  -3, 56
            2004,  -6, 55
            2003,  -5, 47
            2002,  11, 55
            2001,   1, 43
            2000,  -2, 56
            """

         # Write your code here.

         =====

         from unittest.gui import TestCaseGui

         class myTests(TestCaseGui):

            def testOne(self):
               self.assertEqual(num_vowels, 'both', "testing whether longest_word is set correctly")

            def testOneA(self):
               self.assertIn('for', self.getEditorText(), "Testing your code (Don't worry about actual and expected values).")

         myTests().main()

  .. activecode:: ps_4_10
         :language: python

         **10.** Write code that will find the year that has the highest total precipitation PLUS snowfall. Do not hard code your answer.
         ~~~~
          # COLUMNS:
          #  0: year
          #  1: lowest temperature (F)
          #  2: highest temperature (F)
          #  3: warmest minimum temperature (F)
          #  4: coldest maximum temperature (F)
          #  5: average minimum temperature (F)
          #  6: average maximum temperature (F)
          #  7: mean temperature (F)
          #  8: total precipitation (in)
          #  9: total snowfall (in)
          # 10: max 24hr precipitation
          # 11: max 24hr snowfall

          temp_data = """
            2016,   6, 51, 36, 15, 19.8, 33.6, 26.7, 1.80, 12.20, 0.51, 3.20
            2015,  -3, 41, 33,  6, 14.6, 28.2, 21.4, 1.81, 15.60, 0.52, 2.90
            2014, -14, 43, 34,  4,  9.3, 24.7, 17.0, 3.48, 37.80, 0.56, 5.60
            2013,  -3, 60, 49, 11, 21.1, 36.3, 28.7, 3.81, 15.60, 0.73, 4.50
            2012,   2, 55, 36, 16, 23.3, 37.1, 30.2, 3.06, 13.90, 0.91, 2.20
            2011,   1, 52, 49, 16, 16.1, 28.2, 22.1, 2.07, 19.80, 0.41, 4.00
            2010,   3, 47, 33, 19, 18.9, 30.3, 24.6, 1.10, 10.50, 0.26, 2.80
            2009, -10, 39, 26,  9, 10.8, 24.9, 17.9, 2.16, 27.00, 0.50, 6.60
            2008,   3, 62, 51, 14, 21.3, 34.7, 28.0, 4.26, 22.70, 1.20, 11.40
            2007,   5, 50, 43, 22, 23.3, 35.0, 29.1, 4.31, 10.30, 1.00, 2.00
            2006,  18, 53, 41, 30, 29.4, 40.5, 34.9, 4.32,  8.40, 0.87, 4.70
            2005,  -3, 56, 33, 14, 16.0, 31.4, 23.7, 4.46, 29.10, 0.72, 9.30
            2004,  -6, 55, 41, 13, 11.6, 26.3, 19.0, 2.22, 23.40, 0.45, 4.50
            2003,  -5, 47, 36, 17, 13.9, 26.5, 20.2, 0.93, 13.80, 0.17, 2.10
            2002,  11, 55, 38, 27, 25.5, 39.3, 32.4, 3.41, 25.40, 1.57, 7.60
            2001,   1, 43, 33, 22, 20.3, 32.0, 26.1, 1.32,  6.70, 0.43, 2.20
            2000,  -2, 56, 37, 14, 16.1, 32.2, 24.1, 1.96, 16.10, 0.33, 4.90
          """

         # Write your code here.

         =====

         from unittest.gui import TestCaseGui

         class myTests(TestCaseGui):

            def testOne(self):
               self.assertEqual(num_vowels, 'both', "testing whether longest_word is set correctly")

            def testOneA(self):
               self.assertIn('for', self.getEditorText(), "Testing your code (Don't worry about actual and expected values).")

         myTests().main()