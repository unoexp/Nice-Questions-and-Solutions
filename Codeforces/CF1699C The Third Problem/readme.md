# [CF1699C The Third Problem](https://codeforces.com/problemset/problem/1699/C)

## tags
`combinatorics` `constructive algorithms` `math` `*1700`

## description
You are given a permutation a1,a2,…,an of integers from 0 to n−1. Your task is to find how many permutations b1,b2,…,bn are similar to permutation a.

Two permutations a and b of size n are considered similar if for all intervals [l,r] (1≤l≤r≤n), the following condition is satisfied:
MEX([al,al+1,…,ar])=MEX([bl,bl+1,…,br]),
where the MEX of a collection of integers c1,c2,…,ck is defined as the smallest non-negative integer x which does not occur in collection c. For example, MEX([1,2,3,4,5])=0, and MEX([0,1,2,4,5])=3.

Since the total number of such permutations can be very large, you will have to print its remainder modulo 109+7.

In this problem, a permutation of size n is an array consisting of n distinct integers from 0 to n−1 in arbitrary order. For example, [1,0,2,4,3] is a permutation, while [0,1,1] is not, since 1 appears twice in the array. [0,1,3] is also not a permutation, since n=3 and there is a 3 in the array.

Input
Each test contains multiple test cases. The first line of input contains one integer t (1≤t≤104) — the number of test cases. The following lines contain the descriptions of the test cases.

The first line of each test case contains a single integer n (1≤n≤105) — the size of permutation a.

The second line of each test case contains n distinct integers a1,a2,…,an (0≤ai<n) — the elements of permutation a.

It is guaranteed that the sum of n across all test cases does not exceed 105.

Output
For each test case, print a single integer, the number of permutations similar to permutation a, taken modulo 109+7.


## input 
```
5
5
4 0 3 2 1
1
0
4
0 1 2 3
6
1 2 4 0 5 3
8
1 3 7 2 5 0 6 4
```


## output
```
2
1
1
4
72
```


## Note
For the first test case, the only permutations similar to a=[4,0,3,2,1] are [4,0,3,2,1] and [4,0,2,3,1].

For the second and third test cases, the given permutations are only similar to themselves.

For the fourth test case, there are 4 permutations similar to a=[1,2,4,0,5,3]:

[1,2,4,0,5,3];
[1,2,5,0,4,3];
[1,4,2,0,5,3];
[1,5,2,0,4,3].

