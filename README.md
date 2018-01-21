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



## `null` safety

In java a big amount of code is defensive, we need to check once and another wheter
something is null before using it, if we dont want to find unexpected `NullPointerException`.

Kotling, as many other modern languages, is null safe because the type explicitly
defines whether an object can be null by unsing the safe call operato (`?`)


For example:
```scala
// This wont compile as Artist cant be null
var notNullArtist: Artis = null
// Artist can be null
var artist: Artist? = null
// Wont compile, artist could be null and we need to deal with that
artist.print()
// will print only if artist is != null
artist?.print()

// Smart cast. We dont need to use safe call operator if we previously
// checked nullity

if(artist != null){
  artist.print()
}
// only use it whrn we are sure it's not null. Will throw an exception otherwise
artist!!.print()

// use elvis operator to give an alternative in case that object is null.
val name = artist=.name? : "empty"
```


## Extension Functions

You can add functions to any class, it's a much readable substitute to the usual
utility classes we all have in projects. For example, adding a method to fragments
to show a toast.

```scala
fun Fragment.toast(message: CharSequence, duration: Int = Toast.LENGTH_SHORT){
  Toast.makeText(getActivity(), message, duration).show()
}
```

And then use it like this:

```scala
fragment.toast("Hell this world")
```
