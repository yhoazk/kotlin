# kotlin
Tutorials and that sort of stuff for the new language kotlin


> http://kotlinlang.org/
[Kotlin is a] statically typed programming language for modern multiplatform applications.

Kotlin is a programming language intended to be a better java. and its designed to be
usable and readable across large teams with skill and discipline variances.



## [Syntax](https://learnxinyminutes.com/docs/kotlin/)


### Comments
The comments are the same as in java, c/c++, scala.
```kotlin
// Single line comment
/*
  Multiline comments
*/
```

It has the same keyword as java to import other libraries or modules
```kotlin
package com.kotlin
```

As in C,C++ and java. The entry point to a kotlin program is a function named
`main`. The function is passed an array containing any command line argument.

```kotlin
fun main(args: Array<String>)
{
  /*Declaring values is done using var o val as in scala*/
  val fooVal = 10 // Vals are costant
  var fooVar = 10 // Vars can be reassigned
  fooVar = 20
}
```

As in Scala, in most cases, kotlin can determine what the type of a variable is.
```kotlin
val foo: Int = 7
```

### Strings

Strings work similar as in Java and Scala
