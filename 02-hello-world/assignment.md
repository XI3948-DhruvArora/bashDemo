---
slug: hello-world
id: un90tlz18rqe
type: challenge
title: Hello World
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
# Get Started

Create a bash file with extension of .sh

```test_script.sh```
```
touch test_script.sh
```

Use nano or vim test_script.sh to edit the script

```chmod -v +x```  hello.sh to set executable permision
```
./hello.sh
sh hello.sh
bash hello.sh
```
Use one of the above methods to run the file

# Variables
In Bash, a variable is a way to store and manipulate data. Variables are used to store values such as strings, numbers, or even the output of commands. Variables are assigned values using the assignment operator (=), and the value of a variable can be accessed by referencing its name preceded by a dollar sign ($).
It's also good practice to use uppercase letters for variable names, making it clear that the variable is not a command.

You can also use the export command to make the variable available to other processes and even other terminal sessions.

# Strings
In Bash, a string is a sequence of characters. Strings can be used to store text, numbers, or any other data that can be represented as text.
Strings can be defined in various ways in Bash:
1. Using double quotes
2. Using single quotes
3. Without quotes
4. Using the <<< operator
The difference between double quotes and single quotes is that when a string is enclosed in double quotes, variable and command substitution are performed, whereas when a string is enclosed in single quotes, the string is treated literally and no variable or command substitution takes place.

There are also various string manipulation commands available in Bash, such as grep, sed, awk, tr, cut , echo and string operations like ${string:start:length} to extract a substring, ${string//substring/replacement} to replace all occurrences of a substring, etc.

Bash also provides a set of string manipulation parameter expansion operations that can be used to perform string operations like ${string:start:length} to extract a substring, ${string//substring/replacement} to replace all occurrences of a substring, etc.

```
#!/bin/bash
var="Hello World"
echo "$var"
printf "%s\n" "$var"
```