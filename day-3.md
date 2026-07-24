# Day 3

Problem: Contains Duplicate

leetcode link: https://leetcode.com/problems/contains-duplicate/

```js
function containsDuplicate(nums) {
  const seen = {};

  for (const num of nums) {
    if (seen[num]) {
      return true;
    }

    seen[num] = true;
  }

  return false;
}
```

Input:
`nums = [1, 2, 3, 1]`

Output:
`true`

Algorithm:
Create an object to keep track of numbers already seen. Loop through the array. If a number is already in the object, return true. If the loop finishes, return false.

Python Solution:

```py
def contains_duplicate(nums):
    seen = {}

    for num in nums:
        if num in seen:
            return True

        seen[num] = True

    return False
```
