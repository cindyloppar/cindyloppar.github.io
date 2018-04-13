---
Layout:
Title: "Context API"
Date: 2018-04-13 09:24 
Categories:
---

# Context API 

## Context 

Context provides a way to pass data through the component tree without having to pass props down manually at every level. Data is passed from parent to child via props, but this can be difficult to use for certain types of props (e.g. locale preference, UI theme) that are required by many components within an application. Context provides a way to share values like this between components without having to explicitly pass a prop through every level of the tree.

## When to Use Context

Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language. For example, in the code below we manually thread through a “theme” prop in order to style the Button component:



class App extends React.Component {
  render() {
    return <Toolbar theme="dark" />;
  }
}

function Toolbar(props) {
  // The Toolbar component must take an extra "theme" prop
  // and pass it to the ThemedButton. This can become painful
  // if every single button in the app needs to know the theme
  // because it would have to be passed through all components.
  return (
    <div>
      <ThemedButton theme={props.theme} />
    </div>
  );
}

function ThemedButton(props) {
  return <Button theme={props.theme} />;
}

Using context, we can avoid passing props through intermediate elements:

// Context lets us pass a value deep into the component tree
// without explicitly threading it through every component.
// Create a context for the current theme (with "light" as the default).
const ThemeContext = React.createContext('light');

class App extends React.Component {
  render() {
    // Use a Provider to pass the current theme to the tree below.
    // Any component can read it, no matter how deep it is.
    // In this example, we're passing "dark" as the current value.
    return (
      <ThemeContext.Provider value="dark">
        <Toolbar />
      </ThemeContext.Provider>
    );
  }
}

// A component in the middle doesn't have to
// pass the theme down explicitly anymore.
function Toolbar(props) {
  return (
    <div>
      <ThemedButton />
    </div>
  );
}

function ThemedButton(props) {
  // Use a Consumer to read the current theme context.
  // React will find the closest theme Provider above and use its value.
  // In this example, the current theme is "dark".
  return (
    <ThemeContext.Consumer>
      {theme => <Button {...props} theme={theme} />}
    </ThemeContext.Consumer>
  );
}


# API 

const {Provider, Consumer} = React.createContext(defaultValue);

Creates a { Provider, Consumer } pair. When React renders a context Consumer, it will read the current context value from the closest matching Provider above it in the tree.

The defaultValue argument is used when you render a Consumer without a matching Provider above it in the tree. This can be helpful for testing components in isolation without wrapping them.

## Provider

<Provider value={/* some value */}>

A React component that allows Consumers to subscribe to context changes.

Accepts a value prop to be passed to Consumers that are descendants of this Provider. One Provider can be connected to many Consumers. Providers can be nested to override values deeper within the tree.

## Consumers

<Consumer>
  {value => /* render something based on the context value */}
</Consumer>

A React component that subscribes to context changes.

Requires a function as a child. The function receives the current context value and returns a React node. The value argument passed to the function will be equal to the value prop of the closest Provider for this context above in the tree. If there is no Provider for this context above, the value argument will be equal to the defaultValue that was passed to createContext().

All Consumers are re-rendered whenever the Provider value changes. Changes are determined by comparing the new and old values using the same algorithm as Object.is. (This can cause some issues when passing objects as value:)