# Day 5

Problem: Maximum Subarray

leetcode link: https://leetcode.com/problems/maximum-subarray/

```js
function maxSubArray(nums) {
  let bestSum = nums[0];
  let currentSum = nums[0];

  for (let i = 1; i < nums.length; i++) {
    currentSum = Math.max(nums[i], currentSum + nums[i]);
    bestSum = Math.max(bestSum, currentSum);
  }

  return bestSum;
}
```

Input:
`nums = [-2, 1, -3, 4, -1, 2, 1, -5, 4]`

Output:
`6`

Algorithm:
Keep track of the current sum and the best sum. For each number, decide if it is better to start a new subarray or keep adding to the current one. Update the best sum when the current sum is bigger.

Python Solution:

```py
def max_sub_array(nums):
    best_sum = nums[0]
    current_sum = nums[0]

    for i in range(1, len(nums)):
        current_sum = max(nums[i], current_sum + nums[i])
        best_sum = max(best_sum, current_sum)

    return best_sum
```
