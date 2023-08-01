# COMPONENTS
A component is a small, reusable code, which is responsible for one part of the application UI. Components are the small parts of a big picture, 
Suppose we have a website, there can be numerous parts in this like - header, footer, banner, contact forms etc. These all small parts are components and together they make the whole website. 

## CREATING REACT COMPONENT

```
const jsx = <tag>Content</tag>
const ComponentName = () => {
    return jsx
}
```

```
const Heading = () =>{
    return(
        <h1>THis is a heading</h1>
    )
}
```

## RENDERING A COMPONENT
To render a component we need to import it and then we can use it with our components. 
