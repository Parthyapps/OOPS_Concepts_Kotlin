# OOPS_Concepts_Kotlin
# OOPS Concepts 
![image](https://github.com/user-attachments/assets/43fffdb8-5f3e-48cb-82ee-96d9f55f196c)

# 1. Class and Object and Encapsulation
 - A class is a blueprint or template for creating objects. 
 - An object is an instance of a class, meaning it is a real-world entity created using the class.
```kotlin
   fun main(){
      val myObj = Car("Honda", 20) // Creating an object with initial values using constructor
      myObj.accessCar()
      println(student.totalMark())// Calling the fun method
  }
  // Student is a class with properties (name) and a function (mark).
  class Student {
      private var name: String = "" //variable properties
      private var mark: Int = 0
      fun totalMark(){
          mark = 25
      }
  }
  // A constructor initializes an object with specific values.
  class Car(var name: String, var speed: Int) {
        //The Car class has a primary constructor (val name: String, var speed: Int).
        fun accessCar(){
            speed +=30
        }
  }
```

# 2.Inheritance
# Reusing properties and methods from a superclass.
# Inheritance allows one class to acquire properties and behavior from another class.

  ```kotlin
  fun main() {
      val dog = Dog()
      dog.eat()  // Inherited from Animal
      dog.bark() // Defined in Dog
  }

      // Parent class
      open class Animal {
          fun eat() {
              println("The animal can drink water")
          }
      }
      
      // Child class
      class Dog : Animal() {
      
          fun bark() {
              println("dog barks")
          }
      }
```

# Encapsulation
 - Encapsulation means restricting direct access to data and
 - providing controlled access through getters and setters.
```kotlin
  fun main() {
    val student = Student() // Creating an object of student
    student.setName("John MR john") // Setting the name using setter
    student.setAge(22)
    println(student.getName() + student.getAge()) // Accessing the name using getter
 }

 // Student is a class with properties (name, age) and a function (accelerate).
class Student {
    // Private variable (hidden from outside)
    private var name: String = "" //variable properties
    private var age: Int = 0
    // Getter method to access the name
    fun getName(): String {
    return name
}
  // Setter method to set the name
  fun setName(name: String) {
    this.name = name
  }
  fun getAge(): Int{
     return age
  }
  fun setAge(i: Int){
     this.age = i
  }
}
```
# 4.Polymorphism
# Polymorphism means "many forms." It allows you to perform a single action in different ways depending on the object type. 
There are two main types of polymorphism:
- Compile-time Polymorphism (Method Overloading): Multiple methods with the same name but different parameters.
```kotlin
   class Calculator {
    fun add(a: Int, b: Int): Int {
        return a + b
    }

    fun add(a: Int, b: Int, c: Int): Int {
        return a + b + c
    }
}

fun main() {
    val calc = Calculator()
    println(calc.add(2, 3))      // Calls first function
    println(calc.add(1, 2, 3))   // Calls second function
}
```
- Runtime Polymorphism (Method Overriding): A subclass provides a specific implementation of a method that is already defined in its superclass.
```kotlin
  open class Animal {
    open fun sound() {
        println("This animal makes a sound.")
    }
}
  class Dog : Animal() {
      override fun sound() {
          println("The dog barks.")
      }
  }
  
  fun main() {
      val animal: Animal = Dog()
      animal.sound() // Calls overridden method in Dog
  }
```
# 5.Abstraction
# Abstraction hides implementation details and exposes only the necessary functionality. It is implemented using abstract classes or interfaces.

```kotlin
abstract class Vehicle {
    abstract fun start() // Abstract method

    fun stop() {
        println("Vehicle stopped.")
    }
}

class Car : Vehicle() {
    override fun start() {
        println("Car starts with a key.")
    }
}

fun main() {
    val car: Vehicle = Car()
    car.start() // Implementation from Car
    car.stop()  // Implementation from Vehicle
}
```

# Interface example
# Interfaces allow multiple inheritance and only declare methods, while abstract classes can have both abstract and concrete methods.
```kotlin
 interface Vehicle {
     fun start()
     fun stop() {
         println("Vehicle stopped.") // Default implementation
     }
 }
 
 class Bike : Vehicle {
     override fun start() {
         println("Bike starts with a button.")
     }
 }
 
 fun main() {
     val bike: Vehicle = Bike()
     bike.start() // Implementation from Bike
     bike.stop()  // Default implementation from Vehicle
 }
```
