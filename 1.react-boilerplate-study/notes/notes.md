# Reselect
Reselect is a library used for slicing your redux state and providing only the relevant sub-tree to a react component. It has three key features:

Computational power
Memoization => 연산이 많이 필요한 작업의 결과물을 캐싱해놓고 여러 번 활용하는 것.
Composability

# Redux Saga

Imagine that your application is fetching data in json format from a back-end. For every API call, ideally you should define at least three kinds of action creators:

API_REQUEST: Upon dispatching this, your application should show a spinner to let the user know that something's happening.
API_SUCCESS: Upon dispatching this, your application should show the data to the user.
API_FAILURE: Upon dispatching this, your application should show an error message to the user.

And this is only for one API call. In a real-world scenario, one page of your application could be making tens of API calls. How do we manage all of them effectively? This essentially boils down to controlling the flow of your application. What if there was a background process that handles multiple actions simultaneously, communicates with the Redux store and react containers at the same time? This is where redux-saga comes into the picture.

The mental model is that a saga is like a separate thread in your application that's solely responsible for side effects. redux-saga is a redux middleware, which means this thread can be started, paused and cancelled from the main application with normal redux actions, it has access to the full redux application state and it can dispatch redux actions as well.

## 결국, 효율적으로 api 호출을 다루기 위해 필요하다!

# Generator Functions
Sagas are nothing but ES6 generator functions. These functions act as normal functions, the only difference is that they can be "paused" and "resumed" at any point in time. redux-saga provides an intuitive, declarative API for managing asynchronous operations.




