## Properties

Kotlin has the ability to use properties similar to `C#`

        class Phone(val number: String) {
          val isEmpty: Boolean  
            get() = number == null

          var areaCode: String
            get() return number.substring(0..3)
            set(value) {
              number = "$value${number.substring(3..number.length)}"
            }
        }

Can set scope on a per property level

        private var age: Int = 0

        var otherAge: Int = 0
          private set

note:

By default anything added through the constructor has a property created for it, 
you cannot overwrite the default properties created by the constructor, so you will
need to convert those properties to be private and then create the custom properties
for what you are trying to do.   


