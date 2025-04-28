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
Next level #2: implement the function with `fold` / `mapfold`.

## Challenge 2: palindrome

Create an operator `is_palindrome_list` to check if a given list of size `N` is a palindrome.
Create another operator `is_palindrome_int` to check if a given number of `N digits is a palindrome.

In both cases, the size `N` shall be a size parameter. You can try to implement with a `forward` or a `foldi`.

A palindrome is a word, phrase, number, or sequence that reads the same backward as forward.

Example:

* List: `[10.0, 23.4, 567.8, 23.4, 10.0]`
* Word: `"radar"` (i.e. list of chars `[ 'r', 'a', 'd', 'a', 'r' ]`)
* Number: `121`

Next level: check if a number is a palindrome without specifying the number of digits.

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
|2 3|  x  |4 1|  =  |14  5|
|1 4|     |2 3|     |10 13|

Detailed computation:

C[0][0] = A[0][0] * B[0][0] + A[0][1] * B[1][0] = 2*4 + 3*2 = 14
C[0][1] = A[0][0] * B[0][1] + A[0][1] * B[1][1] = 2*1 + 3*3 =  5
C[1][0] = A[1][0] * B[0][0] + A[1][1] * B[1][0] = 1*4 + 4*2 = 10
C[1][1] = A[1][0] * B[0][1] + A[1][1] * B[1][1] = 1*1 + 4*3 = 13
```

## Challenge 10: Narcissistic number

Return whether a given number is a Narcissistic number in base 10.

A Narcissistic Number (also known as an Armstrong Number) is a positive integer that is equal to the sum of its own digits, each raised to the power of the total number of digits in the number. In this challenge, we will use the base 10 system.

For example, take `9474` (4 digits), which is narcissistic:

```swan
    9^4 + 4^4 + 7^4 + 4^4 = 6561 + 256 + 2401 + 256 = 9474
```

and `1234` (4 digits), which isn't:

```swan
    1^4 + 2^4 + 3^4 + 4^4 = 1 + 16 + 81 + 256 = 354
```

