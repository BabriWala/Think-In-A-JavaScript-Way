> Here in this code.

```
    var x = 20;

    console.log(x); // It will give us 20
```
> But  if we check this below code

```
    // This is called window scope or root
    var x = 20;

    function myFun(){
        // This is called function world
        var y = 20;

        console.log(`${x} from my function`)
        // Here in this code it will output 20 because it's inherit from it's parents.
    }

    console.log(x); // It will give us 20
```

> Here below if we just change x value in my Function world than it will change rooot x value:

```
    // This is called window scope or root
    var x = 20;

    function myFun(){
        // This is called function world
        var y = 20;

        x = 30

        console.log(`${x} from my function`)
        // Here in this code it will output 30 because it's inherit from it's parents.
    }

    console.log(x); // It will give us 30
```

> But if we declare with var in function scope than it will not change the root var it will create his own world variable like this: 

```
    // This is called window scope or root
    var x = 20;

    function myFun(){
        // This is called function world
        var y = 20;

        var x = 30

        console.log(`${x} from my function`)
        // Here in this code it will output 30 because it's inherit from it's parents.
    }

    console.log(x); // It will give us 20
```

> But What happen here is when we reassign x value without var keyword than the x will search in myFun's world that if there was an declaration with var x but there was no declaration with var x then it will go it's parenst world and seet that there was no declaration with var then he will create a var and then assign a value to x. In this way he assign value

```
    // This is called window scope or root

    function myFun(){
        // This is called function world
        var y = 20;

        x = 30

        console.log(`${x} from my function`)
        // Here in this code it will output 30 because it's inherit from it's parents.
    }

    console.log(window.x); // It will give us 30
```

> If we use use strict mode than it will give us an error and it will safe us from accidentally throwing an error.

```
    "use strict";
    // This is called window scope or root

    function myFun(){
        // This is called function world
        var y = 20;

        x = 30

        console.log(`${x} from my function`)
        // Here in this code it will output 30 because it's inherit from it's parents.
    }

    console.log(window.x); // It will give us 30
```
> Last of all if we use var when declaring a variable than it will be safe for us.