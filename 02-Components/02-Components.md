Components are independent reusable bits of code. They serve the same purpose as JavaScript functions, but work in isolation and return HTML.

### Function Based Component

Syntax:

```js
function Component() {
  return <div>Component</div>;
}

export default Component;
```

this returns JSX - JavaScript XML

(JSX allows us to write HTML in React. JSX makes it easier to write and add HTML in React.)

Let us create a component name App

Write in app.js

```js
function App() {
  return <h1>Hello Tushar</h1>;
}

export default App;
```

Rules:

- the component name must start with Capital Letter
- you have to export the component and import it to the index.js like below:

```js
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(<App />);
```

### Class Based Component

Creating a component named App using class system.

```js
// function App() {
// return <h1>Hello Tushar</h1>;
// }

import { Component } from "react";

class App extends Component {
  render() {
    return <h1>This is Class Component</h1>;
  }
}

export default App;
```

We will skip the class based component and now let us bring back the focus on function based component.

Ok now what is happening behind the scene? Copy your code in app.js which you created using function based component and go to babeljs.io/repl . Paste your code and you will be returned with new lines of codes to the right. Copy the new codes and replace it in your vscode. Notice everything works fine.

Our Code:

```js
function App() {
  return (
    <section>
      <h1>Noor Tushar</h1>
      <p>This is Noor Tushar learning React.</p>
    </section>
  );
}

export default App;
```

Translated Code:

```js
import { jsx as _jsx } from "react/jsx-runtime";
import { jsxs as _jsxs } from "react/jsx-runtime";
function App() {
  return _jsxs("section", {
    children: [
      _jsx("h1", {
        children: "Noor Tushar",
      }),
      _jsx("p", {
        children: "This is Noor Tushar learning React.",
      }),
    ],
  });
}
export default App;
```

But do not worry we do not need to write the translated code. It is just for understanding.
