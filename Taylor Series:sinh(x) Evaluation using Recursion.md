# 📐 Taylor Series:sinh(x) Evaluation using Recursion in Python

## 🎯 AIM:
To write a Python program to evaluate the value of **sinh(x)** for **n terms** using recursion.

---

## 🧠 ALGORITHM:

1. **Start**
2. Read input for variable `x` (angle or number)
3. Read input for variable `n` (number of terms)
4. Define a function `fact(n)`:
   - If `n <= 1`, return 1
   - Else, return `n * fact(n - 1)` (recursive factorial)
5. Define a function `sinh(x, n)`:
   - If `n == 0`, return `x`
   - Else, return `(pow(x, 2*n + 1) / fact(2*n + 1)) + sinh(x, n - 1)`
6. Call the `sinh(x, n)` function and print the result
7. **Stop**

---

## 💻 PROGRAM:
```
def sinh(x, n, current_term=0):
 
    if n == 0:
        return 0
    else:
        term = (x ** (2*current_term + 1)) / factorial(2 * current_term + 1)
        return term + sinh(x, n-1, current_term + 1)
def factorial(num):
    if num == 0:
        return 1
    else:
        return num * factorial(num - 1)

x = float(input())
n = int(input())
result = sinh(x, n)

print(f"The value of sinh({x}) using Taylor Series with {n} terms is: {result}")
````
## OUTPUT:
```
Input         Result
  1       Enter the number of terms in the Taylor Series: 10
```
## RESULT:
The program was successful
