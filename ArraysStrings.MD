## Javascripts Arrays/Strings methods

### Index:
- [.push()](#push)
- [.pop()](#pop)
- [.unshift()](#unshift)
- [.shift()](#shift)
- [.splice()](#splice)
- [.slice()](#slice)
- [.substr()](#substr)
- [.substring()](#substring)
- [.concat()](#concat)
- [.padStart()](#padstart)
- [.padEnd()](#padend)
- [.charAt()](#charat)
- [.charCodeAt()](#charcodeat)
- [.split()](#split)
- [.isArray()](#isarray)
- [.length](#length)
- [.endsWith()](#endswith)
- [.fromCharCode()](#fromcharcode)
- [.includes()](#includes)
- [.indexOf()](#indexof)
- [.lastIndexOf()](#lastindexof)
- [.localeCompare()](#localecompare)
- [.repeat()](#repeat)
- [.search()](#search)
- [.startsWith()](#startswith)
- [.valueOf()](#valueof)
- [.reverse()](#reverse)
- [.copyWithin()](#copywithin)
- [.entries()](#entries)
- [.every()](#every)
- [.fill()](#fill)
- [.filter()](#filter)
- [.find()](#find)
- [.findIndex()](#findindex)
- [.forEach()](#foreach)
- [.join()](#join)
- [.keys()](#keys)
- [.JSON.stringify()](#stringify)
- [.JSON.parse()](#parse)



### push()

```js
array = [1,2,3,4];

array.push(5);
console.log(array);

[1,2,3,4,5]    // '5' was added to the array.
         ^
```

### pop()
```js
array = [1,2,3,4];

array.pop();
console.log(array);
[1,2,3]       // Last value was removed.
       ^
```

### unshift()

```js
array = [1,2,3,4];

array.unshift(0);
console.log(array);

[0,1,2,3,4]   // '0' value was added in the first index.
 ^
```

### shift()

```js
array = [0,1,2,3,4];

array.shift();
console.log(array);
[  1,2,3,4]   // first index value was removed.
  ^
```

### splice();

- splice(start)
- splice(start, deleteCount)
- splice(start, deleteCount, item1)
- splice(start, deleteCount, item1, item2, itemN)

```js
Start:
array = ['a','b','c'];

console.log(array.splice(0,1));

'a'      // returns from 0 index, 1 element and then it is removed from the array.

console.log(array);
['b','c']; 
```

```js

array= ['a','b','c','d'];

array.splice(1,0, 'x');

console.log(array);

[ 'a', 'x', 'b', 'c', 'd' ]   // 'x' was added at the index '1' removing '0' elements.
        ^
```

### slice()

- slice(indexStart, indexEnd)

```js
array= ['a','b','c','d'];

console.log(array.slice());
['a','b','c','d']   // returns a copy of the array.

```

```js
array= ['a','b','c','d'];

console.log(array.slice(0,2));
['a','b']     // returns array content starting from '0' index until '2' without including the last index.

```

```js
array= ['a','b','c','d'];

console.log(array.slice(-1));
['c']        // reverse reading of the array, only 1 element.

```

```js
array= ['a','b','c','d'];

console.log(array.slice(-2));
['b','c']    // reverse reading of the array, 2 elements.

```

### substr()

- substr(start, length)

```js
str = "Hello World";

console.log(str.substr(0,4));
"Hell"       // Reading '4' elements starting from '0' index.

```

### substring()

- .substr(indexStart, indexEnd)

```js
str = "Hello World";

console.log(str.substring(0,2));
"He"       // Reading from index '0' until index '2' without including the value in the last index specified.
```

### concat()

 - .concat(stringOrigin, stringToAdd)
 
```js
str = "Hello";

str.concat(str, " ");            // add space to the string 'str'
console.log(str);

"Hello ";

str.concat(str,"World");         // add 'World' to the string 'str'
console.log(str);

"Hello World"
```

```js
str = "Hello";

str.concat(str, " ", "World");    // adding several strings at the end
console.log(str);

"Hello World"
```

### padStart()

    - .padStart(quantity, character)
    
```js
const nums = "55";

// added '0' at the beginning of the string to complete length of 4.
console.log(nums.padStart(4,0));

"0055"
```

```js
const nums = "55";

console.log(nums.padStart(10,0));

// added '0' at the beginning of the string to complete length of 10.
"0000000055"
```

### padEnd()

- .padEnd(quantity, char)
- .padEnd(4,0)
  
```js
const nums = "55";
console.log(nums.padEnd(4,0));

// added '0' at the end of the string completing length of '4'.
"5500"
```

### charAt()
   
   - .charAt(index)


```js
const nums = "The Night fox";

console.log(nums.charAt(4));
"N"      // returns char at index 4.

```

### charCodeAt()

    - .charCodeAt(index)

```js
const nums = "The Night fox";

console.log(nums.charCodeAt(4));

78       // returns unicode of the char at index '4'
```

### split()

    - .split(char)

```js
const str = "a-b-c-d";

const array = str.split("-");
console.log(array)

[ 'a', 'b', 'c', 'd' ]     // Creates an array from the string using the char "-" as a delimiter.
```

```js
const str = "abcd";

const array = str.split("");
console.log(array)

[ 'a', 'b', 'c', 'd' ]     // Creates an array from the string without a delimiter.
```


### isArray()

    - Array.isArray(array)
    
```js
const arr = ['a', 'b'];

console.log(Array.isArray(arr))

true      // Check if it's an array
```


### length

```js
const arr = ['a', 'b'];

console.log(arr.length)

2       // Indicates the length of the array
```

```js
const str = "Hello world";

console.log(str.length)

11      // Length of the string
```


### endsWith()

     .endsWith(value)

```js
const str = "Hello Universe";

console.log(str.endsWith("Universe");

true     // Verified that 'Universe' is the end of the String.
```


### fromCharCode()

     - String.fromCharCode(code)
     
```js
console.log(String.fromCharCode(65));

'A'      // Get the value represented by charcode '65'
```

### includes()

    - .includes(value)


```js
const str = "abcd";

console.log(str.includes('ab'));

true    // indicates that 'ab' is included in the string.
```


### indexOf()

    - .indexOf(value)


```js
const str = "Happy Coding!";

console.log(str.indexOf("Coding"));

6         // at index 6 start the word "Coding"
```


### lastIndexOf()

    - .lastIndexOf(value)


```js
const str = "This is a String!";

console.log(str.lastIndexOf('i'));

13        // 13 is the last index of the char 'i'
```

### localeCompare()

    - .localeCompare(string)


```js
const str = "content";
console.log(str.localeCompare("stri"));
1        // 1 Indicates stri occurs after 'str'.

```

```js
const str = "content";
console.log(str.localeCompare("string"));
0         // 0 Indicates strings are equivalent.

```

```js
const str = "content";
console.log(str.localeCompare("string bigger"));
-1        // -1 Indicates "string bigger" occurs before 'str'

```

### repeat()

   - .repeat(times)


```js
const str = "123";

console.log(str.repeat(3));

"123123123"       // repeats the content of 'str'  '3' times
```


### search()

   - .search("text")


```js
const str = "Looking for some text in the string";

console.log(str.search("in"));

4         // returns the index of the found text in the 'str'
```


### startsWith()

   - .startsWith("text")


```js
const str = "Checking the starts of the string";

console.log(str.startsWith("Checking"));

true       // Indicates that the content of the 'str' starts with the value "Checking".
```

### valueOf()

    - .valueOf()
    

```js
const str = "Getting the Value";

console.log(str.valueOf());

'Getting the Value'   // prints the value of 'str'.
```


### reverse()

    - .reverse()


```js
const arr = [1,2,3,4,5]

console.log(arr.reverse());

[5,4,3,2,1]        // Shows the array inverted.
```


### copyWithin()

   - .copyWithin(target, start)


```js
const arr = [0,1,2,3];

console.log(arr.copyWithin(3,1));

[0,1,2,1]          // replaced value of index '3' by value at index '1'.
```

### entries()

    - .entries()


```js
const arr = ["Banana", "Orange"];

arr.entries();

Returns array iterator with key/value pairs:
[0,"Banana"]
[1,"Orange"]
```


### every()

    - .every()


```js
const arr = [1,2,3,4,5];

console.log(arr.every( (e) => e<10));

true           // Indicates that every value in 'arr' is lower than '10'
```

### fill()

   - .fill()


```js
const arr = [1,2,3,4,5];

arr.fill(0);

[0,0,0,0,0]    // fills an array with static values
```


### filter()

   - .filter()


```js
const arr = [1,2,3,4,5];

console.log(arr.filter( (e) => e>2));

[3,4,5]       // shows only values greater than '2'.
```

### find()

    - .find()


```js
const arr = [1,20,32,43];

console.log(arr.find( (e) => e>20));

32           // Gets first element in array with the condition (greater than 20).
```

### findIndex()

    - .findIndex()


```js
const arr = [1,20,32,43];

console.log(arr.findIndex( (e) => e>20));

2            // Gets index of the first element that matches with the condition (greater than 20).
```


### forEach()

    - .forEach()


```js
const arr = [1,2,3,4,5];

arr.forEach((e) => console.log(e));

1
2
3
4
5               // Iterates over every element within the array 'arr'.
```


### join()

    - .join(value)


```js
const arr = [1,2,3,4];

console.log(arr.join(""));

'1234'          // Convert an array in a string without spaces between
```

```js
const arr = [1,2,3,4];

console.log(arr.join("-"));

'1-2-3-4'       // Convert an array in a string utilizing char '-' as delimiter.
```

### keys()

    - .keys()


```js
const arr = [1,2,3,4];

arr.keys();    // returns an Iterator with the key values of the array. It can be iterated by a for. 

Example:
[1,2,3,4].keys().forEach( (e) => console.log(e))
0
1
2
3             // We get the key values within the array
```


### stringify()

    - .JSON.stringify()


```js
JSON.stringify({"key": "value"})

'{"key":"value"}'   // return the object as a string.
```

### parse()

```js
JSON.parse('{"name": "john","age":30}')

{ name: 'john', age: 30 }    // Returns a JSON formatted
```
