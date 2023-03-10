# Learn With PluralSight: [Java EE 7: Getting Started][course]

1. Course Overview [[GITHUB][m01.gh]]
2. Java EE: Getting Started [[GITHUB][m02.gh]]
3. Setting up the Java EE Environment [[GITHUB][m03.gh]]
4. **Bootstrapping the Java EE Application** [[GITHUB][m04.gh]]
5. Defining the Domain Model [[GITHUB][m05.gh]]
6. Adding a Transactional Repository [[GITHUB][m06.gh]]
7. Testing the Java EE Application [[GITHUB][m07.gh]]
8. Validating Data [[GITHUB][m08.gh]]
9. Injecting Beans [[GITHUB][m09.gh]]
10. Exposing a REST Service [[GITHUB][m10.gh]]
11. Documenting the REST Service [[GITHUB][m11.gh]]
12. Setting up the Angular Environment [[GITHUB][m12.gh]]
13. Bootstrapping the Angular Application [[GITHUB][m13.gh]]
14. Designing the User Interface [[GITHUB][m14.gh]]
15. Navigating Through Components [[GITHUB][m15.gh]]
16. Invoking the REST Service [[GITHUB][m16.gh]]
17. Revisiting the Application [[GITHUB][m17.gh]]

# 4. Bootstrapping the Java EE Application

1. create app folder
2. create maven dir structure
3. add pom.xml
4. install JavaEE dependencies
5. add minimum Java code

## Maven Archetype

- project templating toolkit
- generating maven projects
- using best practices
- create archetypes
- reuse existing archetypes

## Maven Directory Structure

- `bookstore-back`
  - `src`
    - `main`
      - `java`: JavaEE code
      - `resources`: JavaEE configuration 
      - `webapp`: JavaEE web configuration
    - `test`: Test classes and configuration
      - `java`
      - `resources`
  - `target`: Generated artifacts
  - `pom.xml`: Configuration and dependencies

## Java EE Dependencies

```xml
<project xmlns:xsi="...">
    <groupId>com.pluralsight.javaee-getting-started</groupId>
    <artifactId>bookstore-back</artifactId>
    <version>1.0</version>
    <packaging>war</packaging> <!-- Web Archive -->
    
    <dependencies>
        <dependency>
            <groupId>javax</groupId>
            <artifactId>javaee-web-api</artifactId>
            <version>7.0</version>
        </dependency>
    </dependencies>
</project>
```

## Running the Java EE Application

Wildfly

- Java EE runtime
- hides technical complexity
- hosts applications
- handles complex low-level details
- administrates the apps

## Java EE Application

- aggregation of components
- configuration
- web resources
- business component
- database access components

## Packaging

- assemble components together
- Web Archive (war)
- deploy it into WildFly
- has standard format
- ready to run

## Maven Build Lifecycle

- **validate** the project,
- **compile** the source code,  
- **test** the compiled code (using JUnit), if the tests pass, then
- **package** compiled code into a war,
- **verify** by running integration tests (with Arquillian), to ensure quality criteria are met  
- **install** package into local repository,

## Bookstore App Deployment

```text
Browser
<-(HTTP, HTML)->
Angular { }
<-(HTTP, JSON)->
Java EE { WildFly @ localhost:8080 }
<->
Database
```

## Demo

- Compile
- Package
- Start WildFly
- Deploy the war
- Execute the app
- Check WildFly admin console


[course]: https://app.pluralsight.com/library/courses/java-ee-getting-started
[m01.gh]: https://github.com/reinielfc/lrn-ps-jee7-getting-started/tree/main
[m02.gh]: https://github.com/reinielfc/lrn-ps-jee7-getting-started/tree/02-JavaEE-GettingStarted
[m03.gh]: https://github.com/reinielfc/lrn-ps-jee7-getting-started/tree/03-SettingUpTheJavaEeEnvironment
[m04.gh]: https://github.com/reinielfc/lrn-ps-jee7-getting-started/tree/04-BootstrappingTheJavaEeApplication
[m05.gh]: https://github.com/reinielfc/lrn-ps-jee7-getting-started/tree/05-DefiningTheDomainModel
[m06.gh]: https://github.com/reinielfc/lrn-ps-jee7-getting-started/tree/06-AddingATransactionalRepositoryzoom
[m07.gh]: https://github.com/reinielfc/lrn-ps-jee7-getting-started/tree/07-TestingTheJavaEeApplication
[m08.gh]: https://github.com/reinielfc/lrn-ps-jee7-getting-started/tree/08-ValidatingData
[m09.gh]: https://github.com/reinielfc/lrn-ps-jee7-getting-started/tree/09-InjectingBeans
[m10.gh]: https://github.com/reinielfc/lrn-ps-jee7-getting-started/tree/10-ExposingARestService
[m11.gh]: https://github.com/reinielfc/lrn-ps-jee7-getting-started/tree/11-DocumentingTheRestService
[m12.gh]: https://github.com/reinielfc/lrn-ps-jee7-getting-started/tree/12-SettingUpTheAngularEnvironment
[m13.gh]: https://github.com/reinielfc/lrn-ps-jee7-getting-started/tree/13-BootstrappingTheAngularApplication
[m14.gh]: https://github.com/reinielfc/lrn-ps-jee7-getting-started/tree/14-DesigningTheUserInterface
[m15.gh]: https://github.com/reinielfc/lrn-ps-jee7-getting-started/tree/15-NavigatingThroughComponents
[m16.gh]: https://github.com/reinielfc/lrn-ps-jee7-getting-started/tree/16-InvokingTheRestService
[m17.gh]: https://github.com/reinielfc/lrn-ps-jee7-getting-started/tree/17-RevisitingTheApplication