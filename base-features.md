# Base Features

React is a JavaScript library for building user interfaces. It is maintained by Facebook and a community of individual developers and companies. React can be used as a base in the development of single-page or mobile applications.

## Using create react app
Creates React apps with no build configuration. Documentation can be found (here)[https://create-react-app.dev/docs/getting-started]

```shell
npm install -g create-react-app
create-react-app react-complete-guide --scripts-version 1.1.5

cd react-complete-guide
npm start
```

## Understanding component basics

App.js
```javascript
import React, { Component } from 'react';
import './App.css';

class App extends Component {
  render() {
    return (
      <div className="App">
        <h1>My first react app</h1>
      </div>
    );
  }
}

export default App;
```

index.js
```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';
import registerServiceWorker from './registerServiceWorker';

ReactDOM.render(<App />, document.getElementById('root'));
registerServiceWorker();
```

## Understanding JSX

JSX is an XML/HTML-like syntax used by React that extends ECMAScript so that XML/HTML-like text can co-exist with JavaScript/React code

JSX is NOT HTML but it looks a lot like it. Differences can be seen when looking closely though (for example className in JSX vs class in "normal HTML"). JSX is just syntactic sugar for JavaScript, allowing you to write HTMLish code instead of nested React.createElement(...) calls.

## Creating a functional component
Components let you split the UI into independent, reusable pieces, and think about each piece in isolation.

When creating components, you have the choice between two different ways:

Functional components (also referred to as "presentational", "dumb" or "stateless" components 
```javascript
const cmp = () => { return <div>some JSX</div> }
```
class-based components (also referred to as "containers", "smart" or "stateful" components)
```javascript
class Cmp extends Component { render () { return <div>some JSX</div> } }
```

## Working with Props

Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called **props**) and return React elements describing what should appear on the screen.

```javascript
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

function App() {
  return (
    <div>
      <Welcome name="Sara" />
      <Welcome name="Cahal" />
      <Welcome name="Edite" />
    </div>
  );
}

ReactDOM.render(
  <App />,
  document.getElementById('root')
);
```

## Children in JSX

In JSX expressions that contain both an opening tag and a closing tag, the content between those tags is passed as a special prop: props.children.
```javascript
<MyComponent>Hello world!</MyComponent>
```

## Using State

The state is an instance of React Component Class can be defined as an object of a set of observable properties that control the behavior of the component. In other words, the State of a component is an object that holds some information that may change over the lifetime of the component.

State simply is a property of the component class, you have to call it state  though - the name is not optional. You can then access it via *this.state* in your class JSX code (which you return in the required render()  method).

Actually, only changes in props  and/ or state  trigger React to re-render your components and potentially update the DOM in the browser

```javascript
class NewPost extends Component { // state can only be accessed in class-based components!
  state = {
    counter: 1
  };  

  render () { // Needs to be implemented in class-based components! Needs to return some JSX!
    return (
      <div>{this.state.counter}</div>
    );
  }
}
```

## Methods




