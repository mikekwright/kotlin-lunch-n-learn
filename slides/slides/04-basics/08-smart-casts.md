## Smart Casts

Often when using other languages you will see the below code

        if (person.isInstance(Worker.class)) {
            Worker worker = (Worker)person ;
            System.out.println(worker.getTool());
        }

In kotlin it will automatically cast your type once you have used an
expression to make sure it is that type.  

        if (person is Worker) {
          println(person.tool)
        }
          
        if (x is String && x.length > 0) {
          ...
        }

        if (x !is String) { 
          ... 
        } else {
          val len = x.length
        }

note: 

This will also automatically cast in when expressions and while loops.  

There is also the ability to have an unsafe cast using the `as` keyword that will throw and
exception, or you can use the `as?` that will return null instead of throwing an exception.  


