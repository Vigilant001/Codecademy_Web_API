# Javascript Basics
** Strings, Console log, Math Operators, Increments, Literals, Typeof **
```javascript 

    console.log('Teaching the world how to code'.length);
    // gives us the length of string

    // Use .toUpperCase() to log 'Codecademy' in all uppercase letters
    console.log('Codecademy'.toUpperCase());

    // Use a string method to log the following string without whitespace at the beginning and end of it.
    console.log('    Remove whitespace   '.trim());

    // Using math operators
    console.log(Math.floor(Math.random()*100));
    console.log(Math.ceil(43.8));
    console.log(Number.isInteger(2017));

    // increment and decrement operator
    let gainedDollar = 3;
    let lostDollar = 50;
    gainedDollar++;
    lostDollar--;

    // String interpolation using template literal
    let myName = 'James';
    let myCity = 'Petaluma';
    console.log(`My name is ${myName}. My favorite city is ${myCity}`);

    // typeof operator
    let newVariable = 'Playing around with typeof.';
    console.log(typeof newVariable);
    newVariable = 1;
    console.log(typeof newVariable);


```
# Conditional Statements
** If Else, Truthy/ Falsy, Ternary, **

```javascript 

    // if else statement
    let hungerLevel = 7;

    if (hungerLevel>7) {
    console.log('Time to eat!');
    } else {
    console.log('We can eat later!');
    }

    // logical operators ( && || ! ) 
    let mood = 'sleepy';
    let tirednessLevel = 6;

    if (mood ==='sleepy' || tirednessLevel>8) {
    console.log('time to sleep');
    } else {
    console.log('not bed time yet');
    }

    // Truthy and Falsy
    let wordCount = 1;

    if (wordCount) {
    console.log("Great! You've started your work!");
    } else {
    console.log('Better get to work!');
    }
        // logs - 'Great! You've started your work!'
    let favoritePhrase = '';

    if (favoritePhrase) {
    console.log("This string doesn't seem to be empty.");
    } else {
    console.log('This string is definitely empty.');
    }
        // logs - 'This string is definitely empty.'

    // Operation Left to Right
    let tool = 'marker';
    let writingUtensil = tool || 'pen';

    console.log(`The ${writingUtensil} is mightier than the sword.`);
        // logs - 'The marker is mightier than the sword'

    // Ternary Operator ? : (is it this, then run next, if not run after colon)
    let favoritePhrase = 'Love That!';

    (favoritePhrase === 'Love That!') ?
    console.log('I love that!') :
    console.log("I don't love that!");

    // Else if Statements
    let season = 'summer';

    if (season === 'spring') {
    console.log('It\'s spring! The trees are budding!');
    } else if (season === 'winter'){
    console.log('It\'s winter! Everything is covered in snow.');
    } else if (season === 'fall'){
    console.log('It\'s fall! Leaves are falling!');
    } else if (season === 'summer'){
    console.log('It\'s sunny and warm because it\'s summer!');
    }
    else {
    console.log('Invalid season.');
    }

    // Switch Case
    let athleteFinalPosition = 'first place';

    switch (athleteFinalPosition) {
    case 'first place':
        console.log('You get the gold medal!');
        break;
    case 'second place':
        console.log('You get the silver medal!');
        break;
    case 'third place':
        console.log('You get the bronze medal!');
        break;
    default:
        console.log('No medal awarded.');
        break;
    }

    // extra note: { code } = a 'block of code' which is handled all together by the compiler
    // ; used at the end of a line is like a coding period

```
# Functions
** If Else, Truthy/ Falsy, Ternary, **

```javascript 

    // Function Declaration
        function getReminder() {
    console.log('Water the plants');
    }

    // Calling a function
    function sayThanks() {
        console.log('Thank you for your purchase! We appreciate your business.');
      }
      sayThanks();
      sayThanks();

    // Function Parameters
        function sayThanks(name) {
    console.log('Thank you for your purchase '+ name + '! We appreciate your business.');
    }
    sayThanks('Cole');

    // Default Parameters (ES6)
        function makeShoppingList(item1 = 'milk', item2 = 'bread', item3 = 'eggs'){
    console.log(`Remember to buy ${item1}`);
    console.log(`Remember to buy ${item2}`);
    console.log(`Remember to buy ${item3}`);
    }

    // Returning a Function
        function monitorCount(rows, columns) {
    return rows * columns;
    }
    const numOfMonitors =
    monitorCount(5,4);

    console.log(numOfMonitors);

    // Helper Functions are also great
        function monitorCount(rows, columns) {
    return rows * columns;
    }
    function costOfMonitors(rows,columns) {
    return monitorCount(rows, columns)*200;
    }
    const totalCost = costOfMonitors(5,4);
    console.log(totalCost);

    // Function Expressions (dont forget these exist)
        const plantNeedsWater = function(day) {
    if (day === 'Wednesday') {
        return true;
    } else {
        return false;
    }
    }
    plantNeedsWater('Tuesday');
    console.log(plantNeedsWater());

    // Arrow Functions (ES6)
    const plantNeedsWater = (day) => {
        if (day === 'Wednesday') {
            return true;
        } else {
            return false;
        }
    };

    // Arrow Function (Concise)
    const plantNeedsWater = day => day === 'Wednesday' ? true : false;
    // Anonymous arrow
    const plantNeedsWater = () => day === 'Wednesday' ? true : false;

    // 


```
# Scope
**  **

```javascript 

    // Block Scope - here the log call on 'skyscraper' throws error
        const city = 'New York City'
    function logCitySkyline() {
    let skyscraper = 'Empire State Building'
    return 'The stars over the '+skyscraper+' in '+city;
    }
    console.log(logCitySkyline());
    console.log(skyscraper);

    // Scope best practice is to put variables inside appropriate functions
        const logVisibleLightWaves = () => {
    let lightWaves = 'Moonlight';
        let region = 'The Arctic';
    if (region === 'The Arctic') {
        let lightWaves = 'Northern Lights';
        console.log(lightWaves);
    }
    console.log(lightWaves);
    };
    logVisibleLightWaves(); // call the function

    // Scope Review:
```
    Scope is the idea in programming that some variables are accessible/inaccessible from other parts of the program.
    Blocks are statements that exist within curly braces {}.
    Global scope refers to the context within which variables are accessible to every part of the program.
    Global variables are variables that exist within global scope.
    Block scope refers to the context within which variables that are accessible only within the block they are defined.
    Local variables are variables that exist within block scope.
    Global namespace is the space in our code that contains globally scoped information.
    Scope pollution is when too many variables exist in a namespace or variable names are reused.

# HTTP Requests
** Resources on the Web **
The internet is made up of a bunch of resources hosted on different servers. The term “resource” corresponds to any entity on the web, including HTML files, stylesheets, images, videos, and scripts. To access content on the internet, your browser must ask these servers for the resources it wants, and then display these resources to you. This protocol of requests and responses enables you view this page in your browser.

This article focuses on one fundamental part of how the internet functions: HTTP.

## What is HTTP?
HTTP stands for Hypertext Transfer Protocol and is used to structure requests and responses over the internet. HTTP requires data to be transferred from one point to another over the network.

The transfer of resources happens using TCP (Transmission Control Protocol). In viewing this webpage, TCP manages the channels between your browser and the server (in this case, codecademy.com). TCP is used to manage many types of internet connections in which one computer or device wants to send something to another. HTTP is the command language that the devices on both sides of the connection must follow in order to communicate.

## HTTP & TCP: How it Works
When you type an address such as www.codecademy.com into your browser, you are commanding it to open a TCP channel to the server that responds to that URL (or Uniform Resource Locator, which you can read more about on Wikipedia). A URL is like your home address or phone number because it describes how to reach you.

In this situation, your computer, which is making the request, is called the client. The URL you are requesting is the address that belongs to the server.

Once the TCP connection is established, the client sends a HTTP GET request to the server to retrieve the webpage it should display. After the server has sent the response, it closes the TCP connection. If you open the website in your browser again, or if your browser automatically requests something from the server, a new connection is opened which follows the same process described above. GET requests are one kind of HTTP method a client can call. You can learn more about the other common ones (POST, PUT and DELETE) in this article.

Let's explore an example of how GET requests (the most common type of request) are used to help your computer (the client) access resources on the web.

Suppose you want to check out the latest course offerings from http://codecademy.com. After you type the URL into your browser, your browser will extract the http part and recognize that it is the name of the network protocol to use. Then, it takes the domain name from the URL, in this case “codecademy.com”, and asks the internet Domain Name Server to return an Internet Protocol (IP) address.

Now the client knows the destination's IP address. It then opens a connection to the server at that address, using the http protocol as specified. It will initiate a GET request to the server which contains the IP address of the host and optionally a data payload. The GET request contains the following text:

GET / HTTP/1.1 Host: www.codecademy.com
This identifies the type of request, the path on www.codecademy.com (in this case, "/") and the protocol "HTTP/1.1." HTTP/1.1 is a revision of the first HTTP, which is now called HTTP/1.0. In HTTP/1.0, every resource request requires a separate connection to the server. HTTP/1.1 uses one connection more than once, so that additional content (like images or stylesheets) is retrieved even after the page has been retrieved. As a result, requests using HTTP/1.1 have less delay than those using HTTP/1.0.

The second line of the request contains the address of the server which is "www.codecademy.com". There may be additional lines as well depending on what data your browser chooses to send.

If the server is able to locate the path requested, the server might respond with the header:

HTTP/1.1 200 OK Content-Type: text/html
This header is followed by the content requested, which in this case is the information needed to render www.codecademy.com.

The first line of the header, HTTP/1.1 200 OK, is confirmation that the server understands the protocol that the client wants to communicate with (HTTP/1.1), and an HTTP status code signifying that the resource was found on the server. The third line, Content-Type: text/html, shows the type of content that it will be sending to the client.

If the server is not able to locate the path requested by the client, it will respond with the header:

HTTP/1.1 404 NOT FOUND
In this case, the server identifies that it understands the HTTP protocol, but the 404 NOT FOUND status code signifies that the specific piece of content requested was not found. This might happen if the content was moved or if you typed in the URL path incorrectly or if the page was removed. You can read more about the 404 status code, commonly called a 404 error, here.

## An Analogy:
It can be tricky to understand how HTTP functions because it's difficult to examine what your browser is actually doing. (And perhaps also because we explained it using acronyms that may be new to you.) Let's review what we learned by using an analogy that could be more familiar to you.

Imagine the internet is a town. You are a client and your address determines where you can be reached. Businesses in town, such as Codecademy.com, serve requests that are sent to them. The other houses are filled with other clients like you that are making requests and expecting responses from these businesses in town. This town also has a crazy fast mail service, an army of mail delivery staff that can travel on trains that move at the speed of light.

Suppose you want to read the morning newspaper. In order to retrieve it, you write down what you need in a language called HTTP and ask your local mail delivery staff agent to retrieve it from a specific business. The mail delivery person agrees and builds a railroad track (connection) between your house and the business nearly instantly, and rides the train car labeled "TCP" to the address of the business you provided.

Upon arriving at the business, she asks the first of several free employees ready to fulfill the request. The employee searches for the page of the newspaper that you requested but cannot find it and communicates that back to the mail delivery person.

The mail delivery person returns on the light speed train, ripping up the tracks on the way back, and tells you that there was a problem "404 Not Found." After you check the spelling of what you had written, you realize that you misspelled the newspaper title. You correct it and provide the corrected title to the mail delivery person.

This time the mail delivery person is able to retrieve it from the business. You can now read your newspaper in peace until you decide you want to read the next page, at which point, you would make another request and give it to the mail delivery person.

## What is HTTPS?
Since your HTTP request can be read by anyone at certain network junctures, it might not be a good idea to deliver information such as your credit card or password using this protocol. Fortunately, many servers support HTTPS, short for HTTP Secure, which allows you to encrypt data that you send and receive. You can read more about HTTPS on Wikipedia.

HTTPS is important to use when passing sensitive or personal information to and from websites. However, it is up to the businesses maintaining the servers to set it up. In order to support HTTPS, the business must apply for a certificate from a Certificate Authority.

 

# Rest (REST)
** REpresentational State Transfer **
REST, or REpresentational State Transfer, is an architectural style for providing standards between computer systems on the web, making it easier for systems to communicate with each other. REST-compliant systems, often called RESTful systems, are characterized by how they are stateless and separate the concerns of client and server. We will go into what these terms mean and why they are beneficial characteristics for services on the Web.

# RPS Game x99
** Solution Notes **

In the project folder, notice the "package.json" file. 
This file is used for telling NPM what to load when "install" commanded

```javascript

const randomInteger = n => Math.floor(Math.random() *n);
// here is a great function expression to use for generating whole number randoms

console.log(`
 // allows for putting mulit lines for log return
`);

```

# Arrays
** for the data structures **

```javascript

// here is an array and we are setting listItem to be the first element.
const famousSayings = ['Fortune favors the brave.', 'A joke is a very serious thing.', 'Where there is love there is life.'];

let listItem = famousSayings[0];
console.log(listItem);

```
note: Variables declared with the const keyword cannot be reassigned. However, elements in an array declared with const remain mutable. 
```javascript

// here is an array and we use .length to find how many elements.
const objectives = ['Learn a new languages', 'Read 52 books', 'Run a marathon'];

console.log(objectives.length);

```
.push() method adds to an array!

```javascript

const chores = ['wash dishes', 'do laundry', 'take out trash'];

chores.push('do one situp','do one yawn');
console.log(chores);

```
You might also see .push() referred to as a destructive array method since it changes the initial array.

.pop() array method removes the last item of an array. It does not take any arguments, only removes last element.
```javascript
const chores = ['wash dishes', 'do laundry', 'take out trash', 'cook dinner', 'mop floor'];

chores.pop();
console.log(chores);

```
Some arrays methods that are available to JavaScript developers include: .join(), .slice(), .splice(), .shift(), .unshift(), and .concat() amongst many others.
```javascript

// here .slice will take only array items between and including 1 to 4.
console.log(groceryList.slice(1, 4));

``` 
### Nested Arrays
```javascript

const nestedArr = [[1], [2, 3]];

console.log(nestedArr[1]); // Output: [2, 3]
console.log(nestedArr[1][0]); // Output: 2
// here the output is 2 because we start with the index 1 and find within it index 0

```
### Arrays Review
Arrays are lists that store data in JavaScript.
Arrays are created with brackets [].
Each item inside of an array is at a numbered position, or index, starting at 0.
We can access one item in an array using its index, with syntax like: myArray[0].
We can also change an item in an array using its index, with syntax like myArray[0] = 'new string';
Arrays have a length property, which allows you to see how many items are in an array.
Arrays have their own methods, including .push() and .pop(), which add and remove items from an array, respectively.
Arrays have many methods that perform different tasks, such as .slice() and .shift(), you can find documentation at the Mozilla Developer Network website.
Some built-in methods are mutating, meaning the method will change the array, while others are not mutating. You can always check the documentation.
Variables that contain arrays can be declared with let or const. Even when declared with const, arrays are still mutable. However, a variable declared with const cannot be reassigned.
Arrays mutated inside of a function will keep that change even outside the function.
Arrays can be nested inside other arrays.
To access elements in nested arrays chain indices using bracket notation.

# Project Secret Message

```javascript
let secretMessage = ['Learning', 'is', 'not', 'about', 'what', 'you', 'get', 'easily', 'the', 'first', 'time,', 'it', 'is', 'about', 'what', 'you', 'can', 'figure', 'out.', '-2015,', 'Chris', 'Pine,', 'Learn', 'JavaScript'];

// remove the last element
secretMessage.pop();
console.log();

// add these two strings elements to end
secretMessage.push('to','Program');

// replace the 'easily' with 'right'
let target = secretMessage.indexOf('easily');

secretMessage[target] = 'right';

// remove the first element
secretMessage.shift();

// add 'Programming' to the beginning
secretMessage.unshift('Programming');

// replace the words between 'get' and 'time' with 'know'
delete secretMessage.slice(6, 10);

secretMessage[6] = 'know';

// in one line print the whole message as normal sentence
console.log(secretMessage.join(' '));
```
# Loops
** learning also how to code without repetition **

## For Loop
```javascript

// here the counter is generated at 0 and then prints 0 to 3
for (let counter = 0; counter < 4; counter++) {
  console.log(counter);
};

// here we can go backwards in the iteration
for (let counter = 3; counter >= 0; counter--){
  console.log(counter)
};

// Here is a nested for loop
let bobsFollowers = ['Joe','Karen','Suzie','Elizabeth'];
let tinasFollowers = ['Joe','Ron','Suzie'];

let mutualFollowers = [];

for (let bobs = 0; bobs < bobsFollowers.length ; bobs++) {
  for (let tinas = 0; tinas <tinasFollowers.length; tinas++) {
    if (bobsFollowers[bobs] === tinasFollowers[tinas]) {
     mutualFollowers.push(bobsFollowers[bobs]);
    }
  }
}
console.log(mutualFollowers); // returns ['Joe','Suzie']

```
## While Loop

The while loop is very useful when we do not know how many times we will be running the loop.
```javascript

// This will draw a random card
const cards = ['diamond', 'spade', 'heart', 'club'];

let currentCard;
while (currentCard != 'spade') {
  currentCard =
    cards[Math.floor(Math.random()*4)];
    console.log(currentCard);
}

// Do ... While loop
let cupsOfSugarNeeded = 7;
let cupsAdded = 0;

do {
  cupsAdded++
} while (cupsOfSugarNeeded>cupsAdded);
console.log(cupsAdded);

// Here is an example of breaking a loop with an if statement
const rapperArray = ["Lil' Kim", "Jay-Z", "Notorious B.I.G.", "Tupac"];

// Write you code below
for (let rapperArrayIndex = 0 ; rapperArrayIndex < rapperArray.length; rapperArrayIndex++){
 
console.log(rapperArray[rapperArrayIndex], rapperArrayIndex);
   if (rapperArray[rapperArrayIndex]==='Notorious B.I.G.'){
    break;
  }
}

```
## Whale Talk Project
** Using nested arrays and for loops to translate vowels into 'whale talk' **

```javascript
const input = 'Limitless Possibilities';

// vowels array
let vowels = ['a','e','i','o','u'];

// empty array to load
const resultArray = [];

// function to run both string and array to cross check for vowels and input them into resultArray
let checkInput = () => {
  for (let i=0; i< input.length; i++) {
    //resultArray.push(input[i])

		for (let v=0; v< vowels.length; v++) {

        if (input[i]===vowels[v]) {
          resultArray.push(input[i]);
        }
      if (input[i]==='e' || input[i]==='u') {
        resultArray.push(input[i]);
      }
      
    }
  }
}
checkInput(); // run that function

// log the resultArray as a string without spaces and then set to upper cases
console.log(resultArray.join('').toUpperCase());


```
# Higher Order Functions

countToThree() would be easy to understand we are most likely logging 1,2,3
More modular and abstracted code makes it easier to read and debug in a larger program

In JavaScript, functions are first class objects, this means that like other objects you've encountered, JavaScript functions can have properties and methods.

```javascript
const is2p2 = checkThatTwoPlusTwoEqualsFourAMillionTimes;

is2p2();

console.log(is2p2.name)
// here we reasigned a managable name and then can find the original name of the function with .name

// Below is the higher order function which takes in funcParameter
const timeFuncRuntime = funcParameter => {
   let t1 = Date.now();
   funcParameter();
   let t2 = Date.now();
   return t2 - t1;
}

const addOneToOne = () => 1 + 1;

timeFuncRuntime(addOneToOne);
```
## Passing Functions

```javascript

// Below we checked consistent output and passed a value with number
const checkThatTwoPlusTwoEqualsFourAMillionTimes = () => {
  for(let i = 1; i <= 1000000; i++) {
    if ( (2 + 2) != 4) {
      console.log('Something has gone very wrong :( ');
    }
  }
};

const addTwo = num => num + 2;

const timeFuncRuntime = funcParameter => {
  let t1 = Date.now();
  funcParameter();
  let t2 = Date.now();
  return t2 - t1;
};
    // Write your code below
let time2p2 = timeFuncRuntime(checkThatTwoPlusTwoEqualsFourAMillionTimes);

const checkConsistentOutput = (func, val) => {
  let firstTry = func(val);
  let secondTry = func(val);
  if (firstTry === secondTry) {
    return firstTry;
  } else {
    return ('This function returned inconsistent results');
  }
}
checkConsistentOutput(addTwo, 3);
console.log(checkConsistentOutput(addTwo, 3));
```

## Iterators
** Notice these uses for parsing arrays **
```javascript

const artists = ['Picasso', 'Kahlo', 'Matisse', 'Utamaro'];

// outputs each item
artists.forEach(artist => {
  console.log(artist + ' is one of my favorite artists.');
});


const numbers = [1, 2, 3, 4, 5];

// going to each item, taking that number and squaring
const squareNumbers = numbers.map(number => {
  return number * number;
});

console.log(squareNumbers);

const things = ['desk', 'chair', 5, 'backpack', 3.14, 100];

// taking each item and filtering only numbers out
const onlyNumbers = things.filter(thing => {
  return typeof thing === 'number';
});

console.log(onlyNumbers);

```
## .forEach() 

```javascript
const fruits = ['mango', 'papaya', 'pineapple', 'apple'];

// Iterate over fruits below
fruits.forEach(fruitItem => {
  console.log('I want to eat a ${fruitItem}.')
})

// this does the same thing by function declaration
function printFruits(element){
  console.log(element);
}
fruits.forEach(printFruits);
// You could also do the above as function expression

```
## .map() 
** this is different than .forEach as it returns a new array! **

```javascript

// because this creates a new array, be sure you are using a unique variable toNew
const animals = ['Hen', 'elephant', 'llama', 'leopard', 'ostrich', 'Whale', 'octopus', 'rabbit', 'lion', 'dog'];

const secretMessage = animals.map(toNew => {return toNew.charAt(0);})

```
## .filter() 
** this method creates a new array like .map() and will check the statement in code block for 'true' to push it to the array **
```javascript
// We are checking for lengths in an array greater than 7
const favoriteWords = ['nostalgia', 'hyperbole', 'fervent', 'esoteric', 'serene'];

    // Call .filter() on favoriteWords below
const longFavoriteWords = favoriteWords.filter(check => {
  return (check.length > 7);
})

```
## .findIndex() 
** This will return the numerical value (the index) of the first found item searched in an array **
```javascript
// Here we do two searches, one for the word 'elephant' and the other for the first element starting with the letter 's'
const animals = ['hippo', 'tiger', 'lion', 'seal', 'cheetah', 'monkey', 'salamander', 'elephant'];

const foundAnimal = animals.findIndex(search => {
  return (search==='elephant');
})

const startsWithS = animals.findIndex(search => {
  if (search.charAt(0)==='s') {
  return search
  }
})

```
## .reduce()
** Method returning single value after iterating through the array, not returning another array. **
The value of accumulator starts off as the value of the first element in the array and the currentValue starts as the second element. 

```javascript

// Here we have two arguments for .reduce() where there is a pointer function having two inputs, as well as the followup of 10, which will add 10 to the accumulator. It is worth noting what the console will log below that...
const newNumbers = [1, 3, 5, 7];

const newSum = newNumbers.reduce((accumulator, currentValue) => {
  console.log('The value of accumulator: ', accumulator);
  console.log('The value of currentValue: ', currentValue)
  return (accumulator + currentValue);
}, 10)
console.log(newSum);
```
Here is the console log:
The value of accumulator:  10
The value of currentValue:  1
The value of accumulator:  11
The value of currentValue:  3
The value of accumulator:  14
The value of currentValue:  5
The value of accumulator:  19
The value of currentValue:  7
26

## Review of Iterators

forEach() is used to execute the same code on every element in an array but does not change the array and returns undefined.

.map() executes the same code on every element in an array and returns a new array with the updated elements.

.filter() checks every element in an array to see if it meets certain criteria and returns a new array with the elements that return truthy for the criteria.

.findIndex() returns the index of the first element of an array which satisfies a condition in the callback function. It returns -1 if none of the elements in the array satisfies the condition.

.reduce() iterates through an array and takes the values of the elements and returns a single value.

All iterator methods takes a callback function that can be pre-defined, or a function expression, or an arrow function.

You can visit the Mozilla Developer Network to learn more about iterator methods (and all other parts of JavaScript!).

## Turn string into array
```javascript

const storyWords = story.split(' ');

```
** Instead of this long array cross check function, we can use the .filter() method **

```javascript

// Instead of using this
const storyWords = story.split(' ');
const betterWords = []

let better = () => {
  for (let i=0; i<storyWords.length; i++) {
    let hasWord = false
    for (let n=0; n<unnecessaryWords.length; n++) {
      if (storyWords[i]===unnecessaryWords[n])
        {
          hasWord = true;
          break;
        }
      }
    if (!hasWord) {
      betterWords.push(storyWords[i])
    }
    }
  }

// we use this. .filter outputs to the new array based on true or false
const storyWords = story.split(' ');

const betterWords = storyWords.filter(neW => {
 
	for (let i=0; i<unnecessaryWords.length; i++) {
        return (neW!==unnecessaryWords[i]);
    }
})

```
overusedWords.forEach(word => {
  words[word] = storyWords.filter(aWord => aWord === word);
})
```javascript

const storyWords = story.split(' ');

const betterWords = storyWords.filter(neW => {
 
	for (let i=0; i<unnecessaryWords.length; i++) {
    if (neW===unnecessaryWords[i]) {
      return false
    }
  }
  return true
})

const wordsOverused = storyWords.filter(check => {
  for (let n=0; n<overusedWords.length; n++) {
    if (check===overusedWords[n]) {
      return (overusedWords[n])
    }
  }
})

// iterate wordsOverused and find not only how many words are used in the story, but also make a new object and show how many times each word is used. 

console.log(betterWords.length);
console.log(wordsOverused);

const words = {};
overusedWords.forEach(word => (
words[word] = storyWords.filter(aWord => aWord === word).length))

console.log(words)

// Find out how many sentances are in the story
let sentances = 0

	// here we started with taking the direct string of story and iterating through each character to find periods or exclamation points.Then we add one to the length of sentances array, to then return the length.

const sentanceCount = () => {
  for (let s=0; s<story.length; s++) {
    if (story[s]==='.' || story[s]==='!')
      sentances++;
  }
  return sentances;
}

console.log(sentanceCount());

// or instead of that Med wrote this one line! Notice he used the .split without a space!

console.log(story.split('').filter(x => '.!'.indexOf(x) > -1).length)

// One way of printing for the user to see formatted answers. What about this object though? 
const specialLog = (theWords, theSentances, theOverused) => {
  console.log('You have '+theWords+
             ' words in this story')
  console.log('You have '+theSentances+
             ' sentances in this story')
  overusedWords.forEach(word => console.log(word + ' is used ' + theOverused[word] + ' times'));
  // here we take the array of words as a key to access each item in the object word, logging the word and its number value stored in the oject array words
  
}
specialLog(storyWords.length, sentanceCount(), words);

```

# Beat Mix Project
** Second project in the course, creating logic for a beat mix pad interface **

```javascript
// create an empty array of 16 with false values?
const createEmptyDrumArray = () => new Array(16).fill(false);

// Drum Arrays
let kicks = createEmptyDrumArray();
let snares = createEmptyDrumArray();
let hiHats = createEmptyDrumArray();
let rideCymbals = createEmptyDrumArray();

const getDrumArrayByName = (name) => {
    switch (name) {
        case 'kicks':
          return kicks;
        case 'snares':
          return snares;
        case 'hiHats':
          return hiHats;
        case 'rideCymbals':
          return rideCymbals;
        default:
          return;
      }
    };

// takes two arguments: a string representing the array name ('kicks', 'snares', 'hiHats', or 'rideCymbals'), and an index number. This function should flip the boolean value in the correct array at the specified index.
const toggleDrum = (arrayName, indexNum) => { 
    const drums = getDrumArrayByName(arrayName);
    if (!drums || index > 15 || index < 0) {
        return;
    }
    drums[index] = !drums[index];
};

// takes an array name string and sets all values in the correct array to false.
const clear = (arrayName) => {
    const drums = getDrumArrayByName(arrayName);
    if (drums) {
        drums.fill(false);
    }
};

// takes an array name string and flips the boolean value of all elements in the correct array.
const invert = (arrayName) => {
    const drums = getDrumArrayByName(arrayName);
    if (!drums) {
        return;
    }
    for (let i =0; i <drums.length; i++) {
        drums[i] = !drums[i];
    }
};

    // this should return an array. if invalid index then return 404. if index is valid the first element of return array should be 200.
    // if requestType is not one of the 'GET' or 'PUT', it should return array with 400 (bad request).
    // If the index was valid, presetHandler should also return a second element in the array. for 'GET' requests, that element should be the preset array at that array index. For 'PUT' requests, it should save the newPresetArray to that index and then also return it as the second element.
    // If you are testing presets with the app itself, you will need to stop and re-start your server to see the changes you write in presetHandler.js take effect.

const getNeighborPads = (x, y, size) => {
    const neighborPads = [];
    if (x >= size || y >= size || x < 0 || y < 0 || size < 1) {
        return neighborPads;
    }
    neighborPads.push([x -1, y]);
    neighborPads.push([x, y - 1]);
    neighborPads.push([x + 1, y]);
    neighborPads.push([x, y +1]);
    return neighborPads.filter((neighbor) => {
        return neighbor.every((val) => {
            return val >= 0 && val < size;
        });
    });
};


```

# Objects
** now allow you to store sets of data at named indices instead of numbered indices. **
```javascript


```

# Modules
** 
