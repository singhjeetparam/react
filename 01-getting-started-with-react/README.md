# WHAT IS REACT
It is a js library used for creating reusable ui components. 

# JSX 
Javascript XML. It allows us to write HTML elements using js code. To create HTML element in react we do not use createElement instead we use JSX .
JSX will be converted to js code on browser using a transpiler - babeljs. babel is a library which transpiles JSX to pure js code. 

```
const jsxElement = <h1>This is a JSX heading</h1>

const welcome = <h1>Welcome to my repo</h1>
```

## JSX ELEMENTS
JSX element can be a single html element or many html element wrapped inside a parent html element

```
const heading = <h1>This is a heading</h1>

const header = (
    <header>
    <ul>
    <li>Home</li>
    <li>Contact</li>
    <li>About Us</li>
    </ul>
    </header>
)
```


In header element, header is a parent html tag for the ul that is inside it. We always need a parent element whenever we want to use multiple elements 

## RENDERING A JSX ELEMENT
To render a jsx element to html documnet, we need to create an index.html file. This will be the only html file in our whole application. This is the reason react is called single page application. 

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>30 Days Of React Challenge</title>
  </head>

  <body>
    <div class="root"></div>

    <script
      crossorigin
      src="https://unpkg.com/react@16/umd/react.development.js"
    ></script>
    <script
      crossorigin
      src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"
    ></script>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
    <script type="text/babel">
      // To get the root element from the HTML document
      const rootElement = document.querySelector('.root')

      // JSX element
      const jsxElement = <h1>I am a JSX element</h1>

      // we render the JSX element using the ReactDOM package
      // ReactDOM has the render method and the render method takes two arguments
      ReactDOM.render(jsxElement, rootElement)
    </script>
  </body>
</html>
```

# STYLING IN REACT 
we can use inline css or we can use "className". We use "class" attribute in html. But in react we need to use "className".  It is preferable to style elements using inline or className only. DO not use IDs.


# INJECTING DATA TO A JSX ELEMENT
So far we have used static data on the jsx element, but we can also pass different data types as dynamic data. This dynamic data could be a string, number, boolean, array or object. To inject data we use curly braces {}.

## INJECTING STRINGS 
```
const welcome = 'Welcome to 30 Days Of React'
const title = 'Getting Started React'
const subtitle = 'JavaScript Library'
const firstName = 'Asabeneh'
const lastName = 'Yetayeh'
const date = 'Oct 2, 2020'

// JSX element, header

// JSX element, header
const header = (
  <header>
    <div className='header-wrapper'>
      <h1>{welcome}</h1>
      <h2>{title}</h2>
      <h3>{subtitle}</h3>
      <p>
        Instructor: {firstName} {lastName}
      </p>
      <small>Date: {date}</small>
    </div>
  </header>
)
```

## INJECTING NUMBERS
```
const numOne = 3
const numTwo = 2

const result = (
  <p>
    {numOne} + {numTwo} = {numOne + numTwo}
  </p>
)

const yearBorn = 1820
const currentYear = new Date().getFullYear()
const age = currentYear - yearBorn
const personAge = <p> {age}</p>
```

## INJECTING ARRAY 
```
const techs = ['HTML', 'CSS', 'JavaScript']

// JSX element, main
const main = (
  <main>
    <div className='main-wrapper'>
      <p>
        Prerequisite to get started{' '}
        <strong>
          <em>react.js</em>
        </strong>
        :
      </p>
      <ul>{techs}</ul>
    </div>
  </main>
)
```

# RENDERING LIST IN REACT 
We need to use loop to render a list in react. But that's the ui part, we also have to add unique key to each of these list items so that they can be individually treated or maintained. 

```
//without key, this will be rendered but it'll show error
const techs = ['html', 'css', 'js']
const techsFormatted = techs.map((tech) => <li>{tech}</li>)

//with keys 
const techs = ['html', 'css', 'js']
const techsFormatted = techs.map((tech) => <li key={tech}>{tech}</li>)
```
