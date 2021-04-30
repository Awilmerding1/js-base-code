# Exercises

Paste the snippets below one at a time into the dev tools console. Think about your answers BEFORE you run the code. When you are ready, invoke the functions

## Tips

Use your debugging tools in these exercises:
- https://www.npmjs.com/package/pryjs
- console.log
- debugger (only if running in the browser)


### Exercise 1

NOTE: Run these in your browser console NOT node

What will the value of `this` be in the console.logs?


```
  function windowFunction() {

    console.log("windowFunction:", this)

    let arrowFunction = () => console.log("arrowFunction:", this)

    function regularFunction(){
      console.log("regularFunction:", this)
    }

    regularFunction()
    arrowFunction()
  }


  let myObj = {myKey: "myValue"}


```

What will we see logged when we call `windowFunction()`?

What will we see logged when we call `windowFunction.call(myObj)`?


### Exercise 2

Add the below two properties to `myObj`. What will the value of `this` be when we invoke the functions?

```
  myObj.regFn = function() {console.log(this)}
  myObj.arrowFn = () => console.log(this)
```


What will we see logged when we call `myObj.regFn()`?

What will we see logged when we call `myObj.arrowFn()`?


### Exercise 3

Paste the code below into your browser console

```
  this.character = "Daisy";

  const game = {
    character: "Mario",
    details: {
      character: "Yoshi",
      characterName: function() {
        return this.character;
      },
      arrowCharacterName: () => this.character
    }
  };

```

What will the values of `this` be that is returned in the following cases:


`game.details.characterName()`

`const characterName = game.details.characterName characterName()
  characterName()
`

`game.details.arrowCharacterName()`


How can we call `game.details.characterName` and see "Mario" returned without changing any values?
