---
slug: calculatefactorial
id: xmkjx9sbvvt4
type: challenge
title: calculate factorial
tabs:
- title: Shell
  type: terminal
  hostname: docker-vm
  workdir: /
difficulty: basic
timelimit: 600
---
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