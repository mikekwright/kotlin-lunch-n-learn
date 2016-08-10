## Extension Methods

Kotlin provides support for extension methods, methods that can be used on a given 
object with the feel that they have been part of that object all along.   

        fun String.addSignature() = this + " my signature"

        val message = "This is my message"
        println(message.addSignature())

You can even have extension methods that will be called for nullable types

        fun Int?.toString(): String {
          if (this == null) {
            return "N/A"
          }

          return toString()
        }

