# Day 2

Problem: Two Sum

leetcode link: https://leetcode.com/problems/two-sum/

```js
function twoSum(nums, target) {
  for (let i = 0; i < nums.length; i++) {
    for (let j = i + 1; j < nums.length; j++) {
      if (nums[i] + nums[j] === target) {
        return [i, j];
      }
    }
  }
}
```

Input:
`nums = [2, 7, 11, 15], target = 9`

Output:
`[0, 1]`

Algorithm:
Use two loops. Check each number with every number after it. If the two numbers add up to the target, return their indexes.

Python Solution:

```py
def two_sum(nums, target):
    for i in range(len(nums)):
        for j in range(i + 1, len(nums)):
            if nums[i] + nums[j] == target:
                return [i, j]
```
