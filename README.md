# Learn-Javascript

## typeof

```
console.log(typeof func);

const func = () => {};

console.log(typeof 1);
console.log(typeof '1');

console.log(typeof null);

console.log(typeof undefined);

console.log(typeof {});

console.log(typeof []);

console.log(typeof func);

console.log(typeof setTimeout(function() {}, 10));

console.log(typeof () => {}); 
```

## Equality

```
console.log([] == []);

console.log(undefined == null);

console.log(undefined === null);

console.log({} == {});

console.log({} === {}); 

console.log({a: 1} == {a: 1});

console.log({a: 1} === {a: 1}); 

const obj = {}

console.log(obj == obj)

console.log(obj === obj)

var number = 100;
if (number == '100')  // Here Comparision between two values using ==. It will compare irrespective of datatype of variable
  alert("Both are equal");    
else    
  alert("Both are not equal"); 
  ```
  
  ## Synchronous vs Asynchronous code
  ```
console.log(1);

setTimeout(() => console.log(2));

Promise.resolve().then(() => console.log(3));

Promise.resolve().then(() => setTimeout(() => console.log(4)));

Promise.resolve().then(() => console.log(5));

setTimeout(() => console.log(6));

console.log(7);
```

## Objects
```
const obj = {
  name: 'John',
  age: 25
}

const obj1 = {
  name: 'John',
  age: 25
}

function func(obj, obj1) {
  obj.name = 'Doe';
  obj1 = {
    name: 'Doe'
  };
  console.log(obj.name); 
  console.log(obj1.name);
}

func(obj, obj1);
console.log(obj.name); 
console.log(obj1.name); 
```

## Arrays

```
const arr1 = [1,2,3]
const arr2 = [1,2,3]

function changeVal(arr1, arr2) {
    arr1[0] = 0
    console.log(arr1) 
    
    arr2 = [4,5,6]
    console.log(arr2) 
}

changeVal(arr1, arr2)
console.log(arr1) 
console.log(arr2)
````
