# puck-remote

A simple example of using a Puck.js button as a remote control.

It misuses the puck's battery level advertisement to indicate whether the button
has been pressed.

Whilst idle, its battery level is set to 0. When the button is clicked once, the
red LED comes on for 3 seconds and the battery level is set to 10. A double click
sets the green LED and a battery level of 20. A triple click sets the blue LED and
a battery level of 30.

This repository includes a node.js app that listens for the changes in advertised
values and prints them out.

- `puck/puck.js` is a sketch to upload to your puck device
- `index.js` is a node.js app that listens for device advertisements and prints
  out values that change.

## Setup your puck

1. Open up the [Espruino Web IDE](https://www.espruino.com/ide/)
2. Connect to your puck device
3. Upload the sketch from `puck/puck.js`
4. Disconnect

## Setup and run the local app

1. Run `npm install` in the root of this repository
2. Run `node index.js`
