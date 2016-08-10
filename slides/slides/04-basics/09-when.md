## When

When is a mix between a `switch` from Java and a matcher in a functional language

        when(count) {
          1 -> println("first") 
          2 -> println("second")
          else -> println("to big")
        }

You can also use ranges and multiple values

        when (count) {
          1,3,5,9 -> println("low odd")
          2,4,6,8 -> println("low even")
          10..100 -> println("under 100")
          !200..300 -> println("not between 200 and 300")
          else -> println("in the 200-300 range")
        }

It even works with types

        when (x) {
          is Int -> print(x + 1)
          is String -> print(x + "str")
          is IntArray -> print(x.sum())
        }


