---
slug: generatefibonnaci
id: 7cdbmlweodpd
type: challenge
title: generate fibonnaci
tabs:
- title: Shell
  type: terminal
  hostname: docker-vm
  workdir: /
difficulty: basic
timelimit: 600
---

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