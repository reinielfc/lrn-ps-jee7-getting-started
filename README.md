# Learn With PluralSight: [Java EE 7: Getting Started][course]

1. Course Overview [[GITHUB][m01.gh]]
2. **Java EE: Getting Started** [[GITHUB][m02.gh]]
3. Setting up the Java EE Environment [[GITHUB][m03.gh]]
4. Bootstrapping the Java EE Application [[GITHUB][m04.gh]]
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

# 2. Java EE: Getting Started

## Understanding Java EE

- Java Enterprise Edition
- extension of Java SE (Standard Edition)
- simplify enterprise application
- simple programming model
- standard
- Java community process
- multiple implementations

### Standard

- at first, you were locked to a proprietary solution (based on standard)
- then open-source frameworks came along (open but not standard), locked to a simple implementation
- Java EE is based on standards
- goes through standardization process of JCP
- described in specification
- portable

### Several Implementations

- GlassFish, open-source, by Oracle
- Apache TomEE, open-source, by Apache
- Payara Server, open-source, derived from GlassFish, by Payara Services Ltd
- JBoss, open-source, by RedHat
- WildFly, open-source, by RedHat, JBoss Community Edition

## What is Angular?

- JS framework
- building front-end web apps
- makes HTML more expressive
- powerful data binding
- built-in back-end comminication
- ecosystem
- supports TypeScript

### TypeScript

- open-source
- superset of JS
- static typing
- OOP
- large apps
- transpiles to JS

## Anatomy of the BookStore App

```text
Browser
<-HTTP, HTML->
Angular App
<-HTTP, JSON->
JavaEE {Java EE App, Arquillian Test Framework}
<-> 
DB
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