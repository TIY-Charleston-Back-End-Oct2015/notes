### Day 1

* Review assignment (dynamic data structures - ATM)
* Running Java code the normal way
  * Main method
  * Jar files
    * File -> Project Structure...
    * Click "Artifacts" and then the plus button
    * JAR -> From modules with dependencies...
    * Choose the main class and click OK
    * Build -> Build Artifacts...
* Review last week's material
  * Arrays and classes
  * Methods
  * Control flow (if, while, for, throw)
  * ArrayLists and HashMaps

### Day 2

* Review assignment (review - inventory)
* Contact project
  * Create a constructor for `Contact`
  * Create `Contact` objects
  * Change their fields
  * Add them to an `ArrayList<Contact>`
  * Get a contact out of the list
  * Search an `ArrayList<Contact>` for someone with a particular name
* Use `String.format` in the ToDo project
* Text adventure
  * Add health and damage to `Player`
  * Create a `Player` constructor
  * Create an `Enemy` class
  * Create a `Character` class that they extend
  * Create a `battle` method in `Character`
  * Create a `toString` method in `Character`
  * Discuss `@Override`
* Contrived example of inheritance
  * Animal
    * Mammal
      * Dog
      * Human
    * Reptile
      * Alligator
      * Turtle
    * Bird
      * Hawk
      * Parrot
* Topics of discussion
  * Review constructors
  * Extending a class (inheritance)
  * The `Object` class

### Day 3

* Review assignment (object-oriented programming - inventory)
* Exercise
  * Loop over string array
  * Use `ArrayList` instead of a primitive array
  * Use `Contact` class instead of strings
  * Generics and casting
* Text adventure
  * Store weapon in `Character` and create `Weapon` class
  * Add weapon's damage in `battle` method
  * Add save feature
* File I/O
  * JSON
  * `File`, `FileWriter`, `FileReader`
* Dependency management
  * Maven
  * Pull in the [JSON library](http://jodd.org/doc/json/)
  * Add to project
    * File -> Project Structure...
    * Click "Libraries" and then the plus button
    * Click "From Maven..."
    * Search for "jodd json"

### Day 4

* Review assignment (file I/O - save JSON)
* Exercise
  * Keep asking for input until valid input is received
  * As a group, create a `HashMap<String, ArrayList<String>>`
* `switch` statements
  * Use in the Zoo project
* Text adventure
  * Save file name constant as `static final`
  * Set breakpoint in `main` to see contents of objects
  * Create bug in `findItem` and set breakpoint
  * Hotswap values
* Debugging with IntelliJ
  * Primitive form of debugging: printing variables
  * Better form of debugging: IntelliJ's debugger
    * Set breakpoint
    * See what variables contain at that moment in time
    * Reload changed classes
      * Can't reload method if it's in the middle of execution
      * Can't reload method if its signature has changed
      * [Notch using this feature](https://www.youtube.com/watch?v=BES9EKK4Aw4)
* Forum
  * Create console-based forum with custom file format
  * Create `Post` and `ArrayList<Post>`
  * Create file and read its contents into the arraylist
  * Loop over posts and print the top ones out
  * Break the loop out into `printPosts`
  * Create an infinite loop that listens for a post # to jump to
