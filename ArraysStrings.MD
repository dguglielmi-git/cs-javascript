## Javascripts Arrays/Strings methods

### Index:
[.push()](#push)
[.pop()](#pop)




### push()

```
array = [1,2,3,4];

array.push(5);
console.log(array);

[1,2,3,4,5]    <--- '5' was added to the array.
         ^
```

### pop()
```
array = [1,2,3,4];

array.pop();
console.log(array);
[1,2,3]       <---  last value was removed.
       ^
```

### unshift()

```
array = [1,2,3,4];

array.unshift(0);
console.log(array);

[0,1,2,3,4]   <--- '0' value was added in the first index.
 ^
```

### shift()

```
array = [0,1,2,3,4];

array.shift();
console.log(array);

[  1,2,3,4]   <-- first index value was removed.
  ^
```

### splice();

- splice(start)
- splice(start, deleteCount)
- splice(start, deleteCount, item1)
- splice(start, deleteCount, item1, item2, itemN)
```
Start:
array = ['a','b','c'];

console.log(array.splice(0,1));

'a'    <--- returns from 0 index, 1 element and then it is removed from the array.

console.log(array);
['b','c']; 
```

```

array= ['a','b','c','d'];

array.splice(1,0, 'x');

console.log(array);

[ 'a', 'x', 'b', 'c', 'd' ]   <--- 'x' was added at the index '1' removing '0' elements.
        ^
```
### slice()

- slice(indexStart, indexEnd)

```
array= ['a','b','c','d'];

console.log(array.slice());
['a','b','c','d']   <--- returns a copy of the array.

```

```
array= ['a','b','c','d'];

console.log(array.slice(0,2));
['a','b']   <--- returns array content starting from '0' index until '2' without including the last index.

```

```
array= ['a','b','c','d'];

console.log(array.slice(-1));
['c']   <--- reverse reading of the array, only 1 element.

```

```
array= ['a','b','c','d'];

console.log(array.slice(-2));
['b','c']   <--- reverse reading of the array, 2 elements.

```

### substr()

- substr(start, length)

```
str = "Hello World";

console.log(str.substr(0,4));
"Hell"       <--- Reading '4' elements starting from '0' index.

```

### substring()

- .substr(indexStart, indexEnd)

```
str = "Hello World";

console.log(str.substring(0,2));
"He"       <--- Reading from index '0' until index '2' without including the value in the last index specified.
```

### concat()

 - .concat(stringOrigin, stringToAdd)
 
```
str = "Hello";

str.concat(str, " ");    <-- add space to the string 'str'
console.log(str);

"Hello ";

str.concat(str,"World"); <-- add 'World' to the string 'str'
console.log(str);

"Hello World";
```

```
str = "Hello";

str.concat(str, " ", "World);    <-- adding several strings at the end;
console.log(str);

"Hello World"
```

### padStart()

    - .padStart(quantity, character)
    
```
const nums = "55";

console.log(nums.padStart(4,0));

"0055"      <--- added '0' at the beginning of the string to complete length of 4.
```

```
const nums = "55";

console.log(nums.padStart(10,0));

"0000000055"        <--- added '0' at the beginning of the string to complete length of 10.
```

### padEnd(quantity, char)
    
    - .padEnd(4,0)
  
```
const nums = "55";
console.log(nums.padEnd(4,0));

"5500"      <--- added '0' at the end of the string completing length of '4'.

```

### charAt()
   
   - .charAt(index)

```
const nums = "The Night fox";

console.log(nums.charAt(4));
"N"      <--- returns char at index 4.

```

### charCodeAt()

    - .charCodeAt(index)

```
const nums = "The Night fox";

console.log(nums.charCodeAt(4));

78     <--- returns unicode of the char at index '4'
```

### split()

    - .split(char)

```
const str = "a-b-c-d";

const array = str.split("-");
console.log(array)

[ 'a', 'b', 'c', 'd' ]     <--- Creates an array from the string using the char "-" as a delimiter.
```

```
const str = "abcd";

const array = str.split("");
console.log(array)

[ 'a', 'b', 'c', 'd' ]     <--- Creates an array from the string without a delimiter.
```


### isArray()

    - Array.isArray(array)
    
```
const arr = ['a', 'b'];

console.log(Array.isArray(arr))

true      <--- Check if it's an array
```


### length

```
const arr = ['a', 'b'];

console.log(arr.length)

2       <--- Indicates the length of the array
```

```
const str = "Hello world";

console.log(str.length)

11      <--- Length of the string
```


### endsWith()

     .endsWith(value)

```
const str = "Hello Universe";

console.log(str.endsWith("Universe");

true     <---- Verified that 'Universe' is the end of the String.
```


### fromCharCode()

     - String.fromCharCode(code)
```
console.log(String.fromCharCode(65));

'A'      <---- Get the value represented by charcode '65'
```

### includes()

    - .includes(value)
    
```
const str = "abcd";

console.log(str.includes('ab'));

true    <--- indicates that 'ab' is included in the string.
```


### indexOf()

    - .indexOf(value)

```
const str = "Happy Coding!";

console.log(str.indexOf("Coding"));

6         <--- at index 6 start the word "Coding"
```


### lastIndexOf()

    - .lastIndexOf(value)

```
const str = "This is a String!";

console.log(str.lastIndexOf('i'));

13         <--- 13 is the last index of the char 'i'
```

### localeCompare()

    - .localeCompare(string)

```
const str = "content";
console.log(str.localeCompare("stri"));
1       <--- 1 Indicates that "stri" is different of the content in 'str'

```

```
const str = "content";
console.log(str.localeCompare("string"));
0       <--- 1 Indicates that "str" is equal than the content in 'str' variable.

```

```
const str = "content";
console.log(str.localeCompare("string bigger"));
-1

```

### repeat()

   - .repeat(times)
   
```
const str = "123";

console.log(str.repeat(3));

"123123123"        <--- repeate the content of 'str'  '3' times
```


### search()

   - .search("text")

```
const str = "Looking for some text in the string";

console.log(str.search("in"));

4     <--- returns the index of the found text in the 'str'
```


### startsWith()

   - .startsWith("text")

```
const str = "Checking the starts of the string";

console.log(str.startsWith("Checking"));

true   <---- Indicates that the content of the 'str' starts with the value "Checking".
```

### valueOf()

    - .valueOf()

```
const str = "Getting the Value";

console.log(str.valueOf());

'Getting the Value'    <--- prints the value of 'str'.
```


### reverse()

    - .reverse()

```
const arr = [1,2,3,4,5]

console.log(arr.reverse());

[5,4,3,2,1]     <--- Shows the array inverted.
```


### copyWithin()

   - .copyWithin(target, start)
   
```
const arr = [0,1,2,3];

console.log(arr.copyWithin(3,1));

[0,1,2,1]     <--- replaced value of index '3' by value at index '1'.
```

### entries()

    - .entries()

```
const arr = ["Banana", "Orange"];

arr.entries();

Returns array iterator with key/value pairs:
[0,"Banana"]
[1,"Orange"]
```


### every()

    - .every()

```
const arr = [1,2,3,4,5];

console.log(arr.every( (e) => e<10));

true     <--- Indicates that every value in 'arr' is lower than '10'
```

### fill()

   - .fill()

```
const arr = [1,2,3,4,5];

arr.fill(0);

[0,0,0,0,0]     <--- fills an array with static values
```


### filter()

   - .filter()

```
const arr = [1,2,3,4,5];

console.log(arr.filter( (e) => e>2));

[3,4,5]       <--- shows only values greater than '2'.
```

### find()

    - .find()
    
```
const arr = [1,20,32,43];

console.log(arr.find( (e) => e>20));

32       <--- Gets first element in array with the condition (greater than 20).
```

### findIndex()

    - .findIndex()


```
const arr = [1,20,32,43];

console.log(arr.findIndex( (e) => e>20));

2      <--- Gets index of the first element that matches with the condition (greater than 20).
```


### forEach()

    - .forEach()


```
const arr = [1,2,3,4,5];

arr.forEach((e) => console.log(e));

1
2
3
4
5        <--- Iterates over every element within the array 'arr'.
```


### join()

    - .join(value)

```
const arr = [1,2,3,4];

console.log(arr.join(""));

'1234'    <--- Convert an array in a string without spaces between
```

```
const arr = [1,2,3,4];

console.log(arr.join("-"));

'1-2-3-4'   <--- Convert an array in a string utilizing char '-' as delimiter.
```

### keys()

    - .keys()

```
const arr = [1,2,3,4];

arr.keys();   <--- returns an Iterator with the key values of the array. It can be iterated by a for. 

Example:
[1,2,3,4].keys().forEach( (e) => console.log(e))
0
1
2
3          <--- We get the key values within the array
```


### JSON.stringify()

    - .JSON.stringify()


```
JSON.stringify({"key": "value"})

'{"key":"value"}'   <--- return the object as a string.
```

### JSON.parse()

```
JSON.parse('{"name": "john","age":30}')

{ name: 'john', age: 30 }    <--- Returns a JSON formatted
```
