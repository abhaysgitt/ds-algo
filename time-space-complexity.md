### **Time & Space Complexity**  

---

#### **Analysis of an Algorithm:**

- Algorithm analysis is the process of evaluating an **algorithm's efficiency**.
- The goal is to predict performance without running the program, so it works efficiently for large inputs.
- The two main aspects of algorithm analysis are:
  - **Time Complexity** - How long an algorithm takes to run as input size increases.
  - **Space Complexity** - How much memory an algorithm uses as input size increases.

---

#### **Time Complexity**

- Time Complexity is the **amount of time** an algorithm takes to complete as the input size (n) increases.

- **Real World Example:**
  - Time complexity can be understood with the example of traveling from your home to the office. Here, the **input size** is affected by factors like:
    - Traffic lights
    - Traffic jams
    - Number of stops
  - Now, let's compare different modes of transport:
    - **Metro** - Even if distance increases, the time taken increases slowly. Like a metro, you can reach faster because it has fewer stops and no traffic.
    - **Bike** - Faster than a bus in small traffic but slows down as traffic increases.
    - **Bus** - Takes more time, especially with more stops and heavy traffic, similar to higher time complexity.
  - ![Time Complexity Example](https://smartprogramming.in/tutorials/dsa-using-java/images/time-complexity-in-dsa-example.jpg)
  - **Conclusion:** Just like metro, bike, and bus have different speeds depending on traffic, algorithms have different **time complexities** depending on input size.

- **Project Example :**
  - There are two shopping applications
  - Both use different algorithms to process orders.
  - **What is Input Size (n)?**
    - Input size means the number of items, orders, or data elements the algorithm needs to process.
    - Example: In a shopping app, input size could be the number of products ordered during a sale.
    - As `n` increases , execution time may increase depending on the algorithm's efficiency.
  - Below is the table showing the time taken by each algorithm for different input sizes (`n`):

    | Example Scenario          | Input Size (n)  | Algorithm A             | Algorithm B             |
    | ------------------------- | --------------- | ----------------------- | ----------------------- |
    | Small orders (Normal day) | 100 orders      | takes 50 ms of time     | takes 70 ms of time     |
    | Moderate sale event       | 1,000 orders    | takes 500 ms of time    | takes 500 ms of time    |
    | Big festive sale          | 10,000 orders   | takes 5,000 ms of time  | takes 3,000 ms of time  |
    | Massive flash sale        | 1,00,000 orders | takes 50,000 ms of time | takes 15,000 ms of time |

  - As the input size increases, Algorithm A takes more time compared to Algorithm B.
  - This means Algorithm B is more efficient for larger inputs.
  - Therefore, we can say that Algorithm B has better **Time Complexity** than Algorithm A.

- **Why Time Complexity is Important ?**
  - It determines the **speed** of the algorithm for large inputs.
  - It helps to compare the different algorithms for the same problem.

- **How Time Complexity is Measured ?**
  - Count how the number of basic operations (assignments, comparisons, loops, etc.) grows with the input size n, ignoring constants and machine-specific factors.
  - Use [asymptotic notations](https://smartprogramming.in/tutorials/dsa-using-java/asymptotic-notations.php) to represent the growth of time complexity:
    - **Big O Notation (O)** - Describes the *upper bound* (commonly used for worst-case).
    - **Omega Notation (Ω)** - Describes the *lower bound* (sometimes used for best-case).
    - **Theta Notation (Θ)** - Describes the *tight bound* (exact growth, not average case).

- **Common Time Complexities :**
  - Below is the table showing common time complexities and their growth rates:

    | Symbol     | Name              | Description                                            | Efficiency       | Notes / Examples                            |
    | ---------- | ----------------- | ------------------------------------------------------ | ---------------- | ------------------------------------------- |
    | O(1)       | Constant Time     | Execution time does not depend on input size.          | ✅ Excellent      | Accessing an array element, HashMap `get()` |
    | O(log n)   | Logarithmic Time  | Time grows slowly as input size increases.             | ✅ Very Good      | Binary Search, balanced BST operations      |
    | O(n)       | Linear Time       | Time grows directly in proportion to input size.       | 👍 Good          | Traversing an array or list                 |
    | O(n log n) | Linearithmic Time | Slightly worse than linear but better than quadratic.  | ⚖️ Acceptable    | Merge Sort, Quick Sort (average case)       |
    | O(n²)      | Quadratic Time    | Time grows proportionally to the square of input size. | ❌ Poor           | Nested loops (e.g., Bubble Sort)            |
    | O(n³)      | Cubic Time        | Time grows cubically with input size.                  | ❌ Very Poor      | Triple nested loops                         |
    | O(2ⁿ)      | Exponential Time  | Time doubles with every additional input element.      | 🚫 Extremely Bad | Recursive Fibonacci without memoization     |
    | O(n!)      | Factorial Time    | Time grows factorially with input size.                | 🚫 Worst         | Generating all permutations                 |

  - Below is the chart showing common time complexities and their growth rates: ![Time Complexity Chart](https://smartprogramming.in/tutorials/dsa-using-java/images/common-time-complexity-in-dsa-java.jpg)
  - **Note:**
    - Here, we have represented all time complexities using *Big O notation (O)* to denote the *worst-case performance* of algorithms.
    - However, time complexities can also be expressed using *Omega (Ω)* for the *best-case* and *Theta (Θ)* for the *average or tight bound* scenarios.

---

#### **Space Complexity**

- Space Complexity is the **amount of memory** an algorithm uses as the input size (n) increases.
- It includes both the **auxiliary space** (temporary space used by the algorithm) and the **input space** (space required to store the input data).

- **Real World Example:**
  - Space complexity can be understood with the example of a library. Here, the **input size** is affected by factors like:
    - Number of books
    - Size of each book
    - Number of shelves
  - Now, let's compare different storage methods:
    - **Digital Library** - Takes less space as it stores books in digital format.
    - **Physical Library** - Takes more space as it stores physical books.
  - Just like digital libraries take less space, algorithms with lower space complexity use less memory.

- **Project Example :**
  - There are two photo-editing applications
  - Both use different algorithms to apply filters to images.
  - **What is Input Size (n)?**
    - Input size means the size of the image or the amount of data the algorithm needs to process.
    - Example: In a photo-editing app, input size could be the file size of the image being edited.
    - As `n` increases , memory usage may increase depending on the algorithm's efficiency.
  - Below is the table showing the memory used by each algorithm for different input sizes (`n`):

    | Example Scenario           | Input Size (n) | Algorithm X        | Algorithm Y        |
    | -------------------------- | -------------- | ------------------ | ------------------ |
    | Small image (Profile pic)  | 1 MB           | uses 5 MB memory   | uses 4 MB memory   |
    | Medium image (Phone photo) | 5 MB           | uses 25 MB memory  | uses 15 MB memory  |
    | Large image (DSLR photo)   | 20 MB          | uses 100 MB memory | uses 50 MB memory  |
    | Ultra HD image (Poster)    | 100 MB         | uses 500 MB memory | uses 300 MB memory |

  - As the input size increases, Algorithm X uses more memory compared to Algorithm Y.
  - This means Algorithm Y is more memory-efficient for larger inputs.
  - Therefore, we can say that Algorithm Y has better **Space Complexity** than Algorithm X.

- **Why Space Complexity is Important ?**
  - It determines the **memory usage** of the algorithm for different input sizes.
  - It helps to choose algorithms that are more **memory-efficient**, especially for large datasets or devices with limited RAM.

- **How Space Complexity is Measured ?**
  - Count how much memory is required by the algorithm, including:
    - Memory for **input data** (input size `n`).
    - Memory for **variables** and **constants**.
    - Memory for **temporary data structures** like arrays, lists, or stacks.
  - Represent the growth of memory usage with **[asymptotic notations](https://smartprogramming.in/tutorials/dsa-using-java/asymptotic-notations.php)**
    - **Big O Notation (O)** - Represents the worst-case memory usage.
    - **Theta Notation (Θ)** - Represents the average-case memory usage.
    - **Omega Notation (Ω)** - Represents the best-case memory usage.



### **Function Expression f(n) of an Algorithm**  

---

#### **Introduction:**

- Function Expression is a **mathematical function** (or expression) that represents **how many operations** an algorithm performs in terms of input size `n`.
- A **function expression** can be either *exact* or *nearly exact (~)*, depending on whether the analysis is **detailed** (counting all operations) or **asymptotic** (focusing only on growth rate and dominant terms).
- It is also called the **growth function** or **cost function** `f(n)` .
- Function Expression is represented by `f(n)`, where `n` is the size of the input.
- **For Example:** For a loop running n times ,
  - `f(n) = 3n + 2`
- **Use of Function Expression :**
  - ***Check performance:*** It helps us see how many steps a program takes when the input grows.
  - ***Find time complexity:*** It is used to convert the total steps into Big O form (like O(n), O(n²)).
  - ***Compare programs:*** Helps us know which program or algorithm runs faster.
  - ***Find slow parts:*** Shows which part of the code takes the most time and needs improvement.

##### **Steps to Calculate Function Expression:**

- 

###### **1. Identify the input size variable (usually n)**

- Determine what changes with the size of the input.
- Usually, this is denoted as n.
- Example:
  ```java
  for (int i = 1; i <= n; i++)
  {
      System.out.println("Hi");
  }
  ```
  - Here, loop depends on n.

- 

###### **2. List the key operations**

- Count each basic instruction or operation that contributes significantly to runtime.
- For example:
  - Assignment (=) → 1 operation
  - Comparison (<,>, ==) → 1 operation
  - Arithmetic (+, -, *, /) → 1 operation
  - Function call → 1 operation

- 

###### **3. Count how many times each operation executes**

- Example:  

  ```java
  for (int i = 1; i <= n; i++)
  {
      System.out.println("Hello");
  }
  ```
  - int i = 0 → runs 1 time.
  - i <= n → runs n+1 times (last check fails).
  - i++ → runs n times.
  - System.out.println("Hello"); → runs n times.

- 

###### **4. Add all operations together**

- Write the expression combining all operation counts. Example:
- From the example above:  

  ```java
  f(n) = 1        // initialization
       + (n + 1)  // comparisons
       + n        // increments
       + n        // print operations
  f(n) = 3n + 2
  ```

- 

###### **5. Simplify the expression (optional)**

- If you’re focusing on asymptotic analysis, keep only the dominant term (e.g., simplify `3n+2` to `O(n)`).
- But if you want exact function expression, keep all terms.

---

#### **Some Examples with their Function Expression:**

- 

##### **Example 1 : Single Loop**

- 

```java
for (int i = 1; i <= n; i++)
{
    System.out.println(i*2);
}
```

- **Function Expression:** `f(n) = 4n + 2`   OR   `f(n) ~ n`

- 

##### **Example 2 — Nested Loops**

- 

```java
for (int i = 1; i <= n; i++)
{
    for (int j = 1; j <= n; j++)
    {
        System.out.println("Hello");
    }
}
```

- **Function Expression:** `f(n) = (2n+2) + n*(3n+2) → 3n² + 4n + 2`
- Nearly exact f(n): (outer loop cost) × (inner loop cost) → `f(n): n × n = n²`.
- In nested loops, the inner loop runs completely for each iteration of the outer loop, so we multiply the costs of both loops.

- 

##### **Example 3 — Rectangular Loops (Different Variables)**

- 

```java
for (int i = 1; i <= n; i++)
{
    for (int j = 1; j <= m; j++)
    {
        System.out.println("Hello");
    }
}
```

- **Function Expression:** `f(n, m) = (2n+2) + n*(3m + 2) → 3nm + 4n + 2`

**Rule:**

- **Nested Loops** → Multiply their costs.
- **Separate Loops** → Add their costs.



### **Asymptotic Notations in DSA**  

---

#### **Asymptotic Notations:**

- There are a lot of standard units to represent and compare quantities.
- **For example:**
  - *Distance Measurement* → Kilometers (km), Meters (m), Centimeters (cm)
  - *Storage Measurement* → Kilobytes (KB), Megabytes (MB), Gigabytes (GB)
  - *Blood Groups* → A+, A-, B+, B-, O+, O-
  - *Temperature Measurement* → Celsius (°C), Fahrenheit (°F), Kelvin (K)
- Similarly, Asymptotic notations are **mathematical tools** used to represent or describe the **time and space complexity** of an algorithm in terms of input size (*n*).
- There are total **5 types of asymptotic notations**:
  1. *Big O* `(O)`
    - **Big O** describes the *maximum time or space* an algorithm can take for large input.
    - It represents an **upper bound** on growth.
    - It is commonly used for the **worst case**, but in theory it can describe any upper limit.
  2. *Big Omega* `(Ω)`
    - **Big Omega** describes the *minimum time or space* an algorithm will take for large input.
    - It represents a **lower bound** on growth.
    - It is sometimes shown as the **best case**, but technically it just means any lower limit.
  3. *Big Theta* `(Θ)`
    - **Big Theta** describes the *exact growth rate* of an algorithm because it is bounded both above and below.
    - It represents a **tight bound**.
    - It shows the **typical or exact growth** and is not tied to best or worst case.
  4. *Little o* `(o)`
    - **Little o** describes functions that grow *strictly slower* than another function, but never equal.
    - It represents a **strictly smaller upper bound**.
    - It is not related to best, worst, or average case—only to **strict growth comparison**.
  5. *Little Omega* `(ω)`
    - **Little omega** describes functions that grow *strictly faster* than another function, but never equal.
    - It represents a **strictly bigger lower bound**.
    - It is not related to best, worst, or average case—only to **strict growth comparison**.
- **NOTE :** We mostly use **Big O Notation** `(O)` to analyze algorithms because:
  - A student is :
    - Good in Physics
    - Average in Maths
    - Worst in Chemestry
    Then student should focus on chemestry to improve overall performance and not get failed in exams.
  - Similarly, we should focus on the **worst-case scenario** of an algorithm so that our algorithm does not fail in any situation.
- Asymptotic Notations give a **high-level, machine-independent** way to analyze algorithm efficiency.
- Instead of actual execution time or memory in MB, they focus on **how these values change as input grows**.

---

#### **Programming Examples :**

- **Program 1 :** (Traverse an Array)
  - 
  ```java
  import java.util.Scanner;

  public class ArrayTraversal
  {
      public static void main(String[] args)
      {
          Scanner sc = new Scanner(System.in);

          // Input size of the array
          System.out.print("Enter number of elements: ");
          int n = sc.nextInt();

          int[] arr = new int[n];

          // Input elements
          System.out.println("Enter " + n + " elements:");
          for (int i = 0; i < n; i++)
          {
              arr[i] = sc.nextInt();
          }

          // Traverse and print elements
          System.out.println("Traversing the array:");
          for (int i = 0; i < n; i++)
          {
              System.out.println(arr[i]);
          }
      }
  }
  ```
  - 

  | Case         | Description                                                                   | Complexity |
  | ------------ | ----------------------------------------------------------------------------- | ---------- |
  | Worst Case   | Even in the worst case, we visit every element once, so complexity is `O(n)`. | `O(n)`     |
  | Average Case | On average, we visit all elements once, so complexity is `Θ(n)`.              | `Θ(n)`     |
  | Best Case    | We still need to visit every element once, so complexity is `Ω(n)`.           | `Ω(n)`     |


- **Program 2 :** (Linear Search in Array)
  - 
  ```java
  import java.util.Scanner;

  public class LinearSearch
  {
      public static void main(String[] args)
      {
          Scanner sc = new Scanner(System.in);

          // Input size of the array
          System.out.print("Enter number of elements: ");
          int n = sc.nextInt();

          int[] arr = new int[n];

          // Input elements
          System.out.println("Enter " + n + " elements:");
          for (int i = 0; i < n; i++)
          {
              arr[i] = sc.nextInt();
          }

          // Input element to search
          System.out.print("Enter element to search: ");
          int key = sc.nextInt();

          // Linear search
          boolean found = false;
          for (int i = 0; i < n; i++)
          {
              if (arr[i] == key)
              {
                  System.out.println("Element found at index: " + i);
                  found = true;
                  break;
              }
          }

          if (!found)
          {
              System.out.println("Element not found in the array.");
          }
      }
  }
  ```
  - 

  | Case         | Description                                                                                                   | Complexity |
  | ------------ | ------------------------------------------------------------------------------------------------------------- | ---------- |
  | Worst Case   | The element is either at the **last position** or not present at all, requiring `n` comparisons.              | `O(n)`     |
  | Average Case | The element is found somewhere in the **middle** of the array, so we make about `n/2` comparisons on average. | `Θ(n)`     |
  | Best Case    | The element is found at the **first position**, so only one comparison is needed.                             | `Ω(1)`     |


### **How to Analyze Time and Space Complexity of an Algorithm**  

---

#### **Introduction:**

- Analyzing (calculating) time and space complexity is an important topic for interviews and competitive programming.
- Why its so important?
  - **Performance Prediction:**
    - Estimate execution time and memory usage before implementation.
  - **Algorithm Comparison:**
    - Choose the most efficient algorithm for large inputs.
  - **Bottleneck Identification:**
    - Detect operations or structures causing slowdowns.
  - **Optimization Guidance:**
    - Decide whether to trade time for space or vice versa.

---

#### **Steps to Analyze Time Complexity:**

**NOTE :** Before analyzing (calculating) time complexity of any algorithm, we should know:

- [Time Complexity](https://smartprogramming.in/tutorials/dsa-using-java/time-and-space-complexity-java-dsa.php)
- [Asymptotic Notations](https://smartprogramming.in/tutorials/dsa-using-java/asymptotic-notations.php)

- 

##### **1. Decide What to Analyze:**

- First, you decide whether you want to analyze best case, worst case or average case.
- Reason: The number of operations (f(n)) may depend on this choice.
- For Example:
  - Eg. 1 - Linear Search:
    - *Best Case:* Element is found at the first position.
    - *Average Case:* Element is found around the middle index.
    - *Worst Case:* Element is at the last position or not present at all.
  - Eg. 2 - Bubble Sort:
    - *Best Case:* Array is already sorted → Only one pass is needed.
    - *Average Case:* Elements are randomly arranged → Multiple passes required.
    - *Worst Case:* Array is sorted in reverse order → Maximum number of swaps and passes.

- 

##### **2. Calculate the Function Expression f(n):**

- We have already learned how to calculate [function expression (f(n)) of the algorithm](https://smartprogramming.in/tutorials/dsa-using-java/function-expression-of-an-algorithm.php) :
  - [Click Here](https://smartprogramming.in/tutorials/dsa-using-java/function-expression-of-an-algorithm.php) to read this topic deeply.
- For Example:
  - Eg. 1 - Linear Search:
    - *Function Expression f(n) for Best Case:* `f(n) = 3`
    - *Function Expression f(n) for Average Case:* `f(n) = (3n / 2) + 3`
    - *Function Expression f(n) for Worst Case:* `f(n) = 3n + 3`
  - Eg. 2 - Bubble Sort:
    - *Function Expression f(n) for Best Case:* `f(n) = 2n + 3`
    - *Function Expression f(n) for Average Case:* `f(n) = (3/2)n² + (3/2)n + 2`
    - *Function Expression f(n) for Worst Case:* `f(n) = (3/2)n² + (3/2)n + 2`

- 

##### **3. Simplify f(n) using below rules:**

- Simplify the function expression f(n) using asymptotic notation rules (usually Big O notation).
  - **Constant Work :**   For eg. :   3   →   1
  - **Drop Constant Terms (add/sub) :**   For eg. :   n + 3   →   n
  - **Drop Constant Multipliers (mult/div) :**   For eg. :   3n   →   n
  - **Drop Lower Order Terms :**   For eg. :   n² + 3n + 2   →   n²
  - **Logarithm Base Change → Ignore Base :**   For eg. :   log₂ n   →   log n
  - etc...
- For Example:
  - Eg. 1 - Linear Search:
    - *Simplified f(n) for Best Case:*
      - *Constant Work :*   →   `3`   →   `1`
    - *Simplified f(n) for Average Case:*
      - *Drop All Constants :*   →   `(3n / 2) + 3`   →   `n`
    - *Simplified f(n) for Worst Case:*
      - *Drop All Constants :*   →   `3n + 3`   →   `n`
  - Eg. 2 - Bubble Sort:
    - *Simplified f(n) for Best Case:*
      - *Drop All Constants :*   →   `2n + 3`   →   `n`
    - *Simplified f(n) for Average Case:*
      - *Drop All Constants & Lower Order Terms :*   →   `(3/2)n² + (3/2)n + 2`   →   `n²`
    - *Simplified f(n) for Worst Case:*
      - *Drop All Constants & Lower Order Terms :*   →   `(3/2)n² + (3/2)n + 2`   →   `n²`

- 

##### **4. State the Final Complexity**

- Write the result in Big-Omega (`Ω`) or or Big Theta (`Θ`) or Big-O (`O`) notation.
- For Example:
  - Eg. 1 - Linear Search:
    - *Best Case:* `Ω(1)`
    - *Average Case:* `Θ(n)`
    - *Worst Case:* `O(1)`
  - Eg. 2 - Bubble Sort:
    - *Best Case:* `Ω(n)`
    - *Average Case:* `Θ(n²)`
    - *Worst Case:* `O(n²)`

