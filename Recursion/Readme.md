Array Sorting
What is Recursion Data Structure.
Example.
Interview Question.
While Loop with Array of strings

Recursion in JavaScript involves a function calling itself to solve a smaller instance of the same problem. This is a common programming technique and can be quite powerful when used appropriately.

Factorial

```jsx
// Step 0: Define a recursive function named factorial
function factorial(item) {
    // Step 1: Check if item is 0
    if (item == 0) {
        // Step 2: If item is 0, return 1 (base case)
        return 1;
    }
    // Step 3: Recursive call to factorial with item - 1
    return item * factorial(item - 1);
}

// Step 4: Initialize a variable data with the value 5
let data = 5;

// Step 5: Call factorial function with data (5)
console.warn(factorial(data));

```

Now, let's break down the execution with the comments:

1. **Function Definition (Step 0):**
    - A recursive function named **`factorial`** is defined, which takes a parameter **`item`**.
2. **Base Case Check (Step 1):**
    - Inside the function, it checks if **`item`** is equal to 0.
3. **Base Case Return (Step 2):**
    - If **`item`** is indeed 0, the function returns 1. This is the base case that stops the recursion.
4. **Recursive Call (Step 3):**
    - If **`item`** is not 0, it makes a recursive call to **`factorial(item - 1)`**. This is where the function calls itself with a smaller value.
5. **Initialization (Step 4):**
    - A variable named **`data`** is initialized with the value 5.
6. **Function Call (Step 5):**
    - The **`factorial`** function is called with the argument **`data`** (5).
7. **Recursive Execution:**
    - The recursive calls continue until the base case is reached (item becomes 0).
8. **Backtracking and Calculation:**
    - The function starts to return values as it backtracks. Each return contributes to the final result by multiplying the current **`item`** with the result of the recursive call.
9. **Final Result (Console Output):**
    - The final result, which is the factorial of 5 (**`5! = 5 * 4 * 3 * 2 * 1`**), is logged to the console.

The provided code demonstrates a recursive approach to calculating the factorial of a number. The recursive nature of the function allows it to break down the problem into smaller subproblems until it reaches a base case, resulting in the final computation.

```jsx
function factorial(item) {
    // Step 1: Check if item is 0
    if (item == 0) {
        // Step 2: If item is 0, return 1 (base case)
        return 1;
    }
    // Step 3: Recursive call to factorial with item - 1
    return item * factorial(item - 1);
}

let data = 5;
// Step 4: Call factorial function with data (5)
console.warn(factorial(data));

```

Now, let's break down the execution:

1. **Initial Call (Step 4):**
    - **`factorial(data)`** is called with **`data`** equal to 5.
2. **Inside the `factorial` function:**
    - **Step 1:** Check if **`item`** is 0. Since **`item`** is 5, we move to the next step.
    - **Step 3:** A recursive call is made to **`factorial(item - 1)`**, i.e., **`factorial(4)`**.
3. **Recursive Call with `item = 4`:**
    - **Step 1:** Check if **`item`** is 0. It's not, so we move to the next step.
    - **Step 3:** Another recursive call is made to **`factorial(3)`**.
4. **Recursive Call with `item = 3`:**
    - **Step 1:** Check if **`item`** is 0. It's not, so we move to the next step.
    - **Step 3:** Another recursive call is made to **`factorial(2)`**.
5. **Recursive Call with `item = 2`:**
    - **Step 1:** Check if **`item`** is 0. It's not, so we move to the next step.
    - **Step 3:** Another recursive call is made to **`factorial(1)`**.
6. **Recursive Call with `item = 1`:**
    - **Step 1:** Check if **`item`** is 0. It's not, so we move to the next step.
    - **Step 3:** Another recursive call is made to **`factorial(0)`**.
7. **Recursive Call with `item = 0`:**
    - **Step 1:** Check if **`item`** is 0. It is, so the base case is reached.
    - **Step 2:** Return 1.
8. **Backtracking:**
    - Now, the previous calls start to resolve.
    - **`factorial(1)`** returns **`1 * 1 = 1`**.
    - **`factorial(2)`** returns **`2 * 1 = 2`**.
    - **`factorial(3)`** returns **`3 * 2 = 6`**.
    - **`factorial(4)`** returns **`4 * 6 = 24`**.
    - **`factorial(5)`** returns **`5 * 24 = 120`**.
9. **Final Result:**
    - The final result is 120, and it is logged to the console.

So, the recursive function calculates the factorial of a number by breaking down the problem into smaller subproblems until it reaches the base case (**`item === 0`**). Each recursive call contributes to the final result.
