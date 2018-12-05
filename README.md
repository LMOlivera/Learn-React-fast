# Learn-React-fast
Are you an impatient student like me? This is the React tutorial for you.


# Index
- [Before we start](#Before)
  - [Things you should know...](#Know)
  - [Tools](#Tools)
- [Introduction](#Introduction)
  - [Virtual DOM](#VirtualDOM)
  - [JSX](#JSX)
- [Basic](#Basic)
  - [What is a React Component?](#ReactComponent)
    - [Function component](#FunctionComponent)
    - [Class component](#ClassComponent)
    - [Input example](#InputExample)
    - [Output example](#OutputExample)
    - [When to use Function or Class component](#WhenFunctionClass)
  - [Props](#Props)
    - [Working in a function](#PropFunction)
    - [Working in a class](#PropClass)
    - [Result](#PropResult)
  - [State](#State)
  - [Lifecycle](#Lifecycle)
    - [Change the state](#ChangeState)
- [Some things to have in mind](#Things)


# <a name="Before">Before we start...</a>
I’m writing this because of **two reasons**:
1. The first is to ensure I know React so well that I can write a tutorial.
2. I consider most tutorials to be very slow and I like going fast and straight to action, so here you will see little text just to know what is going on. Because of this I will mention some features I will not be using because I consider them unnecesary, if you want you can research them on your own.


### <a name="Know">Things you should know...</a>
I assume you already know basic HTML and CSS, and have a good knowledge of Javascript. If you don't, I recommend you study and learn those first because you will not understand this **fast** tutorial.


### <a name="Tools">Tools</a>
- [codepen.io](https://codepen.io/LeWanderer/pen/rqBPqO): Codepen allows you to write HTML, CSS and Javascript while seeing the results. Here is the link for a React.js template I made, just fork it and work on your own while reading this tutorial C:
- [React CDN](https://reactjs.org/docs/cdn-links.html): You can use React through it's CDN.


# <a name="Introduction">Introduction</a>
React.js is an Open Source library developed by Facebook Developers, for building User Interfaces (UI). React makes user interfaces very easy to build by cutting each page into pieces. We call these pieces **components**.

<img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/components.png?raw=true" alt="Google components">

React is fairly easy to understand and at this moment has an excellent reputation and a great community. It supports ES6 and can perform client-side as well as server side rendering.

**Note:** Represents View in Model-View-Controller architectural pattern, that means you will need more tools in the future to cover the Model and Controller part.


### <a name="VirtualDOM">Virtual DOM</a>
<img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/DOM%20and%20Virtual%20DOM.png?raw=true" alt="DOM and Virtual DOM comparison">

Consider a page displaying a list containing 10 items and one is getting updated. DOM will rebuild the entire list making it work 10 times more than what is necessary.

Virtual DOM is an abstract, lightweight copy of DOM. It can be changed as and when we want and then can be saved to the real DOM. Whenever a change occurs, Virtual DOM efficiently rerenders the DOM. It is much faster than DOM. It has the same properties as a real DOM object.


### <a name="JSX">JSX</a>
<img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/JSX%20example%201.png?raw=true" alt="JSX Example 1">
<img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/JSX%20example%202.png?raw=true" alt="JSX Example 2">

React uses a syntax extension of JavaScript called JSX that allows you to write HTML directly within JavaScript (but JSX is **NOT** HTML). It is not necessary to use it but I recommend it as it makes your code more readable.

![#f03c15](https://placehold.it/15/f03c15/000000?text=+) `However, because JSX is not valid JavaScript, JSX code must be compiled into JavaScript. The transpiler Babel is a popular tool for this process.` 

![#f03c15](https://placehold.it/15/f03c15/000000?text=+) `Self-enclosing tags: An important way in which JSX differs from HTML is the idea of self-enclosing tags.` 

<img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/Self-enclosing%20tags.png?raw=true" alt="Self-enclosing tag">

<img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/Self-enclosing%20tags%20output.png?raw=true" alt="Self-enclosing tag output">


**Note**: You can use Javascript inside HTML (JSX) writing {code} (example in second picture). If you don't understand the code above please don't panic and come back in a few minutes.


# <a name="Basic">Basic</a>
Building Blocks of ReactJS
A typical ReactJS program constitutes:
- Components (Next section!).
- Elements: An element describes what you want to see on the screen. Unlike browser DOM elements, React elements are plain objects, and are cheap to create. In the official documentation they talk more about them, but I consider them a waste of time so I’m not gonna cover them.
<img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/Element%20example.png?raw=true" alt="Element example">

- Props
- State
- Lifecycle


### <a name="ReactComponent">What is a React Component?</a>
Javascript function/class that represents a piece of a webpage. To build a page, we call these functions/classes in a certain order, put the result together, and show it to the user.


##### <a name="FunctionComponent">Function component</a>
<img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/Function%20component%201.png?raw=true" alt="Function component example 1">
<img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/Function%20component%202.png?raw=true" alt="Function component example 2">


##### <a name="ClassComponent">Class component</a>
<img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/Class%20component.png?raw=true" alt="Function component example 1">

If we call the OurFirstComponent() function we’ll get back a bit of JSX. We can use something called ReactDOM.render(Component,locationForComponent) to put it on the page.


##### <a name="InputExample">Input example</a>
<img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/ReactDOM.render%20example.png?raw=true" alt="ReactDOM.render() example">


##### <a name="OutputExample">Output example</a>
<img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/ReactDOM.render%20test%20result.png?raw=true" alt="ReactDOM.render() result">


##### <a name="WhenFunctionClass">When to use Function or Class component</a>
The main difference between Function or Class is that Classes have more features, like state, lifecycle, handling events, etc. You will learn about them soon.


### <a name="Props">Props</a>
Inputs accepted by components.

##### <a name="PropFunction">Working in a function</a>
<img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/Function%20prop%20example.png?raw=true" alt="Function prop example">


##### <a name="PropClass">Working in a class</a>
<img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/Class%20prop%20example.png?raw=true" alt="Class prop example">


##### <a name="PropResult">Result</a>
<img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/Prop%20output%20example.png?raw=true" alt="Prop output example">


### <a name="State">State</a>
State is similar to props, but it is private and fully controlled by the component. You have to add a constructor to the class in order to initialize the state.

<img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/Component%20with%20state%20example.png?raw=true" alt="Component with state example">

<img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/Component%20with%20state%20output.png?raw=true" alt="Component with state output">

##### <a name="ChangeState">Change the state</a>

<img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/How%20to%20change%20the%20state.png?raw=true" alt="Change state">


### <a name="Lifecycle">Lifecycle</a>
You can see an excelent example of lifecycle in [this pen](https://codepen.io/gaearon/pen/amqdNA?editors=0010) (you should be able to understand it). There are **two** important methods in every React Component: componentDidMount() and componentWillUnmount(). 

- componentDidMount(): When the component is rendered on the website this method is triggered. In the example it creates a setInterval for tick().
- componentWillUnmount(): If for some reason the component is removed from the DOM, this method will be triggered. In the example clears the interval created by componentDidMount().


# <a name="Things">Some things to have in mind</a>
- It is consider a bad practice to change a Parents state from Child. Try to think how will you manage Parents and Childs before programming, it will save you a lot of time.
  - However, you can do this by binding a Parent function to the Child.
- Keep in mind you can style components in four ways:

  - You can give JSX a className (you can't use "class" because it is not HTML, it's JSX) to select it from CSS:
  <img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/Styling%20components%20-%20CSS%20Stylesheet.png?raw=true" alt="Styling by Stylesheet">
  
  - Inline styling:
  <img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/Styling%20components%20-%20Inline%20styling.png?raw=true" alt="Styling by inline-styling">
  
  - CSS Modules:
  <img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/Styling%20components%20-%20CSS%20Modules.png?raw=true" alt="Styling by inline-styling">
 
  - Styled components:
  <img align="middle" src="https://github.com/LeWanderer/Learn-React-fast/blob/draft/images/Styling%20components%20-%20Styled-components.png?raw=true" alt="Styling by styled components">
  

