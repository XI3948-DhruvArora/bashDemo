---
slug: countwordsinstring-reverseastring
id: xehbe8ln0dka
type: challenge
title: countWordsInString reverseAString
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
# Count words in a string
```
read str
echo "$str" | wc -w
```


# Reverse a string
```
  read str
  revstr=`echo $str | rev`
  echo $revstr

# Or you can do it using for loop

  strlen=${#s}
  for (( i=$strlen-1; i>=0; i-- ));
  do
      revstr=$revstr${s:$i:1}
  done
  echo $revstr
```

# AWK
In Bash, awk is a command-line utility for text processing. It is a powerful tool for working with text files, especially large ones, and it is often used for data extraction, manipulation, and reporting.
awk is a programming language in itself, which means that it has its own syntax and commands.

The pattern is a regular expression that awk uses to match lines in the input file. If no pattern is specified, the action is applied to all lines.

The action is a set of commands that awk performs on the lines that match the pattern. If no action is specified, awk simply prints the matching lines.
awk provides various built-in variables such as $0, $1, $2, etc., that can be used to access fields of the input line. By default, fields are separated by whitespaces, but this can be changed using the -F option.
awk also provides various built-in functions such as length, substr, split, etc., that can be used to perform string operations.

It's also worth noting that awk is powerful for data manipulation and reporting, it can be used to perform calculations, filtering, and formatting of data in a way that is much more efficient than trying to accomplish the same task with a series of grep, sed, and cut commands.

awk is a versatile tool and it's widely used in the Unix-based systems. It is a powerful tool for text processing and data manipulation, it can be used to perform complex operations on text files and it's a must-have tool in any Linux administrator or developer's toolbox.



# Print All unique words in file/string

```
#If user needs to give input, the below statement will take input, pree enter and cntrl+D when finished. Input will be in form of a file
awk '{for(i = 1; i <= NF; i++) {a[$i]++}} END {for(k in a) if(a[k] == 1) {print  k, a[k]}}

#else if file is input, f is file
awk '{for(i = 1; i <= NF; i++) {a[$i]++}} END {for(k in a) if(a[k] == 1) {print  k, a[k]}}' f
```

# Count number of unique words
```
awk '{for(i = 1; i <= NF; i++) {a[$i]++}} END {for(k in a) if(a[k] == 1){counter++} print "Unique words in file " FILENAME " are: "counter}' file.txt
```