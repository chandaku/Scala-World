# Scala-World
Scala:

https://www.youtube.com/watch?v=-8V6bMjThNo

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
		
		


		val dinousour = new Carnivore {
			override eat(animal:Animal):Unit = println(“I am dinosaur so I can eat almost anything”)
		}

		object MySinglton {
 			 val mySpecialVariable = 12345
  			def mySpecialMethod():Int = 1234
  			def apply(x:Int):Int = x+1
		}
		
		println(MySinglton(65))

		object Animal { // Companions - Companion Object (Singlton)
  		// Companion can access each other private/protected variables and methods
  		val canLiveForever = false
		}

		val canLive = Animal.canLiveForever

		println(canLive)
		
		**************************************** Case Class

		case class Person(name: String, age: Int)

		val person = Person(“Harry”, 39)


		

	}
	
**************************** Pattern Matching (Swtich case of Java) ****************

```
val anInteger = 55
val result = anInteger match {
case 1 => "This is one"
case 2 => "This is two"
case 3 => "This is 3"
case _ => "This is $anInteger"
}
print(result)
```

Deconstruct an Object while pattern match
with case class decomposition

```
case class Person(name: String, age: Int) 

val harry = Person("Harry", 43) // Person.apply

val result = harry match {
	case Person(n, a) => "This is $n having age $a"
	case _ => "Not sure who this is?"
}

println(result)
```
tuples deconstruction

```
val aTuple = ("Hi", "welcome")

val result = aTuple match {
case (a, b) => "Tuple Matched"
case _ => "Default one"
}
```

Decompose list for pattern match 

```
val aList = List(1, 2, 3)

val result = aList match {
case List(_, 2, _) => "List having 2 object with 2 and second postion"
case _ => "Default one"
}
```
//If PM Does not match anything, it will throw error
// case are executed in order of sequence

**********************************************ADVANCE FEATURES**********************
```
object Advanced extends App {

lazy val aLazyValue = 55

	lazy val aLazyWithSideEffects = {
	print("I am so lazy")
	44
	}
	
	val eagerResult = aLazyWithSideEffects + 1;

//************************
// Learn Option, Try, Future, Implicit


}
```

Some differentiator concepts for scala 
Interpolator = s" $a"
infix = if only argument for a method then a method can be called as object method argument
FunctionX = Function1, Function2 .... Function22
