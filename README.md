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
const friendsAtYourParty = 0;
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







    * [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

        ## Contributing

Please read[CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

            ## Versioning

We use[SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

                ## Authors

                * ** Billie Thompson ** - * Initial work * -[PurpleBooth](https://github.com/PurpleBooth)

                    See also the list of[contributors](https://github.com/your/project/contributors) who participated in this project.

                        ## License

This project is licensed under the MIT License - see the[LICENSE.md](LICENSE.md) file for details

## Acknowledgments

    * Hat tip to anyone whose code was used
        * Inspiration
        * etc
