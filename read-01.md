# Node Ecosystem, TDD
## Read: 01 - Class 01  

### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-01.md).

### For this class, I will provide answers for the following questions:

1. Describe (in plain English) what `Array.map()` does
2. Describe (in plain English) what `Array.reduce()` does
3. Provide code snippets showing how to use `superagent()` to fetch data from a URL and log the result
   - With normal Promise `.then()` syntax
   - Again with `async` / `await` syntax
4. Explain promises as though you were mentoring a Code 301 level student
5. Are all callback functions considered to be Asynchronous? Why or Why Not?


## Array.map()

`map` calls a provided callback function once for each element in an array, in order, and constructs a new array from the results. callback is invoked only for indexes of the array which have assigned values.

**Syntax**
```
array.map(function(currentValue, index, arr), thisValue)
```

**Example**
```
const array1 = [1, 4, 9, 16];
const map1 = array1.map(x => x * 2);

//this will return a new array: Array [2, 8, 18, 32]
```


## Array.reduce()

It reduces the array to a single value. The `reduce()` method executes a provided function for each value of the array (from left-to-right). The return value of the function is stored in an accumulator (result/total). `reduce()` does not execute the function for array elements without values.

**Syntax**
```
array.reduce(function(total, currentValue, currentIndex, arr), initialValue)
```

**Example**
```
function add(a, b) {
    return a + b;
}

const sampleArray = [1, 2, 3, 4];

const sum = sampleArray.reduce(add, 0);
console.log(‘The sum total is:’, sum);

//  The sum total is: 10
```

## Superagent()

**with `.then()`**
```
superagent.get('/api/pet')
 .then(console.log)
 .catch(console.error);
```

**with `async` / `await`**
```
(async () => {
  try {
    const res = await superagent.get('/api/pet');
    console.log(res);
  } catch (err) {
    console.error(err);
  }
})();
```

## Promises

The Promise constructor takes a function (an executor) that will be executed immediately and passes in two functions: ***resolve*** , which must be called when the Promise is resolved (passing a result), and ***reject*** , when it is rejected (passing an error).


## Are all callback functions considered to be Asynchronous? Why or Why Not?

JavaScript functions in general are not asynchronous. Some very limited set of functions have an asynchronous API:
`addEventListener`, `setTimeout`, `setInterval`. These are the only 3.
They allow you to pass in a callback that may get called eventually. Such as when a timer expires, or when a user clicks on something, or when an `AJAX` request completes.

More interesting information I read about this question in this [thread](https://stackoverflow.com/questions/15141118/are-javascript-functions-asynchronous)



