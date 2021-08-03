#  In memory storage


## Understanding the JavaScript Call Stack:



![img](https://www.javascripttutorial.net/wp-content/uploads/2019/12/JavaScript-Call-Stack-step-3.png)


* *What is a `call`?*

`When a function is invoked`

* *How many `calls` can happen at once?*

`one at a time`


* *What does LIFO mean?*

`Last In, First Out (LIFO) principle : When we say that the call stack, operates by the data structure principle of Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.`


* *What causes a Stack Overflow?*

`A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.`



## JavaScript error messages: 


![img](https://buildwoofunnels.com/wp-content/uploads/2019/01/error_firefox.jpg)



* *What is a `refrence error`?*


`happend when you try to use a variable that is not yet declared`


* *What is a `syntax error`?*

`when you have something that cannot be parsed in terms of syntax`

* *What is a `range error`?*

` Happend when I Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.`


* *What is a `tyep error`?*

`when the types (number, string and so on) you are trying to use or access are incompatible`

* *What is a breakpoint?*

`will make your program stop at that point only if a condition is met, this is awesome for when you want to debug huge cycles for specific values. The breakpoint can also be achieved by putting a debugger statement in your code in the line you want to break.`

* *What does the word `debugger` do in your code?*

`that allows you to step through another program one line at a time. This is very useful when trying to identify incorrect code and analyze how a program "flows". Key concepts include: Breakpoints, Stepping, and Viewing data.`