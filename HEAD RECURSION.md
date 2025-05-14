# 🔁 Types of Recursion: Head Recursion in Python

## 🎯 AIM:
To write a Python program to demonstrate **Head Recursion** by finding and printing the sequence based on the sum of all digits (even or odd adjusted input).

## 🧠 ALGORITHM:

1. **Start**
2. Define a recursive function `fun(n)`
3. In the function:
   - Create a recursive call at the **beginning** (Head Recursion)
   - Print the result after the recursive call
4. Take input from the user
5. If input is odd, convert it to the next even number
6. Call the recursive function
7. **Stop**

## 💻 PROGRAM:
```
def sum_of_digits(n):
    """Return the sum of digits of a number"""
    return sum(int(digit) for digit in str(n))

def head_recursive_sequence(n):
    if n <= 0:
        return
   
    sum_digits = sum_of_digits(n)
    if sum_digits % 2 == 0:
        head_recursive_sequence(n - 2)
    else:
        head_recursive_sequence(n - 1)
    print(n, end=' ')

number = 10
print(f"Head Recursion Sequence starting from {number}:")
head_recursive_sequence(number)
```
## OUTPUT:
```
Input           Result

 10           Head Recursion Sequence starting from 10:
              1 2 3 4 6 8 10
```
## RESULT:
The program was successful.
