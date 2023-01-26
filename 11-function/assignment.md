---
slug: function
id: 2yfsrwtt3o9z
type: challenge
title: functions
tabs:
- title: Shell
  type: terminal
  hostname: docker-vm
  workdir: /
difficulty: basic
timelimit: 600
---
#Functions

In bash, a function is a block of code that can be executed multiple times with a single command. Functions are defined using the keyword "function" followed by the function name, and the code block is enclosed in curly braces. The syntax for calling a function is to simply enter the function name followed by any required arguments. Functions can also accept input parameters and return values. Functions can be useful for organizing and reusing code in a bash script.

```
#!/usr/bin/env bash
ARG=$1

function mimic {
  if [[ -z $ARG ]]; then
    ARG='world'
  fi
  echo "hello $ARG"
}

mimic $ARG
```