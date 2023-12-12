# Array Sorting(Bubble Sort)

Array Sorting
Basic Understanding
Understand Solution with Whiteboard
Write Code and understand step by step
Interview Question

**SORTING THROUGH Nested Loops**

In this example, the outer loop iterates through the array, and the inner loop finds the minimum element in the unsorted part of the array. After finding the minimum element, it swaps it with the element at the current index of the outer loop.

Note that while nested loops are used here, more efficient sorting algorithms like quicksort or mergesort are commonly preferred for larger datasets due to their better performance.

```jsx
function selectionSort(arr) {
  var len = arr.length;
  
  for (var i = 0; i < len - 1; i++) {
    // Assume the current index is the minimum
    var minIndex = i;
    
    for (var j = i + 1; j < len; j++) {
      // If the element at j is less than the element at minIndex, update minIndex
      if (arr[j] < arr[minIndex]) {
        minIndex = j;
      }
    }

    // Swap the minimum element with the element at the current index
    var temp = arr[i];
    arr[i] = arr[minIndex];
    arr[minIndex] = temp;
  }

  return arr;
}

// Example usage:
var myArray = [5, 3, 8, 4, 2];
var sortedArray = selectionSort(myArray.slice());
console.log(sortedArray); // Output: [2, 3, 4, 5, 8]
```

**How Bubble Sort Works** 

Bubble sort is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. The pass through the list is repeated until the list is sorted. Here's a step-by-step breakdown of how bubble sort works in JavaScript for arrays:

```jsx

function bubbleSort(arr) {
  var len = arr.length;

  // Outer loop: Iterate through the array
  for (var i = 0; i < len - 1; i++) {

    // Inner loop: Compare and swap adjacent elements
    for (var j = 0; j < len - 1; j++) {

      // Compare adjacent elements
      if (arr[j] > arr[j + 1]) {

        // Swap if the current element is greater than the next element
        var temp = arr[j];
        arr[j] = arr[j + 1];
        arr[j + 1] = temp;
      }
    }
  }

  return arr;
}

// Example usage:
var myArray = [5, 3, 8, 4, 2];
var sortedArray = bubbleSort(myArray.slice());
console.log(sortedArray); // Output: [2, 3, 4, 5, 8]
Here's how the bubble sort algorithm works:
```

1. **Outer Loop (`i`):**
    - The outer loop iterates through the array from the first element to the second-to-last element (**`len - 1`** times).
2. **Inner Loop (`j`):**
    - The inner loop iterates through the array from the first element to the second-to-last element (**`len - 1`** times).
3. **Comparison and Swap:**
    - Within the inner loop, adjacent elements (**`arr[j]`** and **`arr[j + 1]`**) are compared.
    - If **`arr[j]`** is greater than **`arr[j + 1]`**, a swap is performed to bring the larger element towards the end.
4. **Repeat:**
    - The inner loop continues until all adjacent elements have been compared and swapped if necessary.
    - The outer loop then moves to the next iteration, and the process repeats until the array is sorted.

It's important to note that bubble sort is not the most efficient sorting algorithm, especially for large datasets, but it's a simple algorithm suitable for educational purposes or small datasets. Other sorting algorithms like quicksort or mergesort are generally more efficient in practice.
