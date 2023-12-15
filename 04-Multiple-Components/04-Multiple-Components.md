Best practice is to create a 'components' folder inside the src folder.
And inside the components folder create .js or .jsx files as per need.

### Steps

1. Example, let us create components -> Add.js

2. Inside the Add.js file use emmet -> ==rafce== for fast component creation but remove the top import.

```js
const Add = () => {
  return <h1>I am from Add Component</h1>;
};

export default Add;
```

Now change your code accordingly.

3. Import your Add component to App.js

```js
import Add from "./components/Add";

function App() {
  return <Add />;
}

export default App;
```

#### And remember for stacking multiple components, wrap it in a single main div/ section.

1. First creating the component

```js
const Greetings = () => {
  return <h1>Greetings Component</h1>;
};

export default Greetings;
```

2. Second exporting the component to App.js
3. Third, wrap it inside a section or a div

```js
import Greetings from "./components/Greetings";
import Add from "./components/Add";

function App() {
  return (
    <section>
      <Add />
      <Greetings />
    </section>
  );
}

export default App;
```
