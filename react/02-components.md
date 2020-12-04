# React Components and Props

> A component is a piece of UI that you can reuse. Just like you're able to reuse code in JavaScript with functions, a component lets you reuse code that renders a part of your UI. Being able to split your UI code into independent, reusable pieces, and think about each piece in isolation is one the most embraced features of React.


+ **Components** are defined as functions or classes. 
+ ```
  function Header() {
    return (
      <header>
        <h1>Title</h1>
        <span>some words</span>
      </header>
    );
  }

  ReactDOM.render(
  <Header />, or <header></header> if you want to nest elements
  document.getElementById('container')
  );
  ```
  + React components are **required to** start with an uppercase letter.
  + Components within components are called compositions.
+ ```
  const Header = () => (
    <Title />
  );

  const Title = () => (
    <h1>Title</h1>
  );
  ```

+ ### Properties
+ > Props: A list of properties used to pass data to a component.  Components are customized and made reusable with props.
+ `<Component propName="propValue" />`
+ Using Props
  + Define the props in a component's JSX tag
  + Enable the use of props in a component
+ Props are passed in as an object and can be accessed with dot notation inside JSX `{ }`.
+ ```
  const Header = (props) => (
    <header>
      <h1>{ props.title }</h1>
      <span className="stats">Player: { props.totalPlayers }</span>
    </header>
  );

  const App = () => (
    <div id="scoreboard">
      <Header title="Scoreboard" totalPlayers={ 1 } />
    </div>
  );
  ```
> An important detail to remember about props is that they are "read only" (or immutable), which means that a component can only read the props given to it, never change them. The (parent) component higher in the tree owns and controls the property values. <br> React components are similar to "pure" functions in JavaScript. They do not attempt to change their inputs, and always return the same result for the same inputs.
  + When a component has more than one prop, you'll often see them written on separate lines and indented
  + ```
    <Header
      title = "Title"
      id = "title"
      total = { 3 }
    > 
    ```
  + `" "` - are used to mimic HTML conventions







[Back to Main](react.md)