# 🔁 Recursion:Palindrome Checker Using Recursion in Python

## 🎯 AIM:
To write a Python program to check whether a given string is a **palindrome** using **recursion**.

---

## 🧠 ALGORITHM:

1. **Start**
2. Define a recursive function `is_palindrome(word)`
   - **Base Case:** If the string length is less than 1, return `True`
   - **Recursive Case:** If the first and last characters match, call the function recursively on the substring without first and last characters
   - Else, return `False`
3. Get input from the user
4. Call the recursive function
5. Print whether the string is a palindrome
6. **Stop**

---

## 💻 PROGRAM:
```
def sum_of_digits(n):
    return sum(int(d) for d in str(n))

def head_recursion(n):
    if n == 0:
        return
    head_recursion(n - 1) 
    print(n, end=' ')

num = 123
digit_sum = sum_of_digits(num)

if digit_sum % 2 == 0:
    adjusted = num + 2
else:
    adjusted = num + 3

print(f"Sum of digits of {num} is {digit_sum}")
print("Printing sequence using head recursion up to adjusted value:")
head_recursion(5)  
```
## OUTPUT:
```
'madam' is a palindrome:
'hello' is not a palindrome.
'racecar' is a palindrome:
```
## RESULT:
The program was successful.
