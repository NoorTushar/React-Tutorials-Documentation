### More rules for JSX:

1. When declaring JSX, if you want to return something which has multiple divs, you need to declare all of the them in one single parent.

Example,

```js
function App() {
  return (
    <div>
      <section>
        <h1>My Name is Tushar</h1>
      </section>
      <section>
        <h1>A new Section</h1>
      </section>
    </div>
  );
}
export default App;
```

2. Make sure to close all the tags. if anything is self closing tag, make sure to close them.

Example:

```js
function App() {
  return (
    <section>
      <h1>A new Section</h1>
      <img />
    </section>
  );
}
export default App;
```

3. How to declare CSS class in JSX

In normal HTML we used to write class only but class is a reserved keyword in JS so we can't use class. Instead we write **==className==**

Example,

```js
function App() {
  return (
    <section>
      <h1 className="title-class">My Name is Tushar</h1>
    </section>
  );
}
export default App;
```

4. Not to use 'for' reserve keyword. For example in forms. Instead use htmlFor. Because for is a reserver keyword in JS for 'ForLoop'

```js
function App() {
  return (
    <form>
      <label htmlFor="name"></label>
      <input type="text" id="name" />
    </form>
  );
}
export default App;
```
