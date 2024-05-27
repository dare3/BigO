### Step One: Simplifying Expressions

Simplify the following big O expressions as much as possible:

1. O(n + 10) => O(n) grows linearly with the input size n.

2. O(100 * n) => O(n) grows linearly with the input size n.

3. O(25) => O(1) constant time complexity.

4. O(n^2 + n^3) => O(n^3) Time complexity as n^3 increases rapidly.

5. O(n + n + n + n) => O(n) grows linearly with the input size n.

6. O(1000 * log(n) + n) => O(n) time complexity.

7. O(1000 * n * log(n) + n) => O(n.log(n))

8. O(2^n + n^2) => O(2^n) exponential growth is faster than polynomial growth(n^2).

9. O(5 + 3 + 1) => O(9) where any constant is expressed as 1; O(1)

10. O(n + n^(1/2) + n^2 + n * log(n)^10) => O(n^2) grows quadratically.

## Step Two: Calculating Time Complexity

Determine the time complexities for each of the following functions. If you’re not sure what these functions do, copy and paste them into the console and experiment with different inputs!

```jsx
function logUpTo(n) {
  for (let i = 1; i <= n; i++) {
    console.log(i);
  }
}
```

Time Complexity: O(n) grows linearly with the input size n.

```jsx
function logAtLeast10(n) {
  for (let i = 1; i <= Math.max(n, 10); i++) {
    console.log(i);
  }
}
```

Time Complexity: O(n) grows linearly with the input size n.

```jsx
function logAtMost10(n) {
  for (let i = 1; i <= Math.min(n, 10); i++) {
    console.log(i);
  }
}
```

Time Complexity: O(1) constant time complexity.

```jsx
function onlyElementsAtEvenIndex(array) {
  let newArray = [];
  for (let i = 0; i < array.length; i++) {
    if (i % 2 === 0) {
      newArray.push(array[i]);
    }
  }
  return newArray;
}
```

Time Complexity:O(n) grows linearly with the input size n.

```jsx
function subtotals(array) {
  let subtotalArray = [];
  for (let i = 0; i < array.length; i++) {
    let subtotal = 0;
    for (let j = 0; j <= i; j++) {
      subtotal += array[j];
    }
    subtotalArray.push(subtotal);
  }
  return subtotalArray;
}
```

Time Complexity: O(n^2) quadratic

```jsx
function vowelCount(str) {
  let vowelCount = {};
  const vowels = "aeiouAEIOU";

  for (let char of str) {
    if(vowels.includes(char)) {
      if(char in vowelCount) {
        vowelCount[char] += 1;
      } else {
        vowelCount[char] = 1;
      }
    }
  }

  return vowelCount;
}
```

Time Complexity: O(n) linear growth

## Part 3 - short answer

Answer the following questions

1. True or false: n^2 + n is O(n^2). TRUE

2. True or false: n^2 * n is O(n^3). TRUE

3. True or false: n^2 + n is O(n).   FALSE

4. What’s the time complexity of the .indexOf array method?  O(n)  is the length of the array will be the worst case .

5. What’s the time complexity of the .includes array method? O(n) is the length of the array will be the worst case.

6. What’s the time complexity of the .forEach array method?  O(n) is the length of the array will be the  worst case.

7. What’s the time complexity of the .sort array method?  O(n^2) is the average of the array will be worst case.

8. What’s the time complexity of the .unshift array method? O(n) because it may require shifting all elements by one position.

9. What’s the time complexity of the .push array method?  O(1) on average, but may be the underlying array needs to be resized.

10. What’s the time complexity of the .splice array method? O(n) because it may require shifting elements.
 
11. What’s the time complexity of the .pop array method?  O(1) because it removes the last element from the array. 

12. What’s the time complexity of the Object.keys() function? O(n) is the number of own enumerable properties of the object.




