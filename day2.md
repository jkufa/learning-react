### Move Components into Separate Files
Typically, best practice is to have each react component in a separate file. So one react component per file. File name should match component name exactly.

Remember why we need to import React from "react"? It's because of JSX! This means we need to import React in all files that have a react component in it.

Now we need to make the file available in other places in the application is by exporting. `export default MyInfo`. This is an ES6 feature.

Also remember to import the new file in your index. `import MyInfo from "./MyInfo"`

Create folder called components to keep your workspace organized! `import MyInfo from "/components/MyInfo"`. This is mainly an example of organizational structure.

### React Parent/Child Components
Create function called `App` to be the entry point into the entire application.

#### Components vs Elements
Rendering `<App/>` component, but maybe it will render some different component! App is the root of the tree. Then components, then Elements. Elements is like html. The App component is most readable when it's filled with strictly subcomponents.


### React Todo App Phase 1
```
// From scratch, initialize the React app
// Render an <App /> component
// Create the <App /> component from scratch
// Have the <App /> component render 3 or 4 checkboxes with paragraphs or spans next to it
// like you're making a todo list with some hard-coded items on it
```