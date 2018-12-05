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

```
## Section one
*this is in italics*
## Section two
some text
## Section Three
**text**
```javascript
// String interpolation using template literal
    let myName = 'James';
    let myCity = 'Petaluma';
    console.log(`My name is ${myName}. My favorite city is ${myCity}`);
```


some text