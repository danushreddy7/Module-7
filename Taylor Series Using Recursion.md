# 📐 Taylor Series Using Recursion in Python

## 🎯 AIM:
To write a Python program to evaluate a **Taylor Series** using **recursion**, where values of `x` and `n` are taken from the user.

## 🧠 ALGORITHM:

1. **Start**
2. Create variables `x` and `n`
3. Get values for `x` and `n` from the user
4. Define a recursive function `series(x, n)`
   - **Base case:** If `n == 0`, return 1
   - **Recursive case:** Return `x**n / n + series(x, n-1)`
5. Print the result
6. **Stop**

## 💻 PROGRAM:
```
def taylor_series(x, n, current_term=0):

    if n == 0:
        return 1
 
    else:
        return (x ** current_term) / factorial(current_term) + taylor_series(x, n-1, current_term + 1)

def factorial(num):
    # Recursive function to calculate factorial
    if num == 0:
        return 1
    else:
        return num * factorial(num - 1)
x = float(input("Enter the value of x: "))
n = int(input("Enter the number of terms in the Taylor Series: "))

result = taylor_series(x, n)

print(f"The value of e^{x} using Taylor Series with {n} terms is: {result}")

```

## OUTPUT:
```
Input         Result
  1        Enter the number of terms in the Taylor Series: 10
```
## RESULT:
The program was successful.
