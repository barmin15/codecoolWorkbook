# Enterprise module (Java branch)

### Java Enterprise and Spring

#### What are the possible uses of reflection?
Reflection gives us information about the class to which an object belongs and also the methods of that class that can be executed by using the object.

#### What is Spring?
Spring is a framework for Java, that provides infrastructure for building, Java based applications following the Inversion of Control principle.ő

#### What is Spring Boot?
Java Spring Boot is an open-source tool that makes it easier to use Java-based frameworks to create microservices and web apps.

#### What is the major difference between the Standard edition (JSE) and Enterprise edition (JEE)? You can choose Spring (Spring Boot) instead of JavaEE. Focus on comparing them.
    Standard Edition: 
        develop APIs for desktop
        good for starting java development
        does not include authentication

    Enterprise Edition:
        suitable for expeirenced developers
        Mainly used for Web application
        Comes with build in authentication

#### What are the advantages of the Spring Framework? Focus on the Core part.
It makes the developers jobs easier with the Inversion of Control, however, we don't exactly know where they are coming from. 

#### What is a servlet? What is the purpose of DispatcherServlet in Spring?
Servlet is a Java Object, that goes through http messages, and helps us generate a answer. 

#### When do you use RestControllers, when just simple Controllers?
Rest controllers for Json data structures, and Controllers for Html (viewable) data structures.

#### What is Spring Application Context?
It is responsible for instantiating, configuring, and assembling the beans.

#### What are the main ways to define a bean in the Application Context?
With annotations (@Bean), or with XML configuration

#### Difference between .jar and .war files.
JAR and WAR files serve different purposes in the Java ecosystem. JAR files are used for packaging and distributing reusable Java libraries,
while WAR files are designed specifically for deploying web applications.

#### What are the major differences between Maven, Ant and Gradle?
Both are used to build and manage software projects.
    
    Gradle
        Gradle's construction time is short and fast
        Gradle's scripts are much shorter and cleaner
        It uses domain specific language (DSL)
    
    Maven
        Maven's performance is slower than Gradle's
        Maven's scripts are slightly longer than Gradle's
        It uses XML

#### What is Maven used for?
Maven is used to build and manage software projects.

#### What does a pom.xml file contains in Maven?
Information of project and configuration information for the maven to build the project such as dependencies, build directory, 
source directory, test source directory, plugin, goals etc.

### Object Relational Mapping, JPA

#### What is an ORM? What are the benefits, when to use?
ORM (object Relational Mapping) is a way to align is programming code with database structures. We use it, when our application wants to access data from databases, 
or want to add data to a database (built in methods, instead of queries).

#### What is the difference between JDBC and JPA? Which are the advantages and disadvantages of each? Give a general overview.
With JDBC we have to write the queries manually, while with JPA we can invoke a method, that will write the query for us.
JDBC is faster, since there is another level to be done with JPA.

#### What is Hibernate? What are the advantages, limitations?
Hibernate is a tool for ORM. It gives us a framework for Database mapped objects.

#### Name 3 different annotations used in JPA, what can they do for you?
    @Entity -> a marker annotation which indicates that this class is an entity.
    @OneToOne -> there is a one to one connection for a value in another value in another table.
    @Table -> same as entity but table
    @Id -> this value will be an id.

#### What is object-relational impedance mismatch?
the mismatch between the way data is represented and manipulated in an object-oriented programming language, and the way it is represented and
manipulated in a relational database.

#### What is a JpaRepository? What are the 2 main methods to define queries in them?
Jpa repository is the logic class that will handle the communication between our database and our application. 
    Example Methods:
        Get
        FindById
        DeleteById

#### Why is the Set preferred over List when we want to store OneToMany relations?
We dont want to store or handle duplications.

#### What kind of inheritance strategies are available? Which annotations are used to solve this?
With the @Inheritance we can set up the way our tables handle inheritance
This will achieve the same as the ManyToMany OneToMany etc.