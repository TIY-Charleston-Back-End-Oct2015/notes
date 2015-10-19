### Day 1

* Review assignment (file I/O continued - countries)
  * Loops
  * Nested data structures
* Exercise
  * Print name combos
  * Create `HashMap` that maps names to lists of `Email` objects
* More review
  * Casting
    * Cast a `long` to an `int`
    * Cast an `Object` (from a raw `ArrayList`) to a `String`
  * Inheritance
    * The `Character` class in the text adventure
* Interfaces
  * Sort an `ArrayList<String>` in JREPL using `Collections.sort`
  * In the `Contacts` class, sort `ArrayList<Contact>` by implementing `Comparable`
  * Definition
    * A list of one or more methods that a class must have
    * Allows code to call methods on objects even if they don't know what those objects are
    * Used all the time in Java itself as well as libraries/frameworks
* Testing with IntelliJ
  * Create test folder
    * File -> Project Structure...
    * Click "Modules"
    * Right-click the "src" folder and click "New Folder"
    * Call it "test"
    * Right-click the "test" folder and click "Tests" to mark it as a test folder
  * Add JUnit 4 to project
    * File -> Project Structure...
    * Click "Libraries" and then the plus button
    * Click "From Maven..."
    * Type in "junit:junit:4.12"
  * Create a test
    * Select a class you want to write tests for
    * View -> Test 
