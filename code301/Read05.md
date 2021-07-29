# Putting it all together


## React Docs - thinking in React:



![img](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRmHxundX1wRLmPI0zisM2K5gMPa3Owbvsq0w&usqp=CAU)



* *How would you break a mock into a component heirarchy?*

`The first thing you’ll want to do is to draw boxes around every component (and subcomponent) in the mock and give them all names and then a rrange them into a hierarchy`

* *What is the **single responsibility principle** and how does it apply to components?*

`a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.`

`The single responsibility principle (SRP) states that every class or module in a program should have responsibility for just a single piece of that program's functionality. Further, the elements of that responsibility should be encapsulated by the responsible class rather than spread out in unrelated classes`

![IMG](https://www.logiqlabs.com/wp-content/uploads/2021/04/SRP.png)



* *What does it mean to build a ‘static’ version of your application?*

`To build a static version of your app that renders your data model, you’ll want to build components that reuse other components and pass data using props`

* *Once you have a static application, what do you need to add?*

`props are a way of passing data from parent to child. If you’re familiar with the concept of state, don’t use state at all to build this static version. State is reserved only for interactivity, that is, data that changes over time. Since this is a static version of the app, you don’t need it.`


* *What are the three questions you can ask to determine if something is state?*

```
1. Is it passed in from a parent via props? If so, it probably isn’t state.

2. Does it remain unchanged over time? If so, it probably isn’t state.

3. Can you compute it based on any other state or props in your component? If so, it isn’t state.

```


* *How can you identify where state needs to live?*

``` 

 Identify every component that renders something based on that state.

 Find a common owner component (a single component above all the components that need the state in the hierarchy).

 Either the common owner or another component higher up in the hierarchy should own the state.

If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.

```