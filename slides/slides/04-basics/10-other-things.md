## Other Things

There are a lot of other things that are very interesting in the language.  

1. `breaks` and `continues` can target loops
2. returns inside of a lambda can break out of outer function (not annonymous functions)
3. Provides a set list of operators that you can overload. 
4. `!!` operator for forcing NPE when need on an object instead of `?`

And of Course it tries to fix [The Billion Dollar Mistake](http://en.wikipedia.org/wiki/Tony_Hoare#Apologies_and_retractions) 
by make use of explicit Nullables.   

        val name: String = "Mike"
        name = null   // Compilation error

        val name: String? = "Mike"
        name = null

note: 

      loop@ for (i in 1..100) {
        for (j in 1..100) {
          if (...)
            break@loop
        }
      }

      
      fun foo() {
        ints.forEach lit@ {
          if (it == 0) return@lit
          print(it)
        }
      }


      // Returns a null from first experssion instead of NPE
      val length = str?.length ?: -1
      // Forces an NPE to occur
      val length = str!!.length


