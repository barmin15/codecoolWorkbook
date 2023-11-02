# General enterprise questions

## Software engineering

### Architectures

#### What is n-tier (or multi-tier) architecture?
Ármin: N tier architecture is the principle of breaking your application into tiers. A Presentation tier, a 
logic tier and data tier. All running on different hardware. This will make sure, that all layers work independently of each other. Thus making your application more secure, 
and simple to maintain.

#### What are microservices? Advantages and disadvantages?
Microservices are an architectural and organizational approach to software development where software is composed of small independent services
that communicate over well-defined APIs.
    
#### What is Separation of Concerns?
Separation of concern is the practice of breaking your module up into smaller parts, with minimal overlapping between the individual units. 

#### What is a layered design and why is it important in enterprise applications?
Layered architecture patterns are n-tiered patterns where the components are organized in horizontal layers. This is the traditional method for designing most software and is meant to be self-independent.
This means that all the components are interconnected but do not depend on each other.
    
#### What is Dependency Injection?
Dependency Injection is the practice of 'injecting' a value/object into our specified environment, rather than hard coding it into hardcoding into it.

#### What is the DAO pattern? When and how to implement?
The DAO pattern is usually implemented with relational databases in applications. It allows you to separate the logic with 'communicating' with the
database, and your application.

#### What is SOA? When to use?
SOA, or service-oriented architecture, the same as microservices, but larger.

### Testing

#### What are unit test, integration test, system test, regression test, acceptance test? What is the major difference between these?
    Unit tests ensure that code behaves as expected in isolation.
    Integration tests verify that components of the system are working together.
    Regression tests catch issues introduced by changes to the codebase. A
    Aceptance tests ensure that the system meets the requirements of the stakeholders.

#### What is code coverage? Why is it used? How you can measure?
Code coverage measures in percentage, how much of your code is covered in tests, thus giving you an estimation, 
of how much of your code may still not be safe for production.

#### What does mocking mean? How would you do it 'manually' (i. e. without using any fancy framework)?
Mocking is when our testable unit is dependent on another object, that we don't have control over, so we 'mock' the object, so that it behaves how we want.
If we were to manually mock, we could create another object for testing, or we could @Overrite the methods inside the object.

#### What is a test case? What is an assertion? Give examples!
A test case is the whole logic your test will follow, while assertion is the condition at the end that will evaluate to a boolean. 

#### What is TDD? What are the benefits?
Test driven development is when you write test for your application before you write the actual code for it. 

#### What are the unit testing best practices? (Eg. how many assertion should a test case contain?)
    write good names
    create simple tests
    aim for maximum test coverage
    ONE ASSERTION IN ONE TEST CASE

#### What is arrange/act/assert pattern?
It is a design pattern for unit tests. First we arrange the data, then we call the logic and lastly we assert the two values.

### DevOps

#### What is continuous integration? Why is CI important?
Continuous integration is when all developers push their to the same big code base, where it gets tested and then built. It works well with AGILE.

#### Why are tests important in the CI workflow?
In order to truly know if your code works, you need to use tests, since it automatically gets pushed to the whole code base.

#### Name some software that help the CI workflow!
Github, gitlab.

#### What is Continuous Delivery?
It is the development style, when if you push your code, it gets tested, and if all tests pass it gets integrated into the code. The code is always ready for deployment, but 
a manual extra is required to actually deploy it, unlike Continuous Deployment.

#### What is Continuous Deployment?
It is the development style, when if you push your code, it gets tested, and if all tests pass, it pushes your code directly to the deployed product.

#### What is DevOps?

### Software Methodologies

#### What kind of software-lifecycle models do you know?
Most important for us is AGILE and SCRUM.
    Agile:
        Involves breaking the project into phases and emphasizes continuous collaboration and improvement.
    Scrum:
        It is an 'Implementation' of agile methodology.
How do they work?
Interpersonal communication is very important. The software is more important than the documentation. Working with the client is 
more important than the contract. Flexibility is very important. 

#### What is a UML diagram? What kind of diagram types do you know?
The purpose of this is visually represent a system along with it's main roles and classes, in order to better understand it.

Other diagrams that we know, are: Class diagram, Activity diagram, Sequence diagram, Communication diagram, State diagram, Timing diagram.

#### What is a UML class diagram? What are the typical elements?
Its purpose is to show us the structure of a system with its main classes and their attributes.

#### What kind of design patterns do you know? Bring at least 3 examples.
There are three main types
    Creational (factory, singleton, abstarct factory, dependency injection)
    Structural 
    Behavioral


#### What is the purpose of the Iterator Pattern?
This pattern is used to get a way to access the elements of a collection object in sequential manner without any need to know 
its underlying representation.

#### What do you know about the SOLID principles?
Helps make object-oriented designs more understandable, flexible, and maintainable.
Single resp, open-closed, liskov subs, interface segr, dependency inverson. 

#### How would you separate data storage code and business logic code (which uses stored data) in an application?
On a different layer, with just as much connection between them, as needed.

## Computer science

### Data Structures
#### What is the difference between Stack and Queue data structure?
Stack follows the LIFO design, while queue follows the FIFO design.

#### What is a graph? What are simple graphs? What are directed graphs? What are weighted graphs?
They are data structure objects, showing some kind of relationship between datas.

#### What are trees? What are binary trees? What are binary search trees?
Ármin: Trees are data structures. A simple Tree structure will consist of parent and child nodes.
A binary tree structure will consist of always one parent node, and two child nodes, child nodes will either have value or be null.
A binary search tree is like a binary tree, but very node to a node's right will be bigger than the node. This makes it a very
easy data structure to search on.

#### How can you store graphs in programs? What are the advantages/disadvantages per each?
Example, Linked List etc. It can be good or bad depending on the size type and more of the data. It takes a constant O1 time to 
hash, and get the stored element. (key can only be immutable).  

#### What are graph traversal algorithms? What is BFS, how does it work? What is DFS, how does it work?
Two types. you select a starting point and only go over to the next, when you've seen all the options. And the nest one is, when you traverse through the whole thing,
and then do the whole way to the end point in another way, until you've been through the whole graph.  

#### How does HashMap work?
It contains key value pairs, it hashes the key, and stores it randomly in memory, it 

#### Why is it important for keys in a hashmap to have an immutable type? (Consider string for example.)
An object is immutable when its state doesn't change after it has been initialized. For example, String is an immutable class and, once instantiated ,
the value of a String object never changes.

Immutability allows us to get the same hash code every time for a key object.

### Algorithms
#### What is QuickSort? Describe the main logic of this sorting algorithm.
Quicksort works by choosing a pivot (element) and sorting all elements, so that to the right of the pivot all elements are greater that it,
and to the left all elements are smaller. This means our pivot is on the right index. Repeat until all elements are on the right index. 

## Software design

### Security

#### What is OAuth2
It refers to the ability of multiple web based servers talking to each other, to access your data, without the need for your password.

#### What is Basic Authentication?
Basic Authentication is a method for an HTTP user agent (e.g., a web browser) to provide a username and password when making a request. 
When employing Basic Authentication, users include an encoded string in the Authorization header of each request they make.

#### What is CORS, why it’s needed in browsers?
CORS is a way for web based applications to talk to each other, when they are running on different servers.

#### How can you initialize a CSRF attack?
With a link, or picture or anything that runs a script in the background.

#### What is JWT used for? Where to store it on client side?
JWT is a Json Web Token, that is used for authentication/authorization beetween the client and the server. Usually On the client side
you either store in the session/local storage or in a cookie. 

### Threaded programming

#### When do you need to use threads in an application?
When you want to maximize the performance of your application. This will lead to simultaneous logics working at the same time. 

#### What is a daemon thread?
Daemon thread in Java is a low-priority thread that performs background operations such as
garbage collection, finalizer, Action Listeners, Signal dispatches, etc.
Daemon thread in Java is also a service provider thread that helps the user thread.

#### What is the difference between concurrent and parallel execution of code?
A concurrent programming language is defined as one which uses the concept of simultaneously executing processes or threads of execution
as a means of structuring a program.

A parallel language is able to express programs that are executable on more than one processor.

#### What is the most important problem developers are faced when using threads?
Ensuring that all threads execute a given sequence in the correct order.

#### In what kind of situations can deadlocks occur? 
When two threads are waiting for each other to finish.

#### What are possible ways to prevent deadlocks from occurring?
If there is a defined logic for threads to start and end.

#### What does critical section or critical region mean in the context of concurrent programming?
Critical section comes when two different threads are trying to work with the same class or data, and the value will not be 
as expected because of this.

    