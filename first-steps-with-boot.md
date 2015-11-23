# First Steps with Spring Boot


- boot is opinionated way to pull together best of breed components
- optimized for apps and services that live in the cloud
- goes nicely with the trend towards microservices
- if u want to do small batches of work u need to break things into small independently deployable services
- most organizations have a wiki page that lists the exhaustive list of things youll need to do to get the service stood up
- spring boot provides a way to remove the wiki page
- its got support for all manner of things
- get started w/ spring boot at start.spring.io
- choose the bits u like; in this article well choose everything and just run with it - kitchen sink experience!
- lets choose jpa / vaadin / rest repositories / thymeleaf / actuator / h2
- naturally you should write a test, so heres a simple unit test
- but we talked about continuous and safe delivery of software into production. this is important.
- code complete != prod ready
- spring boot aims to help w/ the things that frustrate our ability to move applications into production.
- part of those things include operations concerns: things that're important but that don't differentiate the application.
- these include thigns that almost all applications need but that nobody enjoys or relishes the opportunity to write. (metrics, health, info, etc)
- there are many ways to access ths information, naturally
- metrics are impkortant: you cant improve what u cant measure. metrics can be collected via REST endpoints as well as through metric aggregation and visualization systems
- once uve made ur application production ready ull need to run it.
- here spring boot has multiple options; of coure u can create a .war and deploy it. or u can choose a .jar
- many orgs version control  tomcat w/ their app
- this implies a smell
- .jar fixes this. the goal isnt to save on shared CLASSPATH librarie space.
- more modern langs like Go dont even have shared dynamic linking
- u can run this .jar anywhere using Spring Boot's exectuable jar feature ; just check it into init.d or system.d
- or, as is very common, just run int on cloud infrastructre: Docerk, OpenShift, Heroku, Google App Engine, Cloud Foundry
