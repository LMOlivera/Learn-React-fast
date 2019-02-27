# Learn-React-fast
Are you an impatient student like me? This is the React tutorial for you.

<p align="center">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/reactjs.png" alt="Google components">
</p>


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
    - [Changing the state](#ChangeState)
  - [Lifecycle](#Lifecycle)
- [Some things to have in mind](#Things)
- [Extra information](#ExtraInfo)


# <a name="Before">Before we start...</a>
I’m writing this because of **two reasons**:
1. The first is to ensure I know React so well that I can write a tutorial.
2. I consider most tutorials to be very slow and I like going fast and straight to action, so here you will see little text just to know what is going on. Because of this I will mention some features I won't cover because I consider them [unnecesary](#ExtraInfo).


### <a name="Know">Things you should know...</a>
I assume you already know basic HTML and CSS, and have a good knowledge of Javascript. If you don't, I recommend you study and learn those first because you will not understand this **fast** tutorial.


### <a name="Tools">Tools</a>
- [codepen.io](https://codepen.io/LMOlivera/pen/rqBPqO): Codepen allows you to write HTML, CSS and Javascript while seeing the results. Here is the link for a React.js template I made, just fork it and work on your own while reading this tutorial C:
- [React CDN](https://reactjs.org/docs/cdn-links.html): You can use React through it's [CDN](#CDN).


# <a name="Introduction">Introduction</a>
React.js is an Open Source library developed by Facebook Developers, for building User Interfaces (UI). React makes user interfaces very easy to build by cutting each page into pieces. We call these pieces **components**.

<p align="center">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/components.png" alt="Google components">
</p>


React is fairly easy to understand and at this moment has an excellent reputation and a great community. It supports [ES6](#ES6) and can perform [client-side as well as server-side rendering](#CSSR).

**Note:** Represents View in Model-View-Controller architectural pattern, that means you will need more tools in the future to cover the Model and Controller part.


### <a name="VirtualDOM">Virtual DOM</a>

<p align="center">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/DOM%20and%20Virtual%20DOM.png" alt="DOM and Virtual DOM comparison">
</p>


Consider a page displaying a list containing 10 items and one is getting updated. DOM will rebuild the entire list making it work 10 times more than what is necessary.

Virtual DOM is an abstract, lightweight copy of DOM. It can be changed as and when we want and then can be saved to the real DOM. Whenever a change occurs, Virtual DOM efficiently rerenders the DOM. It is much faster than DOM. It has the same properties as a real DOM object.


### <a name="JSX">JSX</a>

<p align="center">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/JSX%20example%201.png" alt="JSX Example 1">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/JSX%20example%202.png" alt="JSX Example 2">
</p>


React uses a syntax extension of JavaScript called JSX that allows you to write HTML directly within JavaScript (but JSX is **NOT** HTML). It is not necessary to use it but I recommend it as it makes your code more readable.

![#f03c15](https://placehold.it/15/f03c15/000000?text=+) However, because JSX is not valid JavaScript, JSX code must be compiled into JavaScript. The [transpiler](#ExtraInfo) Babel is a popular tool for this process. 

![#f03c15](https://placehold.it/15/f03c15/000000?text=+) Self-enclosing tags: An important way in which JSX differs from HTML is the idea of self-enclosing tags.

<p align="center">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/Self-enclosing%20tags.png" alt="Self-enclosing tag">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/Self-enclosing%20tags%20output.png" alt="Self-enclosing tag output">
</p>


**Note**: You can use Javascript inside HTML (JSX) writing {code} (example in second picture). If you don't understand the code above please don't panic and come back in a few minutes.


# <a name="Basic">Basic</a>

### Building Blocks of ReactJS

A typical ReactJS program constitutes:
- [Components](#ReactComponent).
- [Elements](#Elements) will not be covered here.
- [Props](#Props).
- [State](#State).
- [Lifecycle](#Lifecycle).


### <a name="ReactComponent">What is a React Component?</a>
Javascript function/class that represents a piece of a webpage. To build a page, we call these functions/classes in a certain order, put the result together, and show it to the user.


##### <a name="FunctionComponent">Function component</a>

<p align="center">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/Function%20component%201.png" alt="Function component example 1">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/Function%20component%202.png" alt="Function component example 2">
</p>


##### <a name="ClassComponent">Class component</a>

<p align="center">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/Class%20component.png" alt="Function component example 1">
</p>


If we call the OurFirstComponent() function we’ll get back a bit of JSX. We can use something called ReactDOM.render(Component,locationForComponent) to put it on the page.


##### <a name="InputExample">Input example</a>
<p align="center">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/ReactDOM.render%20example.png" alt="ReactDOM.render() example">
</p>


##### <a name="OutputExample">Output example</a>
<p align="center">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/ReactDOM.render%20test%20result.png" alt="ReactDOM.render() result">
</p>


##### <a name="WhenFunctionClass">When to use Function or Class component</a>
The main difference between Function or Class is that Classes have more features, like state, lifecycle, handling events, etc. You will learn about them soon.


### <a name="Props">Props</a>
Inputs accepted by components.

##### <a name="PropFunction">Working in a function</a>
<p align="center">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/Function%20prop%20example.png" alt="Function prop example">
</p>


##### <a name="PropClass">Working in a class</a>
<p align="center">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/Class%20prop%20example.png" alt="Class prop example">
</p>


##### <a name="PropResult">Result</a>
<p align="center">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/Prop%20output%20example.png" alt="Prop output example">
</p>


### <a name="State">State</a>
State is similar to props, but it is private and fully controlled by the component. You have to add a constructor to the class in order to initialize the state.

<p align="center">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/Component%20with%20state%20example.png" alt="Component with state example">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/Component%20with%20state%20output.png" alt="Component with state output">
</p>


##### <a name="ChangeState">Changing the state</a>
<p align="center">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/How%20to%20change%20the%20state.png" alt="Change state">
</p>


### <a name="Lifecycle">Lifecycle</a>
You can see an excelent example of lifecycle in [this pen](https://codepen.io/gaearon/pen/amqdNA?editors=0010) (you should be able to understand it). 

<p align="center">
    <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/React%20Lifecycle.jpeg" alt="React Lifecycle">
  </p>
  
- componentDidMount(): When the component is rendered on the website this method is triggered. In the example it creates a setInterval for tick(). Great place to initiate network requests. Keep in mind that using setState() in componentDidMount() will cause a re-render of the component, affecting performance.
- componentWillUnmount(): If for some reason the component is removed from the DOM, this method will be triggered. In the example clears the interval created by componentDidMount().
- shouldComponentUpdate(): Invoked whenever new props or state is being received by the component. If you consider that props/state don't need to update the component you should return false. Otherwise, true.
- componentDidUpdate(): It allows you to interact with the DOM when the component has been updated.
- static getDerivedStateFromProps(): His only purpose is to enable a component to update its state depending of changes in his props.
- getSnapshotBeforeUpdate(): Called just before the most newly rendered output is attached to the DOM. It returns a snapshot value or null and this returned value is always passed as a parameter to componentDidUpdate().

Legacy lifecycle methods:
Here are old methods that even the [official documentation of React](https://reactjs.org/docs/react-component.html#legacy-lifecycle-methods) encourages not to use.

- UNSAFE_componentWillMount(): Called before the component is being mounted. If you need to set the initial state of a component, use constructor() instead. If you plan to use any functions that create any side effects or subscriptions, use componentDidMount() instead.
- UNSAFE_componentWillReceiveProps(): It creates bugs and inconsistencies. If you need to fetch data or create an animation, you should rather use componentDidMount().
- UNSAFE_componentWillUpdate(): Unless shouldComponentUpdate() returns false, this method is being triggered when new props or state are being received. You can use UNSAFE_componentWillUpdate() to execute preparation before an update. Do not use this.setState()inside it. Use componentDidMount() instead.


# <a name="Things">Some things to have in mind</a>
- It is consider a bad practice to change a Parents state from Child. Try to think how to manage Parents and Childs before programming, it will save you a lot of time.
  - However, you can do this by binding a Parent function to the Child.
- Keep in mind you can style components in four ways:

  - You can give JSX a className (you can't use "class" because it is not HTML, it's JSX) to select it from CSS: This is the way everyone styles components when learning React. However, one issue that will arise you begin adding more components lies in the naming of your components a all style rules declared are globally scoped. This is a problem where, for example, you had two elements with the same name, created by either you or your teammate.
  
  <p align="center">
    <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/Styling%20components%20-%20CSS%20Stylesheet.png" alt="Styling by Stylesheet">
  </p>
    
  - Inline styling: One thing to take into consideration is that it is an object, so that means no dashes (e.g. font-weight) as in regular CSS. The style properties are written using camelCase. So font-weight will be fontWeight and so on. Conditional styling is also possible here. 
  CONS: With this method, pseudo selectors like :hover as well as media queries can be used when there are only like 2 or 3 properties that doesn’t require the use of media queries or pseudo selectors, and/or in situations where there will be a need for conditional styling.
  
  <p align="center">
    <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/Styling%20components%20-%20Inline%20styling.png" alt="Styling by inline-styling">
  </p>
    
  - CSS Modules: CSS Modules are very similar to writing CSS in external stylesheets (as in the first method). The only difference is that the styles are locally scoped unlike with traditional external stylesheets. This means that style rules won’t clash together or overwrite each other. You basically use the same methods as you would normally use when styling components using traditional CSS. It also allows you to use all the nice methodolgies like BEM. You can read more about it here: [CSS Modules](https://github.com/css-modules/css-modules).
  
  <p align="center">
    <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/Styling%20components%20-%20CSS%20Modules.png" alt="Styling by inline-styling">
  </p>
   
  - Styled components: This is considered a bad practice, you shouldn't mix Javascript with CSS.
  
  <p align="center">
    <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/Styling%20components%20-%20Styled-components.png" alt="Styling by styled components">
  </p>


# <a name="ExtraInfo">Extra information</a>
If you are here it means there are some concepts you probably don't know. I don't want you to waste time searching them, so here they are.

- <a name="Elements">Elements</a>: An element describes what you want to see on the screen. Unlike browser DOM elements, React elements are plain objects, and are cheap to create. In the [official documentation](https://reactjs.org/docs/rendering-elements.html) they talk more about them, but I consider it is a waste of time because you will be using **Class Components** most of the time.
<p align="center">
  <img src="https://github.com/LMOlivera/Learn-React-fast/blob/master/images/Element%20example.png" alt="Element example">
</p>

- <a name="CDN">CDN</a> (Content Delivery Network): Geographically distributed group of servers which work together to provide fast delivery of Internet content. A CDN allows for the quick transfer of assets needed for loading Internet content including HTML pages, javascript files, stylesheets, images, and videos. The popularity of CDN services continues to grow, and today the majority of web traffic is served through CDNs, including traffic from major sites like Facebook, Netflix, and Amazon. 
A properly configured CDN may also help protect websites against some common malicious attacks, such as Distributed Denial of Service (DDOS) attacks. 

- <a name="ES6">ECMAScript6</a>: ECMA (European Computer Manufacturers Association) is an organization dedicated to define the standard for Javascript. ES6 is the latest update of it, which includes a lot of improvements like "let" and "const" variable, arrow functions, spread operator, etc. I recommend you investigate it well because it adds a lot of extra functionality to Javascript.

- <a name="CSSR">Client-side/Server-side rendering</a>: This means who is going to be in charge of the rendering of the webpage. Thanks to the variety of Frontend Frameworks we usually do client-side rendering (everything is handled by your web browser). This doesn't mean we don't use Server-side anymore (in this case the server had to do everything, often slowing things down).

- <a name="Transpiler">Transpiler</a>: Tool that reads code written in one programming language to produce equivalent code in another.

