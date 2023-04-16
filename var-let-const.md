> Check thi below code
```
    if(true){
        var varvariable = 20;
    }
    console.log(varvariable)
    // Here the output will be 20

    if(true){
        let letvariable = 30;
    }
    console.log(letvariable)
    // But here the output will give us an error
```
> If we see above code that var is function scope means its accassable in function scope but we cannot access it from outside.On the other hand let is block scope it is only limited to block scope and if we imagine that this full code is inside a function than we can access varvariable from anywhere but let is different.

> If we just console.log inside of block scope then it will give us an exact output.
```
    if(true){
        let letvariable = 30;
        console.log(letvariable)
        // The output will be 30
    }
    
```
> Look these code

```
    if(true){
        var varvariable = 20;
        var varvariable = 30;
    }
    console.log(varvariable)
    // Here the output will be 30
```
> But here
```
    var varvariable = 30;
    console.log(varvariable)
    // Here the output will be 30

    if(true){
        var varvariable = 20;
        
    }
    console.log(varvariable)
    // Here the output will be 20
```
> If we see another example of var and let

```
    var varvariable = 30;
    console.log(varvariable)
    // Here the output will be 30

    if(true){
        var varvariable = 20;
    }
    console.log(varvariable)
    // Here the output will be 20
```

> If we try to redeclare a variable with let keyword it will give me and error but we can change it
```
    if(true){
        let letVariable = 20;
        // let letVariable = 20; // It will give us an error 
        
        letVariable = 20; // It will work smoothly
    }
    console.log(letVariable)
    // an error
```
> In const keyword we cannot redeclare or reassign the variable. but we can change it's value like object and array.

```
    if(true){
        const constVariable = {
            name : 'foo',
        }

        constVariable.name = 'bar';
    }
    console.log(constVariable)
    // {name : 'bar}
```
> But with var keyword it is function scope if we defined a variable inside a function we cannot access this variable from outside the function but if we want to access a outside variable of the function than we can access it from inside the function.
```
    var yellow = "yellow";

    function foo() {
        console.log(yellow);
        // It will give us yellow

        var bar = "bar";
        console.log(bar);
        // it will output it bar
    }
    console.log(bar);
    // It will give us an error that it is not defined or block scope

    foo();
```

> So last thing is that a parent cannot access child's thing but a child can access parent's thing.