# Exercises

## Tips

Use your debugging tools in these exercises:
- https://www.npmjs.com/package/pryjs
- console.log
- debugger (only if running in the browser)

## Part 1: Scoping and Hoisting

Instructions: Paste the code snippets below into the `index.js` file one at a time. BEFORE invoking the defined functions, your job is to determine what all of the console.log statements will print out. Once you have some answers, invoke the functions and run the file (`node index.js`) to see if you're right!

### Exercise 1
```
function scopey() {
  var a = "first Value";
  let b = "first Value";
  const c = "first Value";
  d = "first Value";

  if (true) {
    var a = "second Value";
    let b = "second Value";
    const c = "second Value";
    d = "second Value";
  }

  // what will each statement log to the console?
  console.log("a (var) is,", a);
  console.log("b (let) is,", b);
  console.log("c (const) is,", c);
  console.log("d (evil) is,", d);
}

```

### Exercise 2
```
  function sayName() {
    console.log("My name is", theName);

    var theName = "Jane Doe";
  }

```

### Exercise 3
```
  function sayName() {
    console.log("My theName is", theName);

    let theName = "Jane Doe";
  }


```

### Exercise 4
```
function sayName() {
  console.log("My name is", theName());

  function theName() {
    return "Jane Doe";
  }
}


```

### Exercise 5
```
  function sayName() {
    console.log("My theName is", theName());

    var theName = function() {
      return "Jane Doe";
    };
  }


```

### Exercise 6

```
var salary = "$1000";
var paid = function() {
  console.log("Original salary was", salary);

  salary = "$5000";

  console.log("My New Salary", salary);
};

```
