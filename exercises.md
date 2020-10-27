# Exercises

Paste the snippets below one at a time into the dev tools console. Think about your answers BEFORE you run the code. When you are ready, invoke the functions

## Tips

Use your debugging tools in these exercises:
- https://www.npmjs.com/package/pryjs
- console.log
- debugger (only if running in the browser)


### Exercise 1

Compare the order of the console.logs using #then vs async await:


Using #then

```

function fetchAstros(){
  const url = "http://api.open-notify.org/astros.json"

    console.log("before fetch")

  fetch(url)
  .then(r => {
    console.log("first then")
    return r.json()
  }).then(astros => {
    console.log("second then")
  })

  console.log("end of fetchAstros")

}

//paste the below into the console at the same time
  fetchAstros()
  console.log("after fetchAstros")

```

Using async-await

```

async function fetchAstros(){
  const url = "http://api.open-notify.org/astros.json"

  console.log("before fetch")

  let response = await fetch(url)

  console.log("after fetch")

  let astroArray = await response.json()

  console.log("end of fetchAstros")

}

//paste the below into the console at the same time

fetchAstros()
console.log("after fetchAstros")

```
