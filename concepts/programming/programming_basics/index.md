---
title: Programming basics
attributions:
  - 'This content was originally published on [DevOpera](http://dev.opera.com), Opera''s Developer Network. .'
readiness: 'Ready to Use'
summary: 'This article covers fundamental principles of programming, using JavaScript as an example language.'
tags:
  - Guides
  - JavaScript
uri: 'concepts/programming/programming basics'

---
**By [Chris Heilmann](http://wait-till-i.com/)**
Originally published February 3, 2009

## <span>Summary</span>

This article covers fundamental principles of programming, using JavaScript as an example language.

## <span>Introduction</span>

As an experienced developer, you will sooner or later have to face people that are just not technical and will consider whatever you do as black magic. Conversely, as a non-technical person, not knowing what someone delivering work for you is doing is a bad starting position. This [Web Standards Curriculum](http://www.w3.org/wiki/Web_Standards_Curriculum) article explains in simple terms what programming is about and hopefully will help both parties involved to steer these non-conversations into more productive waters.

It will also help novice web developers to take on-board some generic programming principles that are essential to understand before learning JavaScript. It may seem boring to begin with, but your work will be a lot more robust, dynamic, and creative (read: a lot more WOW factor) if you get these rudimentary principles down in the first place. Learning the basic fundamentals of programming is important before you start working in particular languages (JavaScript, in the case of this course).

## <span>Order, I will have order!</span>

Programming in the most basic form is issuing commands and seeing that they get executed. It is a mixture of math and linguistics: you define a lot of calculations and you need to tell machines to solve them by giving orders using the right grammar. Grammar in programming is syntax and differs a lot from language to language.

For example, the following two code snippets fulfill the same task, but the former is JavaScript and the latter is PHP:

``` js
var fahrenheit = prompt('Enter temperature in Fahrenheit', 0);
var celsius = (fahrenheit - 32) * 5 / 9;
alert(celsius);
```

```
$fahrenheit = $_GET['fahrenheit'];
$celsius = ($fahrenheit - 32) * 5 / 9;
echo $celsius;
```

 Try out the JavaScript [Fahrenheit to Celsius conversion example](http://dev.opera.com/articles/view/programming-the-real-basics/fahrenheit.html).

Programming languages are *interpreted* to be turned into actions or results. Some languages, such as JavaScript, are interpreted by a web browser; all you need to do to make them “do stuff” is put them inside an HTML document and open this in a browser. Other programming languages need to be translated (compiled) in an extra step to become executable. Deep down, all computers only understand zeros and ones, but above that there are multiple levels of languages fulfilling different tasks.

## <span>Variables</span>

The first step towards understanding programming is looking back at algebra. If you remember from school, algebra starts with writing terms such as the following:

    3 + 5 = 8

You start performing calculations when you introduce an unknown, for example x below:

    3 + x = 8

Shifting those around you can determine x:

    x = 8 - 3
    -> x = 5

When you introduce more than one, you make your term more flexible - you are using variables:

    x + y = 8

You can change the values of x and y and the formula can still be true:

    x = 4
    y = 4

or

    x = 3
    y = 5

The same works with programming languages -— in programming, variables are containers for values that can vary. Variables can hold all kinds of values and also the results of calculations. Variables have a name and a value separated by an equals sign (=). Variable names can be any letter or word, but bear in mind that there are restrictions from language to language of what you can use, as some words are reserved for other functionality.

To keep things easy, let's use JavaScript as an example programming language in this article (logical, since this section of the web standards curriculum is all about JavaScript programming). The following defines two variables, calculates the result of adding the two and defines this result as a value of a third variable.

``` js
var x = 5,
    y = 6,
    result = x + y;
```

 The interpreter goes through the code instruction by instruction, with each instruction ending in a semicolon. The semicolon notifies the interpreter of the end of an instruction, much like a full stop or an exclamation mark defines the end of a sentence in human languages.

In English, this construct would be as follows:

-   Define a new variable (that is the `var` keyword) called `x` and assign it the value `5`.
-   Define a new variable called `y` and assign it the value `6`.
-   Define a new variable called result and assign it the result of adding `x` and `y` as its value. End of statement. (As there is a calculation in the assignment of the variable result the interpreter then checks the value of `x`, checks the value of `y`, adds the two and sets the value of result to the outcome — `11`.)

You can do all kinds of calculations with variables by adding operators in between them. There are the classics like adding with a plus sign operator and subtracting with a minus sign operator. For multiplication you have to use an asterisk (\*) and for division, a slash (/). The following example shows some calculations that are possible. Notice the texts preceded by a double slash (//) — these are JavaScript comments. When a JavaScript interpreter encounters these in a script it will not try to execute what follows on that line, and skips it: these are comments made for humans and not to be interpreted by the browser.

``` js
var x = 5,
    y = 6,
    z = 20,
    multiply = x * y * z;

// multiply will be 600
var divide = x / y;
// divide will be 0.8333333333333334
var addAndDivide = (x + z) / y;
// addAndDivide = 4.166666666666667
var half = (y + z) / 2;
// half will be 13
```

 As you can see, you can mix and match any variable, and also use variables along with fixed values in calculations; you can also group them with parentheses to override the natural order of operators (parentheses first, then multiplication or division, then adding or subtracting and all those math lesson classics).

### <span>Variable types</span>

However, this would be boring, as we can do all that with a simple calculator (after we typed 5318008, then turned it around and giggled, of course). Computers are more sophisticated and can make use of more complex variables. This is where variable types come in. Variables come in several types and different languages support different ones. The most common ones are:

-   Float: a number, like `1.21323`, `4`, `100004` or `0.123`
-   Integer: a natural number like `1`, `12`, `33`, `140` but not `1.233`
-   String: a line of text like "`boat`", "`elephant`" or "`damn, you are tall!`"
-   Boolean: either `true` or `false`, but nothing else
-   Arrays: a collection of values like `1,2,3,4,'I am bored now'`
-   Objects: a representation of an object. Objects are constructs that try to model instances of objects in the real world by having properties and methods. For example, you could model a cat as an object and define that it has four legs, one tail, and that it is ginger. You can also define that it has a way of purring by defining a `purr()` method and that it might demand a cheeseburger with a `getCheeseBurger()` method. You can also re-use the `cat` object and define another cat with all the properties of the original one but a gray color.

JavaScript is a “loosely typed” language, which means that you do not have to explicitly declare what type of data the variables are. You just need to use the `var` keyword to indicate that you are declaring a variable, and the browser will work out what data type you are using from the context and use of quotes.

#### <span>Floats and integers</span>

There is nothing magical or strange going on with these. You define variables and set their values to any number type.

``` js
var fahrenheit = 123,
    celsius = (fahrenheit - 32) * 5/9,
    clue = 0.123123;
```

 Floats and integers can be modified with any mathematical operators.

#### <span>Booleans</span>

Booleans are simple “yes or no” definitions. You assign them by using the `true` or `false` keywords.

``` js
var doorClosed = true,
    catCanLeave = false;
```

#### <span>Strings</span>

Strings are lines of text that can contain any character. You define them in JavaScript by enclosing the text in single quotes or double quotes.

``` js
var surname = 'Heilmann',
    name = "Christian",
    age = '33',
    hair = 'Flickr famous';
```

 You can concatenate (a technical term that means “join together”) strings using the + operator but you cannot subtract strings from one another. For string modification you need to use functions the language provides you with. Simple concatenation, on the other hand, is as easy as this:

``` js
var surname = 'Heilmann',
    name = 'Christian',
    age = '33',
    hair = 'Flickr famous',
    message = 'Hi, I am ' + name + ' ' + surname + '. ';

message += 'I am ' + age + ' years old and my hair is ' + hair;
alert(message);
```

 Try out the [string concatenation example](http://dev.opera.com/articles/view/programming-the-real-basics/flickrfamous.html).

The += operator is a shortcut for "message = message +". The product of this script is the string “Hi, I am Christian Heilmann. I am 33 years old and [my hair is Flickr famous](http://flickr.com/photos/tags/thehairofchristianheilmann/)”.

There is a catch to remember when using concatenation versus adding values. If you want to add two values you need to make sure that both are numbers, not strings. The [concatenation versus addition](http://dev.opera.com/articles/view/programming-the-real-basics/concatvsadd.html) example shows the difference between the two. “5”+“3” is 53 and not 8! The easiest way to convert a string to a number is by prepending it with a “+”, as shown in the example.

Most languages will not care if you use single or double quotes to enclose the string, as long as you do not mix them. To stop the JavaScript interpreter from becoming confused about where the end of the string is, you need to comment out quotes contained in the string with a backslash:

``` js
// this will cause an error, as the interpreter doesn't know
// what the things after the ' are. The string defined here is
// 'Isn'.
var stringWithError = 'Isn't it hard to get things right?';
// This is not an error, all is fine
var stringWithoutError = 'Isn\'t it hard to get things right?';
```

#### <span>Arrays</span>

Arrays are very powerful constructs. An array is a collection of values, and each of the values can be a variable, or a real value. For example:

``` js
var pets = new Array('Boomer','Polly','Mr.Frisky');
```

 You can access each of the values with the **array** counter, which is the index number in the array -— think of it as being like looking up chapters in a book. The syntax is `arrayname[index]`. So for example `pets[1]` would give you the string “Polly”. But wait! I hear you ask—shouldn’t it be `pets[2]` for Polly, given that it is the **second** value in the array? **No**—the counter is not 2, as computers start counting at 0, not at 1! This is a very common cause of confusion and errors.

Arrays automatically get a special information source for you: `length`. If you check the value of `pets.length` you will get 3 as there are 3 items in this array.

Arrays are great for describing collections of things that have something in common, and every language comes with dozens of handy functions to manipulate them—sorting, filtering, searching and so on.

#### <span>Objects</span>

If you have a collection of items that need more detailed descriptions than just a running number, then an Array will not quite give what you need, and you will need to create an object. Objects are constructs in programming that represent or model real things, such as people, vehicles or tools.

Objects are a big and very clever and versatile part of programming and explaining them in detail here would be beyond the scope of this article. Let’s just say that an object is a thing that has several properties. Say for example you have a person object; you can define the different properties by appending them with a dot:

``` js
var person = new Object();
person.name = 'Chris';
person.surname = 'Heilmann';
person.age = 33;
person.hair = 'Flickr famous';
```

 You can access the properties with dot notation (`person.age` would give you 33) or with the square bracket notation (`person['name']` gets you “Chris”). You will learn more about JavaScript objects later on in the course.

That is about the short and long of what value types variables can be. Another big part of programming is the structure and logic of your program. This is where two more programming ideas come into play: conditions and loops.

## <span>Conditions</span>

A condition is a test for something. Conditions are very important for programming, in several ways:

First of all, conditions can be used to ensure that your program works, regardless of what data you throw at it for processing. If you blindly trust data, you will get into trouble and your programs will fail. If you test that the thing you want to do is possible and has all the required information in the right format, that will not happen, and your program will be a lot more stable. Taking such precautions is also known as programming defensively.

The other thing conditions can do for you is allow for branching. You might have encountered branching diagrams before, for example when filling out a form. Basically, this refers to executing different “branches” (parts) of code, depending on if the condition is met or not.

The easiest condition is an `if` statement and its syntax is `if (condition) { do this … }`. The condition has to be true for the code inside the curly braces to be executed. You can for example test a string and set the value of another string dependent on its value:

``` js
var country = 'France',
    weather,
    food,
    currency,
    message;

if (country === 'England') {
  weather = 'horrible';
  food = 'filling';
  currency = 'pound sterling';
}

if (country === 'France') {
  weather = 'nice';
  food = 'stunning, but hardly ever vegetarian';
  currency = 'funny, small and colourful';
}

if (country === 'Germany') {
  weather = 'average';
  food = 'wurst thing ever';
  currency = 'funny, small and colourful';
}

message = 'this is ' + country + ', the weather is ' + weather + ', the food is ' + food + ' and the ' + 'currency is ' + currency;
alert(message);
```

 Try it out yourself in my [Weather if statement example](http://dev.opera.com/articles/view/programming-the-real-basics/weather.html). Change the value of the country variable to see the different messages.

The conditional part is the country followed by the three equal signs. Three equal signs mean that the condition tests if the variable country has the value you test against but also the correct variable (data)type. You can test conditions with double equal signs, too, but that would mean that `if (x == 5)` would be true for x being 5 and x being “5”. Depending on what your program is doing, this could make quite a difference.

Other conditional test examples:

-   `x > 0` - is x bigger than zero?
-   `x < 0` - is x less than zero?
-   `x <= 4` - is x less than or equal to four?
-   `x != 'hello'` - is x not 'hello'?
-   `x` - does x exist?

Conditions can also be nested. Say for example you want to make sure that the country variable is set in the earlier example; you can do that this way:

``` js
var country = 'Germany',
    weather,
    food,
    currency,
    message;

if (country) {
    if (country == 'England') {
        weather = 'horrible';
        food = 'filling';
        currency = 'pound sterling';
    }

    if (country == 'France') {
        weather = 'nice';
        food = 'stunning, but hardly ever vegetarian';
        currency = 'funny, small and colourful';
    }

    if (country == 'Germany') {
        weather = 'average';
        food = 'wurst thing ever';
        currency = 'funny, small and colourful';
    }

    message = 'this is ' + country + ', the weather is ' + weather + ', the food is ' + food + ' and the ' + 'currency is ' + currency;
    alert(message);
}
```

 Try it out yourself in my [Safe-weather if statement example](http://dev.opera.com/articles/view/programming-the-real-basics/saferweather.html). Change the value of the country variable to see the different messages.

Whereas the earlier example would always try to create the message regardless of country being available—and thus possibly throwing an error or stating “this is **undefined**, the weather...” this version is more secure. If country is not defined the message will never be created. Furthermore you can concatenate different conditions with “or” or “and” statements, to test whether either statement is true, or both are true, respectively. In JavaScript “or” is written as | and “and” is written as &&\_ Say you want to test if the value of x is between 10 and 20—you could do that with a condition stating `if(x > 10 && x < 20)`\_ If you want to make sure that country is either “England” or “Germany” you use `if(country== 'England'  | country== 'Germany')`.

There is also an `else` clause that will be applied every time the first condition isn’t true. This is very powerful if you want to react to any value, but single out one in particular for special treatment:

``` js
var umbrellaMandatory;
if(country == 'England'){
  umbrellaMandatory = true;
} else {
  umbrellaMandatory = false;
}
```

 Conditions are great, but they are a bit limited. What if you want to do something over and over again? Say your job is to add a paragraph tag around each of the values in an array? Using only conditions you’d need to hard-code cases for arrays of all the different lengths you'd be likely to come across:

``` js
var names = new Array('Chris','Dion','Ben','Brendan');
var all = names.length;
if(all == 1){
  names[0] = '<p>' + names[0] + '</p>';
}
if(all == 2){
  names[0] = '<p>' + names[0] + '</p>';
  names[1] = '<p>' + names[1] + '</p>';
}
if(all == 3){
  names[0] = '<p>' + names[0] + '</p>';
  names[1] = '<p>' + names[1] + '</p>';
  names[2] = '<p>' + names[2] + '</p>';
}
if(all == 4){
  names[0] = '<p>' + names[0] + '</p>';
  names[1] = '<p>' + names[1] + '</p>';
  names[2] = '<p>' + names[2] + '</p>';
  names[3] = '<p>' + names[3] + '</p>';
}
```

 This is just terrible and inflexible. Programming is meant to make our life easier and if you find yourself writing the same code over and over again, you are probably doing something wrong. Good programming means leaving the boring tasks to the machines and focusing on what you want to achieve.

In this case we need a **loop** instead of a condition, as we are doing exactly the same thing to each and every one of the items in the array, and the length doesn’t really matter. You’ll see the above example rewritten using a loop in the next section—compare the two, and see how much shorter the latter is!

## <span>Loops</span>

Loops are repetitive conditions where one variable in the loop changes. The easiest form of a loop is the `for` statement. This one has a syntax that is similar to an `if` statement, but with more options:

``` js
for(condition;end condition;change){
  // do it, do it now
}
```

 Normally what you do with a `for` loop is to execute the code in the curly braces several times. For this you need to define an iterator variable and keep changing it during the loop until the variable value meets the end condition (which causes the interpreter to exit the loop and carry on to the next part of the code). For example:

``` js
for(var i = 0;i < 11;i = i + 1){
  // do it, do it now
}
```

 Here we define a variable `i` as having an initial value of 0 and then do a check to see if it has reached 11 yet (is it smaller than 11?). The change equation—`i = i + 1`—adds one to `i` every time the loop executes and goes through another iteration. This means that this loop executes 11 times. If you add two to `i` on every iteration it executes only 6 times:

``` js
for(var i = 0;i < 11;i = i + 2){
  // do it, do it now
}
```

 Using a loop the paragraph adding example we saw above gets a lot shorter and simpler:

``` js
var names = new Array('Chris','Dion','Ben','Brendan');
var all = names.length;
for(var i=0;i<all;i=i+1){
  names[i] = '<p>' + names[i] + '</p>';
}
```

 Notice that you can use the value of `i` as the array counter inside the loop. This is the power of loops—not only can you do the same thing over and over again; you also know in every iteration how many times you have already done it.

## <span>See also</span>

### <span>Exercise questions</span>

-   Why does this code fail? `var x = hello world`?
-   Is this valid code? `var x = 'elephant';var y = "mouse";`
-   What does this condition test for? `if(x > 10 && x < 20 && x !== 13 && y < 10)`
-   What does this condition do? `if(b < 10 && b > 20)`?
-   Loop over an array with the items “peter”,“paul”,“mary”,“paddington bear”,“mr.ben”,“zippy” and “bagpuss”. Add a paragraph around each of them and add a paragraph with a class “odd” to every second one of them. Tip: you can test for every second item using the modulo operator `i % 2 == 0`
