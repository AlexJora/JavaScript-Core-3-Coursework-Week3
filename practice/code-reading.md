# Code reading

## Question 1

Take a look at the following code:

```
1    let x = 1;
2    function f1()
3    {
4        let x = 2;
5        console.log(x);
6    }
7    console.log(x);
```

Explain why line 4 and line 6 output different numbers.
First variable has global scope and second one has function scope. Both variables are called x but they are different. 

## Question 2

Take a look at the following code:
Variable x has global scope so can be used in the function f1. Variable y has function scope and doing console.log(y) will give undefine

```
let x = 10

function f1()
{
    console.log(x)
    let y = 20
}

console.log(f1())
console.log(y)
```

What will be the output of this code. Explain your answer in 50 words or less.

## Question 3

Take a look at the following code:
Result will be 9. Variable x is a primitive data type and is passed to a function by value. If you change the value of a primitive data type inside a function, this change won't affect the variable in the outer scope.

```
const x = 9;

function f1(val) {
  val = val + 1;
  return val;
}

f1(x);
console.log(x);



const y = { x: 9 };

function f2(val) {
  val.x = val.x + 1;
  return val;
}

f2(y);
console.log(y);
```
What will be the output of this code. Explain your answer in 50 words or less.
Result will be 10. Variable y is object.JavaScript passes objects by reference, when you change a property of that object within the function, the change will be reflected in the outer scope.

