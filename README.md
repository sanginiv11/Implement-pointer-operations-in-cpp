# Implementation of Pointer Operations in C++  

### Objective  
To explore and demonstrate different pointer operations in C++ through **call by value** and **call by reference** methods.  

**Tools Used:** MinGW Compiler, Visual Studio Code, and Online C++ Compilers.  

***

## **Program 1: Call by Value**  
### Concept and Explanation  
In this approach, **copies** of the variables are passed to the function. Inside the `swap()` function, the values appear to interchange, but these modifications only apply to the local copies, leaving the original `a` and `b` unchanged in `main()`. This technique highlights that **call by value never changes the actual data in the calling function—it only modifies duplicates inside the function.**

### Algorithm  
1. Start  
2. Define a function `swap(x, y)`  
3. Save `x` in a temporary variable `aa`  
4. Assign `y` to `x`  
5. Assign `aa` to `y`  
6. Print the swapped values inside the function  
7. In `main()`, call `swap(a, b)`  
8. Print the original values of `a` and `b`  
9. Stop  

***

## **Program 2: Call by Reference (using pointers)**  
### Concept and Explanation  
Here, instead of passing variable copies, we provide **the addresses of variables** to the function. Using pointers (`*x`, `*y`), the function directly accesses and updates the original variables. Therefore, after execution, both `a` and `b` actually get swapped in `main()`. Unlike the previous method, this ensures **changes are permanent outside the function**, making it useful for real data modification.  

### Algorithm  
1. Start  
2. Define a function `swap(int *x, int *y)`  
3. Store the value of `*x` in a temporary variable `aa`  
4. Assign `*y` to `*x`  
5. Assign `aa` to `*y`  
6. Print swapped results inside the function  
7. In `main()`, call `swap(&a, &b)`  
8. Print updated values of `a` and `b`  
9. Stop  

***

## **Program 3: Call by Reference with Increment (using reference variables)**  
### Concept and Explanation  
This method uses **C++ reference variables** so that the function directly works on the original variable without explicitly using pointers. A reference parameter `int &x` points to the actual memory of variable `a`. When `x` is increased by 45 inside the function, `a` itself gets updated. This process is simpler than pointer syntax yet provides the same direct modification facility.  

### Algorithm  
1. Start  
2. Define a function `swap(int &x)`  
3. Declare a constant value `aa = 45`  
4. Increment `x` by `aa`  
5. Print the updated value inside the function  
6. In `main()`, set `a = 3`  
7. Print the original value of `a`  
8. Call `swap(a)`  
9. Stop  

***

## **Conclusion**  
These three programs illustrate **different ways of passing arguments to functions in C++**:  

- **Call by value** → passes copies, so the original variables remain unchanged.  
- **Call by reference using pointers** → passes addresses, allowing real changes to original variables.  
- **Call by reference using references** → a cleaner syntax that directly modifies the original data without dealing with pointer operators.  

Altogether, these examples show that the **choice of parameter passing method** depends on whether the original data should remain untouched or be updated by the function.  
