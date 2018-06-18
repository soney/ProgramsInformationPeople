..  Copyright (C)  Paul Resnick.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

Accumulator Pattern Strategies
==============================

When you first start learning accumulation patterns it's sometimes difficult to determine what pattern, if any, is best for the problem you're trying to solve. 
Depending on what information you're given and what result you want, using accumulation may or may not be necessary. 
If the problem is simple, such as determining how many e's are in a string, then you may be better off using existing methods, such as the ``count`` method. 
If it's more complicated, such as counting the number of occurrances of multiple things in a string or list, then accumulation may be appropriate.

Certain actions are likely to involve accumulation patterns. 
This includes counting the frequency of something, determining a total, and creating a string or list from another string or list. 
Though this is not a complete list of cases where accumulation may be necessary, keeping this in mind can help when creating solutions to prompts and problems.

One aspect of writing an accumulation pattern is determining the type of the accumulator variable. 
In this textbook a prompt will specify what the returned value should be (like asking for the 'biggest number' or 'a list of first words in sentences').
However, not every problem will be clearly defined.
Regardless, as a programmer you're tasked with coming up with a solution. 
When it comes to deciding the type the accumulator variable should be, this may be dictated by the problem you're solving but it can also depend on how *you* want to solve something. 

For example, say you want to extract different parts of a string and then recombine those parts into a new string. 
Think about what type your accumulator variable could be. So far you know of two options that might make sense. 
A string is the most obvious choice as that's what you want the end result to be. However, this task could also be accomplished with an accumulator variable that is a list. 
The solution could then use the ``join`` method or even another accumulation pattern to get the desired final outcome. 
Using either the string or the list is fine, but one of them might make your job easier so it's important to think about how the type would affect your actions.



