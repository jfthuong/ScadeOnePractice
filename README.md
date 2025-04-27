# Challenges to practice Scade One / Swan Language

Challenges to practice knowledge of [Scade One](https://www.ansys.com/products/embedded-software/ansys-scade-one).

The software can be downloaded for free in the Student version here: https://www.ansys.com/academic/students/ansys-scade-student

... the challenges are inspired by challenges for C language

## Challenge 1: Sum of digits

Given a five digit integer, get the sum of its digits.

Example:

```swan
sum_of_digits(12345) -- returns 15
```

Next level: update the function to take an integer of any number of digits as an input.

## Challenge 2: palindrome

Create an operator to check if a given string or number is a palindrome.

A palindrome is a word, phrase, number, or sequence that reads the same backward as forward, ignoring spaces, punctuation, and capitalization.

Example:
Word: `"radar"` (reads the same backward as forward)
Number: `121` (reads the same backward as forward)

## Challenge 3: number of vowels & consonants

Write an operator to count the number of vowels and consonants in a given list of chars.

Example:

```swan
count_vowels_and_consonants( [ 'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j' ] ) -- returns 3, 7
```

## Challenge 4: occurrences of numbers

Given a string `s` consisting of alphabets and digits, find the frequency of each digit in the given string.

e.g. `a11472o5t6` => `0 2 1 0 1 1 1 1 0 0`
... corresponding to  0 1 2 3 4 5 6 7 8 9

## Challenge 5: factorial

Implement an operator to calculate the factorial of a given positive integer using recursion.

## Challenge 6: Fibonacci

Generate the first `N` (a constant) numbers in the Fibonacci sequence.
The Fibonacci sequence is a series of numbers in which each number (after the first two) is the sum of the two preceding ones,
usually starting with 0 and 1.

Example: `N = 10` => `0, 1, 1, 2, 3, 5, 8, 13, 21, 34`

## Challenge 7: Prime numbers

Write an operator to check if a given number is a prime number.

## Challenge 8: Count subsets

<!-- ? Is it  DOABLE? -->
Write an operator that counts the number a given list (of chars or numbers) has a given subset of length 3, without overlap.

Examples:

* `count_substr( [1, 1, 1, 2, 2, 2], [1, 1, 1])` should return 1
* `count_substr( [1, 1, 1, 2, 2, 1, 1, 1], [1, 1, 1])` should return 2
* `count_substr( [1, 1, 1, 1, 1, 2, 2, 2], [1, 1, 1])` should return 1

You can use state machines to do that.

Next level: accept a subset of any length (specified as a size parameter).

## CHallenge 9: Matrix multiplication

Write a function that accepts two square (2x2) matrices (two dimensional arrays), and returns the product of the two.
Only square matrices will be given.

Example:

```swan
  A         B          C
|1 2|  x  |3 2|  =  | 5 4|
|3 2|     |1 1|     |11 8|
```

Detailled computation

```swan
C[0][0] = A[0][0] * B[0][0] + A[0][1] * B[1][0] = 1*3 + 2*1 =  5
C[0][1] = A[0][0] * B[0][1] + A[0][1] * B[1][1] = 1*2 + 2*1 =  4
C[1][0] = A[1][0] * B[0][0] + A[1][1] * B[1][0] = 3*3 + 2*1 = 11
C[1][1] = A[1][0] * B[0][1] + A[1][1] * B[1][1] = 3*2 + 2*1 =  8
```

## Challenge 10: Narcissistic number

A Narcissistic Number (or Armstrong Number) is a positive number which is the sum of its own digits, each raised to the power of the number of digits in a given base. In this challenge, we restrict ourselves to decimal (base 10).

For example, take `153` (3 digits), which is narcissistic:

```swan
    1^3 + 5^3 + 3^3 = 1 + 125 + 27 = 153
```

and `1652` (4 digits), which isn't:

```swan
    1^4 + 6^4 + 5^4 + 2^4 = 1 + 1296 + 625 + 16 = 1938
```

The Challenge: return 'true' or 'false' depending upon whether the given number is a Narcissistic number in base 10.
