# Code reading

## Question 1

Take a look at the following code:

```
1    let x = 1;
2    function f1()
3      {
4        let x = 2;
5        console.log(x);
6    }
7    console.log(x);
```

Explain why line 4 and line 6 output different numbers.

Line 4 and line 6 output different numbers because of the scope.In line 4 x is a local variable which means we can  read the value just inside of his bock code. Otherwise,in line 6 the console.log(x) is referring to global variable in line 1,x = 1. 

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

The output is going to be: 
10
y is not define
The console.log() in line 34 is going to call the f1() and the f1() is going to output the value of 10 which is referring to the global variable x in line 26. In line 35 we are trying to console.log(y) but y exist just inside the f1() because is a local variable and we can't access it outside its scope.

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
The first console.log() it wil output 9 because we are passing the argument by value so,the function it changes the value of x just inside the function scope.
The second console.log() it will output {x: 10} because objects and arrays are passed as reference so,the function modifies the original object.
