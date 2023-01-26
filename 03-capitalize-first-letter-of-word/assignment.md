---
slug: capitalize-first-letter-of-word
id: mppybupj8j09
type: challenge
title: Capitalize first Letter of word
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

# Capatalize first letter of word, all first letters in sentence, all letters in word, all particular alphabets in a sentence


In a Bash script, the caret (^) symbol can be used in conjunction with variables to replace a specific string or character in the value of the variable with another string or character. Here it is used to capitalize the first letter in the string. When two caret symbols are used the capitalize all letters in the string.

```
#!/bin/bash
read var
echo ${var}
# First letter
echo ${var^}
#All leters
echo ${var^^}

# Capatalize if word starts with h
echo ${var^h}
# Capatalize all e in a sentence
echo ${var^^e}
# Capatalize all e and h in a sentence
echo ${var^^[eh]}
'''



