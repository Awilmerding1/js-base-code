# Exercises

Paste the snippets below one at a time into the index.js file. Think about your answers BEFORE you run the code. When you are ready, open the index.html file in the browser and open the developer tools

## Tips

Use your debugging tools in these exercises:
- https://www.npmjs.com/package/pryjs
- console.log
- debugger (only if running in the browser)


### Exercise 1

What order will we see these logged in?

```
console.log("start")

setTimeout(() => console.log("set timeout 2 sec"), 2000)

setTimeout(() => console.log("set timeout 1 sec"), 1000)

setTimeout(() => console.log("set timeout 1 sec"), 0)

console.log("end")


````


### Exercise 2

What order will we see these logged in?


```


let url = "http://api.open-notify.org/astros.json"

console.log("start")

setTimeout(() => console.log("set timeout 1 sec"), 0)

fetch(url).then(r => console.log("in first then"))

console.log("end")


```



### Exercise 3

What order will we see these logged in?


```

let url = "http://api.open-notify.org/astros.json"

setTimeout(() => console.log("set timeout 1 sec"), 0)

console.log("start")

fetch(url).then(r => console.log("in first then")).then(console.log("in second then"))

console.log("end")


```


### Exercise 4

What order will we see these logged in?


```

let url = "http://api.open-notify.org/astros.json"

console.log("start")

fetch(url).then(r => console.log("in first then")).then(console.log("in second then")).catch(console.log("in catch"))

console.log("end")


```


### Exercise 5

What order will we see these logged in?


```


let url = "http://api.open-notify.org/astros.json"

console.log("start")

fetch(url).then(r => console.log("in first then")).then(console.log("in second then")).catch(function(e) { console.log("in catch")})

console.log("end")


```



### Exercise 6

What order will we see these logged in?

Note: typo in the url
```


let url = "http://api.open-noify.org/astros.json"

console.log("start")

fetch(url).then(r => console.log("in first then")).then(console.log("in second then")).catch(function(e) { console.log("in catch")})

console.log("end")


```
