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

### Contributing
If you like the project, shoot a :star2: and feel free to fork & send PR.

### License

[MIT licensed](./LICENSE)
