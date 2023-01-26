---
slug: palindrome
id: uihncg6alrrx
type: challenge
title: Palindrome
tabs:
- title: Shell
  type: terminal
  hostname: docker-vm
  workdir: /
difficulty: basic
timelimit: 600
---

# Palindrome
A palindrome is a word, phrase, number, or other sequence of characters which reads the same backward or forward. Allowances may be made for adjustments to capital letters, punctuation, and word dividers.
For example, the word "madam" is a palindrome because it reads the same backward as forward. The number "1001" is also a palindrome because it reads the same backward as forward.
Palindromes can be found in a variety of different forms, including words, phrases, numbers, and even dates. Some well-known examples include: "A man, a plan, a canal: Panama", "Able was I ere I saw Elba" and "Madam, in Eden, I'm Adam"
Palindromes can be found in many different forms, and they are a fascinating and versatile aspect of language and mathematics.


# Check if the given string is palindrome

```
read str
s2=`echo $str | rev`
if [[ "$str" == "$s2" ]];
then
    echo "yes, given string is a palindrome"
else
    echo "no, given string is not a palindrome"
fi
```