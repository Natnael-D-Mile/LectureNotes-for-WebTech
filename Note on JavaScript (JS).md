# Note on JavaScript (JS)

# Brief Intro

<aside>
💡 JavaScript is the world's most popular programming language. It is indeed the programming language of the Web.

</aside>

- JS is a high-level, interpreted programming language primarily used for developing dynamic websites & web apps. It’s also used ***to develop mobile apps, desktop apps, games,*** ***to add interactivity to websites, &*** nowadays JavaScript can be used for **server-side programming**, ***machine learning*** and ***AI***.
- It was created by Brendan Eich in 1995 & has since become one of the most popular programming languages worldwide.
- JavaScript is supported by all modern web browsers & can also be used on the server-side with the help of Node.js.
- ***JavaScript (JS)*** has increased in popularity in recent years and has been the leading programming language for last ten years and is the most used programming language on GitHub.

# Basic Setup

1. Install node.js
2. Install a browser (Google Chrome is advisable:)
3. Install a code editor (VS Code is advisable:)

# Adding JS to a Web Page

JavaScript can be added to a web page in 4 different ways. These are:

- ***Inline script***
- ***Internal script***
- ***External script***
- ***Multiple External scripts***

The following sections show different ways of adding JavaScript code to your web page.

## Inline Script

- Let’s try to figure out what inline script is using this hands-on example:

*Create a project folder on your desktop or in any location, name it 30DaysOfJS and create an **`index.html`** file in the project folder. Then paste the following code and open it in a browser.*

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
<title>30DaysOfScript:Inline Script</title>
</head>
<body>
<button onclick="alert('Welcome to 30DaysOfJavaScript!')">Click Me</button>
</body>
</html>
```

Now, you just wrote your first inline script. We can create a pop up alert message using the *`alert()`* built-in function.

---

## Internal Script

- The internal script can be written in the *`head`* or the *`body`*, but it’s preferred to put it on the body of the HTML document.

e.g. 1:  (head part)

 

```jsx
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>30DaysOfScript:Internal Script</title>
    <script>
      console.log('Welcome to 30DaysOfJavaScript')
    </script>
  </head>
  <body></body>
</html>
```

e.g. 2:  (body part)

```jsx
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>30DaysOfScript:Internal Script</title>
  </head>
  <body>
    <button onclick="alert('Welcome to 30DaysOfJavaScript!');">Click Me</button>
    <script>
      console.log('Welcome to 30DaysOfJavaScript')
    </script>
  </body>
</html>
```

<aside>
✂️ Open the browser console to see the output from the `console.log()`.

</aside>

---

## External Script

- Similar to the internal script, the external script link can be on the header or body, but it is preferred to put it in the body.
- First, we should create an external JavaScript file with .js extension. All files ending with .js extension are JavaScript files.
- Create a file named introduction.js inside your project directory and write the following code and link this .js file at the bottom of the body.

```jsx
console.log('Welcome to 30DaysOfJavaScript')
```

<aside>
👇🏽 External script in the *head*:

</aside>

```jsx
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>30DaysOfJavaScript:External script</title>
    <script src="introduction.js"></script>
  </head>
  <body></body>
</html>
```

<aside>
👇🏽 External script in the *body*:

</aside>

```jsx
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>30DaysOfJavaScript:External script</title>
  </head>
  <body>
    <!-- JavaScript external link could be in the header or in the body --> 
    <!-- Before the closing tag of the body is the recommended place to put the external JavaScript script -->
    <script src="introduction.js"></script>
  </body>
</html>
```

<aside>
✂️ Open the browser console to see the output of the `console.log()`.

</aside>

---

## **Multiple External Scripts**

- We can also link multiple external JavaScript files to a web page. Create a `helloworld.js` file inside the 30DaysOfJS folder and write the following code…

```jsx
console.log('Hello, World!')
```

```jsx
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Multiple External Scripts</title>
  </head>
  <body>
    <script src="./helloworld.js"></script>
    <script src="./introduction.js"></script>
  </body>
</html>
```

<aside>
🚨 *Your main.js file should be below all other scripts*. It’s very important to remember this.

</aside>

---

---

# **Intro to Data types**

→ In JavaScript & also other programming languages, there are different types of data types. 

→ The following are **JavaScript *primitive* data types**: *String, Number, Boolean, undefined, Null*, & *Symbol*.

# Checking Data types

- To check the data type of a certain variable, we use the **typeof** operator.
- e.gs.

```jsx
console.log(typeof 'Natnael') // string
console.log(typeof 7) // number
console.log(typeof true) // boolean
console.log(typeof null) // object 
console.log(typeof undefined) // undefined
```

# Comments

- Commenting in JavaScript is similar to other programming languages. Comments are important in making your code more readable.
- There are 2 ways of commenting:

→ *Single line commenting*

```jsx
// let firstName = 'Natnael'; single line comment
// let lastName = 'Yismaw'; single line comment
```

→ *Multi-line commenting*

```jsx
/*
  let location = 'Addis';
  let age = 20;
  let isMarried = false;
 */
```

# Variables

- Variables are *containers* of data. Variables are used to *store* data in a memory location.
- When a variable is declared, a memory location is reserved. When a variable is assigned to a value (data), the memory space will be filled with that data.
- To declare a variable, we use *var*, *let*, or *const* keywords.

<aside>
💭 For a variable that changes at a different time, we use *let*. If the data does not change at all, we use *const*. For example, PI, country name, gravity do not change, and so we can use *const*.

</aside>

<aside>
✅ A valid JavaScript **variable name** must follow the following rules:

- A JS variable name shouldn’t begin with a number.
- A JS variable name doesn’t allow special characters except dollar sign & underscore.
- A JS variable name follows a camelCase convention.
- A JS variable name shouldn’t have space between words.
</aside>

- The following are examples of valid JavaScript variables:

```jsx
firstName
lastName
country
capitalCity
age
isMarried

first_name
last_name
is_married
capital_city

num1
num_1
_num_1
$num1
year2020
year_2020
```

- Example of invalid variables:

```jsx
first-name
1_num
num_#_1
```

<aside>
😀 Let us declare variables with different data types. To declare a variable, we need to use *let* or *const* keyword before the variable name.

</aside>

```jsx
// Syntax
let nameOfVariable = value
```

e.gs. :

```jsx
// Declaring different variables of different data types
let nickName= 'Natisha'
let country = 'Ethiopia'
let city = 'Addis'
let mile= 101
let isMarried = false

console.log(firstName, lastName, country, city, mile, isMarried)
```

```jsx
Natisha Ethiopia Addis 101 false
```

# Delve into Data Types

- In the previous section, we mentioned a little bit about data types.
- Data types describe the characteristics of data.
- They can be divided into two:
1. Primitive data types
2. Non-primitive data types (Object References)

**Primitive Data Types**

Primitive data types in JavaScript include:

1. Numbers - Integers, floats
2. Strings - Any data under single quote, double quote or backtick quote
3. Booleans - true or false value
4. Null - empty value or no value
5. Undefined - a declared variable without a value
6. Symbol - A unique value that can be generated by Symbol constructor

<aside>
📌 *Primitive* data types are immutable(non-modifiable) data types. Once a primitive data type is created we cannot modify it.

</aside>

**Non-Primitive Data Types**

Non-primitive data types in JavaScript includes:

1. Objects
2. Arrays

<aside>
📌 *Non-primitive* data types are modifiable or mutable. We can modify the value of non-primitive data types after it gets created.

</aside>

<aside>
⚠️ Non-primitive data types cannot be compared by value. Even if two non-primitive data types have the same properties and values, they are not strictly equal.

</aside>

e.g. 

```jsx
let nums = [1, 2, 3]
let numbers = [1, 2, 3]

console.log(nums == numbers)  // false
```

<aside>
👍🏽 Rule of thumb, we do not compare non-primitive data types. Do not compare arrays, functions, or objects.

</aside>

<aside>
⚠️ This is why Non-primitive values are referred to as reference types, because they are being compared by reference instead of value. Two objects are only strictly equal if they refer to the same underlying object.

</aside>

e.g. 

```jsx
let nums = [1, 2, 3]
let numbers = nums

console.log(nums == numbers)  // true
```

---

## **Numbers**

Numbers are integers and decimal values which can do all the arithmetic operations.

e.g.

```jsx
let age = 10
const gravity = 9.81  // we use const for non-changing values, gravitational constant in  m/s2
let mass = 72         // mass in Kilogram
const PI = 3.14       // pi a geometrical constant
const bodyTemp = 37      // oC average human body temperature, which is a constant

console.log(age, gravity, mass, PI, bodyTemp)
```

### Math Object

In JavaScript the Math Object provides a lots of methods to work with numbers.

### Random Number Generator

The JavaScript Math Object has a random() method number generator which generates number from 0 to 0.999999999...

```jsx
let randomNum = Math.random() // generates 0 to 0.999...
```

---

## Strings

Strings are texts, which are under ***single*** , ***double***, ***back-tick*** quote.

### String Concatenation

Connecting two or more strings together is called concatenation. 

e.g.

```jsx
let firstName = 'Natnael'
let lastName = 'Yismaw'
let language = 'JavaScript'
let job = 'student'
let space = ' '   // empty space string

let fullName = firstName + space + lastName; // concatenation, merging two string together.
console.log(fullName);
```

```jsx
Natnael Yismaw
```

**Long Literal Strings:** If the string length is too big & does not fit in one line, we can use the backslash character (\) at the end of each line to indicate that the string will continue on the next line.

**Escape Sequences in Strings**

- \n :new line
- \t  :Tab, means 8 spaces
- \\  :Back slash
- \'  :Single quote
- \"  :Double quote

### String Methods

- Everything in JavaScript is an object. A string is a primitive data type that means we can not modify it once it is created.
- The string object has many string methods. There are different string methods that can help us to work with strings.

1. *length*: The string *length* method returns the number of characters in a string included empty space.

e.g. 

```jsx
let js = 'JavaScript'
console.log(js.length)         // 10
let firstName = 'Natty'
console.log(firstName.length)  // 5
```

2.  *Accessing characters in a string*: We can access each character in a string using its index. In programming, counting starts from 0. The first index of the string is zero, and the last index is the length of the string minus one.

e.g. 

```jsx
let string = 'JavaScript'
let firstLetter = string[0]

console.log(firstLetter)           // J

let lastLetter = string[9]
console.log(lastLetter)            // t
```

3.  *toUpperCase()*: this method changes the string to uppercase letters.

4. *toLowerCase()*: this method changes the string to lowercase letters.

e.g.

```jsx
let string = 'JavaScript'

console.log(string.toUpperCase())     // JAVASCRIPT

let firstName = 'Natnael'

console.log(firstName.toUpperCase())  // NATNAEL

let country = 'EthiopiA'

console.log(country.toLowerCase())   // ethiopia
```

5. *substr()*: It takes two arguments, the starting index and number of characters to slice.

6. *substring()*: It takes two arguments, the starting index and the stopping index but it doesn't include the character at the stopping index.

7. *split()*: The split method splits a string at a specified place.

e.g.

```jsx
let string = 'JavaScript'
console.log(string.substr(4,6))    // Script

let country = 'Finland'

console.log(country.substring(0, 3))   // Fin
console.log(country.substring(3, 7))   // land

let string = '30 Days Of JavaScript'

console.log(string.split())     // Changes to an array -> ["30 Days Of JavaScript"]
console.log(string.split(' '))  // Split to an array at space -> ["30", "Days", "Of", "JavaScript"]
```

8. *includes()*: It takes a substring argument and it checks if substring argument exists in the string. *includes()* returns a boolean. If a substring exist in a string, it returns true, otherwise it returns false.

9. *replace()*: takes as a parameter the old substring and a new substring.

e.g.

```jsx
let country = 'Finland'

console.log(country.includes('fin'))     // false
console.log(country.includes('Fin'))     // true
console.log(country.includes('Land'))    // false

let string = '30 Days Of JavaScript'
console.log(string.replace('JavaScript', 'Python')) // 30 Days Of Python
```

10. *charAt()*: Takes index and it returns the value at that index.

11. *charCodeAt()*: Takes index and it returns char code (ASCII number) of the value at that index.

e.g.

```jsx
let string = '30 Days Of JavaScript'
console.log(string.charAt(0))        // 3

let string = '30 Days Of JavaScript'
console.log(string.charCodeAt(3))        // D ASCII number is 68
```

12. *concat()*: it takes many substrings and joins them.

13. *search*: it takes a substring as an argument and it returns the index of the first match. The search value can be a string or a regular expression pattern.

14. *repeat()*: it takes a number as argument and it returns the repeated version of the string.

e.g.

```jsx
let country = 'Eth'
console.log(country.concat("iopia")) // Ethiopia

let string = 'I love JavaScript'
console.log(string.search('love'))          // 2

let string = 'love'
console.log(string.repeat(5)) // lovelovelovelovelove
```

---

## **Booleans**

Boolean value is either true or false. The use of these data types will be clear when you start the comparison operator because it returns a boolean value.

e.g. 

```jsx
let isLightOn = true
let isRaining = false
let isHungry = false
let truValue = 4 > 3    // true
let falseValue = 4 < 3  // false
```

## Undefined

If we declare a variable and if we do not assign a value, the value will be undefined. In addition to this, if a function is not returning the value, it will be undefined.

```jsx
let firstName
console.log(firstName) //not defined, because it is not assigned to a value yet
```

## Null

```jsx
let empty = null
console.log(empty) // -> null , means no value
```

---

### **Changing Data Type (Casting)**

- We use *parseInt()*, *parseFloat()*, *Number()*, *+ sign*, *str()*
- When we do arithmetic operations string numbers should be first converted to integer or float if not, it returns an error.

### String to Int

We can convert string to number using the following methods:

- parseInt()
- Number()
- Plus sign(+)

```jsx
let num = '10'
let numInt = parseInt(num)
console.log(numInt) // 10

let num = '11'
let numInt = Number(num)
console.log(numInt) // 11

let num = '12'
let numInt = +num

console.log(numInt) // 12
```

**String to Float**

We can convert string float to number using the following methods:

- parseFloat()
- Number()
- Plus sign(+)

```jsx
let num = '9.81'
let numFloat = parseFloat(num)
console.log(numFloat) // 9.81

let num = '2.81'
let numFloat = Number(num)
console.log(numFloat) // 2.81

let num = '7.71'
let numFloat = +num
console.log(numFloat) // 7.71
```

**Float to Int**

We use the following method to convert float to int:

- parseInt()

```jsx
let num = 9.81
let numInt = parseInt(num)

console.log(numInt) // 9
```

# Operators & Date

# Operators:

### Assignment operators

An equal sign in JavaScript is an assignment operator. It uses to assign a variable.

### Arithmetic Operators

Arithmetic operators are mathematical operators.

- Addition(+): a + b;  Subtraction(-): a - b;  Multiplication(*): a * b; Division(/): a / b;  Modulus(%): a % b;  Exponential(**): a ** b

### Comparison Operators

In programming we compare values, we use comparison operators to compare two values. We check if a value is greater or less or equal to other value.

### Logical Operators

The following symbols are the common logical operators: &&(ampersand) , ||(pipe) and !(negation). The && operator gets true only if the two operands are true. The || operator gets true either of the operand is true. The ! operator negates true to false and false to true.

### Increment & **Decrement** Operators

In JavaScript we use the increment operator & Decrement operator to increase & decrease a value stored in a variable, respectively. The increment/ decrement could be pre or post increment/ decrement. Let us see them:

Pre-increment & Post-increment

```jsx
let count = 0
console.log(++count)        // 1
console.log(count)          // 1

let count = 0
console.log(count++)        // 0
console.log(count)          // 1
```

Pre-decrement & Post-decrement

```jsx
let count = 0
console.log(--count) // -1
console.log(count)  // -1

let count = 0
console.log(count--) // 0
console.log(count)   // -1
```

### Ternary Operators

Ternary operator allows to write a condition. Another way to write conditionals is using ternary operators.

e.g. 

```jsx
let isRaining = true
isRaining
  ? console.log('You need a rain coat.')
  : console.log('No need for a rain coat.')
isRaining = false

isRaining
  ? console.log('You need a rain coat.')
  : console.log('No need for a rain coat.')
```

```jsx
You need a rain coat.
No need for a rain coat.
```

---

# **Window Methods:**

**Window alert() method:** displays an alert box with a specified message and an OK button.

**Window prompt() method:** displays a prompt box with an input on your browser to take input values and the input data can be stored in a variable.

**Window confirm() method:** displays a dialog box with a specified message, along with an OK and a Cancel button.

```jsx
alert('Welcome to 30DaysOfJavaScript')

let number = prompt('Enter number', 'number goes here')
console.log(number)

const agree = confirm('Are you sure you like to delete? ')
console.log(agree) // result will be true or false based on what you click on the dialog box
```

---

# **Date Object**

Time is an important thing. We like to know the time a certain activity or event. In JavaScript current time and date is created using JavaScript Date Object.

---

# Conditionals

- Conditional statements are used for make decisions based on different conditions.
- Conditions can be implementing using the following ways:

**if, if else, if else if else, switch, ternary operator.**

## if

```jsx
// syntax
if (condition) {
  //this part of code runs for truthy condition
}
```

## if else

```jsx
// syntax
if (condition) {
  // this part of code runs for truthy condition
} else {
  // this part of code runs for false condition
}
```

## if else if else

```jsx
// syntax
if (condition) {
     // code
} else if (condition) {
   // code
} else {
    //  code

}
```

## switch

Switch is an alternative for **if else if else** .

```jsx
switch(caseValue){
  case 1:
    // code
    break
  case 2:
   // code
   break
  case 3:
   // code
   break
  default:
   // code
}
```

## Ternary Operators

Another way to write conditionals is using ternary operators.

```jsx
let isRaining = true
isRaining
  ? console.log('You need a rain coat.')
  : console.log('No need for a rain coat.')
```

---

# Arrays

## Intro

In contrast to variables, an array can store *multiple values*. Each value in an array has an *index*, and each index has *a reference in a memory address*.

In JS, an array is a collection of different data types which are ordered and changeable(modifiable). An array allows storing duplicate elements and different data types. An array can be empty, or it may have different data type values.

<aside>
⚠️ In JS, an array can contain different data types. Unlike some other programming languages that require arrays to have a consistent data type for all elements, JavaScript allows you to have a mix of different data types within the same array.  For example, you can create an array that contains numbers, strings, booleans, objects, or even other arrays.

</aside>

```jsx
Here's an example: 
var myArray = [1, "Hello", true, { name: "John" }, ["apple", "banana"]];
```

## **How to create an array with values**

- Array of elements with the same data type

```jsx
const numbers = [0, 3.14, 9.81, 37, 98.6, 100] // array of numbers
const webTechs = ['HTML', 'CSS', 'JS', 'React', 'Redux', 'Node', 'MongDB'] // array of strings, web technologies

// Print the array and its length

console.log('Numbers:', numbers)
console.log('Number of numbers:', numbers.length)

console.log('Web technologies:', webTechs)
console.log('Number of web technologies:', webTechs.length)
```

```jsx
//outputs
Numbers: [0, 3.14, 9.81, 37, 98.6, 100]
Number of numbers: 6
Web technologies: ['HTML', 'CSS', 'JS', 'React', 'Redux', 'Node', 'MongDB']
Number of web technologies: 7
```

- Array of elements with different data types

```jsx
const arr = [
    'Natnael',
    250,
    true,
    { country: 'Ethiopia', city: 'Addis' },
    { skills: ['HTML', 'CSS', 'JS', 'C++', 'Python'] }
] // arr containing different data types
console.log(arr)
```

```jsx
//Using split to create an array
let js = 'JavaScript'
const charsInJavaScript = js.split('')

console.log(charsInJavaScript) // ["J", "a", "v", "a", "S", "c", "r", "i", "p", "t"]
```

### Modifying array element

An array is mutable(modifiable). Once an array is created, we can modify the contents of the array elements.

```jsx
const numbers = [1, 2, 3, 4, 5]
numbers[0] = 10      // changing 1 at index 0 to 10
numbers[1] = 20      // changing  2 at index 1 to 20

console.log(numbers) // [10, 20, 3, 4, 5]
```

### Methods to manipulate array

There are different methods to manipulate an array. These are some of the available methods to deal with arrays: *Array, length, concat, indexOf, slice, splice, join, toString, includes, lastIndexOf, isArray, fill, push, pop, shift, unshift*

→**Array constructor**

```jsx
const arr = Array() // creates an an empty array
console.log(arr)

const eightEmptyValues = Array(8) // it creates eight empty values
console.log(eightEmptyValues) // [empty x 8]
```

→**fill() method:** fill all the array elements with a static value

→**********************************concat() method:********************************** to concatenate two arrays

→ **indexOf() method**: to check if an item exist in an array. If it exists, it returns the index else it returns -1.

```jsx
const four4values = Array(4).fill(4) // it creates 4 element values filled with '4'
console.log(four4values) // [4, 4, 4, 4]

const firstList = [1, 2, 3]
const secondList = [4, 5, 6]
const thirdList = firstList.concat(secondList)
console.log(thirdList) // [1, 2, 3, 4, 5, 6]

const numbers = [1, 2, 3, 4, 5]

console.log(numbers.indexOf(5)) // -> 4
console.log(numbers.indexOf(0)) // -> -1
console.log(numbers.indexOf(1)) // -> 0
```

→**toString():** Converts array to string

```jsx
const numbers = [1, 2, 3, 4, 5]
console.log(numbers.toString()) // 1,2,3,4,5

const names = ['Natnael', 'Asabeneh', 'Elias', 'Brook']
console.log(names.toString()) // Natnael,Asabeneh,Elias,Brook
```

→**slice()**: To cut out a multiple items in range. It takes two parameters :starting and ending position. It doesn't include the ending position.

```jsx
const numbers = [1,2,3,4,5]

  console.log(numbers.slice()) // -> it copies all  item
  console.log(numbers.slice(0)) // -> it copies all  item
  console.log(numbers.slice(0, numbers.length)) // it copies all  item
  console.log(numbers.slice(1,4)) // -> [2,3,4] // it doesn't include the ending position
```

→**push()**: adding item in the end. 

```jsx
// syntax
const arr  = ['item1', 'item2','item3']
arr.push('new item')
console.log(arr)
// ['item1', 'item2','item3','new item']
```

→**pop()**: removing item in the end.

```jsx
const numbers = [1, 2, 3, 4, 5]
numbers.pop() // -> remove one item from the end
console.log(numbers) // -> [1,2,3,4]
```

→unshift(): Adding array element in the beginning of the array

→shift(): Removing one array element in the beginning of the array.

→reverse(): reverse the order of an array.

```jsx
const numbers = [1, 2, 3, 4, 5]
numbers.reverse() // -> reverse array order
console.log(numbers) // [5, 4, 3, 2, 1]
```

→**sort()**: arrange array elements in ascending order. 

```jsx
const webTechs = ['HTML','CSS','JavaScript','React','Redux','Node','MongoDB']

webTechs.sort()
console.log(webTechs) // ["CSS", "HTML", "JavaScript", "MongoDB", "Node", "React", "Redux"]

webTechs.reverse() // after sorting we can reverse it
console.log(webTechs) // ["Redux", "React", "Node", "MongoDB", "JavaScript", "HTML", "CSS"]
```

## **Array of arrays**

Array can store different data types including an array itself.

e.g.

```jsx
const firstNums = [1, 2, 3]
const secondNums = [1, 4, 9]

const arrayOfArray =  [[1, 2, 3], [1, 2, 3]]
console.log(arrayOfArray[0]) // [1, 2, 3]

 const frontEnd = ['HTML', 'CSS', 'JS', 'React', 'Redux']
 const backEnd = ['Node','Express', 'MongoDB']
 const fullStack = [frontEnd, backEnd]
 console.log(fullStack)   // [["HTML", "CSS", "JS", "React", "Redux"], ["Node", "Express", "MongoDB"]]
 console.log(fullStack.length)  // 2
 console.log(fullStack[0])  // ["HTML", "CSS", "JS", "React", "Redux"]
 console.log(fullStack[1]) // ["Node", "Express", "MongoDB"]
```

---

# Loops

Most of the activities we do in life are full of repetitions. Such kind of tedious and repetitive task can be carried out using loops. In programming languages (including JS) to carry out repetitive task, we use different kinds of loops. These are:

## 1. for loop

e.g

```jsx
for(let i = 0; i <= 5; i++){
  console.log(i)
}
// 0 1 2 3 4 5

for(let i = 0; i <= 5; i++){
  console.log(`${i} * ${i} = ${i * i}`)
}
/*
0 * 0 = 0
1 * 1 = 1
2 * 2 = 4
3 * 3 = 9
4 * 4 = 16
5 * 5 = 25
*/

```

## 2. while loop

e.g.

```jsx
let i = 0
while (i <= 5) {
  console.log(i)
  i++
}

// 0 1 2 3 4 5
```

## 3. do while loop

e.g.

```jsx
let i = 0
do {
  console.log(i)
  i++
} while (i <= 5)

// 0 1 2 3 4 5
```

## 4. for of loop

We use for of loop for arrays.

```jsx
for (const element of arr) {
  // code goes here
}
```

e.g.

```jsx
for (const num of numbers) {
  console.log(num * num)
}

// 1 4 9 16 25
```

### break

Break is used to interrupt a loop.

### continue

We use the keyword *continue* to skip a certain iterations.

---

# Functions

- A function is a reusable block of code or programming statements designed to perform a certain task.
- It’s declared by a function keyword followed by a name, followed by parentheses ().
- A parentheses can take a parameter. If a function take a parameter it will be called with argument. A function can also take a default parameter.
- Function makes our code *clean & easy to read, reusable, & easy to test.*
- A function can be declared or created in couple of ways:
    - *Declaration function*
    - *Expression function*
    - *Anonymous function*
    - *Arrow function*
    
    ## Function Declaration
    
    Let us see how to declare a function and call a function.
    
    ```jsx
    //declaring a function without a parameter
    function functionName() {
      // code goes here
    }
    functionName() // calling function by its name and with parentheses
    ```
    
    **Function without a parameter and return:**
    
    ```jsx
    // function without parameter
    function addTwoNumbers() {
      let numOne = 10
      let numTwo = 20
      let sum = numOne + numTwo
    
      console.log(sum)
    }
    
    addTwoNumbers() // a function has to be called by its name to be executed
    ```
    
    **Function with a parameter:**
    
    ```jsx
    // function with one parameter
    function functionName(parm1) {
      //code goes here
    }
    functionName(parm1) // during calling or invoking one argument needed
    
    function areaOfCircle(r) {
      let area = Math.PI * r * r
      return area
    }
    
    console.log(areaOfCircle(10)) // should be called with one argument
    ```
    
    **Function with many parameters:**
    
    ```jsx
    // function with multiple parameters
    function functionName(parm1, parm2, parm3,...){
      //code goes here
    }
    functionName(parm1,parm2,parm3,...) // during calling or invoking three arguments needed
    
    // this function takes array as a parameter and sum up the numbers in the array
    function sumArrayValues(arr) {
      let sum = 0;
      for (let i = 0; i < arr.length; i++) {
        sum = sum + arr[i];
      }
      return sum;
    }
    const numbers = [1, 2, 3, 4, 5];
        //calling a function
    console.log(sumArrayValues(numbers));
    ```
    
    ## **Anonymous Function**
    
    are anonymous function or without name.
    
    ```jsx
    const anonymousFun = function() {
      console.log(
        'I am an anonymous function and my value is stored in anonymousFun'
      )
    }
    ```
    
    ## **Expression Function**
    
    are anonymous functions. After we create a function without a name and we assign it to a variable.
    
    To return a value from the function we should call the variable.
    
    ```jsx
    // Function expression
    const square = function(n) {
      return n * n
    }
    
    console.log(square(2)) // -> 4
    ```
    
    ## **Self Invoking Functions**
    
    are anonymous functions which do not need to be called to return a value.
    
    ```jsx
    (function(n) {
      console.log(n * n)
    })(2) // 4, but instead of just printing if we want to return and store the data, we do as shown below
    
    let squaredNum = (function(n) {
      return n * n
    })(10)
    
    console.log(squaredNum)
    ```
    
    ## Arrow function
    
    Arrow function is an alternative to write a function, however function declaration and arrow function have some minor differences.
    
    Arrow function uses arrow instead of the keyword *function* to declare a function. Let us see both:
    
    ```jsx
    // This is how we write normal or declaration function
    // Let us change this declaration function to an arrow function
    function square(n) {
      return n * n
    }
    
    console.log(square(2)) // 4
    
    const square = n => {
      return n * n
    }
    
    console.log(square(2))  // -> 4
    
    // if we have only one line in the code block, it can be written as follows, explicit return
    const square = n => n * n  // -> 4
    ```
    
    ### **Function with default parameters**
    
    Sometimes we pass default values to parameters, when we invoke the function if we do not pass an argument the default value will be used.
    
    ```jsx
    function greetings(name = 'Natnael') {
      let message = `${name}, welcome to 30 Days Of JavaScript!`
      return message
    }
    
    console.log(greetings())
    console.log(greetings('Asabeneh'))
    ```
    
    ---
    

# Objects

## Scope

→ Variable is the fundamental part in programming. A variable can be declared at different scope.

→ Variables scopes can be:

- Global
- Local

### **Global scope**

A globally declared variable can be accessed every where in the same file. But the term global is relative. It can be global to the file or it can be global relative to some block of codes.

### Local scope

A variable declared as local can be accessed only in certain block code.

- Block Scope
- Function Scope

---

## Object

To create an object literal, we use two curly brackets.

An empty object

```jsx
const person = {}
```

### Creating an object with values

Now, the person object has firstName, lastName, age, location, skills and isMarried properties. The value of properties or keys could be a string, number, boolean, an object, null, undefined or a function.

Let us see some examples of object.

```jsx
const person = {
  firstName: 'Natnael',
  lastName: 'Yismaw',
  age: 20,
  country: 'USA',
  city: 'Boston',
  skills: [
    'HTML',
    'CSS',
    'JavaScript',
    'React',
    'Node',
    'MongoDB',
    'Python',
    'Express.js'
  ],
  isMarried: false
}
console.log(person)
```

### Getting values from an object

We can access values of object using two methods:

- using . followed by key name if the key-name is a one word
- using square bracket and a quote

```jsx
...
// accessing values using .
console.log(person.firstName)
console.log(person.lastName)
console.log(person.location) // undefined

// value can be accessed using square bracket and key name
console.log(person['firstName'])
console.log(person['lastName'])
console.log(person['location']) // undefined
```

**Creating object methods**

```jsx
...
getFullName: function() {
    return `${this.firstName} ${this.lastName}`
  }
}

console.log(person.getFullName())
// Natnael Yismaw
```

### Setting new key for an object

An object is a mutable data structure and we can modify the content of an object after it gets created.

### Object Methods

There are different methods to manipulate an object. Let us see some of the available methods.

*Object.assign()*: To copy an object without modifying the original object

*Object.keys()*: To get the keys or properties of an object as an array

*Object.values()*:To get values of an object as an array

*Object.entries()*:To get the keys and values in an array

*hasOwnProperty()*: To check if a specific key or property exist in an object