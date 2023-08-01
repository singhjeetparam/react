# SETTING UP REACT
Now it's totally upon you whether you want to use vite or cra. 
All the steps to set up can be found on their website



# BREAKDOWN OF CODE
```
// we are importing react object from react library
import React from 'react'


//functional component name App. It's a js arrow function
const App = () => {
  // any sort of funtionality other than rendering UI is done before return 
  // an array 
  const skills = ['html', 'css', 'sass', 'js', 'react', 'redux', 'mongoDB', 'python']
  // mapping over that array
  const skill = skills.map((skill) => <li key={skill}>{skill}</li>)

  // all UI rendering is done by return 
  return (
    <div className='skills-container'>
     <ul className="skills-list">
     // this is the variable that we have generated using mapping over the skills array
      {skill}
     </ul>
    </div>
  )
}

//exporting this js function
export default App

```


# FILE STRUCUTRE OF A REACT PROJECT 

```
my-vite-react-app/
  ├── node_modules/
  ├── public/
  │   ├── favicon.ico
  │   └── index.html
  ├── src/
  │   ├── components/
  │   │   ├── App.js
  │   │   └── ...
  │   ├── index.css
  │   └── main.js
  ├── .gitignore
  ├── package.json
  ├── vite.config.js
  └── README.md

```

- node-modules - this folder contains all the dependencies that we have installed in our folder. 
- public - this folder contains static assets that don't need to be processed. 
- src - this folder contains all the majority of our code 
- src/components - this folder contains all the components
- src/index.css - global css file 
- src/main.js - entry point of our application. It contains the main code that render main react component typically it is named as App
- .gitignore - files that are ignored by the git
- package.json - this file conatins the list of dependencies and other meta data 
