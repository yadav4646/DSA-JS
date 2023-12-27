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


----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                                                                                                IN-DIRECT RECURSION
# Indirect ****Recursion****

What is Indirect Recursion?

**Indirect recursion occurs when two or more functions are involved in a circular calling pattern. In other words, Function A calls Function B, and then Function B calls Function C, and eventually, Function C or another function calls back to Function A, forming a loop.**

Here's a simple example to illustrate indirect recursion:

```jsx
javascriptCopy code
// Function A
function functionA() {
  console.log("Function A");
  functionB(); // Function A calls Function B
}

// Function B
function functionB() {
  console.log("Function B");
  functionC(); // Function B calls Function C
}

// Function C
function functionC() {
  console.log("Function C");
  functionA(); // Function C calls back to Function A, forming a loop
}

// Call Function A to start the indirect recursion
functionA();

```

In this example, Function A calls Function B, which in turn calls Function C. Finally, Function C calls back to Function A, creating a circular or indirect recursion. When you run this code, you'll see an output that continuously cycles through the messages from Function A, Function B, and Function C.

It's important to use caution with indirect recursion to avoid infinite loops. Proper base cases or exit conditions should be implemented to ensure that the recursion eventually stops. In some cases, indirect recursion can be useful for solving certain problems, but it requires careful design to prevent unintended consequences.

https://www.youtube.com/watch?v=Njy2vF-X-K8&list=PL8p2I9GklV47TMMnPzqnkCtSOS3ebr4O7&index=12

```jsx
javascriptCopy code
<script>
    // Initial amount of money
    let money = 100;

    // Variable to track the total number of apples bought
    let totalApple = 0;

    // Function to buy apples
    function buyApple(x) {
        // Step 1: Check if there is still money to buy apples
        if (x > 0) {
            // Step 2: Display the current amount of money and total apples
            console.warn(`I have Rs. ${x}, bought ${totalApple} apples.`);

            // Step 3: Call the function to buy more apples
            buyMore(x);
        } else {
            // Step 4: If there is no more money, display the total number of apples bought
            console.warn(`I don't have more money. Bought ${totalApple} apples.`);
        }
    }

    // Function to buy more apples
    function buyMore(x) {
        // Step 5: Increment the total number of apples
        totalApple++;

        // Step 6: Recursively call the buyApple function with reduced money (x - 20)
        buyApple(x - 20);
    }

    // Step 7: Start the process by calling buyApple with the initial amount of money
    buyApple(money);
</script>

```

Now, let's go through the execution with comments:

1. **Initial Setup (Step 7):**
    - The process begins by calling **`buyApple(money)`** with an initial amount of Rs. 100.
2. **Buying Apples (Steps 1-6):**
    - Inside the **`buyApple`** function, it checks if there is enough money (**`x > 0`**).
    - If there is money, it displays the current amount of money and the total number of apples bought, then calls the **`buyMore`** function.
    - The **`buyMore`** function increments the total number of apples and calls **`buyApple`** recursively with reduced money (**`x - 20`**).
    
    **Console Output:**
    
    ```css
    cssCopy code
    I have Rs. 100, bought 0 apples.
    I have Rs. 80, bought 1 apples.
    I have Rs. 60, bought 2 apples.
    I have Rs. 40, bought 3 apples.
    I have Rs. 20, bought 4 apples.
    I don't have more money. Bought 5 apples.
    
    ```
    
3. **Recursive Calls:**
    - The process continues with recursive calls until there is no more money (**`x <= 0`**).
    - Each recursive call reduces the amount of money by Rs. 20 and increments the total number of apples.
4. **Final Output:**
    - When the person runs out of money, the code prints a message indicating the total number of apples bought.

In the console output, you can see the sequence of messages indicating the amount of money and the total number of apples at each step. The person buys an apple for Rs. 20 until there is no more money left. The final message indicates the total number of apples bought.
