# JS Basics reminder

Full list

### CONST: single threaded, the order it happens

JS is single threaded code.const means unchanging value.You cant change it later.let does that.You can omit;.JS will put them there is execution.  

```
const monthlyRent= 500;
const yearlyRent = monthlyRent * 12;
console.log(yearlyRent);
```

### let : mutable

```
let friendsAtYourParty = 0;
friendsAtYourParty = friendsAtYourParty + 1;
friendsAtYourParty = friendsAtYourParty + 1;
friendsAtYourParty = friendsAtYourParty + 1;
friendsAtYourParty = friendsAtYourParty + 1;
friendsAtYourParty = friendsAtYourParty + 1;
friendsAtYourParty = friendsAtYourParty + 1;
console.log(friendsAtYourParty);
```


### var

this is different again it has scope.  let has block level scope , var has function level scope

result is 10. Instead use a loop!

### Numbers, strings boleans

Strings: series of characters either singe quotes, double quotes or back ticks.

```
const nyName = `Archie`;
console.log(myName);

```

result:

```
"Brian Holt"
```

template strings 2015!

```
const firstName = "Brian";
const lastName = "Holt";

const sentence = "Hello " + firstName + " " + lastName + "! How are you!?";
const sentenceWithTemplate = `Hello ${ firstName } ${ lastName } !How are you! ? `;

console.log(sentence);
console.log(sentenceWithTemplate);
```


## Boleans

true and false

```
const codeIsWorking = true;


```

## IF ELSE


```
const skyIsBlue = true;

if (skyIsBlue) {
  console.log("The sky is blue!");
} else {
  console.log("The sky is … not blue?");
}
```

result

```
"The sky is blue!"
undefined
```

```
const temperatureToday = 86;

if (temperatureToday >= 86) {
  console.log("The sky is blue!");
} else {
  console.log("The sky is … not blue?");
}

```

## CONDITIONALS


```
const skyIsBlue = true;

if (skyIsBlue) {
  console.log("The sky is blue!");
} else {
  console.log("The sky is … not blue?");
}
```

result

```
"The sky is blue!"
undefined
```

## Cohersion

Explain what these tests test and why

```
if (2 + 2 1== 4) {
  console.log(
    "Oh thank god, the fundamental principles of mathematics still hold true."
  );
} else {
  console.log("Uh, panic?");
}
```

result

```
"Uh, panic?"
```

## else if

```
const friendsAtYourParty = 0;

if (friendsAtYourParty === 0) {
  console.log("Cool, now I have a lot of nachos to myself.");
} else if (friendsAtYourParty >= 4) {
  console.log("Perfect amount to play some Mario Kart.");
} else {
  console.log("Wooooo turn on the dance music!");
}
```

result

```
"Perfect amount to play some Mario Kart."
undefined
```

## Loops

run 11 (cos 0)times and break out

```
let friendsAtYourParty = 0;
while (friendsAtYourParty < 10) {
  friendsAtYourParty = friendsAtYourParty + 1;
}
console.log(friendsAtYourParty);
//result 10
//or
let friendsAtYourParty = -100;
while (friendsAtYourParty < 10) {
  friendsAtYourParty = friendsAtYourParty + 1;
}
console.log(friendsAtYourParty);
//result 10

```

Do loop does loop once only, very rare in code. Remember you can crash browser with infinite loop


## different increments

that do exactly the same thing. 

``` 

let friendsAtYourParty = 0;
friendsAtYourParty = friendsAtYourParty + 1;
friendsAtYourParty += 1;
friendsAtYourParty++;
++friendsAtYourParty;
console.log(friendsAtYourParty);
```
** means squared

## For loop

```
let friendsAtYourParty = 0;
for (let i = 0; i <= 10; i++) {
  friendsAtYourParty++;
}
console.log(friendsAtYourParty);
```
result 10

## Functions

all before was procedural programming. Everything this way is crappy. Generally variables are nouns (John jane) and functions are verbs "greet".

```
function addTwo(number) {
  return number + 2;
}

const finalAnswer = addTwo(5);
console.log(finalAnswer);

//I can reuse this loads of times
console.log(addTwo(100));
```
### Another function
```
function greet(firstName, lastName, honorific, greeting) {
  return `${greeting} ${honorific} ${lastName}! I’m extremely pleased you could join us, ${firstName}! I hope you enjoy your stay, ${honorific} ${lastName}.`;
}
console.log(greet("Brian", "Holt", "Lord", "Salutations"));
console.log(greet("Jack", "Sparrow", "Captain", "A-hoy"));
```

## Calling functions

invoke a function. Parenthesis after it. someFunctionName(); log is a function being called.

```
const finalAnswer = addTwo();

```

##  Passing  a function

pass a variable here or even a string 

```
const myHomeCity = "Salt Lake City";
const myHomeState = "Utah";
const myHomeCountry = "USA";

function logOutYourHome(city, state, country) {
  console.log(`You are from ${city}, ${state} ${country}.`);
}

logOutYourHome(myHomeCity, myHomeState, myHomeCountry);

```

## Scope

We'll talk about scope multiple times but we'll start off here with it. Every time you call a function, it has its own scope. Other things can't peek into it; it just has its own little workspace for it work with. Once its done, any variable that you haven't explicitly held on to or returned at the end is discarded. For example:


```
function addFive(number) {
  const someVariable = "you can't see me outside this function";
  return number + 5;
}

addFive(10);
console.log(someVariable);
```

Not defined. You can't console log it outside its environment OUT OF SCOPE. Outside the scope you cant look at it, it's gone. Ask yourself WHERE WAS IT DECLARED? Console log in the let, the var, the const.

## Exercise

```
const A = "A";
let F;

function doStuff(B) {
  console.log(B);
  const C = "C";
  let H = "H";
  if (1 + 1 === 2) {
    const D = "D";
    H = "something else";
  }
  console.log(D);
  console.log(H);
  F = "F";
}

let E = 0;
while (E < 3) {
  E++;
  console.log(A);
  const G = "G";
}
console.log(E);
console.log(G);

doStuff("B");
console.log(B);
console.log(C);
console.log(F);

```

## Built ins

pre built by JS. Example strings have functions.

```
const sentence = "ThIs HaS wEiRd CaSiNg On It";
console.log(sentence.toLowerCase());
```

result: "this has weird casing on it". Check out the ndn. In console write "some string".    and options appear. Editor also does this. Try Math.round(5.1); equals 5.

Try console.log(Math.floor(5.9999)); result is 5.
console.log(Math.ceil(5.9999)); result is 6.

## Objects and Arrays

```
const person = {
  name: "Brian Holt",
  city: "Seattle",
  state: "WA",
  favoriteFood: "🌮",
  wantsTacosRightNow: true,
  numberOfTacosWanted: 100
};
console.log(person);
console.log(person.name);
console.log(person["name"]); // same as the line above; definitely prefer using the other one
```
result:
```
Object {
  "city": "Seattle",
  "favoriteFood": "🌮",
  "name": "Brian Holt",
  "numberOfTacosWanted": 100,
  "state": "WA",
  "wantsTacosRightNow": true,
}
"Brian Holt"
"Brian Holt"
undefined
```

Above is inside of the object person I want this key.

This is called an object. They're extremely useful in JavaScript; they're how you'll group together like-information so that they can be used together. They contain a bunch of keys and values. The keys are on the left side of the : and represent how you get that piece data of out of the object. name is one such key, and the way I get the name of the

Used in conjunction with functions they're very powerful. Take this example:

```
const person1 = {
  name: "Brian",
  ageRange: "25-35"
};
const person2 = {
  name: "Jack",
  ageRange: "65-75"
};

function suggestMusic(person) {
  if (person.ageRange === "25-35") {
    console.log("We think you'll like Daft Punk your crazy millenial.");
  } else if (person.ageRange === "65-75") {
    console.log(
      "You're obviously going to like Johnny Cash. He walks the line."
    );
  } else {
    console.log(
      "Uh, maybe try David Bowie? Everyone likes David Bowie, right?"
    );
  }
}

suggestMusic(person1);
suggestMusic(person2);
```

result

```

"We think you\'ll like Daft Punk your crazy millenial."
"You\'re obviously going to like Johnny Cash. He walks the line."
undefined

```

### Objects can even have their functions! Let's see that.

```
const dog = {
  name: "dog",
  speak() {
    console.log("woof woof");
  }
};

dog.speak();

```
result

```
"woof woof"
undefined
```


## Nested objects

```
const me = {
  name: {
    first: "Brian",
    last: "Holt"
  },
  location: {
    city: "Seattle",
    state: "WA",
    country: "USA"
  }
};

console.log(me);
```

result

```

Object {
  "location": Object {
    "city": "Seattle",
    "country": "USA",
    "state": "WA",
  },
  "name": Object {
    "first": "Brian",
    "last": "Holt",
  },
}
undefined
```

You can tree forever in json objects. They have to have UNIQUE KEYS.

## Context 'THIS' REFERS TO WHAT EVER THIS OBJECT IS ON!!!!

Simlar field to scope. Using the above object, wouldn't it be nice if we could use a function to nicely print where that person was from?

```

const me = {
  name: {
    first: "Brian",
    last: "Holt"
  },
  location: {
    streetNumber: 500,
    street: "Fakestreet",
    city: "Seattle",
    state: "WA",
    zipCode: 55555,
    country: "USA"
  },
  getAddress() {
    return `${this.name.first} ${this.name.last}
${this.location.streetNumber} ${this.location.street}
${this.location.city}, ${this.location.state} ${this.location.zipCode}
${this.location.country}`;
  }
};

console.log(me.getAddress());

```

result

```
"Brian Holt
500 Fakestreet
Seattle, WA 55555
USA"
undefined

```

this USUALLY applies to "nearest object". This refers to me const. What if I write this outside an object. If youre in a global scope it becomes entire "window"= global context

try

```
this === window;

```
result is true

## LOG mouse position
```
console.log(this === window);
console.log(this.scrollY);
console.log(window.scrollY);

```

result

```
true
0
0
undefined
```
Try 
```
window.

```

to find a ton of things you can use. When it breaks its not obvious. Rule of thumb is where are functions called and in what context.

## Arrays

An ordered list of something. And they start at 0. Like a for loop. Its the way it is for devs.


```
const daysOfTheWeek = [
  "Monday",
  "Tuesday",
  "Wednesday",
  "Thursday",
  "Friday",
  "Saturday",
  "Sunday"
];
console.log(daysOfTheWeek);
console.log(daysOfTheWeek[0]);
console.log(daysOfTheWeek[1]);
console.log(daysOfTheWeek[6]);

```
result

```

Array [
  "Monday",
  "Tuesday",
  "Wednesday",
  "Thursday",
  "Friday",
  "Saturday",
  "Sunday",
]
"Monday"
"Tuesday"
"Sunday"
undefined

```

Count prime numbers in array

```
const primeNumbers = [1, 2, 3, 5, 7, 11, 13, 17];
console.log(primeNumbers.length);
console.log(primeNumbers.join(" | "));
```

result

```
8
"1 | 2 | 3 | 5 | 7 | 11 | 13 | 17"
undefined
```

## Push onto an array

add an extra object. Use Push.

```
const courses = [
  { teacher: "Kyle Simpson", course: "JS Function Lite" },
  { teacher: "Sarah Drasner", course: "Intro to Vue" },
  { teacher: "Brian Holt", course: "Complete Intro to React v3" },
  { teacher: "Steve Kinney", course: "State Management" }
];

courses.push({ teacher: "Sean Larkinn", course: "Webpack" });

console.log(courses);

courses[2] = { teacher: "Brian Holt", course: "Complete Intro to React v4" };

console.log(courses);

```

That was overwriting.

## forEach: Use it constantly. It's functional programming.  Console log a whole array.

We use a for loop.
```
const cities = [
  "Seattle",
  "San Francisco",
  "Salt Lake City",
  "Amsterdam",
  "Hong Kong"
];

// method 1
for (let i = 0; i < cities.length; i++) {
  console.log(cities[i]);
}

// method 2, index indicates their position
cities.forEach(function(city, index) {
  console.log(index, city);
});
```

### Method means function.

for each is technically a method. A anonymous function.


## The DOM (document object model)

the way js enteracts with html and css. Its  on window. console.log is part of the document object model.

et's first chat about what a browser is and how your code gets from you writing it to being on run in a browser.

In a typical circumstance.

1. You write code in your editor (like VSCode)
2. You put your code on a server so that other people can get it
3. Someone visits your website

    1. (Lots of stuff happens here. For now we're not going to talk about it)
    2. Their browser makes a request to your server for your index.html
    3. Your server sends them a copy of the html
    4. The browser reads the HTML, sees you have a my-script.js script tag on there
    5. Browsers makes another request for my-script.js from your server
    6. Your server sends them a copy of my-script.js
    7. The browser reads the JavaScript code and begins executing the code
    8. Same process happens with CSS too.

## change a dom element

```
<style>
  .red-square {
    width: 100px;
    height: 100px;
    background-color: crimson;
  }
</style>

<div class="red-square"></div>

<script>
  const redSquare = document.querySelector('.red-square');
  redSquare.style.backgroundColor = 'limegreen';
</script>

```

 result green square!

ANOTHER:

```

<ul>
  <li class="js-target">Unchanged</li>
  <li class="js-target">Unchanged</li>
  <li>Won't Change</li>
  <li class="js-target">Unchanged</li>
  <li>Won't Change</li>
  <li class="js-target">Unchanged</li>
</ul>
<script>
  const elementsToChange = document.querySelectorAll('.js-target');
  for (let i = 0; i < elementsToChange.length; i++) {
    const currentElement = elementsToChange[i];
    currentElement.innerText = "Modified by JavaScript!";
  }
</script>

```

RESULT:
Modified by JavaScript!
Modified by JavaScript!
Won't Change
Modified by JavaScript!
Won't Change
Modified by JavaScript!


## Event listeners

```
<button class="event-button">Click me!</button>
<script>
  const button = document.querySelector('.event-button');
  button.addEventListener('click', function () {
    alert("Hey there!");
  });
  </script>

```
With input, amazing example.

```
<input placeholder="type into me!" class="input-to-copy" />
<p class="p-to-copy-to">Nothing has happened yet.</p>
<script>
  const input = document.querySelector('.input-to-copy');
  const paragraph = document.querySelector('.p-to-copy-to');

  input.addEventListener("keyup", function() {
    paragraph.innerText  = input.value;
  });
</script>

```

### Change. 

```
<style>
  .color-box {
    background-color: limegreen;
    width: 100px;
    height: 100px;
  }
</style>
<div class="color-box"></div>
<input class="color-input" placeholder="Type a color here!" />
<script>
  const input = document.querySelector('.color-input');
  const paragraph = document.querySelector('.color-box');

  input.addEventListener("change", function() {
    paragraph.style.backgroundColor  = input.value;
  });
</script>
```

## Event delegation

One event listener for all 5.

```
<div class="button-container">
  <button>1</button>
  <button>2</button>
  <button>3</button>
  <button>4</button>
  <button>5</button>
</div>
<script>
  document.querySelector('.button-container').addEventListener('click', function(event) {
    alert(`You clicked on button ${event.target.innerText}`);
  });
</script>
```

### prevent default

```
event.preventDefault();
event.stopPropagation();
```

## AJAX

Asynchronous javascript and xml(we dont use xml anymore, we use json).

Ajax means request info from api(appli programming interf) = somewhere to request data

email refresh button is ajax

https://github.com/toddmotto/public-apis


### Fetch

```
    const DOG_URL = "https://dog.ceo/api/breeds/image/random";

const promise = fetch(DOG_URL);

promise
  .then(function(response) {
    const processingPromise = response.json();
    return processingPromise;
  })
  .then(function(processedResponse) {
    console.log(processedResponse);
        const img = document.createElement("img");
    img.src = processedResponse.message;
    img.alt = "Cute doggo";
    doggos.appendChild(img);
  });

console.log("this will log first");

```

fetch gives you a promise. fetch is asynchronous. It fetches JSON. Javascript Object Notation

Return it on page:


```

const DOG_URL = "https://dog.ceo/api/breeds/image/random";

const doggos = document.querySelector(".doggos");

function addNewDoggo() {
  const promise = fetch(DOG_URL);
  promise
    .then(function(response) {
      const processingPromise = response.json();
      return processingPromise;
    })
    .then(function(processedResponse) {
      const img = document.createElement("img");
      img.src = processedResponse.message;
      img.alt = "Cute doggo";
      doggos.appendChild(img);
    });
}

document.querySelector(".add-doggo").addEventListener("click", addNewDoggo);

```


## NODE.js

Start a localserver 

```
const http = require("http");

const server = http.createServer(function(req, res) {
  console.log(`user visited ${req.url}`);
  res.end("hello!");
});

console.log("listening on http://localhost:3000");
server.listen(3000);

```
save as server.js

Go to your terminal and run node server.js. You should see the "listening on http://localhost:3000" message logged out. Navigate your browser to http://localhost:3000. You should see the text hello! responded back to you. 

*  You dont know javascript book


        ## Contributing

Please read [FULLTUTO ](https://btholt.github.io/intro-to-web-dev-v2) for details on code.
