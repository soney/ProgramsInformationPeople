..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

Week 1 Assessment 3
-------------------

**Check your understanding**

.. mchoice:: question3_2_1_1
   :answer_a: tex.forward(20)
   :answer_b: forward() + 20
   :answer_c: forward(20)
   :answer_d: forward(20).tex
   :answer_e: text.forward(10 + 10)
   :feedback_a: Correct.
   :feedback_b: Incorrect, this does not use the turtle method necessary to move a turtle forward.
   :feedback_c: Incorrect, how would the program know what turtle should be moving?
   :feedback_d: Incorrect, the formatting is incorrect.
   :feedback_e: Correct, you are allowed to write expressions inside of methods.
   :correct: a, e
   :practice: T
   :topics: PythonTurtle/InstancesAHeardofTurtles

   What is the correct way to tell a turtle to move forward 20 pixels? Select as many as apply.

.. mchoice:: question3_2_1_2
   :answer_a: turtle(Turtle)
   :answer_b: turtle.Turtle()
   :answer_c: Turtle.turtle()
   :answer_d: Turtle(turtle)
   :feedback_a: Incorrect, when making a new instace of the Turtle class, you need to use dot notation.
   :feedback_b: Correct.
   :feedback_c: Incorrect, Turtle represents the class and should be second.
   :feedback_d: Incorrect, when making a new instace of the Turtle class, you need to use dot notation.
   :correct: b
   :practice: T
   :topics: 

   Which is the correct way to make a new instance of the Turtle class?

.. mchoice:: question3_2_1_3
   :answer_a: The Turtle class.
   :answer_b: The same turtle that is used in each drawing your programs make.
   :answer_c: A unique 'turtle' that you can use to draw.
   :feedback_a: Though each instance does use the Turtle class, this is not the best answer.
   :feedback_b: Each instance that is made using the Turtle class is unique. Remember how you can have multiple 'turtles' in a single drawing? Each of those are different turtles but they are all instances of the Turtle class.
   :feedback_c: Correct.
   :correct: c
   :practice: T
   :topics: 

   What does each instance of the Turtle class represent?

.. mchoice:: question3_2_1_4
   :answer_a: Change the value of an attribute.
   :answer_b: Return values.
   :answer_c: Create new attributes and set their value.
   :answer_d: Delete instances of a class.
   :answer_e: None of the above.
   :feedback_a: Correct, methods can change the value that is associated with an attribute. 
   :feedback_b: Correct, methods can return values.
   :feedback_c: Correct, methods can create new attributes and then set that attribute's value.
   :feedback_d: Incorrect, methods cannot delete instances of a class.
   :feedback_e: Incorrect, methods can do at least one of the above. Take another look.
   :correct: 
   :practice: T
   :topics: 

   Select all of the following things that methods can do:


.. mchoice:: question3_2_1_5
   :answer_a: student.title()
   :answer_b: title.student()
   :answer_c: title.student
   :answer_d: student(title)
   :answer_e: student.title
   :feedback_a: Incorect, this is not the structure used to refer to an attribute.
   :feedback_b: Incorect, this is not the structure or order used to refer to an attribute.
   :feedback_c: Incorrect, this is not the order used to refer to an attribute.  
   :feedback_d: Incorrect, this would be the syntax for a function named ``student`` being called on a variable named ``title``.
   :feedback_e: Correct.
   :correct: e
   :practice: T
   :topics: 

  For an instance that is assigned to the variable ``student``, what is the propper way to refer to the ``title`` attribute/instance variable?

 .. mchoice:: question3_2_1_6
   :answer_a: True
   :answer_b: False
   :feedback_a: Correct. Just like the variables you've learned about so far, you can assign values to an attribute and look up the values that are assigned to the attribute.
   :feedback_b: Incorrect. The only difference is the structure that is used to refer to it.
   :correct: a
   :practice: T
   :topics: 

   True or False, attributes/instance variables are just like other variables in Python?