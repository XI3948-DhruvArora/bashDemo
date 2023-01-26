---
slug: palidrome-generatefibonacci-calculatefactorial
id: s5gkgglmfr1n
type: challenge
title: palidrome generateFibonacci calculateFactorial
teaser: A short description of the challenge.
notes:
- type: text
  contents: Replace this text with your own text
difficulty: basic
timelimit: 600
---

# Palindrome
A palindrome is a word, phrase, number, or other sequence of characters which reads the same backward or forward. Allowances may be made for adjustments to capital letters, punctuation, and word dividers.
For example, the word "madam" is a palindrome because it reads the same backward as forward. The number "1001" is also a palindrome because it reads the same backward as forward.
Palindromes can be found in a variety of different forms, including words, phrases, numbers, and even dates. Some well-known examples include: "A man, a plan, a canal: Panama", "Able was I ere I saw Elba" and "Madam, in Eden, I'm Adam"
Palindromes can be found in many different forms, and they are a fascinating and versatile aspect of language and mathematics.


# Check if the given string is palindrome

```
read str
s2=`echo $str | rev`
if [[ "$str" == "$s2" ]];
then
    echo "yes, given string is a palindrome"
else
    echo "no, given string is not a palindrome"
fi
```

# Fibonnaci


The Fibonacci series is a sequence of numbers in which each number is the sum of the two preceding ones, usually starting with 0 and 1. The series goes as 0, 1, 1, 2, 3, 5, 8, 13, 21, 34 and so on. The series is named after the Italian mathematician Leonardo Fibonacci, who introduced the sequence to Western mathematics in the 13th century.

The Fibonacci series also has many practical applications in computer science, particularly in the design of algorithms, such as the Fibonacci search technique. It also appears in financial market analysis and in the modeling of certain phenomena in physics and biology.
The Fibonacci series can be generated in many ways in programming languages such as Bash, one way to generate the series is by using a loop and the recursive function.

# Generate Fibonnaci series
```
read N

a=0
b=1

echo "The Fibonacci series is : "
for (( i=0; i<N; i++ ))
do
    echo -n "$a "
    fn=$((a + b))
    a=$b
    b=$fn
done
```

# Factorial


In mathematics, the factorial of a non-negative integer n, denoted by n!, is the product of all positive integers less than or equal to n. The factorial of 0 is defined to be 1.
For example, the factorial of 5 (written as 5!) is 5 x 4 x 3 x 2 x 1 = 120.


# Calculate factorial
```
read N
fact=1

for (( i=1; i<=N; i++ ))
do
    fact=$((fact * i))
done
echo $fact
```