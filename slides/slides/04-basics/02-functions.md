## Functions

Defined with the `func` keyword, and the return type is placed at the end.  

        fun max(left: Int, right: Int): Int {
          ...
        }

Functions can also be defined using expression bodies much like scala 

        fun max(left: Int, right: Int) = ...

note:

So a general function follows the pattern of having the type at the end of the function, 
at this seems to make it more readable and flow better. 

Also note that when using an expression body the `return` statement can be ommitted, 
as well as the return type of the function itself (as this is inferred).  




