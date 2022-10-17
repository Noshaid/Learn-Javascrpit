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



```
//You have to find indexes of two such elements so that after adding sum is equal to target
//input = [2,5,8,7]
//target = 9
//output = 0,3

//input = [2,1,8,4]
//target = 5
//output = 1,3

//input = [0,4,2,1]
//target = 3
//output = 2,3

const arr = [2,5,8,7]
const target = 9

function getArr() {
    let dict = new Map();
    for (let i = 0; i < arr.length; i++) {
        let difference = target - arr[i];
        if (dict.has(difference)) {
            return [dict.get(difference), arr[i]];
        } else {
            dict.set(arr[i], i); 
        }
    }
    return []
}
console.log(getArr())
```
