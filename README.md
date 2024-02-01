# The .filter() Method

## Introduction
Imagine you have a list of things, and you need to check if each meets a certain condition. You could go through each item one by one, or you can try and group them and see which things are alike. When coding imagine having to filter through an array containing  hundreds of items and checking to see if each meets a certain condtion. it would be near impossible and time consuming to do so. This is where the .filter() method comes in hand.

## Learning Objectives

1. Learn the syntax and basic usage of the .filter() method.
2. Learn how to apply .filter() on arrays to manipulate and filter data effectively.
3. Understand that .filter() does not modify the original array but creates a new(shallow copy) one. 
4. Learn where .filter() is beneficial, such as filtering data based on certain criteria.


## .filter()

 The .filter() method  is used to create a new array by filtering elements from an existing array based on a specified condition. It allows you to selectively include only the elements that meet the condition you set. The original array remains unchanged, and the new array contains only the elements that passed the filtering condition.

# Syntax

Array.prototype.filter()

Example :

```js
const words = ['spray', 'elite', 'exuberant', 'destruction', 'present'];
const result = words.filter((word) => word.length > 6);
console.log(result);
Expected output: Array ["exuberant", "destruction", "present"]
```
Breakdown :


words: The original array on which you want to apply the filter.
word(element): A callback function that is executed for each element in the array. The element parameter represents the current element being processed.
word.length: The condition specified inside the function is applied for a particular element(word), that element(word) will be included in the new array.
result/return: the result will display the new aray which will included the specified condition of words that have longer than 6 characters.


Example:


 Create a function using the .filter method to return an array of sneakers only size 10
 
```js

function filterSize10Sneakers(sneakers) {
  return sneakers.filter(sneaker => sneaker.size === 10);
}
const size10Sneakers = filterSize10Sneakers(sneakers);
```


 # Destructive/Non-Destructive Array Methods

It is important to remember that .filter is a non-destructive array method, meaning it will not alter the original array but instead when make a copy of the array with the specified request/condition asked in the function.


# When to utilize .filter

1. Filtering Data: When you have an array of data and you need specific elements/value of the array.

2. Removing Elements: The same can be said when you want to remove specific elements/values from the array

3. Working with Objects: When dealing with an array of objects and you want to filter objects based on a property value.

4. Loops: In MY understanding .filter in a way allows the replacement of the for loop, instead of iterating ove the index with the .filter you are searching for the specified element


# Time Complexity 


The time it takes for the filter function to go through all the sneakers in the array is directly correlated to the number of sneakers  in the array.

In this case, our function is looking for sneakers with size 10. So, it needs to check each sneaker to see if it's size 10.

The filter function goes through each sneaker one by one and checks if its size is 10. If there are more sneakers, it will take longer because it has to check each one.

Therefore, the time it takes for our function to find all the size 10 sneakers is directly related to how many sneakers there are in total. So, we say the time complexity of our function is O(n), where n is the number of sneakers in the array.

## Resources :

Used as guidance : https://github.com/10-6-pursuit/unit-fundamentals/blob/main/loops/readme.md


Array : https://chat.openai.com/share/0a2c9a4a-66ee-46da-876c-ab76267c0f7f


Definition : https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter

test : https://replit.com/@ArielaCollado/Sneakers#index.js
