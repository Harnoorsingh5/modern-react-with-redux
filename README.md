# React Notes
JS library created by Facebook - used by instagram and Netflix
Used to create JS driven dynamic web pages

## How react works?
we create components in our project for different part of application
For e.g, we have different components for navbar, search box and footer. 
So it is react job to inject these components into DOM
Question is how it does this?
* It takes in all the components and create a javascript representation of the DOM known as virtual DOM.
* Then it takes that virtual DOM and it actually renders it to the browser and creates the Actual DOM.
* The idea here is that anytime there is a change in a component the virtual dom helps to change the actual DOM in quite fast and efficient manner.
* For e.g there is a change in state of searchbox, then react create a new virtual DOM for that component.
* Then  it compares it to the old one, and is able to change the actual DOM easily as it knows where the change has to be made.

## Creating a react app:
```
	npx create-react-app my-app
	cd my-app
	npm start
```

## What is App function?
![picture](https://github.com/Harnoorsingh5/modern-react-with-redux/blob/master/images/AppComponent.png)

Componenet in react has two jobs:
* They produce jsx  
* They also handle user events; such as user typing into a text input or clicking on a button

Jsx:
* Set of instructions that tells react what we want to show on the screen
* Jsx elements are created to tell the React to create normal HTML element (like, div, span, h1, table, etc.)
* To Tell React to show another component (created by user)

## process flow of jsx
![picture](https://github.com/Harnoorsingh5/modern-react-with-redux/blob/master/images/question.png)
- When ever a Jsx is rendered, react is going to iterate over each element inside that block of jsx
- For every element it going to ask a question, Is this a DOM element? 
- if yes; then show  div on the screen to user
- if no it is a component; then call the component function and inspect all jsx we get back

## How index.js renders App componenet?
![picture](https://github.com/Harnoorsingh5/modern-react-with-redux/blob/master/images/indexjs.png)