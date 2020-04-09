_April 9th_

Chris here, just to point out that there is now just **one socket** created for this whole repo. It's created in _src/index.js_, and is made available in all the other components.

### SEPARATION

I forgot to bring this up in today's standup - it might be nice to have some separation of all the _socket.on_ functions we'll be creating, so we don't have a million in one file.

In this repo currently:

**Pre-Game** socket functions - like _socket.on("login"...), socket.on("player left the game"...)_ are kept in the react component **App.jsx**.

**In-Game** socket functions - like _socket.on("movement"...), socket.on("drop letter on worm"...)_ are kept in the phaser component **MainScene.js**.

I'm not wedded to this formation or anything! Just that it might be nice to keep in mind, so we know where to find which function. Maybe we'll even create more components in the future, to separate them out more.

### THE CHAIN

**index.js** (javascript) invokes **App.jsx** (react) which invokes **ReactGameHolder.jsx** (react) which invokes **PhaserGameCreator.js** (phaser) which finally invokes **MainScene.js** (phaser).

And that's how the socket is created just once, in _index.js_, and then passed all down the chain, so all componenents have access to the very same one socket object.

### IF YOU WANT TO PASS DATA FROM REACT TO PHASER

If you get some data in **App.jsx**, first you must pass it on props to **ReactGameHolder.jsx** - you'll find the invocation near the beginning of the render statement inside _App.jsx_.

Then inside **ReactGameHolder.jsx** you need to set that data from props to state.

And so now, inside the phaser component **MainScene.js**, you can access that data no problem! That's because I've given the phaser component _MainScene.js_ access to the react component _ReactGameHolder.jsx_'s state, as _this.game.react.state_.
