## Introduction To Redux
This is a pre made create-react-app project. When you run npm start the web page that comes up may appear familiar. A dashboard is a common type of user interface used to show a variety of information that is important in making decisions. It is usually read only which is perfect for practicing redux reducers. The data is currently being passed to components through props. Change the code to implement redux and remove any passing of props. The end user should see no change in the interface.

### Key vocabulary
Redux reducers, store & containers

### Objective
* Remove prop inheritance from all React components without changing the dashboard UI

### Evidence of Completion
* The dashboard looks the same as before
* The `App` component declared inside `src/index.js` no longer takes state props
* Components declared inside `src/App.js` no longer take props

### Sub Objectives
* Put all new files in the `src` folder
* Create and export reducers
* Create and export a store
* Provide store to components
* Create and export containers

### Setup
* fork
* clone
* npm install
* npm start

### Reducers
* Create a new folder called `reducers`
* Create a file in this folder called index.js
* Import combineReducers from redux
* Create a reducer function for each piece of data in state.js
  * newComments
  * newTasks
  * newOrders
  * tickets
  * orders
  * tasks
  * messages
* Remember 2 parameters state and action. Remember to return state
* Combine the reducers and export

### Create the store
* Create a store.js file
* Import createStore from redux
* Import state from state.js
* Import reducers from reducers/index
* Create the store and export it

### Provide store to App component
* In index.js:
  * Import Provider from react-redux
  * Import store from store.js
  * Use the Provider component to wrap App
  * Give Provider a prop “store” and the value of the store

### Create Containers
* Create a `container` folder.
* Create containers for the following components:
  * Tickets
  * TransactionPanel 
  * TopNav
  * TasksPanel
  * Comments
  * Orders
  * Tasks
* In each `container` file:
  * Import connect from react-redux
  * Create a function called mapStateToProps that takes parameter state
  * Return an object. Decide what prop the component needs and this will be a key on the object
  * Decide what data from state the component needs and that will be the value on the object
  * Use the connect function and mapStateToProps to turn the component into a container
  * Export the container

### Import containers into App component
* Inside `App.js`:
  * Remove each component with a prop assignment
  * replace it with the appropriate container.

