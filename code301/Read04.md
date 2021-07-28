# React and Forms
![img](https://i.ytimg.com/vi/t3r9xW-sxqs/maxresdefault.jpg)


## React Docs - Forms:



![img](https://i1.wp.com/www.csscodelab.com/wp-content/uploads/2020/05/responsive-login-form-in-react-js.png?fit=1102%2C738&ssl=1)



* *What is a "Controlled Component"?*

`A Controlled Component is a Component that takes its current value through props and notifies changes through callbacks functions like onChange`

* *Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why*

`we should update the state with their responses as soon as they enter them (to be more dynamic and to display the state for them after submit , the displayed value will update as the user types)`

* *How do we target what the user is entering if we have an event handler on an input field?*

`event.target.value`


## The Conditional (Ternary) Operator Explained: 


![img](https://scotch-res.cloudinary.com/image/upload/w_auto,q_auto:good,f_auto/v1562952581/jqctyinrganjts991d3w.jpg)



* *Why would we use a ternary operator?*

`to simplify your if-else statements that are used to assign values to variables`


* *Rewrite the following statement using a ternary statement:*

```
 if(x===y){
 console.log(true);
  } else {
 console.log(false);
  }
```

**Answer**

```
x===y ? (console.log(true)) : (console.log(false))
```