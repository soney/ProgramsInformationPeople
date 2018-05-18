..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

Week 5 Assessment 2
-------------------

**Check your understanding**

.. mchoice:: question5_2_1_1
   :answer_a: 
   .. sourcecode:: python
   
   nums = [4, 5, 2, 93, 3, 5]
   s = 0
   for n in nums:
       s = s + 1

   :answer_b: 
   .. sourcecode:: python
   
   nums = [4, 5, 2, 93, 3, 5]
   s = 0
   for n in nums:
       s = n + n
   :answer_c: 
   .. sourcecode:: python
   
   nums = [4, 5, 2, 93, 3, 5]
   s = 0
   for n in nums:
       s = s + n
   :answer_d: none of the above would be appropriate for the problem.
   :feedback_a: this pattern will only count how many items are in the list, not provide the total accumulated value.
   :feedback_b: this would reset the value of s each time the for loop iterated, and so by the end s would be assigned the value of the last item in the list plus the last item in the list.
   :feedback_c: yes, this will solve the problem.
   :feedback_d: one of the patterns above is a correct way to solve the problem.
   :correct: c
   :practice: T
   :topics: 

   Given that we want to accumulate the total sum of a list of numbers, which of the following accumulator patterns would be appropriate?

.. mchoice:: question5_2_1_2
   :answer_a: 
   .. sourcecode:: python
   
   lst = ['plan', 'answer', 5, 9.29, 'order, items', [4]]
   s = 0
   for n in nums:
       s = s + n
   :answer_b: 
   .. sourcecode:: python
   
   lst = ['plan', 'answer', 5, 9.29, 'order, items', [4]]
   for n in nums:
       s = 0
       if type(n) == type("string"):
           s = s + 1
   :answer_c: 
   .. sourcecode:: python
   
   lst = ['plan', 'answer', 5, 9.29, 'order, items', [4]]
   s = ""
   for n in nums:
       s = s + n
   :answer_d: 
   .. sourcecode:: python
   
   lst = ['plan', 'answer', 5, 9.29, 'order, items', [4]]
   s = 0
   for n in nums:
       if type(n) == type("string"):
           s = s + 1
   :answer_e: 
   .. sourcecode:: python
   
   lst = ['plan', 'answer', 5, 9.29, 'order, items', [4]]
   for n in nums:
       s = ""
       if type(n) == type("string"):
           s = s + n
   :answer_f: none of the above would be appropriate for the problem. 
   :feedback_a: how does this solution know that the element of lst is a string and that s should be updated?
   :feedback_b: what happens to s each time the for loop iterates?
   :feedback_c: reread the prompt again, what do we want to accumulate?
   :feedback_d: yes, this will solve the problem.
   :feedback_e: reread the prompt again, what do we want to accumulate?
   :feedback_f: one of the patterns above is a correct way to solve the problem.
   :correct: d
   :practice: T
   :topics: 

   Given that we want to accumulate the total number of strings in the list, which of the following accumulator patterns would be appropriate?

.. mchoice:: question5_2_1_3
   :answer_a: sum
   :answer_b: x
   :answer_c: S
   :answer_d: total
   :answer_e: accum
   :answer_f: none of the above
   :feedback_a: no, though sum might be clear, it is also the name of a commonly used function in python, and so there can be issues if sum is used as an accumulator variable.
   :feedback_b: no, S is not a clear enough name to be used for an accumulator variable.
   :feedback_c: no, S is not a clear enough name to be used for an accumulator variable.
   :feedback_d: yes, total is a good name for accumulating numbers.
   :feedback_e: yes, accum is a good name. It's both short and easy to remember.
   :feedback_f: at least one of the answers above is a good name for an accumulator variable.
   :correct: d, e
   :practice: T
   :topics: 

   Which of these are good names for an accumulator variable? Select as many as apply.

.. mchoice:: question5_2_1_4
   :answer_a: item
   :answer_b: y
   :answer_c: elem
   :answer_d: z
   :answer_e: char
   :answer_f: none of the above
   :feedback_a: yes, item can be a good name to use as an iterator variable.
   :feedback_b: no, y is not likely to be a clear name for the iterator variable.
   :feedback_c: yes, elem can be a good name to use as an iterator variable, especially when iterating over lists.
   :feedback_d: no, z is not likely to be a clear name for the iterator variable.
   :feedback_e: yes, char can be a good name to use when iterating over a string, because the iterator variable would be assigned a character each time.
   :feedback_f: at least one of the answers above is a good name for an iterator variable.
   :correct: a, c, e
   :practice: T
   :topics: 

   Which of these are good names for an iterator variable? Select as many as apply.

.. mchoice:: question5_2_1_5
   :answer_a: num_lst
   :answer_b: p
   :answer_c: sentence
   :answer_d: names
   :answer_e: none of the above
   :feedback_a: yes, num_lst is good for a sequence variable if the value is actually a list of numbers.
   :feedback_b: no, p is not likely to be a clear name for the iterator variable.
   :feedback_c: yes, this is good to use if the for loop is iterating through a string.
   :feedback_d: yes, names is good, assuming that the for loop is iterating through actual names and not something unrelated to names.
   :feedback_e: at least one of the answers above is a good name for a sequence variable
   :correct: a, c, d
   :practice: T
   :topics: 

   Which of these are good names for a sequence variable? Select as many as apply.

.. mchoice:: question5_2_1_6
   :answer_a: accumulator variable: x | iterator variable: s | sequence variable: lst
   :answer_b: accumulator variable: total | iterator variable: s | sequence variable: lst
   :answer_c: accumulator variable: x | iterator variable: sentences | sequence variable: word_lst
   :answer_d: accumulator variable: total | iterator variable: sentences |sequence variable: word_lst
   :answer_e: none of the above
   :feedback_a: though lst may be a good name, x and s are not clear names for accumulator and iterator variables.
   :feedback_b: though total and lst may be good names, x is not a clear name for the iterator variable.
   :feedback_c: though sentences and word_lst are good names, x is not the best name for an accumulator variable.
   :feedback_d: yes, this combination of variable names is the most clear.
   :feedback_e: 
   :correct: 
   :practice: T
   :topics: 

   Given the following scenario, what are good names for the accumulator variable, iterator variable, and sequence variable? You are writing code that uses a list of sentences and accumulating the total number of sentences that have the word 'happy' in them.

