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

### Day 2

* Review assignment (review - people)
* Desktop UI with Java FX
  * Install [Scene Builder](http://www.oracle.com/technetwork/java/javase/downloads/javafxscenebuilder-1x-archive-2199384.html)
  * Build a to-do app and a web browser
    * New Project -> Java FX template
    * Run blank project
    * Look at the three files you start with
    * Edit title and window size in Main.java
    * Use Scene Builder to change sample.fxml
    * Edit Controller.java
      * Implement `Initializable`
      * Implement an action method
      * Bring in controls using `@FXML`
      * Make all buttons set min size to USE_PREF_SIZE
      * To-do app
        * Create an `ObservableList`
        * Set the `ListView` to use it
        * Wire up the "Add", "Toggle", and "Remove" buttons
      * Web browser
        * Wire up the "Go" button
        * Allow hitting enter in URL textfield
        * Implement `ChangeListener` to update the URL textfield
        * Wire up the back and forward buttons
  * Build as a JAR file
    * File -> Project Structure...
    * Click on "JavaFXApp.jar"
    * Click on "Create Manifest..."
    * Click OK
    * Build -> Build Artifacts...
    * Click on "Build"
