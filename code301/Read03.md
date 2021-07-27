# Passing Functions as Props
![img](https://i.ytimg.com/vi/szmS_M-BMls/maxresdefault.jpg)


## React Docs - lists and keys:



![img](https://i.ytimg.com/vi/0sasRxl35_8/maxresdefault.jpg)



* *What does .map() return?*

`Return the output of the function inside it into an array(like take value from array make some changes on it then return it to another array).`

* *If I want to loop through an array and display each value in JSX, how do I do that in React?*

`You can build collections of elements and include them in JSX using curly braces {}.and we loop through this array that we build using the JavaScript map() function.`

* *Each list item needs a unique ____.*

` a key is to use a string that uniquely identifies a list item`

* *What is the purpose of a key?*

`To identify which items have changed.`



## The Spread Operator: 


![img](https://miro.medium.com/max/1200/1*ck6Fs5k54T8Yv09D2dS0jA.png)



* *What is the spread operator?*

`new addition to the set of operators in JavaScript ES6. It takes in an iterable (e.g an array) and expands it into individual elements.`
`spread syntax refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments`


* *List 4 things that the spread operator can do.*

1. `Copying an array`
2. `Concatenating or combining arrays`
3. `Using Math functions`
4. `Using an array as arguments`


* *Give an example of using the spread operator to combine two arrays.*


```
let arr1 = [1,2,3]
let arr2 = [4,5,6]
console.log([...arr1, ...arr2])
```
in the console :
```
[1,2,3,4,5,6]
```

* *Give an example of using the spread operator to add a new item to an array*


```
let arr1 = [3, 4, 5];
let arr2 = [1, 2, ...arr1]; 
```
```
then arr2 = [1,2,3,4,5]
```


* *Give an example of using the spread operator to combine two objects into one*

```
const objectOne = {hello: "🤪"}
const objectTwo = {world: "🐻"}
const objectThree = {...objectOne, ...objectTwo, laugh: "😂"}
console.log(objectThree) // Object { hello: "🤪", world: "🐻", laugh: "😂" }
const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("😂".repeat(5))}}
objectFour.laugh() // 😂😂😂😂😂
```