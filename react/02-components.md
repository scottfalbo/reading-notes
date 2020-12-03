# React Components

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



[Back to Main](react.md)