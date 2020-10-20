# Exercises

Paste the snippets below one at a time into the dev tools console. Think about your answers BEFORE you run the code. When you are ready, invoke the functions

## Tips

Use your debugging tools in these exercises:
- https://www.npmjs.com/package/pryjs
- console.log
- debugger (only if running in the browser)


### Exercise 1

What will the return values be?

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

What will the below return values be

```
game.details.characterName
game.details.characterName()
const characterName = game.details.characterName characterName()
game.details.arrowCharacterName()

````

How can we start off with game.details.characterName and get "Mario" without changing the details using =?
