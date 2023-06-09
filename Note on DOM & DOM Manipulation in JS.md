# Note on DOM & DOM Manipulation in JS

<aside>
💡 *DOM is a platform that allows programs & scripts to dynamically access & update the content, structure, and style of a document.* In short, it defines a standard for accessing docs.

</aside>

<aside>
💡 The W3C DOM is separated into 3 different parts: Core DOM, XML DOM & HTML DOM.

</aside>

<aside>
💡 HTML DOM is standard model for HTML documents

</aside>

<aside>
💡 HTML DOM talks about the idea that we can manipulate HTML elements using JS (or other programming languages).

</aside>

# The HTML DOM (Document Object Model)

→ The HTML DOM helps in enabling JS to access & change all the elements of an html document. This means JS gets the power to create dynamic html.

→ The DOM represents a web page as a *tree of objects. This means that in DOM, all html elements are defined as **objects.***

→ The browser is the one that creates the **D**ocument **O**bject **M**odel of a web page when it’s loaded in the browser.

→ Tnx to this model, JS can :

- change all the html elements, all the html attributes, & all the css styles in the page
- remove existing html elements & attributes
- add new html elements & attributes
- react to all existing html events in the page
- create new HTML events in the page.

<aside>
📌 **RECAP: The HTML DOM is a standard for how to get, change, add, or delete HTML elements.**

</aside>

---

**Getting or Finding elements**

→ Often, with JS, we want to manipulate HTML elements. To do so, we’ve to find the elements first. There are several ways to do this. The common ones are:

Getting HTML elements 

- by id
- by class name
- by tag name
- by using querySelector methods

*The code below has four h1 elements. Let us see the different methods to access the h1 elements.*

```jsx
<!DOCTYPE html>
  <html lang="en">
    <head>
      <title>Document Object Model Example</title>
    </head>
    <body>

     <h2 class='title' id='first-title'>First Title</h1>
     <h2 class='title' id='second-title'>Second Title</h1>
     <h3 class='title' id='third-title'>Third Title</h1>
     <h2></h2>

    </body>
  </html>
```

**a) Getting HTML elements by id**

→ is the easiest way to find an HTML element

→***getElementsById()*** targets a single HTML element

```jsx
//syntax
document.getElementById('id')
```

e.g.

```jsx
let firstTitle = document.getElementById('first-title')
console.log(firstTitle) // <h2>First Title</h2>
```

**b) Getting HTML elements by class name**

→***getElementsByClassName()*** method is used to get all HTML elements with the same class name.

→It returns an HTMLCollection object

```jsx
//syntax
document.getElementsByClassName('classname')
```

e.g.

```jsx
const allTitles = document.getElementsByClassName('title')

console.log(allTitles) //prints HTMLCollection(3)
console.log(allTitles.length) // 3
console.log(allTitles[0])  //First Title

for (let i = 0; i < allTitles.length; i++) {
  console.log(allTitles[i]) // prints each elements in the HTMLCollection
}
```

**c) Getting HTML elements by tag name**

→***getElementsByTagName()***: takes a tag name as a string parameter & returns an HTMLCollection object.

```jsx
// syntax
document.getElementsByTagName('tagname')
```

e.g. 

```jsx
const allTitles = document.getElementsByTagName('h2')

console.log(allTitles) //HTMLCollections
console.log(allTitles.length) // 3

for (let i = 0; i < allTitles.length; i++) {
  console.log(allTitles[i]) // prints each elements in the HTMLCollection
}
```

d) **Getting HTML elements by using querySelector methods**

*document.querySelector() : used to select html element(s) by tag name, by id or by class name.*

e.g.

```jsx
let firstTitle = document.querySelector('h2') // select the first available h2 element
let firstTitle = document.querySelector('#first-title') // select id with first-title
let firstTitle = document.querySelector('.title') // select the first available element with class title
```

*document.querySelectorAll() :* used to select html elements by its tag name or class. It returns a nodeList. We can use ***for loop*** or ***forEach*** to loop through each nodeList elements.

e.g.

```jsx
const allTitles = document.querySelectorAll('h2') // selects all the available h2 elements in the page

console.log(allTitles.length) // 3
for (let i = 0; i < allTitles.length; i++) {
  console.log(allTitles[i])
}
```

---

## **Adding Text to HTML element**

→ We can add a text content using the property *textContent* or innerHTML. This also means that we can change the contents of an html element.

→ *textContent* is meant to add text to an HTML element, however innerHTML can add a text or HTML element or elements as a child.

**Adding Text content using textContent**

e.g.

```jsx
const titles = document.querySelectorAll('h2')    //check this out
titles[2].textContent = 'Fourth Title'
```

**Adding Text Content using innerHTML**

e.g.

```jsx
<!DOCTYPE html>
<html>
  <head>
    <title>innerHTML Example</title>
  </head>
  <body>
    <div id="myDiv">
      <h1>Welcome!</h1>
      <p>This is some content.</p>
    </div>

    <button onclick="changeContent()">Change Content</button>

    <script>
      function changeContent() {
        var otherDiv = document.getElementById('myDiv');
        otherDiv.innerHTML = '<h1>New Heading</h1><p>New content</p>';
      }
    </script>
  </body>
</html>
```

In the above example, we’ve an html page with a **`<div>`** element having the id "myDiv". Inside the **`<div>`**, there is an **`<h1>`** heading and a **`<p>`** paragraph.

Below the **`<div>`**, there is a **`<button>`** element with an **`onclick`** attribute. When the button is clicked, it triggers the **`changeContent()`** function.

In the JavaScript code, the **`changeContent()`** function selects the **`<div>`** element with the id "myDiv" using **`getElementById()`**. Then, it uses “the **`innerHTML`** property” to modify the content of the **`<div>`**.

When the button is clicked, the content inside the **`<div>`** is replaced with the new HTML markup specified in the **`innerHTML`** assignment. In this case, the **`<h1>`** heading is changed to "New Heading" and the **`<p>`** paragraph is changed to "New content".

<aside>
⚠️ See the e.g on innerHTML from Asabeneh :)

</aside>

---

**Adding attribute**

→Common HTML attributes: id, class, src, style, href , title, alt. 

- Using ***setAttribute()*** method

→It takes 2 parameters the type of the attribute and the name of the attribute.

e.g. *(adding class & id for the fourth title)*

```jsx
const titles = document.querySelectorAll('h2')
titles[2].setAttribute('class', 'title')
titles[2].setAttribute('id', 'fourth-title')
```

- Without ***setAttribute()***

e.g.

```jsx
const titles = document.querySelectorAll('h2')
titles[2].className = 'title'                     //CROSS CHECK z index position
titles[2].id = 'fourth-title'
```

<aside>
😀 We can specifically add/remove class attributes using the classList method. Id there’s already existing class, then it doesn’t override it, instead it appends (i.e. adds additional class).

</aside>

```jsx
//another way to setting an attribute: .classList.add
titles[3].classList.add('title', 'header-title')
//another way to setting an attribute: .classList.remove
titles[3].classList.remove('title', 'header-title')
```

---

---

# Manipulating DOM Object (or simply, DOM Manipulation)

## **Creating Element(s)**

**a) Creating a single element**

→We use the method ***document.createElement()***. The method takes an HTML element tag name as a string parameter.

```jsx
// syntax
document.createElement('tagname')
```

e.g.

```jsx
<!DOCTYPE html>
<html>

<head>
    <title>Document Object Model:Me learning from Mr Asabeneh</title>
</head>

<body>

    <script>
        let title = document.createElement('h1')
        title.className = 'title'
        title.style.fontSize = '30px'
        title.textContent = 'Creating HTML element using DOM'

        console.log(title)
    </script>
</body>

</html>
```

<aside>
☝🏽 The above code dynamically creates an **`<h1>`** element using the DOM & sets its class name, font size, & text content.

</aside>

**b) Creating multiple elements**

→Here, we should use loop. Using loop, we can create as many HTML elements as we want.

e.g.

```jsx
<!DOCTYPE html>
<html>

<head>
    <title>Document Object Model:Me learning from Mr Asabeneh</title>
</head>

<body>

    <script>
        let title
        for (let i = 0; i < 3; i++) {
            title = document.createElement('h1')
            title.className = 'title'
            title.style.fontSize = '30px'
            title.textContent = i
            console.log(title)
        }
    </script>
</body>

</html>
```

## **Appending child to a parent element**

→To see a created element on the HTML document, we should append it to the parent as a child element.

→To access the HTML document body, we use *document.body*. w/h supports the *appendChild()* method.

e.g.

```jsx
<!DOCTYPE html>
<html>

<head>
    <title>Document Object Model:Me learning from Mr Asabeneh</title>
</head>

<body>

    <script>
        // creating multiple elements & appending to parent element
        let title
        for (let i = 0; i < 3; i++) {
            title = document.createElement('h1')
            title.className = 'title'
            title.style.fontSize = '30px'
            title.textContent = i
            document.body.appendChild(title)
        }
    </script>
</body>
</html>
```

### **Removing a child element from a parent node**

→To remove a child element from a parent node in JavaScript using the DOM, you can utilize the **`removeChild()`** method.

e.g.

```jsx
<!DOCTYPE html>
<html>
  <head>
    <title>Remove Child Example</title>
  </head>
  <body>
    <div id="parent">
      <h1>Parent Element</h1>
      <p>This is a child element.</p>
    </div>

    <button onclick="removeChildElement()">Remove Child Element</button>

    <script>
      function removeChildElement() {
        var parent = document.getElementById('parent');
        var child = parent.querySelector('p'); // Select the <p> element within the parent

        parent.removeChild(child); // Remove the child element from the parent
      }
    </script>
  </body>
</html>
```

<aside>
☝🏽 In the JS code, the **`removeChildElement()`** function first selects the parent element using **`getElementById()`** and stores it in the **`parent`** variable. Then, it uses **`querySelector()`** on the parent to select the specific child element to be removed, which is the **`<p>`** element in this case. The selected child element is stored in the **`child`** variable.

Finally, the **`removeChild()`** method is called on the parent element, passing the child element as the argument. This removes the child element from the parent node, effectively removing it from the DOM.

</aside>