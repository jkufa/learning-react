material: https://scrimba.com/p/p7P5Hd/cWKkvVuL

# Day 1 notes
### What we will learn
1. Components
2. JSX (react wrapper for js)
3. Styling Components
4. Props (passing data)
5. States (maintain/change)
6. Event handling (interactivity)
7. Lifecycle methods (timing events)
8. APIs --- HTTP
9. Forms

Should already know: HTML, CSS, js, ES6

### What we're building
1. Todolist application
2. Meme generator

### Why use react?
1. Speed
  * Virtual DOM
2. Ability to create reusable web components 
ex: 
```<body>
     <MyNavbar/>
     <MainContent/>
     <MyFoort/>
    <footer/>
```
3. Maintained by Facebook, so lots of quality contributers
4. Hirable

### ReactDOM & JSX
commonly will use `import`

index.js:

`import React from "react"
import ReactDOM from "react-dom"

ReactDOM.render(what_to_render, where_to_render) // takes 2 arguments
`

In Index.html:
`<div id="root"></div>` This going to be sticking everything we create. Basically a container for all react

so `ReactDOM.render(<h1>Hello world!</h1>, document.getElementById)` notice the inline html. This is possible thanks to JSX. This is why you need to import React! *Note: cannot use more than one JSX element next to each other*. ex: `<h1>Hello world!</h1><p>This is a paragraph</p>` will throw an error. However, you can wrap both elements together and it will work!

### Practice 1
 ```js
import React from "react"
import reactDOM from "react-dom"

ReactDOM.render(<div>
                  <ul style>
                    <li>US</li>
                    <li>Australia</li>
                    <li>New Zealand</li>
                  </ul>
                </div>, document.getElementById("root"))
```

### React Functional Components
Best way to avoid a bunch of inline html when rendering!
syntax is camelcase
```js
function MyApp() {
  return (
    <ul>
      <li>1</li>
      <li>2</li>
      <li>3</li>
    </ul>
  )
}

reactDOM.render(
  <MyApp />,
  document.getElementById("root")
  )
```

### Practice 2
```js
import React from "react"
import reactDOM from "react-dom"

function MyInfo() {
  return(
    <div>
      <h1>Jack</h1>
      <p> Hi, I'm Jack, and design is my thing. 
          I'm a 20-year-old Junior at Missouri S&T.
      </p>
      <ul>Top Vacation Spots
        <li> France</li>
        <li> Japan</li>
        <li> Phillipenes</li>
      </ul>
    </div>
  )
}

reactDOM.render(<MyInfo />,document.getElementById("root"))
```