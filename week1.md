### Install Party

* Install [JDK 8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
* Install [IntelliJ Community Edition](https://www.jetbrains.com/idea/download/)
* Install the JREPL IntelliJ plugin
  * Preferences -> Browse repositories… -> Search for “JREPL”

### Day 1

* Overview of the class
* History of Java
  * Low level vs high level
  * Context of Java's birth in the 90's
  * How it works (bytecode, VM, etc)
* Intro to Java
  * Create HelloWorld IntelliJ project inside this repository
  * Start the REPL
    * Tools -> Start JREPL
  * Scalar variables
    * int
    * double
    * boolean
  * Compound variables (data structures)
    * Sequential vs associative
    * Arrays and classes
      * Position array
      * Position class
    * Class vs object (blueprint vs house)
    * Built-in classes
      * Essentially the entire language consists of classes
      * `String` is one of the most common
    * You can make arrays of objects and objects containing arrays
      * To-do array
      * Contact class
      * Two-dimensional array representing pixels
    * Show example of lack of data structure usage
    * Scenarios - A data structure that holds...
      * A tweet
      * Web browser history
      * Every keyboard code and the character it represents
      * The points scored for each player on a team
      * The departure time for every plane in an airline's fleet

### Day 2

* Writing code in a file
  * Create the Contact class from yesterday in a file
  * Use the class in JREPL
  * You need to add "public" to access it from JREPL
  * A class is more than just a data structure; it can contain code
  * All code must exist inside a class
  * Create `setName` and `getName` methods
    * Can be useful over direct field access if you want to enforce constraints
    * Interesting comments from [Notch](http://notch.tumblr.com/post/15782716917/coding-skill-and-the-decline-of-stagnation) on getters and setters
  * Create a constructor that takes a name
* Work through examples of using string methods in the REPL
  * Look up the Java doc for `String`
  * Call methods
    * `charAt`
    * `contains`
    * `indexOf`
    * `split`
    * `startsWith`
    * `substring`
    * `toUpperCase`
    * `trim`
  * Mutation
    * Strings are immutable; their methods return a new string if necessary
    * Mutation is a common source of bugs; a variable can contain something you didn't expect
* Static methods and fields
  * They're stored in the class rather than in each object
  * Use static methods if it is "standalone" (no need to access fields)
  * Static methods and fields (look at the ones in `Math` and `System`)
  * Create a static method `isValidName` in our project and run it in the REPL
