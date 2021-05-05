# Methods

## Array Methods

1) Map : Create a new array with the result of the callback function (this function is executed for each item same as forEach)
Time Complexity: 0(n)
Example :

const users = [
    {name:'Luis', age:15},
    {name:'Jose', age:18},
    {name:'Aaron', age:40}
];
const userDescriptions = users.map(item => {
   return `Hello my name is ${item.name} and I have ${item.age} years old.`
});
console.log(userDescriptions); 
/*["Hello my name is Luis and I have 15 years old.",
 "Hello my name is Jose and I have 18 years old.",
 "Hello my name is Aaron and I have 40 years old."] */

2)Reduce : Return a single value after applying the reduction function for each element.
Time Complexity: 0(n)
Example :
const users = [
  {name:'Luis', age:15},
  {name:'Jose', age:18},
  {name:'Aaron', age:40}
];

const reducer= (accumulator, item)=> accumulator + item.age;
const totalAge =  users.reduce(reducer,0);
const ageAverage = totalAge / users.length;
console.log(`Total ${totalAge}, Average ${ageAverage}`); // Total 73, Average 24.333333333333332


3) Filter :Create a new array with the elements that apply the given filter condition as true.
Time Complexity: 0(n)
Example :
const users = [
  {name:'Luis', admin:true},
  {name:'Jose', admin:true},
  {name:'Aaron'}
];
const adminUsers =  users.filter(item => item.admin);
console.log(adminUsers); // [{name: "Luis", admin: true},{name: "Jose", admin: true}]



4)forEach :Just execute a function for each element in the array.
Time Complexity: 0(n)
Example :
const names = ['Luis','Jose','John','Aaron'];

names.forEach(item => {
    console.log(item);
}); 
/* Print all user names
  Luis Jose John  Aaron 
*/


5) Sort  – sorts the array in-place, then returns it.

Time Complexity: 0(n log(n))
Example :
const names = ['Luis','Jose','John','Aaron'];
console.log(names.sort()); // (4) ["Aaron", "John", "Jose", "Luis"]

/*complex sorting*/
const users = [
    {name:'Luis', age:25},
    {name:'Jose', age:20},
    {name:'Aaron', age:40}
];
const compareFuc = (item1,item2) => {
  return item1.age - item2.age;
};
console.log(users.sort(compareFuc));
/**
 [{name: "Jose", age: 20}, {name: "Luis", age: 25}, {name: "Aaron", age:40}]
 */


6) Slice :Return a copy of a sub array between two index, start and end.

Time Complexity: 0(n)

Example :

const users = [
  {name:'Luis', age:15},
  {name:'Jose', age:18},
  {name:'Aaron', age:40}
];

const  adults = users.slice(1, users.length);
console.log(adults); // (2) [{name: "Jose", age: 18}, {name: "Aaron", age: 40}]


7. indexOf() - 
Time Complexity : 0(n)

Return the first index of the element that exists in the array, and if not exists return-1.

Example : 
const names = ['Luis','Jose','John','Aaron'];
console.log(names.indexOf("John")); // 2
console.log(names.indexOf("Michelle")); // -1

8)Pop :Delete the last element of the array

Time Complexity: 0(1)
Example :
const names = ['Luis','John','Jose','Aaron'];
console.log(names.pop()); //Aaron
console.log(names); // (3) ["Luis", "John", "Jose"]



9)Shift : Delete the first element of the array

Time Complexity: 0(n)
Example :
const names = ['Luis','John','Jose','Aaron'];
console.log(names.shift()); // Luis
console.log(names); // (3) ["John", "Jose", "Aaron"]

10)Push :Add a new element to the end of the array.

Time Complexity: 0(1)
Example :
const names = ['Luis','John','Jose'];
names.push("Aaron");
console.log(names); // (4) ["Luis", "John", "Jose", "Aaron"]


11)Unshift :Add one or more elements in the beginning of the array

Time Complexity: 0(n)
Example :
const names = ['Luis','John','Jose'];
console.log(names.unshift("Aaron")); // 4
console.log(names); // (4) ["Aaron", "Luis", "John", "Jose"]


12)Includes method is used to know either a particular element is present in the array or not and accordingly, it returns true or false i.e, if the element is present, then it returns true otherwise false.
Time Complexity: 
Example : O(1) 
Input : [1, 2, 3, 4, 5].includes(2);
Output: true
Input : [1, 2, 3, 4, 5].includes(9);
Output: false


13)indexOf :Return the first index of the element that exists in the array, and if not exists return-1
Time Complexity: 0(n)
Example :
const names = ['Luis','Jose','John','Aaron'];
console.log(names.indexOf("John")); // 2
console.log(names.indexOf("Michelle")); // -1

14)every:This function Return a boolean value as true if all the items apply the given condition, and false if not.
Time Complexity: 0(n)
Example :

const users = [
  {name:'Luis', active:true},
  {name:'Jose', active:true},
  {name:'Aaron', active:false}
];
const isAllUsersActive = users.every(item => item.active);
console.log(isAllUsersActive); // false











###String Methods


1)charAt :The charAt() method returns the character at the specified index in a string.
The index of the first character is 0, the second character is 1, and so on.
Time Complexity: O(1)
Example :
Return the first character of a string:

var str = "HELLO WORLD";
var res = str.charAt(0)


2)charCodeAt
Time Complexity: O(1)
Example :
Return the Unicode of the first character in a string (the Unicode value for "H"):

var str = "HELLO WORLD";
var n = str.charCodeAt(0);

3)Concat :Create a new array with the union of two or more arrays.

Time Complexity: 0(n)
Example :
const names1 = ["Luis","Jose"];
const names2 = ["John","Aaron"];
const newArray = names1.concat(names2,["Michelle"]);
console.log(newArray); // (5) ["Luis", "Jose", "John", "Aaron", "Michelle"]

4)Includes :The includes() method determines whether a string contains the characters of a specified string.

This method returns true if the string contains the characters, and false if not.
Time Complexity: O(1)

Example
Check if a string includes "world":

var str = "Hello world, welcome to the universe.";
var n = str.includes("world");

5)indexOf : Return the first index of the element that exists in the array, and if not exists return-1
Time Complexity: 0(n)
Example:
Find the first occurrence of the letter "e" in a string, starting the search at position 5:

var str = "Hello world, welcome to the universe.";
var n = str.indexOf("e", 5);

6)Match :The match() method searches a string for a match against a regular expression, and returns the matches, as an Array object.
Time Complexity: O(n)
Example:
Search a string for "ain":

var str = "The rain in SPAIN stays mainly in the plain";
var res = str.match(/ain/g);

7)Repeat :returns a new string with a specified number of copies of the string it was called on.

Time Complexity: O(1)
Example :
Make a new string by copying a string twice:

var str = "Hello world!";
str.repeat(2);

8)Replace :The replace() method searches a string for a specified value, or a regular expression, and returns a new string where the specified values are replaced.
Time Complexity: O(n)
Example :
Return a string where "Microsoft" is replaced with "Apple":

var str = "Visit Microsoft!";
var res = str.replace("Microsoft", "Apple");


9)Search :The search() method searches a string for a specified value, and returns the position of the match.

Time Complexity: O(1)
Example :
Perform a case-sensitive search:

var str = "Mr. Blue has a blue house";
var n = str.search("blue");

10)Slice :Return a copy of a sub array between two index, start and end.

Time Complexity: 0(n)
Example :
const users = [
  {name:'Luis', age:15},
  {name:'Jose', age:18},
  {name:'Aaron', age:40}
];

const  adults = users.slice(1, users.length);
console.log(adults); // (2) [{name: "Jose", age: 18}, {name: "Aaron", age: 40}]

11)Split :The split() method is used to split a string into an array of substrings, and returns the new array.

Time Complexity:O(N) 
Example:
Split a string into an array of substrings:

var str = "How are you doing today?";
var res = str.split(" ");

12)Substr :method extracts parts of a string, beginning at the character at the specified position, and returns the specified number of characters.
Time Complexity: O(N)
Example :
Extract parts of a string:

var str = "Hello world!";
var res = str.substr(1, 4);


13)toLowerCase :method converts a string to lowercase letters
Time Complexity: O(N)
Example 
Convert the string to lowercase letters:

var str = "Hello World!";
var res = str.toLowerCase();

14)toUpperCase :method converts a string to uppercase letters.
Time Complexity: O(n)
ExampleConvert the string to uppercase letters:

var str = "Hello World!";
var res = str.toUpperCase(); 

15)Trim: method removes whitespace from both sides of a string.
Time Complexity: O(N)
Example :

Remove whitespace from both sides of a string:

var str = "       Hello World!        ";
alert(str.trim());
