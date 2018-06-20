## 📝 Author
[<img src="https://media.licdn.com/dms/image/C5103AQE3SdZqmIyW0A/profile-displayphoto-shrink_200_200/0?e=1533168000&v=beta&t=reTZbwaCbB9R9V47Q9XiBGgGpY6_dS0KSK_gA8WsVCc" align="right" height="70" width="70">](http://armanbhuiyan.com)

##### Arman Bhuiyan <kbd>[Github](https://github.com/arman37) / [LinkedIn](https://www.linkedin.com/in/arman-bhuiyan) / [Facebook](https://www.facebook.com/arman.it37) / [Site](http://armanbhuiyan.com) /  [E-Mail](mailto:arman.it37@gmail.com)</kbd>

# Learning Redux

[ <br />
&nbsp; :diamond_shape_with_a_dot_inside: State Management Library <br />
&nbsp; :diamond_shape_with_a_dot_inside: Framework Agnostic <br />
&nbsp; :diamond_shape_with_a_dot_inside: Action <br />
&nbsp; :diamond_shape_with_a_dot_inside: Reducer <br />
&nbsp; :diamond_shape_with_a_dot_inside: Store <br />
&nbsp; :diamond_shape_with_a_dot_inside: Immutable <br />
&nbsp; :diamond_shape_with_a_dot_inside: Read-only State <br />
&nbsp; :diamond_shape_with_a_dot_inside: Pure Function <br />
&nbsp; :diamond_shape_with_a_dot_inside: Single Source Of Truth <br />
&nbsp; :diamond_shape_with_a_dot_inside: Predictable State Change <br />
&nbsp; :diamond_shape_with_a_dot_inside: Verb-oriented <br />
]

[ <br />
&nbsp; :diamond_shape_with_a_dot_inside: A component shouldn’t include logic to fetch data, and data shouldn’t be stored in a component’s state. <br />
&nbsp; :diamond_shape_with_a_dot_inside: Redux holds up the state within a **single location**. <br />
&nbsp; :diamond_shape_with_a_dot_inside: With Redux the logic for fetching and managing the state **lives outside React**. <br />
&nbsp; :diamond_shape_with_a_dot_inside: Redux gives each React component the exact piece of state it needs. <br />
&nbsp; :diamond_shape_with_a_dot_inside: Redux says that the state is **immutable** and cannot be changed in place. <br />
&nbsp; :diamond_shape_with_a_dot_inside: Even when using Redux it is totally fine to have stateful components. Not every piece of the application’s state should go inside Redux. <br />
&nbsp; :diamond_shape_with_a_dot_inside: The tradeoff that Redux offers is to add indirection to **decouple “what happened” from “how things change”**. <br />
]

## :hash: We should consider using Redux for:
&nbsp; :arrow_right: Data fetching and caching. <br />
&nbsp; :arrow_right: Things that are like “global variables” (e.g. authentication). <br />
&nbsp; :arrow_right: Things that have very complex update logic (e.g. a multimedia post editor). <br />
&nbsp; :arrow_right: Things that many distant components care about. <br />
&nbsp; :arrow_right: When the state tree shape is too different from the UI tree shape. <br />
&nbsp; :arrow_right: Variables that are annoying to explicitly pass down the React tree. <br />
&nbsp; :arrow_right: Update logic that is too complex to express with a bunch of `setState()`s. <br />
&nbsp; :arrow_right: Multiple React components that need to access the same state but do not have any parent/child relationship. <br />
&nbsp; :arrow_right: We start to feel awkward passing down the state to multiple components with props. <br />
&nbsp; :arrow_right: Isn't useful for smaller apps. It really shines when it comes to develop a complex React application. <br />

## :hash: Store:
&nbsp; :arrow_right: The Redux store is like a brain: it’s in charge for **orchestrating all the moving parts** in Redux <br />
&nbsp; :arrow_right: When building Redux apps, the first thing you need to think about is **state**. <br />
&nbsp; :arrow_right: The state of the application lives as a **single, immutable object** within the store. <br />
&nbsp; :arrow_right: It is usually a good idea to draft a JSON sample of your state tree with some placeholder data. <br />
&nbsp; :arrow_right: Each key in this single object represents a branch of the state tree. <br />
&nbsp; :arrow_right: The store handles state updates by passing the current state and action through a single reducer. <br />
&nbsp; :arrow_right: `createStore` is the function for creating the Redux store.  <br />
&nbsp; :arrow_right: `createStore` takes a reducer as the first argument. We may also pass an initial state to createStore for server side rendering. Anyway, **the state comes from reducers**. <br />
&nbsp; :arrow_right: As soon as the store receives an action it triggers a reducer that returns the next state. <br />
&nbsp; :arrow_right: Provides `getState` for accessing the current state of the application. <br />
&nbsp; :arrow_right: Provides `dispatch` for dispatching an action. <br />
&nbsp; :arrow_right: Provides `subscribe` for listening on state changes. <br />

## :hash: Reducer:
&nbsp; :arrow_right: A reducer is just a Javascript function. <br />
&nbsp; :arrow_right: State updates are handled by reducers. <br />
&nbsp; :arrow_right: A reducer takes two parameters: the **current state** and an **action**. <br />
&nbsp; :arrow_right: Reducers produce the state. The state is not something we create by hand. <br />
&nbsp; :arrow_right: While an initial state is useful for SSR, in Redux the **state must return entirely from reducers**. <br />
&nbsp; :arrow_right: No SideEects in Reducers. Reducers should be **predictable**. <br />
&nbsp; :arrow_right: A reducer function must be **pure** since redux state is **immutable**. <br />
&nbsp; :arrow_right: A reducer function has a switch statement (although unwieldy, a naive reducer could also use if/else). <br />
&nbsp; :arrow_right: The reducer **calculates the next state** depending on the action type. Moreover, it should return at least the initial state when no action type matches. <br />
&nbsp; :arrow_right: The resulting state is a copy of the current state plus the new data. <br />
&nbsp; :arrow_right: Split a big reducer into separate functions and combine them with `combineReducers` function. <br />

## :hash: Action:
&nbsp; :arrow_right: In a nutshell, actions are events. **An object describing what happened**.  <br />
&nbsp; :arrow_right: Actions provide instructions about what should change in the application state along with the necessary data to make those changes. <br />
&nbsp; :arrow_right: When we dispatch an action through the store, the action is sent through the reducers and the state is updated. <br />
&nbsp; :arrow_right: This ensures that neither the views nor the network callbacks will ever write directly to the state. <br />
&nbsp; :arrow_right: Actions send data from the application (user interactions, internal events such as API calls, and form submissions) to the store. The store gets information only from actions. <br />
&nbsp; :arrow_right: Redux actions are nothing more than Javascript objects consisting of type & payload property. <br />
&nbsp; :arrow_right: Only way to change the state is by sending a signal to the store. This signal is an action. <br />
&nbsp; :arrow_right: “**Dispatching an action**” is the process of sending out a signal. <br />
&nbsp; :arrow_right: It is a best practice to **wrap every action within a function**. Such function is an action creator. <br />
&nbsp; :arrow_right: The action creators are functions that return an action. <br />
&nbsp; :arrow_right: The type property is nothing more than a string. Since strings are prone to typos and duplicates it’s better to have action types declared as constants. <br />
&nbsp; :arrow_right: As actions are just plain objects, they can be logged, serialized, stored, and later replayed for debugging or testing purposes. <br />

## :hash: Middleware:
&nbsp; :arrow_right: Middleware serves as the glue between two different layers or different pieces of software. <br />
&nbsp; :arrow_right: It acts on the store’s dispatch pipeline. <br />
&nbsp; :arrow_right: In Redux, middleware consists of a series of functions that are executed in a row in the process of dispatching an action. <br />
&nbsp; :arrow_right: Each piece of middleware is a function that has access to the action, a dispatch function, and a function that will call next. <br />


## :hash: react-redux:
&nbsp; :arrow_right: The key for connecting a React component with Redux is **connect**. It takes at least one argument. <br />
&nbsp; :arrow_right: **connect** connects a React component with the Redux store. <br />
&nbsp; :arrow_right: **connect** takes two or three arguments(`mapStateToProps` & `mapDispatchToProps`) depending on the use case. <br />
&nbsp; :arrow_right: `mapStateToProps` connects a part of the Redux state to the props of a React component and takes state object as a parameter and returns another object. <br />
&nbsp; :arrow_right: `mapDispatchToProps` connects Redux actions to React props and takes dispatch function as a parameter and returns another object. <br />
&nbsp; :arrow_right: **Provider** is an higher order component, it wraps up your whole React application and makes it aware of the entire Redux’s store and gets the store as a prop. <br />

## :hash: redux-thunk:
&nbsp; :arrow_right: By default, Redux action creators don’t support asynchronous actions like fetching data. <br />
&nbsp; :arrow_right: Thunk allows us to write action creators that return a function instead of an action. The inner function can receive the store methods `dispatch` and `getState` as parameters. <br />
&nbsp; :arrow_right:  <br />
&nbsp; :arrow_right:  <br />


### Contributing
If you like the project, shoot a :star2: and feel free to fork & send PR.

### License

[MIT licensed](./LICENSE)
