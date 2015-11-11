## Week 6 - Spring

### Day 1

* Create HelloSpring
  * Create project from template
    * Go to [Spring Initializr](https://start.spring.io/)
    * Choose "Gradle Project"
    * Group is `com.theironyard` and artifact is `HelloSpring`
    * Click "Switch to the full version"
    * Check the following options:
      * Web
      * Mustache
      * PostgreSQL
    * Download and unzip the project
    * Import into IntelliJ
    * Choose "Import project from external model" and select Gradle
    * Click Next and Finish
  * MVC
    * Model (SQL)
    * View (HTML)
    * Controller (Java)
  * Create `/person` route that returns HTML
    * `src/main/resources/templates/person.html`
    * `src/main/java/com/theironyard/HelloSpringController.java`
    * Add arguments for name, city and age, and use `@RequestParam` to set default values
  * Create `/person.json` route that returns JSON
    * `src/main/java/com/theironyard/Person.java`
    * `src/main/java/com/theironyard/HelloSpringJsonController.java`
    * Add arguments for name, city, and age, and use `@RequestParam` to set default values
  * Create `/` route that returns HTML
    * `src/main/resources/templates/home.html`
    * Add `home` method to `HelloSpringController`
    * Add `login` method to `HelloSpringController`
* Build JAR file
  * Click the Gradle tab on the right edge of the window
  * HelloSpring -> Tasks -> build -> build
  * It will be in `build/libs`

### Day 2

* Review assignment (spring - microblog)
* Exercise (reverse number)
* Java build systems
  * Ant (2000)
    * First major Java build tool
    * Uses `build.xml`
  * Maven (2004)
    * Introduced downloadable dependencies
    * Uses `pom.xml`
  * Gradle (2012)
    * Customizable, uses a real programming language
    * Can use Maven libraries
    * Uses `build.gradle`
  * IDE-specific projects (IntelliJ and Eclipse)
* PostgreSQL
  * Download and run [Postgres.app](http://postgresapp.com/)
  * Open `psql`
  * `\l`
  * `\du`
  * `CREATE DATABASE hellodb;`
  * `\c hellodb`
  * `CREATE TABLE test (id SERIAL, stuff VARCHAR);`
  * `INSERT INTO test VALUES (DEFAULT, 'hello world');`
  * `SELECT * FROM test;`
  * `DROP TABLE test;`
* HelloDatabase
  * Download and add library: [PostgreSQL Driver](https://jdbc.postgresql.org/download/postgresql-9.4-1205.jdbc42.jar)
  * Change connection URL to `"jdbc:postgresql://localhost:5432/hellodb"`
  * Use `DECIMAL` instead of `DOUBLE`
* Writing direct SQL queries
  * Problems
    * Dialects differ between databases
    * Easy to make typos
    * Going between the database and Java objects is busy work
  * Solutions
    * SQL wrapper libraries: JOOQ
    * Object-Relational Mapping libraries: Hibernate
* Create BeerTrackerSpring
  * Create project from template with the following options
    * Web
    * JPA
    * Mustache
    * PostgreSQL
  * Create `beertracker` database in psql
  * In `src/main/resources/application.properties` add:
    * `spring.datasource.url=jdbc:postgresql://localhost:5432/beertracker`
    * `spring.jpa.generate-ddl=true`
  * Create `Beer` class that uses `@Entity`, `@Id`, and `@GeneratedValue`
  * Create `src/main/resources/templates/home.html`
  * Create `BeerTrackerController` with a `/` and `/add-beer` route
  * Create `BeerRepository` interface that extends `CrudRepository`
  * Use `@Autowired` to bring the repo into the controller
  * In `/add-beer`, create a `Beer` object and save it to the repo
  * In `/`, add the beers to the `Model`

### Day 3

* Review assignment (spring - microblog continued)
* Exercise (palindrome detector)
* BeerTrackerSpring
  * Add a column
    * Add `Integer calories` to `Beer`
    * Add support for calories in `home.html`
    * Add calories in the `/add-beer` route
  * Add type filter
    * In `home.html`, add links for each beer type
    * Add `findByType` to `BeerRepository`
    * Modify the `/` route to use it if the `type` parameter isn't null
  * Add type and calories filter
    * Add `findByTypeAndCalories` to `BeerRepository`
    * Modify the `/` route to use it if the `type` and `calories` parameters aren't null
    * Add `findByTypeAndCaloriesIsLessThanEqual` to `BeerRepository`
  * More query methods
    * `findFirstByType`
    * `countByType`
    * `findByTypeOrderByNameAsc`
    * [Tutorial](http://www.petrikainulainen.net/programming/spring-framework/spring-data-jpa-tutorial-creating-database-queries-from-method-names/)
  * Add search form
    * In `home.html`, add search form
    * Add `searchByName` to `BeerRepository` with `@Query`
  * Add a user class and do joins
    * Create `User` with `@Table(name = "users")`
    * Create `src/main/resources/templates/login.html`
    * Create `/login` route and return the template in the `/` route
    * Create `/logout` route and add link in `home.html`
    * Create `UserRepository` interface with `findOneByName`
    * Add `UserRepository` to the controller and use it in the `/login` route
    * Add `User` to `Beer` with `@ManyToOne`
    * Edit `home.html` to show the username next to each item
    * Add `List<Beer>` to `User` with `@OneToMany(mappedBy = "user")`
    * Add a `showMine` parameter to the `/login` route and a link to `home.html`
    * Insert a default user at startup by creating an init method with `@PostConstruct`
