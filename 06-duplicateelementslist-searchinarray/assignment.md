---
slug: duplicateelementslist-searchinarray
id: 2tnyr7erw8x7
type: challenge
title: duplicateElementsList searchInArray
teaser: A short description of the challenge.
notes:
- type: text
  contents: Replace this text with your own text
difficulty: basic
timelimit: 600
---
# Duplicate element in a list
```
readarray arr
echo ${arr[@]}
echo "${arr[@]}" | sort -uz
uniqs_arr=($(for a in "${arr[@]}"; do echo "${a}"; done | sort -u))
echo ${uniqs_arr[@]}

#Or  you can use the way of associative array, in which you can map an element to the key, and using its propery it will always be unique

readarray arr
declare -A uniq_tmp

for a in "${arr[@]}"; do
    uniq_tmp[$a]=0 # assigning a placeholder
done

echo "${!uniq_tmp[@]}"
```

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