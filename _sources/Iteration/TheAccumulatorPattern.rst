.. _accum_pattern:
      
The Accumulator Pattern
=======================

One common programming "pattern" is to traverse a sequence, **accumulating** a value as we go, 
such as the sum-so-far or the maximum-so-far. That way, at the end of the traversal we have accumulated a single
value, such as the sum total of all the items or the largest item.

The anatomy of the accumulation pattern includes:
   - **initializing** an "accumulator" variable to an initial value (such as 0 if accumulating a sum)
   - **iterating** (e.g., traversing the items in a sequence)
   - **updating** the accumulator variable on each iteration (i.e., when processing each item in the sequence)
   
For example, consider the following code, which computes the sum of the numbers in a list.

.. activecode:: iter_accum1

   nums = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
   accum = 0
   for w in nums:
       accum = accum + w
   print(accum)

In the program above, notice that the variable ``accum`` starts out with a value of 0.  
Next, the iteration is performed 10 times.  Inside the for loop, the update occurs. 
``w`` has the value of current item (1 the first time, then 2, then 3, etc.). 
``accum`` is reassigned a new value which is the old value plus the current value of ``w``.

This pattern of iterating the updating of a variable is commonly referred to as the **accumulator pattern**. 
We refer to the variable as the **accumulator**. This pattern will come up over and over again. Remember that the key
to making it work successfully is to be sure to initialize the variable before you start the iteration. Once inside 
the iteration, it is required that you update the accumulator.

Here is the same program in codelens.  Step thru the function and watch the "running total" accumulate the result.

.. codelens:: iter_accum2
   :python: py3

   nums = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
   accum = 0
   for w in nums:
      accum = accum + w
   print(accum)


.. note::

    What would happen if we indented the print accum statement? Not sure? Make a prediction, then try it and find out.

We can use the accumulation pattern is count the number of something or to sum up a total. The above examples only 
covered how to get the sum for a list, but we can also count how many items are in it if we wanted to.

.. activecode:: iter_accum3

   nums = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
   count = 0
   for w in nums:
       count = count + 1
   print(count)

In this example we don't make use of ``w`` even though the iterator variable is a necessary part of constructing a for 
loop. Instead of adding the value of ``w`` to ``count`` we add a 1 to it, because we're incrementing the value of 
count when we iterate each time through the loop. Though in this scenario we could have used the ``len`` function, 
there are other cases later on where len won't be useful but we still need to count.

**Check your understanding**

.. mchoice:: test_question5_4_1
   :answer_a: It will print out 10 instead of 55
   :answer_b: It will cause a run-time error
   :answer_c: It will print out 0 instead of 55
   :feedback_a: The variable accum will be reset to 0 each time through the loop. Then it will add the current item. Only the last item will count.  
   :feedback_b: Assignment statements are perfectly legal inside loops and will not cause an error.
   :feedback_c: Good thought: the variable accum will be reset to 0 each time through the loop. But then it adds the current item.
   :correct: a
   :practice: T
   :topics: Iteration/TheAccumulatorPattern

   Consider the following code:

   .. code-block:: python

      nums = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
      for w in nums:
         accum = 0
         accum = accum + w
      print(accum)
   
   What happens if you put the initialization of accum inside the for loop as the first
   instruction in the loop?


.. parsonsprob:: question5_4_1p
   :practice: T
   :topics: Iteration/TheAccumulatorPattern

   Rearrange the code statements so that the program will add up the first n odd numbers where n is provided by the user.
   -----
   n = int(input('How many odd numbers would you like to add together?'))
   thesum = 0
   oddnumber = 1
   =====
   for counter in range(n):
   =====
      thesum = thesum + oddnumber
      oddnumber = oddnumber + 2
   =====
   print(thesum)

