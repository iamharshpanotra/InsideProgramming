# Basics of Array

## What is an Array?
An **array** is a data structure that stores a collection of elements of the same data type. These elements can be integers, strings, characters, or even pairs like `pair<int, int>`.

### Key Characteristics:
- All elements in an array must be of the **same data type**.
- Arrays are stored in **contiguous memory locations**.
- Elements are accessed using **zero-based indexing**.

---

## Declaring an Array
To declare an array of integers with a size of 6:
```cpp
int arr[6];
```
- If declared inside the `main()` function, the array will contain **garbage values** initially.
- If declared **globally** (outside `main()`), the array is initialized with **all elements set to 0**.

### Example:
```cpp
#include<iostream>
using namespace std;

int arrGlobal[6]; // Global array, initialized with 0s

int main() {
    int arrLocal[6]; // Local array, contains garbage values
    return 0;
}
```

---

## Array Size Limits
The maximum size of an array depends on whether it is declared **inside** or **outside** `main()`:
- **Inside `main()`**: Maximum size = `10^6` (1,000,000 elements)
- **Globally**: Maximum size = `10^7` (10,000,000 elements)

### Example:
```cpp
int globalArray[10000000]; // 10^7 elements (valid globally)

int main() {
    int localArray[1000000]; // 10^6 elements (valid inside main)
    return 0;
}
```

---

## Accessing Array Elements
Elements in an array are accessed using **indices**. The first index starts at `0`, followed by `1, 2, 3, ... n-1`.

### Example: Iterating through an array
```cpp
#include<iostream>
using namespace std;

int main() {
    int arr[5] = {10, 20, 30, 40, 50};
    int n = 5;
    
    for(int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    return 0;
}
```
**Output:**
```
10 20 30 40 50
```

---

## Summary
- An array is a **fixed-size data structure** that stores elements of the same type.
- **Local arrays** (inside `main()`) contain **garbage values** unless explicitly initialized.
- **Global arrays** are **automatically initialized to 0**.
- The maximum size depends on the scope:
  - **Inside `main()`**: `10^6`
  - **Global scope**: `10^7`
- Elements are accessed via **zero-based indexing**.
- **Looping through an array** is a common operation using a `for` loop.
