<a href="https://reactjs.org/docs/hooks-state.html">Docs</a>

# Related topic : React Hooks
Let's quickly explain what is going on in this line:

const [count, setCounter] = useState(0);

useState(0) returns a tuple where the first parameter count is the current state of the counter and setCounter is the method that will allow us to update the counter's state. We can use the setCounter method to update the state of count anywhere

<strong>What is a Hook?</strong>
A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components. We’ll learn other Hooks later.

<strong>When would I use a Hook?</strong>
If you write a function component and realize you need to add some state to it, previously you had to convert it to a class. Now you can use a Hook inside the existing function component. We’re going to do that right now!

<strong>What does calling useState do?</strong>
It declares a “state variable”. Our variable is called count but we could call it anything else, like banana. This is a way to “preserve” some values between the function calls — useState is a new way to use the exact same capabilities that this.state provides in a class. Normally, variables “disappear” when the function exits but state variables are preserved by React.

<strong>What do we pass to useState as an argument?</strong>
The only argument to the useState() Hook is the initial state. Unlike with classes, the state doesn’t have to be an object. We can keep a number or a string if that’s all we need. In our example, we just want a number for how many times the user clicked, so pass 0 as initial state for our variable. (If we wanted to store two different values in state, we would call useState() twice.)

<strong>What does useState return?</strong>
It returns a pair of values: the current state and a function that updates it. This is why we write const [count, setCount] = useState(). This is similar to this.state.count and this.setState in a class, except you get them in a pair.

# related (other hook function)
<a href  = "https://reactjs.org/docs/hooks-effect.html">
Using the Effect Hook</a>