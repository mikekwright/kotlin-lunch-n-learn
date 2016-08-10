## Classes

Data classes (value objects) are similiar to those in Scala

        class User(val name: String, var age: Int))

Constructor keyword can be required

        class Tester public @Inject constructor(val application: String) {
          ...
        }

Create an instance of a class as if you were calling a function.  

        val me = User("Mike", 35)

note:

It kotlin there is one primary constructor (that is the one defined on the class itself), 
however you can have multiple secondary constructors.  

Secondary constructors are created by using the work constructor within the body of the
class, but must reference the primary constructor by the end.   

        class Person(val name: String) {
          constructor(name: String, parent: Person) : this(name) {
            parent.children.add(this)
          }
        }

Also you might need to have an default empty arg constructor for serialization libraries 
such as jackson.  With kotlin this can occur when you have all the arguments in the 
primary constructor filled with defaults.  

        class Person(val name: String = "") 

