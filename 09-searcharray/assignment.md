---
slug: searcharray
id: 6mrh2xvywqaa
type: challenge
title: searchInArray
tabs:
- title: Shell
  type: terminal
  hostname: docker-vm
  workdir: /
difficulty: basic
timelimit: 600
---
# Search Element in an Array
```
arr=("apple" "banana" "mango" "cherry" "mango" "grape")
element="mangos"
index=-1

for i in "${!arr[@]}";
do
    if [[ "${arr[$i]}" = "${element}" ]];
    then
        index=$i
        break
    fi
done

if [ $index -gt -1 ];
then
    echo "Index of Element in Array is : $index"
else
    echo "Element is not in Array."
fi
```