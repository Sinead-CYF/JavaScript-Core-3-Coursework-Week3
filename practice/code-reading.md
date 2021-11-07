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

Answer: Is it because of the block scope? x = 2 only exists inside the function. 

## Question 2

Take a look at the following code:

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

Console.logging function f1 will print 10 because it has access to the global variable x. Trying to console.log y will return undefined because it does not have access to variable y, as it's limited in bloc scope to the function.  

## Question 3

Take a look at the following code:

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

calling f1(x) returns the value 10 inside the function due to operations present in the function.  
Console.logging (x) returns 9 becaus eit can only access the original value of ex and no the operations. 
Same for f2(), but if you console.log (y) an object will be printed. 
