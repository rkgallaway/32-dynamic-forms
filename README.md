![CF](http://i.imgur.com/7v5ASc8.png) LAB 32
=================================================

## Lab 32: Dynamic Forms

### Author: Ryan Gallaway

### Links and Resources

[![Build Status](https://www.travis-ci.com/rkgallaway/32-dynamic-forms.svg?branch=master)](https://www.travis-ci.com/rkgallaway/32-dynamic-forms)

* [repo](https://github.com/rkgallaway/32-dynamic-forms)
* [travis](https://www.travis-ci.com/rkgallaway/32-dynamic-forms)
* [AWS deployment](http://xyz.com) (when completed)
* [code sandbox 1](https://codesandbox.io/s/8xqynwv8m9)
* [code sandbox 2](http://xyz.com) (if necessary)


### Modules
#### `modulename.js`
##### Exported Values and Methods

* Use a static .json file to bring in the players schema (you can simply import it)
* Implement all of the restful methods in the Redux Store for the player schema
  * GET - Retrieve one item
  * POST - Create New Item
  * PUT - Replace an item
  * DELETE - Remove an item
* Display a list of every element in the store, updating the list with every action taken on individual items.

### Create a generic `<Record/>` component
In the first phase, you created a form that can edit a single model. In this phase, you will be genericizing that component.

* Rename your editor component to `<Record />`
* It should dynamically load the correct schema json file based on a prop on the component given by the container component.
* Based on the schema
  * Draw the correct form
  * Connect to the right part of the store.
  * Ensure that the record list is from the right part of state
  * Ensure that your REST actions are using the right part of state


### Turn it on!
* Instead of importing .json files, connect the `<Record />` component to an API server to fetch the actual Schema from the API
* This should be optional. Use a flag of some kind to tell your component to read from a local .json file or connect to a server.
* Use a variable to identify the API server so that your application is deployable.

###### Testing
* Test the reducers to make sure that each action is properly manipulating state
* Test the form behavior to ensure that added items are showing in the list, updates are showing real time changes, etc.

#### Running the app
* `npm start`
* Endpoint: `/foo/bar/`
  * Returns a JSON object with abc in it.
* Endpoint: `/bing/zing/`
  * Returns a JSON object with xyz in it.

#### Tests
* `npm test`
* What assertions were made?
* What assertions need to be / should be made?

#### UML
![Lab 32 Dynamic Fomrs UML](./assets/uml.jpg)
* image will be uploaded upon completion
