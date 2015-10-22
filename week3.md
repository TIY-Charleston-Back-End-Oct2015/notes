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
* Install [Scene Builder](http://www.oracle.com/technetwork/java/javase/downloads/javafxscenebuilder-1x-archive-2199384.html)
* Create a project
  * New Project -> JavaFX template
  * Run blank project
  * Look at the three files you start with
  * Edit Main.java to set the title and window size
  * Edit sample.fxml via Scene Builder
    * Make all buttons set min size to USE_PREF_SIZE
  * Edit Controller.java
    * Implement `Initializable`
    * Implement action/keyboard methods
    * Bring in controls using `@FXML`
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

### Day 3

* Review assignment (javafx - contacts)
* Install [Android Studio](https://developer.android.com/sdk/index.html)
* Download the latest SDK
  * At the main screen, go to: Configure -> SDK Manager
  * Download the SDK for Android 4.0.3
* Install Intel HAXM (allows Android emulators to run faster)
  * Go to `~/Library/Android/sdk/extras/intel/Hardware_Accelerated_Execution_Manager`
  * Double-click "IntelHAXM.dmg" and run the installer
* Create a project
  * At the main screen, go to: Start a new Android Studio project
  * Give it a name and type "theironyard.com" as the company domain, and click "Next"
  * Select Android 4.0.3 and click "Next"
  * Select "Empty Activity" and click "Next"
  * Click "Finish"
* Configure an emulator
  * In your project, click the "Android Virtual Device Manager" button
  * Click on "Create Virtual Device..."
  * Select a device and click "Next..."
  * Select an Android version and click "Next..."
  * Make sure "Use Host GPU" is checked
  * Click "Show Advanced Settings"
  * Set the RAM to 1GB (so Intel HAXM will work)
* To-do app
  * Add listview, text field, and button
  * Set listview width/height to `match_parent`
  * Create variables for all controls and use `findViewById` in `onCreate`
  * Create an `ArrayAdapter` and connect it to the listview
  * Implement `View.OnClickListener` and connect it to the button
  * Implement `AdapterView.OnItemLongClickListener` and connect it to the listview
* Web browser
  * Remove action bar
    * Edit `res/values/styles.xml`
    * Change "DarkActionBar" to "NoActionBar"
  * Add text field, three buttons, and webview
  * Create variables for all controls and use `findViewById` in `onCreate`
  * Create and set a `WebViewClient`
  * Implement `View.OnClickListener` and connect it to all the buttons
  * Add internet permission to AndroidManifest.xml
    * `<uses-permission android:name="android.permission.INTERNET" />`
  * Create an anonymous class based on `WebViewClient`
    * Override the `onPageStarted` method to update the address bar

### Day 4

* Review assignment (android - contacts)
* Create a project
  * Download and run [the setup app](https://libgdx.badlogicgames.com/download.html)
  * Uncheck everything except "Desktop"
  * Open the project in IntelliJ
  * Run -> Edit Configurations...
  * Change the "Working directory" to point to the `core/assets` subfolder
* Create HelloGame
  * Create `x` and `y`
  * Continuously increment `x`
  * Create `move` method
    * Create `if` statements that use `Gdx.input.isKeyPressed` to change the position
    * Set `xVelocity` and `yVelocity` to `MAX_VELOCITY` in the `if` statements
    * Change `x` and `y` by the `xVelocity` and `yVelocity` multiplied by `Gdx.graphics.getDeltaTime()`
    * Dampen `xVelocity` and `yVelocity`
* Create SuperKoalio
  * Create `x`, `y`, `xVelocity`, and `yVelocity`
  * Load the koala `Texture` and split it by width (18) and height (26)
  * Set `stand` texture to `grid[0][0]`
  * Copy the `move` method from HelloGame
  * Add gravity and jump velocity
  * Set `jump` texture to `grid[0][1]`
  * Use a `FitViewport` so the screen scales as the window is resized
  * Add `walk` animation
* Build as a JAR file
  * Click the "Gradle" tab on the right side of the IntelliJ window
  * :desktop -> Tasks -> other -> dist
  * The JAR file will be in `desktop/build/libs`
