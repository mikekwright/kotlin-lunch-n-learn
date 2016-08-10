## Lambdas

Like many of the newer (and older) languages, Kotlin support lambdas

        val sum = { x: Int, y: Int -> x + y }
        // Typed
        val sum: (Int, Int) -> Int = { x, y -> x + y }

There are also library functions that are higher order functions (meaning they take
a function as an arg).  

        max(strings, { a, b -> a.length < b.length })

        names.filter { name.length < 3 }

There are also `annonymous functions` that are defined differently

        fun(x: Int, y: Int): Int = x + y

note: 

Kotlin also has added the notion of an `inline`, for those who have programmed in 
C\C++ before the inline should be a common idea, although not often used since most
compilers are able to optimize better then we as humans can.  

However in kotlin the idea is that instead of using the dynamically generated closure
based method it will adjust to manually inline the code.  And there is a corresponding
noinline that you can use as well.  


        inline fun foo(method: () -> Unit, noinline other: () -> Unit) {
          ....
        }

Annonymous functions will allow you to specify the return type, where lambda's don't have that.  

        
