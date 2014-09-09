# Beispiele

## Folie 5
```scala
val charakter = new Character(‘x’)
val big = new java.math.BigInteger(“12345”)

import java.math._
import java.math.BigInteger
import java.math.{BigInteger, BigDezimal=>JBigDezimal}
```
___________________________________________________
## Folie 6
```scala
var name = "hallo Welt"    
var nameHasUpperCase = name.exists{x => x.isUpper}
```
__________________________________________________
## Folie 7
```scala
var numbers = List(1, 2, 3, 4)
var numbers: List[Int] = List[Int](1, 2, 3, 4) 
```
___________________________________________________
## Folie 8
```scala
scala>1+1
res0: Int = 2

scala>res0 * 3
res1: Int = 9

var multiline = {
var a = 5
var b = 7
a*b
}

scala> val multiLine =
    | "Das ist die naechste Zeile"
multiLine: String = Das ist die naechste Zeile

scala> val oops =
    |
    |
You typed two blank lines.  Starting a new command.)
```
_______________________________________________
## Folie 9
```scala
case class Person(name: String, vorname: String)
```
_______________________________________________
## Folie 10
```scala
var a = if (true) 5 else 7    // a = 5
var b = if (false) 5 else 7	  // b = 7
```
_________________________________________________
## Folie 11
```scala
scala> var hallo: String = “Hallo Welt!”
hallo: String = Hallo Welt!

scala> hallo = “Hallo Planet!”
hallo: String = Hallo Planet!


println(hallo)
Hallo Welt!

scala> val jahr = 2010
jahr: Int = 2010
jahr = 2013
```
______________________________________
## Folie 13
```scala
def ausgabe(): Unit = {println(“hallo”)} 
entspricht: 
def ausgabe() {println(“hallo”)}
entspricht:
def ausgabe(){
	println(“Hallo”)
	()
}
```
__________________________________________
## Folie 15
```scala
var a = while (i < lisy.length) {
	42
	i = i+1}

val l = List(1, 2, 3)
val a = for(x <- l) println(x)
```
____________________________
## Folie 27
++
```scala
val list = List(1,2,3,4,5)
val array = Array(6,7,8,9)    
val list2 = list ++ array    
println(list2)    
```
exists

```scala
val list1 = List(1,2,4,5,7)
val myFunction = {(x: Int) => x % 2 == 0}
list1.exists(myFunction)
```

filter:
```scala
val list1 = List(1,33,26,146,32,55,26,217,24,326)
val list2 = list1.filter((x: Int) => x > 50)
val list4 = list1.filter(_ > 100)
```

foreach
```scala
val myList4 = List(1,6,3,9,4)                     
myList4.foreach(i => println(i))    
```

map
```scala
val list12 = List(1,2,3,4)        
val list13 = list12.map(x => x+1)            
list13  
```
_______________________________                            
## Folie 29
```scala
def malUndPlus(x: Int) = {
	val a = x*2
	val b = x+2
	val c = “hallo”
	(a, b, c)
}
malUndPlus(7) //(Int, Int, String)=(14,9, “hallo”) in einem Objekt 2 werte
```
__________________________________________________     
## Folie 31
```scala
val landStad = Map(
  "Deutschland" -> "Berlin",
  "Frankreich"  -> "Paris",
  "Italien" -> "Rom")                        

landStad foreach { kv => println(kv._1 + ": " + kv._2) } 
```                                         
_____________________________________    
## Folie 32	
```scala
  def fak(n : Int): Int = {
    if (n == 0) 1
    else n * fak(n-1)
  }

private def fak3(n: Int, accu: Int): Int = {
  if (n == 0) accu
  else fak3(n-1, n * accu)
}
def fak4(n: Int) = fak3(n, 1)


def fak2(n: Int): Int = {
  def loop(n: Int, accu: Int): Int = {
    if (n == 0) accu
    else loop(n-1, n * accu)
  }  
loop(n, 1)
} 
  
fak2(5);
```

