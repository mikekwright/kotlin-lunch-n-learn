## Example

### Hello World

        fun main(args : Array<String>) {
          val scope = "world"
          println("Hello, $scope!")
        }

### Elvis - ?:

        fun sayHello(maybe : String?, neverNull : Int) {
          val name : String = maybe ?: "stranger"
          println("Hello $name")
        }

