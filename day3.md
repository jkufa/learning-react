### Styling React with CSS
Basically when you're styling just know that you have to use `className=` instead of 'class` and adding properties only works on elements, not components.

### JSX to Javascript and back
What if you want to stick a var inside a element of html?

```js
function App() {
  const firstName = "Bob"
  const lastName = "Ziroll"
  
  return (
    <h1>Hello firstName + " " + lastName!</h1>
  )
}
```
This won't work. You need to encapsulate it in curly braces for it to be interpreted as javascript instead of JSX.

```js
function App() {
  const firstName = "Bob"
  const lastName = "Ziroll"
  
  return (
    <h1>Hello {firstName + " " + lastName}!</h1>
  )
}

// { enter javascript!
// } leave javascript!
```

```js
import React from "react"
import ReactDOM from "react-dom"

function App() {
  const date = new Date()
  const hours = date.getHours()
  let timeOfDay
  
  if (hours < 12) {
    timeOfDay = "morning"
  } else if (hours >= 12 && hours < 17) {
    timeOfDay = "afternoon"
  } else {
    timeOfDay = "night"
  }
  
  return (
    <h1>Good {timeOfDay}!</h1>
  )
}

ReactDOM.render(<App />, document.getElementById("root"))
```

#### React Inline Styles with the Style Property
if you try to do inline styling there will be an error, since we aren't actually in html. JSX expects style to be an object, not a string. You need 2 sets of curly braces, one to encapsulate in in javascript, the other is to make it an object.

When there is a dash, make it camelCase ex: background-color => backgroundColor

When you have a lot of inline styling, make a new object! You can call it styles. This avoids cluttering up inline html when adding styling.

```js
import React from "react"
import ReactDOM from "react-dom"

function App() {
  const date = new Date()
  const hours = date.getHours()
  let timeOfDay
  const styles = {
    fontSize: 30
  }
  
  if (hours < 12) {
    timeOfDay = "morning"
    styles.color = "#04756F"
  } else if (hours >= 12 && hours < 17) {
    timeOfDay = "afternoon"
    styles.color = "#2E0927"
  } else {
    timeOfDay = "night"
    styles.color = "#D90000"
  }
  
  return (
    <h1 style={styles}>Good {timeOfDay}!</h1>
  )
}

ReactDOM.render(<App />, document.getElementById("root"))
```