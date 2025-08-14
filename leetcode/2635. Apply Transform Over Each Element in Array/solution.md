[link do problema](https://leetcode.com/problems/apply-transform-over-each-element-in-array/description/)

Given an integer array arr and a mapping function fn, return a new array with a transformation applied to each element.

The returned array should be created such that returnedArray[i] = fn(arr[i], i).

Please solve it without the built-in Array.map method.

 

Example 1:

Input: arr = [1,2,3], fn = function plusone(n) { return n + 1; }
Output: [2,3,4]
Explanation:
const newArray = map(arr, plusone); // [2,3,4]
The function increases each value in the array by one. 


Solução:

```typescript
function map(arr: number[], fn: (n: number, i: number) => number): number[] {
    let newArray = [];

    arr.forEach((item, i) => {
        newArray.push(fn(item, i));
    })

    return newArray;
};
```
