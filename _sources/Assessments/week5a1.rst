..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

Week 5 Assignment 1
-------------------

**Check your understanding**

.. mchoice:: question5_1_1_1
   :answer_a: byzo
   :answer_b: x
   :answer_c: z
   :answer_d: c
   :feedback_a: this is the variable with our string, but it does not accumulate anything.
   :feedback_b: this is the iterator variable. It changes each time but does not accumulate.
   :feedback_c: this is a variable inside the for loop. It changes each time but does not accumulate or retain the old expressions that were assigned to it.
   :feedback_d: yes, this is the accumulator variable. By the end of the program, it will have a full count of how many items are in byzo.
   :correct: d
   :practice: T
   :topics: 

   Which of these is the accumulator variable?
   .. sourcecode:: python

   byzo = 'hello world!'
   c = 0
   for x in byzo:
       z = x + "!"
       print(z)
       c = c + 1

.. mchoice:: question5_1_1_2
   :answer_a: cawdra
   :answer_b: elem
   :answer_c: t
   :feedback_a: yes, this is the sequence that we iterate over.
   :feedback_b: this is the iterator variable. It changes each time but is not the whole sequence itself.
   :feedback_c: this is the accumulator variable. By the end of the program, it will have a full count of how many characters are in the items are in cawdra.
   :correct: a
   :practice: T
   :topics: 

   Which of these is the sequence?
   .. sourcecode:: python

   cawdra = ['candy', 'daisy', 'pear', 'peach', 'gem', 'crown']
   t = 0
   for elem in cawdra:
       t = t + len(elem)

.. mchoice:: question5_1_1_3
   :answer_a: item
   :answer_b: lst
   :answer_c: num
   :feedback_a: yes, this is the iterator variable. It changes each time but is not the whole sequence itself.
   :feedback_b: this is the sequence that we iterate over.
   :feedback_c: this is the accumulator variable. By the end of the program, it will have the total value of the integers that are in lst.
   :correct: a
   :practice: T
   :topics: 

   Which of these is the iterator variable?
   .. sourcecode:: python

   lst = [5, 10, 3, 8, 94, 2, 4, 9]
   num = 0
   for item in lst:
       num += item

.. mchoice:: question3_2_1_2
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

   Which accumulation pattern is implemented in this code?
   .. sourcecode:: python

   TODO



