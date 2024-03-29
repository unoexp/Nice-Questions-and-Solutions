# [CF1691D Max GEQ Sum](https://codeforces.com/problemset/problem/1691/D)

## tags
`binary search` `constructive algorithms` `data structures` `divide and conquer` `implementation` `two pointers` `*1800`

## description
You are given an array a of n integers. You are asked to find out if the inequality
max(ai,ai+1,…,aj−1,aj)≥ai+ai+1+⋯+aj−1+aj
holds for all pairs of indices (i,j), where 1≤i≤j≤n.

Input
Each test contains multiple test cases. The first line contains the number of test cases t (1≤t≤105). Description of the test cases follows.

The first line of each test case contains a single integer n (1≤n≤2⋅105)  — the size of the array.

The next line of each test case contains n integers a1,a2,…,an (−109≤ai≤109).

It is guaranteed that the sum of n over all test cases does not exceed 2⋅105.

Output
For each test case, on a new line output "YES" if the condition is satisfied for the given array, and "NO" otherwise. You can print each letter in any case (upper or lower).


## input

```
3
4
-1 1 -1 2
5
-1 2 -3 2 -1
3
2 3 -1
```

## output
```
YES
YES
NO
```


## Note
In test cases 1 and 2, the given condition is satisfied for all (i,j) pairs.

In test case 3, the condition isn't satisfied for the pair (1,2) as max(2,3)<2+3.


