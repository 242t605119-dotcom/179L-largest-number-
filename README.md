# LeetCode 179 - Largest Number

## Problem

Given a list of non-negative integers, arrange them so that they form the **largest possible number**.

Return the result as a string.

### Example

```text
Input: nums = [10,2]
Output: "210"
```

Another example:

```text
Input: nums = [3,30,34,5,9]
Output: "9534330"
```

## Approach

Simply sorting the numbers normally will not always give the largest number.

For two numbers `a` and `b`, compare:

```text
a + b
b + a
```

If `a + b` is larger, `a` should come before `b`.

### Example

For `3` and `30`:

```text
330
303
```

Since `330` is larger, `3` should come before `30`.

So we use a custom sorting rule.

## Algorithm

1. Convert all numbers to strings.
2. Compare two numbers by checking `a + b` and `b + a`.
3. Sort the numbers using this custom comparison.
4. Join all numbers together.
5. If the result starts with `0`, return `"0"`.

## Important Edge Case

For:

```text
nums = [0, 0]
```

The result should be:

```text
"0"
```

not:

```text
"00"
```

So the code checks whether the final result starts with `0`.

## Complexity

* **Time Complexity:** `O(n log n × k)`
* **Space Complexity:** `O(n)`

where `n` is the number of elements and `k` is the average number of digits.

## Key Concepts

* Custom Sorting
* String Comparison
* Comparator
* Greedy Approach
* `cmp_to_key`

## What I Learned

This problem helped me understand that normal numerical sorting is not always enough.

The important idea is to decide the order of two numbers by checking which concatenation produces the larger value.

## LeetCode Details

* **Problem:** 179
* **Title:** Largest Number
* **Language:** Python
* **Difficulty:** Medium

## Author

T.Nandhini
