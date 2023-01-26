---
slug: first-even-number
id: tiygxuwccjar
type: challenge
title: first even number
teaser: A short description of the challenge.
notes:
- type: text
  contents: Replace this text with your own text
tabs:
- title: Shell
  type: terminal
  hostname: docker-vm
  workdir: /
difficulty: basic
timelimit: 600
---
# Pick first Even number

# Loops
In Bash, loops are used to repeatedly execute a set of commands. There are several types of loops available in Bash, including:
for loops: used to iterate through a list of items.

1. while loops: used to repeatedly execute a set of commands as long as a certain condition is true.
2. until loops: used to repeatedly execute a set of commands until a certain condition is true. The syntax for an until loop is similar to that of a while loop.
3. for-in loops: used to iterate through the elements of an array.

It's worth noting that in the loops the commands inside the loop will be executed repeatedly until the condition is met. Also, the conditions in the loops can be any valid command or command line that returns a 0 or non-zero exit status, where 0 means success and non-zero means failure.

# Conditional Statements
In Bash, if statements are used to perform conditional operations. An if statement allows you to execute a set of commands if a certain condition is true.
You can also use the elif (else if) and else statements to specify additional commands to be executed in case the condition of the if statement is false.

The if statement can be used with different types of conditions, such as:
File conditions: to check if a file exists, is a directory, is a regular file, etc.
String conditions: to check if a string is empty, if it starts with a certain character, etc.
Numeric conditions: to check if a number is greater than, less than, equal to, etc.

It's important to note that the conditions in the if statement can be any valid command or command line that returns a 0 or non-zero exit status, where 0 means success and non-zero means failure.

Also, it's worth noting that in Bash the test command can be shortened to [ and the closing bracket ] is necessary to close the command, so the syntax becomes if [condition]; then ...
The if statement is a fundamental building block of any shell script, and it allows you to control the flow of your script and make decisions based on the results of different tests or conditions.


# Arrays
In Bash, an array is a way to store multiple values in a single variable. Each value in an array is called an element, and elements can be of different types, such as strings, integers, or even other arrays.
An array can be created by assigning a list of values to a variable, with the values separated by spaces, and the array variable name enclosed in parentheses:
You can also create an array by assigning a string to a variable and using the IFS (Internal Field Separator) variable to specify the delimiter.
You can access the elements of an array by using the variable name followed by the index of the element in square brackets.

**That arrays in Bash are indexed starting from 0.**



```
read -a arr

for i in ${arr[@]}
do
    if [ $((i%2)) == 0 ]
    then
        echo $i
        break
    fi
done
```