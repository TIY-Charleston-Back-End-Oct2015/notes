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

* Overview of Git
  * Why track changes?
    * Collaboration
    * Revert mistakes
    * Offsite backup
  * Interesting comments from [Tarn Adams](https://www.reddit.com/r/IAmA/comments/1avszc/im_tarn_adams_of_bay_12_games_cocreator_of_dwarf/c919fo8) on version control
    * Find a middle ground between good practice and getting things done
  * History of VCSes
    * CVS (1990)
    * SVN (2000)
    * Git (2005)
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

### Day 3

* Review instance/static fields and methods
  * Start with data classes (classes that only contain fields)
  * Methods let you write code that reads from and writes to those fields
  * Constructors are methods that run right when the object is created
* Git
  * Create a repo and clone it via IntelliJ
  * Write code, commit, and push
  * Show diff
  * Three ways to revert your changes
    * If not committed yet
      * Under Local Changes, right-click the file you want to revert
      * Click "Revert..."
    * If committed but not pushed
      * Under Log, right-click the commit you want to go back to
      * Click "Reset Current Branch to Here..."
      * Choose "Hard"
    * If committed and pushed
      * Under Log, right-click the commit you want to revert
      * Click "Create Patch..."
      * Check "Reverse patch" and create it
      * Under the VCS menu, choose "Apply Patch..."
      * Delete the patch file
      * Commit your changes
* Create a text-based game
  * Demonstrate use of arrays/classes, static methods, and control flow
* Use `Scanner` to read console input
  * Unlike output, input requires creating an object
  * Book analogy: Reading requires a bookmark, but writing is simply appending at the end
* Control flow
  * Conditionals
  * Loops
  * Recursion
  * Exceptions
