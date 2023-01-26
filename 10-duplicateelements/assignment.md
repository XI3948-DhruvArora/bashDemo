---
slug: duplicateelements
id: g2wbzb1xwxgx
type: challenge
title: duplicate Elements
tabs:
- title: Shell
  type: terminal
  hostname: docker-vm
  workdir: /
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
