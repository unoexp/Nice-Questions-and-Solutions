# [CF1715D 2+ doors](https://codeforces.com/problemset/problem/1715/D)

## tags
`2-sat` `bitmasks` `graphs` `greedy` `*1900`

## desctiprion
The Narrator has an integer array a of length n, but he will only tell you the size n and q statements, each of them being three integers i,j,x, which means that ai∣aj=x, where | denotes the bitwise OR operation.

Find the lexicographically smallest array a that satisfies all the statements.

An array a is lexicographically smaller than an array b of the same length if and only if the following holds:

in the first position where a and b differ, the array a has a smaller element than the corresponding element in b.
Input
In the first line you are given with two integers n and q (1≤n≤105, 0≤q≤2⋅105).

In the next q lines you are given with three integers i, j, and x (1≤i,j≤n, 0≤x<230) — the statements.

It is guaranteed that all q statements hold for at least one array.

Output
On a single line print n integers a1,a2,…,an (0≤ai<230) — array a.

## input
```
4 3
1 2 3
1 3 2
4 1 2
```

## output
```
0 3 2 2 
```


## input
```
1 0
```

## output
```
0 
```


## input
```
2 1
1 1 1073741823
```
## output
```
1073741823 0 
```


## note

Note
In the first sample, these are all the arrays satisfying the statements:

[0,3,2,2],
[2,1,0,0],
[2,1,0,2],
[2,1,2,0],
[2,1,2,2],
[2,3,0,0],
[2,3,0,2],
[2,3,2,0],
[2,3,2,2].




