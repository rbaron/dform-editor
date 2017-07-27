# dform-editor

![img](http://i.imgur.com/MSrQDmf.gif)

[dform](https://github.com/rbaron/dform) is a set of libraries for managing dynamic forms. The dynamic forms are described through a JSON schema. Client libraries -- targeting, for example, the web or mobile environments -- read a dform JSON schema and render the forms accordingly.

This repository hosts a simple web-based editor for such schemas. It helps you make sure the dform schema you're creating is well-formed. There's also a web render of the form (which relies on [react-dform](https://github.com/rbaron/react-dform)) so you can use your form in real time as you edit it in order to make sure it behaves as expected.

For examples of client libraries, check [react-dform](https://github.com/rbaron/react-dform) (web) and [react-native-dform](https://github.com/rbaron/react-native-dform) (react-native).

# Installation

```sh
$ npm install dform-editor
```
or
```sh
$ yarn add dform-editor
```

# Usage
There are two ways to run the editor.

### In your own app, using React

This package exports a `<SchemaEditor>` component, which you can use in your app and implement the business logic that best suit your needs. For example:

```javascript
import React from 'react'
import ReactDOM from 'react-dom'
import { SchemaEditor } from 'react-dform'

class App extends React.Component {
  render() {
    return (
      <SchemaEditor onSchemaChange={s => console.log('New valid schema:', s)} />
    )
  }
}

ReactDOM.render(
  <App />,
  document.getElementById('react-app'),
);
```

### Cloning this repo and running the built-in app

This is usefull for getting up and running quick. Just clone this repository and run:

```sh
$ npm run watch
```

This will run a dev server with the editor on http://localhost:8080/.


# License

MIT.
