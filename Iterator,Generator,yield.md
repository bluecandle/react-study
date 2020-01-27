<h1>
<a href ="https://dev.to/beccaliz/es6-generators-for-state-management-in-react-h7b">
Reference
</a>
</h1>

# Iterator
For a function to implement the iterator protocol, it must return an object with a next function. This next function returns an object with the attributes value and done.

## example
<code>
function createColorIterator() {
  let i = 0;
  const colors = ["red", "yellow", "blue"];
  return {
    next: () => {
      if (i < colors.length) {
        let value = colors[i];
        i++;
        return {
          value: value,
          done: false
        };
      } else {
        return {
          value: undefined,
          done: true
        };
      }
    }
  };
}

let iterator = createColorIterator();

console.log(iterator.next());
// { value: "red", done: false }
console.log(iterator.next());
// { value: "yellow", done: false }
console.log(iterator.next());
// { value: "blue", done: false }
console.log(iterator.next());
// { value: undefined, done: true }
</code>

Also, I should note that any iterables in JS (Array, String, Map, Set, etc.) have a property called Symbol.iterator that returns an iterator.

## example
<code>
const colors = ["red", "yellow", "blue"];
const iterator = colors[Symbol.iterator]();

console.log(iterator.next());
// { value: "red", done: false }
// ...same as above
</code>

# Generator

So, iterators are great! But building one from scratch can mean writing a lot of boilerplate. This is where generators come in! Generators are special functions that do some ES6 magic for you to create an iterator. Generators can be super helpful for asynchronous programming, though I’m not really going to get into that here.

For example, I can now use function* syntax to re-write my iterator with a lot less code.
## example
<code>
function* createColorIterator() {
  let i = 0;
  const colors = ["red", "yellow", "blue"];
  while (i < colors.length) {
    const color = colors[i];
    i++;
    yield color;
  }
}

console.log(iterator.next());
// { value: "red", done: false }
// ...same as above
</code>

# Yield

 Generator function uses the yield keyword. <strong>When a generator encounters this keyword, it immediately exits the function and returns the value after yield. The function execution can then be resumed when next is called again. </strong>

