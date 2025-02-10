# OOPS_Concepts_Kotlin
# OOPS Concepts 
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
