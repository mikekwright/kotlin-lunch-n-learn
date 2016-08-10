## Companion Object

Kotlin does not have the notion of statics inside of classes, it recommends those be at a
package level instead.  

It also does provide a static-like mechanism know as a companion object, however this is 
closer to a singleton as the companion objects are actually instantiated.  

        class MyClass {
          companion object Factory {
            fun create(): MyClass = MyClass()
          }
        }

        val instance = MyClass.create()
        val companion = MyClass.Factory

note:

With the companion object, you can completely ommit the name of the companion object which will
have it default to `Companion`

        class MyClass {
          companion object {
          }
        }

        val companion = MyClass.companion


