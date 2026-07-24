# Day 1

Problem: FizzBuzz

leetcode link: https://leetcode.com/problems/fizz-buzz/

```js
function fizzBuzz(n) {
  const result = [];

  for (let i = 1; i <= n; i++) {
    if (i % 15 === 0) {
      result.push("FizzBuzz");
    } else if (i % 3 === 0) {
      result.push("Fizz");
    } else if (i % 5 === 0) {
      result.push("Buzz");
    } else {
      result.push(String(i));
    }
  }

  return result;
}
```

Input:
`n = 5`

Output:
`["1", "2", "Fizz", "4", "Buzz"]`

Algorithm:
Loop from 1 to n. If the number is divisible by 3 and 5, add FizzBuzz. If it is only divisible by 3, add Fizz. If it is only divisible by 5, add Buzz. Otherwise add the number as a string.

Python Solution:

```py
def fizz_buzz(n):
    result = []

    for i in range(1, n + 1):
        if i % 15 == 0:
            result.append("FizzBuzz")
        elif i % 3 == 0:
            result.append("Fizz")
        elif i % 5 == 0:
            result.append("Buzz")
        else:
            result.append(str(i))

    return result
```
