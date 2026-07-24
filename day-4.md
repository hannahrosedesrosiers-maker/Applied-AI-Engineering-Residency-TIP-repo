# Day 4

Problem: Valid Palindrome

leetcode link: https://leetcode.com/problems/valid-palindrome/

```js
function isPalindrome(s) {
  let cleaned = "";

  for (const char of s.toLowerCase()) {
    if ((char >= "a" && char <= "z") || (char >= "0" && char <= "9")) {
      cleaned += char;
    }
  }

  let left = 0;
  let right = cleaned.length - 1;

  while (left < right) {
    if (cleaned[left] !== cleaned[right]) {
      return false;
    }

    left++;
    right--;
  }

  return true;
}
```

Input:
`s = "A man, a plan, a canal: Panama"`

Output:
`true`

Algorithm:
Make the string lowercase and remove spaces and punctuation. Use two pointers, one at the start and one at the end. If the characters do not match, return false. If they all match, return true.

Python Solution:

```py
def is_palindrome(s):
    cleaned = ""

    for char in s.lower():
        if char.isalnum():
            cleaned += char

    left = 0
    right = len(cleaned) - 1

    while left < right:
        if cleaned[left] != cleaned[right]:
            return False

        left += 1
        right -= 1

    return True
```
