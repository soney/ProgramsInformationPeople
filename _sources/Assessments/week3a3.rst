..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

Week 3 Assessment 3
-------------------

**Check your understanding**

.. mchoice:: question3_3_1_1
   :answer_a: yes
   :answer_b: no
   :feedback_a: Yes, the intent by the programmer was not executed properly if they wanted to print the list ['q', 'u'] because of aliasing.
   :feedback_b: If the intent was to print the list ['q', 'u'] then aliasing would cause a problem because z also replaces the 'u' with an 'i'.
   :correct: a
   :practice: T
   :topics: 

   Could aliasing cause potential confusion in this problem?

   b = ['q', 'u', 'i']
   z = b
   b[1] = 'i'
   z.remove('i')
   print(z)

.. mchoice:: question3_3_1_1
   :answer_a: yes
   :answer_b: no
   :feedback_a: Though both lists have changed, it is not as likely to cause confusion.
   :feedback_b: These operations on the lists are not likely to cause confusion.
   :correct: b
   :practice: T
   :topics: 

   Could aliasing cause potential confusion in this problem?

   b = ['q', 'u', 'i']
   z = b
   b[1] = 'i'
   for elem in b:
       print(elem)
   for item in z:
       print(item)


 .. mchoice:: question3_1_1_1
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

