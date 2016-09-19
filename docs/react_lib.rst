React
=====================

`bebo-react`

A Bebo SDK wrapper for React.js

You can find it here: https://github.com/bebo/bebo-react

Installation
------------------

**Install from npm**::

    npm install bebo-react — save

Usage
------

**Bootstrap your app**::

    import React from 'react';
    import BeboReact from 'bebo-react';
    import App from '/path/to/App';

    BeboReact.render(
      <App />,
      document.getElementById('app'), // your app root container
      {
        disableKeyboardDoneStrip: true // optional, true || false
      }
    );

**Wrap your components**::

    import React from 'react';
    import { withBebo } from 'bebo-react';
    class App extends React.Component {
    // your component logic
    // the Bebo SDK is available via this.props.bebo
      render() {
        this.props.bebo.callin()
      }
    }

    export default withBebo(App); // this is where the magic happens

That’s all! The wrapper will likely expand as we figure out more common use cases. 

Feedback
------------

Got an idea on how to improve it? Please feel free to submit a pull request or file an issue on Github, or talk to me on twitter, I’m `@jnsdls <https://twitter.com/jnsdls>`_.