# Learn With PluralSight: [Java EE 7: Getting Started][course]

1. Course Overview [[GITHUB][m01.gh]]
2. Java EE: Getting Started [[GITHUB][m02.gh]]
3. Setting up the Java EE Environment [[GITHUB][m03.gh]]
4. Bootstrapping the Java EE Application [[GITHUB][m04.gh]]
5. **Defining the Domain Model** [[GITHUB][m05.gh]]
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

# 5. Defining the Domain Model

## What is a Domain Model?

- describes the business
- system of abstractions
  - that represent an aspect of reality or something of interest
- represented by an object
  - that incorporates both behavior and data
- nouns in our domain (books for a bookstore)
  - are made the focus in order to recognize the domain

## Book Object

```java
public class Book {
    private String    title;
    private String    description;
    private Float     unitCost;
    private String    isbn;
    private Date      publicationDate;
    private Integer   nbOfPages;
    private String    imageURL;
    private Language  language;

    // constructors, accessors, behavior
}
```

## What is Object Relational Mapping?

- brings databases and objects together
- objects have a transient state
- only available when the JVM is running
- some objects need to be _persisted_
  - meaning that they are stored and can get reused later
- relational databases store state
- mapping b/w objects and tables
  - the principle of ORM is to delegate this task to external tools or frameworks like JPA

## What is Java Persistence API (JPA)?

- maps objects to relational database
- client needs to use the **entity manager**
  - API used to perform database related operations
- persistence objects are called **entities**
- CRUD operations
- query language JPQL
  - allows us to retrieve data w/ and object-oriented syntax


## What is an Entity?

- term _entity_ should be used rather than objects
- _objects_ are instances that just live in memory
- _entities_ are objects that live shortly in memory and persistently in a database
- mapped to a database, and need a
- _persistent identity_ that uniquely identifies them in the database
- JPA brings eye-level of obstruction by _removing all the JDBC boilerplate_ code of mapping attributes to database columns
- yet JPA uses JDBC underneath and relies on it to connect to the database

## Book Entity w/ JPA

```java
@Entity
public class Book {
  @Id
  @GeneratedValue(strategy = GenerationType.AUTO) // increments value
  private Long id;
  
  @Column(length = 200)
  private String title;

  @Column(length = 10000)
  private String description;

  @Column(name = "public_date")
  @Temporal(TemporalType.DATE)
  private Date publicationDate;
  //...
}
```

## Deployment Descriptor

`persistence.xml`
```xml
<persistence xmlns:xsi="...">
  <persistence-unit name="bookStorePU">
    <properties>
      <property
        name="javax.persistence.schema-generation.database.action"
        value="drop-and-create" />
      <property
        name="javax.persistence.schema-generation.scripts.action"
        value="drop-and-create" />
      <property
        name="javax.persistence.schema-generation.scripts.create-target"
        value="bookStoreCreate.ddl" />
    </properties>
  </persistence-unit>
</persistence>
```

## Anatomy of the BookStore Application

```text
Angular {}
Java EE { Book }
<-JDBC->
Database
```

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