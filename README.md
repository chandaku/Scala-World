# Scala-World
Scala:

Everything is a value
We write code block that generally return a value

Val aCodeBlock = {
	Val aCodeValue = 67
	aCodeLocal + 3
}

	def myFunction(x: Int, y Int) : Int {
	y+x
	}

def factorial(n : int) : Int {
if(n<=1) 1
Else n* factorial(n-1)
}

// In scala we don’t use loops or iterations we mostly use recursions

//unit type  = (no meaningful value = void)

// Types of SIDE EFFECTS

Def myUnitFunction():Unit = {
println(“I don’t love unit function”)
}

Val theUnit = ()



/***********************************************************/
Object Orientation


	object ObjectOrientation extends App {

		class Animal  {
		val age = 0;
		def eat() = println(“I am eating”)
		}

		//Inheritance
		class Dog(val name: String) extends Animal

		val aDog = new Dog(“Hatchi”)

		// Constructor Arguments are not fields have to put val before constructor argument
		aDog.age…!!!!!

		//subType Polymorphism
		val animal:Animal = new Dog(“Hatchi”)



		class WalkAnimal extends Animal
 		
		val walkAnimal:WalkAnimal 
		
		//abstract class
		abstract class WalkAnimal {
			val hasLegs = true;
			def walk(): Unit
		}

		// Interfaces

		trait Carnivore  {
		def eat(animal:Animal):Unit

		}

		//single class inheritance, multi trait mixing
		class Crocodlie extends Animal with Carnivore {
		
		override def eat(animal:Animal): Unit = println(“Elating with animal”)

		}
		

	}
