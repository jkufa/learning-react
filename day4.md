#### React Todo App - Phase 2
CSS Used by Bob:
```css
body {
    background-color: whitesmoke;
}

.todo-list {
    background-color: white;
    margin: auto;
    width: 50%;
    display: flex;
    flex-direction: column;
    align-items: center;
    border: 1px solid #efefef;
    box-shadow:
    /* The top layer shadow */
        0 1px 1px rgba(0,0,0,0.15),
            /* The second layer */
        0 10px 0 -5px #eee,
            /* The second layer shadow */
        0 10px 1px -4px rgba(0,0,0,0.15),
            /* The third layer */
        0 20px 0 -10px #eee,
            /* The third layer shadow */
        0 20px 1px -9px rgba(0,0,0,0.15);
    padding: 30px;
}

.todo-item {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    padding: 30px 20px 0;
    width: 70%;
    border-bottom: 1px solid #cecece;
    font-family: Roboto, sans-serif;
    font-weight: 100;
    font-size: 15px;
    color: #333333;
}

input[type=checkbox] {
    margin-right: 10px;
    font-size: 30px;
}

input[type=checkbox]:focus {
    outline: 0;
}
```

#### React Props 1: Understanding the Concept
* anchor tags need an href to make any sense at all
```html
<a href="https://google.com">This is a link</a>
```
* img tag needs a source property
```html
<img src=""/>
```
* input tag can take additional properties such as placeholder, type, name, etc.
```html
<input placeholder="First Name" name="" type=""/>
```

#### React Props 2: Reusable Components
Look at websites such as YouTube and try and see how it might be organized in code if React was being used. Example: Each video likely would be a videoTile react component that has components inside of it such as image, <h3>, timestamp box, etc. The takeway away is its important to make dynamic reusable components. 

#### React Props
example:

in App.js
```jsx
            <ContactCard 
                name="Mr. Whiskerson" 
                imgUrl="http://placekitten.com/300/200" 
                phone="(212) 555-1234" 
                email="mr.whiskaz@catnap.meow"
            />
```

in ContactCard.js
```jsx
function ContactCard(props) {
    return (
        <div className="contact-card">
            <img src={props.imgUrl}/>
            <h3>{props.name}</h3>
            <p>Phone: {props.phone}</p>
            <p>Email: {props.email}</p>
        </div>
    )
}
```

```jsx
function ContactCard(props) {
    if(props.contact == null)
    {
        return (
            <div className="contact-card">
                <img src={props.imgUrl}/>
                <h3>{props.name}</h3>
                <p>Phone: {props.phone}</p>
                <p>Email: {props.email}</p>
            </div>
        )   
    }
    else
    {
        return (
            <div className="contact-card">
                <img src={props.contact.imgUrl}/>
                <h3>{props.contact.name}</h3>
                <p>Phone: {props.contact.phone}</p>
                <p>Email: {props.contact.email}</p>
            </div>
        )
    }
}
```



#### React Props and Styling Practice
