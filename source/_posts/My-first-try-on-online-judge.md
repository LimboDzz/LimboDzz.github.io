---
title: My first try on online judge
date: 2021-09-22 18:53:15
tags:
- LeetCode
- Javascript
---

## Problem

![img](https://i.bmp.ovh/imgs/2021/09/8b42c6c3e69fda35.png)

## Wrong Answer

```js
    function indexOf(arr, item) {
        let n=0;
        arr.forEach(i=>{
            if(i==item) return n;
            n++;
        })
        return -1;
    }
```

## Accepted

```js
    function indexOf(arr, item) {
        let n=0;
        for(let i=0;i<arr.length;i++){
            if(arr[i]==item) return n;
            n++;
        }
        return -1;
    }
```

## What learnt

I confused **Array.prototype.forEach** with **For Loop**.

The **forEach()** method executes a provided function once for each array element.

While the **For** statement loops through the same code block till the condition is met.

So in the wrong answer ```return n;``` only returns out of the arrow function, not the loop, ending in always output a -1 for any given array.

## References

1. <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach>