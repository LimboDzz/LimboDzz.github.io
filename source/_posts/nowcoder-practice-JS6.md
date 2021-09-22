---
title: nowcoder/practice/JS6
date: 2021-09-22 20:27:21
tags:
- LeetCode
---

## Problem
![img](https://i.bmp.ovh/imgs/2021/09/5774274abed555c9.png)

## Accepted

- Mine

    ```js
        function truncate(arr) {
            return arr.slice(undefined,-1);
        }
    ```

- Others'

    ```js
        function truncate(arr) { 
            var newArray = arr.slice(0, arr.length - 1); 
            return newArray;
        }
    ```

## What learnt

Slice(start, end) returns a **copy** of the original array.

- If *start* left undefined, slice starts from the index 0.
- If *start* is greater than the index range of the sequence, an empty array is returned.
- A negative index can be used, indicating an offset from the end of the sequence. slice(2,-1) extracts the third element through the second-to-last element in the sequence.
- If end is omitted or greater than the length of the sequence, slice extracts through the end of the sequence (arr.length).

Splice(start, delNum, ...newElems) do the modification **in place**.

## References

1. <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice>
2. <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice>
