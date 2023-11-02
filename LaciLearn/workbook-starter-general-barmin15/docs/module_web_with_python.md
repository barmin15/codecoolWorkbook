# Web Module Questions

### Functional patterns

#### What is a callback function?
A callback function is a function passed as an argument to another function.
  Example: 
    'document.getElementById("button").addEventListener("click", onClick());'
      -> in this case onClick() is a callback function

#### What is ECMA script ? What is the difference between Javascript & ECMA script ?
ECMA script is a blueprint for creating browser based scripting languages. Javascript is an implementation of this blueprint.

#### What is the difference between `let` & `var` ?
Let keyword's scope is block scope while var's scope is a function scope.

#### Write an example where using the `var` declaration instead of the `let` could create a hard to debug code.
  Example:
    ```function processArray(array) {
        for (var i = 0; i < array.length; i++) {
        console.log('Element ', array[i]);
      }

        console.log('I can use variable i outside the loop ', i);
    }```
    In this case i cant create another variable called i or call another for with i variable in the processArray function.

#### Give a practical example where you would use the `reduce` function in javascript.
  Example: 
    ```const myNums = [1,2,3,4,5];
    var sum = myNums.reduce((accumulator, currentValue) => {
      return accumulator + currentValue
    },0);```
    Here the answer would be 15.
    The recude method summed numbers values the array. 

#### Give a practical example where you would use the `map` function in javascript.
  Example:
    ```var arr = [1,2,3];
    var doubledArr = arr.map((item) => item * 2);```
    Here we doubled all values in the 'arr' array.

#### Give a practical example where you would use the `filter` function in javascript.
  Example:
    ```var arr = [1,2,3,4,5];
      var evenArr = arr.filter((item) => item % 2 == 0);```
      Here we created a new array with only the even values of the original array.

### Web basics

#### What is a web server?
A web server has two parts. The SOFTWARE and the HARDWARE.
  Software:
    On the software side, a web server includes several parts that control how web users access hosted files. At a minimum, this is an HTTP server. An HTTP server is software that understands URLs (web addresses) and HTTP.
  Hardware: 
    On the hardware side, a web server is a computer that stores web server software and a website's component files
    (Html, css, js) -> files

#### Explain the client-server architecture.
In the client-server architecture, when the client computer sends a request for data to the server through the internet, the server accepts the requested process and deliver the data packets requested back to the client.  

#### What is the difference between synchronous and asynchronous execution?
Synchronous code executes one line of code after the other, while asynchronous code allows multiple lines of code to run at the same time.

#### What is `npm`? Why is it useful?
Node Package Manager or also known as npm is the worlds largest sofware libarary. It is a package manager for Node.js. It helps javascript developers to share packaged modules of code.

#### What is the difference between the `depdendencies` & `devDependencies` in a `package.json` file ?
Dependency is an object that contains the library, which your project requires for production environments and functioning effectively. devDependencies are those packages in the package.json file that you need only for project development purposes. Example- Babel, Webpack, etc.

#### What would be the impact of javascript `fetch` if it was not asyncronous ?
There would be a big/small delay in the code, while we wait for the fetch to resolve.

#### What benefits would it bring to a developer to use the `Postman` application ?
It's a lot easier than using curl in the terminal. It is a good way to test, the responisbility of your API.

#### List the parts of the URL.
https://www.codecool.com:80/student/progbas?sortname=asc&age=28#daytime
  Parts:
    sceme: 'https://'
    subdomain: 'www'
    domain: 'codecool'
    top level domain: 'com'
    path: '/student/progbas'
    query string params: '?sortname=asc&age=28'
    fragment: '#daytime'

#### What is query parameter?
It's a way to send information to the server about the filtering of response data through the URL.

#### What kind of HTTP status codes do you know?
  Examples:
    200 'OK' - everything is ok
    404 - not found
    400 - bad request
    403 - forbidden
    401 - unauthorized
    500 - internal server error

#### How does an HTTP Request look like? What are the most relevant HTTP header fields?
There are 3 parts of a Http request : Request line, Header, Body
  Request line: method + url (+ http1.1)
  Header: authorization, content type etc.
  Body: Json or some kind or bundled data (payload)

#### How does an HTTP Response look like? What are the most relevant HTTP header fields?
It contains 3 parts, the status line, headers and body.
  Status line: protocol + status code. A typical status line looks like: HTTP/1.1 404 Not Found.
  Headers: Content-type + a lot of information can be here
  Body: Not all responses have this, but there is some kind of payload here.

#### Why should you ignore the `node_modules` folder in `.gitignore` ?
It can take up a lot of space, and it conforms to your own device's architecture, so it may not work properly with another device.

### Rest API: Serve and Fetch

#### Why is it recommend for a developer to use the http methods `get`, `put`, `delete` ?
It is a good convenction to use, since the server/client side will understand the request more. 

#### How does a `POST` request look like when it is made from a web browser (on the front end written) ?
``fetch('url',{ headers: {
      'Accept': 'application/json',
      'Content-Type':'application/json'
    },
    {
      method: 'POST',
      body: 'JSON.stringify('object')
    }
  })
  .then(res => res.json())
  .then(res => console.log(res));``

#### What is an API?
API is a software intermediary that allows two applications to talk to each other. APIs are an accessible way to extract and share data within and across organizations.

#### What is REST API?
REST API conforms to the design principles of REST. REST is a softerarchitecture (for web). For example REST gives us CRUD operations (Create, Read, Update, Delete), it also gives us six guidelines to follow.

#### What is JSON and how do we use it?
Json (javascript object notation) is derived from javascript, it is used to transport and store data. Typically, JSON is used when data is sent from a server to a web page (in a json file the objects key is in a string form). It's name can be misleading, since it is a "programming language independent" format, that many (including) javascript use.

#### What is API versioning ?
API versioning is the practice of managing changes to an API and ensuring that these changes are made without disrupting clients.

#### Give 3 examples of HTTP response status codes ? Explain what each number means.
  Examples:
      200 'OK' - everything is ok
      404 - not found
      400 - bad request
      403 - forbidden
      401 - unauthorized
      500 - internal server error

### Advanced JavaScript

#### How does the `ternary operator` looks like in javascript?
  Example: return num > 5 ? console.log("big num") : console.log("small num");
Ternary operator is a shorter version of the if-else statement used mainly in frameworks, such as REACT where you  can render components with it.

#### How to import a function from another module in JavaScript?
  Example: ```const lib = require('./library') 
    --in another module:
    let area = function (length, breadth) {
        let a = length * breadth;
        console.log('Area of the rectangle is ' + a + ' square unit');
    }

    module.exports = {
        area
    }```
In this case we exported the are function from one module with module.exports, and imported it with require in another module.

#### What is a shallow copy on an object?
Shallow copy is a bit-wise copy of an object, only the reference addresses are copied.

#### What is a callback function? Tell some examples of its usage.
A function that is executed after another function has finished execution.
  Example: 
    'document.getElementById("button").addEventListener("click", onClick());'
      -> in this case onClick() is a callback function

#### What is object destructuring in javascript?
Object destructuring is when we extract properties from objects, and assign them to new variable.

#### What is array destructuring in javascript?
  Example: 
      ```var names = ["laci", "armin"];

         var [laci, armin] = hehe

         console.log(armin + " " + laci)```
Here we decleared an array, and then in the next line we passed arguments (by index number) into the array.

#### What is the spread operator in `js` ?
Spread syntax "expands" an array into its elements, while rest syntax collects multiple elements and "condenses" them into a single element. 

#### What are the differences between the `arrow` function and the regular `function`?
The main differences are :
  syntax
  arrow function doesnt have a 'this' keyword
  both of them can be anonymous, however arrow function can't have a name

#### What is the `import` keyword used for?
Import keyword is used to import modules, and individual exports from those modules. Import is a newer keyword than require.

#### What is the `required` used for?
Require keyword is used to import modules between javascript files. You can only import the whole module unlike with the import keyword.

#### What are template literals?
Template literals are 'backtics' allowing multi-line string, and variables inside the string.
  Example: 
    ``` '`string text ${expression} string text`' ```

### Testing basics

#### What is code coverage? Why is it used?
Code coverage measures the percentage your tests cover your source code. This gives us a good idea, of how much of our code needs testing.

#### What is a test case? What is an assertion? Give examples!
A test case refers to the actions required to verify a specific feature or functionality in software testing. Assertion is checking, if the output matches our result.
  Example: 
    test case: with a function, that adds two numbers together, we call it with 3 and 4.
    assertion: 7 equals the output of our tested function

#### What are the unit testing best practices? (Eg. how many assertion should a test case contain?)
The more the merrier, but even in the worst cases, you have to check for edge cases, to see if the code works fine.
  Example: -1, 00.1, 2, 13103133, 's'

#### What is arrange/act/assert pattern?
Arrange: manage inputs, importing functions, creating input variables.
Act: calling the function with our arguments.
Assert: checking if the result equals our answer

#### How do you test asynchronous code with `jest` ?
Example: 
      ```test('the data is peanut butter', () => {
    return fetchData().then(data => {
      expect(data).toBe('peanut butter');
    });
  });```

we either test with expect() + .toBe() ot with await


#### What is `setup` & `teardown` in jest ?
Often with test cases, we have to initalize starter values, and after we need to clear them, so we have the Beforeeach, and AfterEach hooks in test cases.

  Example: 
        ```beforeEach(() => {
      initializeCityDatabase();
    });

    afterEach(() => {
      clearCityDatabase();
    });

    test('city database has Vienna', () => {
      expect(isCity('Vienna')).toBeTruthy();
    });

    test('city database has San Juan', () => {
      expect(isCity('San Juan')).toBeTruthy();
    });```


#### Give an example when you would use in `jest` the `toBe` & `toEqual` assertions.
We would use the toBe in asynchronous functions, and the toBe in synchronous.

### React basics

#### What benefits does it bring for a developer to use `components` (opposed of writing all the code in a single file) ?
It is more maintanable, more readable, more testable, easier to navigate, easier to render html elements without a long if-else or ternary operator (follows REACT guidlines).

#### What is the difference between Element and Component?
An html element is static, while a REACT component is dynamic, because there can be code defined in it.

#### How do you pass values between components in `react`?
You pass them as props (key, value pairs)

#### What is `key` prop?
React needs every element to render to be unique, thus every chunk of elements under the same parent element needs to have a unique key.

#### How does a child component pass data to it's parent component ?
  Example: 
  parent: 
      ```
      import { useState } from 'react';

  function App() {
  const [data, setData] = useState("no value");

  function testChild(thing){
    setData(thing)
  }
    return (
      <div className="App">
          <Child
          funky = {testChild}
          />
      </div>
    );
  }

  export default App;```

  child: 
    ```
    export default function Child({funky}){

  function onHandle(){
      funky("data's value");
  }

      return <button onClick={(e) => onHandle()}>Add value</button>
  }
    ```
We call the function that was given through the parent to the child as a prop with the value we want to pass as the argument.

#### Write the code to create in JSX an HTML DIV element that has the innerText the contents of the variable `let name = 'Andrew'`

Code:
    ```
    let name = 'Andrew';

    return <>
              <div>{name}<div>
          </>
    ```

#### Write the code to create in JSX an unordered list from the array `let names = ["Mathew", "John", "Maverik"]`

let names = ["Mathew", "John", "Maverik"]
return <>
        <ul>
        {names.map((name, i) => ( <li key={i}>{name}</li> ))}
        </ul>
       </>

#### Write the code to set the background color red of a div in JSX.


return <>
        <div style={{backgroundColor='red'}}></div>
       </>
### Testing react

#### What are unit tests, integration tests? What is the major difference between these two?
Unit Testing	
  It tests small modules or a piece of code of an application or a product	
  It's a quick write-and-run test	

Integration Testing
  Two or more units of a program are combined and tested as a group
  It is slower to run

#### What does `mocking` mean from a testing perspective ? Give an example when you would use it.
Mokcking is used, when the testable unit is depending on another unit, out of our control, so we mock 'mock the logic and the output' of the case/function it depends on to, test the logic of our testable unit.

#### How do you test that function was called `at least` 2 times using `jest` ?
  Example: 
    ```expect(drink).toHaveBeenCalledTimes(2);```
  
With the toHaveBeenCalledTimes() and pass the number (how many times called) as the argument.

#### Name 4 benefits a developer gets from writing tests.
More maintanable, smaller units, readable code, the code works as expected. 

### React patterns

#### What is the difference between Real DOM and Virtual DOM?
Virtual DOM is a blueprint of dom, for what and how it can change. REACT uses this with the ReactDOM.
Virtual dom will never become DOM itself, only the changes, 'nodes' will apply to DOM from Virtual DOM.

#### When adding an item to an array, why is it necessary to pass a new array to the `useState` hook ?
Because 'setData' doesn't know what data is/was, it only overrites the data.

#### Describe what techniques or tools you use to debug a react app.
Always have inspector mode open, console.log()'s can also help, the feedback in the terminal also helps, there is also an extension, called react developer tools that helps.

#### What is the difference between a react `class` component & a `functional` component ?
The older version of react used class based components. Class components implements OOP syntax and principles. It must include the render() method
in order to render DOM elements.

#### Name 3 lifecycle states in a react `functional` component.
  Examples:
    inserting elements into the DOM (mounting)
    updating components in DOM (update)
    removing components from the DOM (unmount)

#### What is conditional rendering in `react` ? Give an example.
If something fits our condition, we render those elements, otherwise we render something else.

#### Write the code that prints to the console `component destroyed` when the component it is part of is removed from the DOM tree.
  Example: 
  ```
    const inDOM = document.body.contains("component");
    if(!inDOM){
      console.log("component destroyed");
    }
  ```
  ```
      class IFrameComponent extends React.Component{
      componentWillUnmount(){
          console.log("Component destroyed.");
      }
  ```

#### Why is there an infinite loop in this code
```function App() {
  const [count, setCount] = useState(0); //initial value of this 
  useEffect(() => {
    setCount((count) => count + 1); //increment this Hook
  }); //no dependency array.
  return (
    <div className="App">
      <p> value of count: {count} </p>
    </div>
  );
}
```

When you use useEffect, you need to specify when a use effect should be called after the component refreshes.

  Example:
    ```
      useEffect(()=>{

      },[])
    ```

#### Why is there an infinite loop in this code
```
  async function App() {
  const [count, setCount] = useState("");
  setCount(count + 1);
  return (
    <div className="App">
      <p> value of count: {count} </p>
    </div>
  );
}
```

Because setCount is a hook, that always refreshes the component.

### Mongo & mongoose

#### What is a database schema ?
A schema is a JSON object that defines the structure and contents of your data

#### Why is the `id` unique in a database ?
Because an id should only identify one object. Each object's id should be different. 

#### What are the advatanges & disadvatages of using `lean()` function in a mongo query ?
  Advantages: 
    find().lean() is way faster than just find
    return them is plain javascript.

  Disadvantages: 
    it doesnt return the getters and setters


#### Write the code to store the object `{name: "Andrew", age: 10}` to a mongo database. You can ignore the part of connection parameters.
  Example:
    ```
          var schema = new mongoose.Schema({
            name: String,
            age: Number
          });
          var User = mongoose.model(“User”, schema);
          var myData = new User({name: "Andrew", age: 10});
          myData.save()
    ```

#### Write the code to delete from a mongo database all employees that are over 18 years. The scheme for an employee is `{name: string, age: int}`. You can ignore the part of connection parameters.


#### Write the code to display in the console from a mongo database the employees who are over 18 years. The scheme for an employee is `{name: string, age: int}`. You can ignore the part of connection parameters.

  ```const result = datas.people.deleteMany({age > 18})```

#### Write the code to update from a mongo database the employees with name='John' and set the new age to 8. The scheme for an employee is `{name: string, age: int}`. You can ignore the part of connection parameters.

  ```db.people.updateMany({name: 'John'},{$set:{age:8}})```

### Authentication (cookies + google)

#### How to properly store passwords?
Store them in a database encrypted.

#### What is encryption and decryption?
Encryption is to change a value by an algorithm and decryption is to change the value back to its original form with an algoryth

#### What is hashing?
Hashing is the practice of transforming a given key or string of characters into another value for the purpose of security. Unlike standard encryption, hashing is always used for one-way encryption, and hashed values are very difficult to decode.

#### What is OAuth2?
OAuth is an open-standard authorization protocol that lets a service use another service without requiring the security details ( username, password, etc.) of the user. 

#### What is the difference between encryption and hashing? When would you use which?
You use encryption when you want to decode it as well. It is very hard to decrypt an encryption.

#### How/where would you store sensitive data (like db password, API key, ...) of your application?
You store it in the enviroment variable.

#### What would you use a session for?
Session is a time period when we interract with the client. So we sould use in when for example a user logs in.
It is managed on the server side.

#### What would you use a cookie for?
Cookies are datas that we send to the server every time we send a request. So we sould use in when for example a user logs in.
It is managed on the client side.

### Mern stack

#### What does `MERN` stand for in the context of web development ?
Mern stack is a full stack application that stands for MongoDb Express React Node that allows you to create a three tier architecture: Front end, Back end, Database

#### What is routing in the context of a `react` app ?
Routing in reactJS is the mechanism by which we navigate through a website or web-application. 

#### What is routing in the context of an `express` app ?
Routing refers to determining how an application responds to a client request to a particular endpoint.

#### What is `CORS` policy ?
Cors policy refers to the ability of your application to communicate with another server from another origin.

#### What advantages does a developer have for using `bootstrap` or `material ui` ?
Bootstrap offers you many advantages, such as saving time and effort on costumizing your application.