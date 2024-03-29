# [CF1721D Maximum AND](https://codeforces.com/contest/1721/problem/D)

## tags
`bitmasks` `divide and conquer` `greedy` `sortings` 

## description

You are given two arrays a and b, consisting of n integers each.

Let's define a function f(a,b) as follows:

let's define an array c of size n, where ci=ai⊕bi (⊕ denotes bitwise XOR);
the value of the function is c1&c2&⋯&cn (i.e. bitwise AND of the entire array c).
Find the maximum value of the function f(a,b) if you can reorder the array b in an arbitrary way (leaving the initial order is also an option).

Input
The first line contains one integer t (1≤t≤104) — the number of test cases.

The first line of each test case contains one integer n (1≤n≤105) — the size of arrays a and b.

The second line contains n integers a1,a2,…,an (0≤ai<230).

The third line contains n integers b1,b2,…,bn (0≤bi<230).

The sum of n over all test cases does not exceed 105.

Output
For each test case print one integer — the maximum value of the function f(a,b) if you can reorder the array b in an arbitrary way.

## input
```
3
5
1 0 0 3 3
2 3 2 1 0
3
1 1 1
0 0 3
8
0 1 2 3 4 5 6 7
7 6 5 4 3 2 1 0
```

## output
```
2
0
7
```

