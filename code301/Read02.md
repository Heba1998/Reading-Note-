# State and Props
![img](https://miro.medium.com/max/786/1*TbIOYXZmhRWphY7NfVZYAw.png)


## React lifecycle :

![img](https://miro.medium.com/max/2000/0*0saPKFiTUk6W3FYp)



* *Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?*

`render`


* *What is the very first thing to happen in the lifecycle of React?*

`constructor()`


* *Put the following things in the order that they happen:*

1. `constructor`
2. `render`
3. `componentDidMount`
4. `React Updates`
5. `componentWillUnmount`


* *What does componentDidMount do?*

`load anything using a network request or initialize the DOM , (dom mainplution , network request)`


## React State Vs Props: 

![img](https://i.stack.imgur.com/wqvF2.png)

* What types of things can you pass in the props?

`as like argument to a function i.e. when you creat a component inside the react and you want to render it you will pas it to props you want to give. (like initial value of the counter)`

* What is the big difference between props and state?

*prps* `props it passes into a component,handeled outside of that component and must be updatee there`

*state* `is handled inside that component and you can updated inside the component`

* When do we re-render our application?

`when the state changed inside the aplication or change the props outside the component`

* What are some examples of things that we could store in state?

`counter or inside a form for checkbox or input element`
