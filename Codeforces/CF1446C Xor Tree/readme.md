# [CF1446C Xor Tree](https://codeforces.com/problemset/problem/1446/C)

## tags
`binary search` `bitmasks` `data structures` `divide and conquer` `dp` `trees` `*2100`

## description
For a given sequence of distinct non-negative integers (b1,b2,…,bk) we determine if it is good in the following way:

Consider a graph on k nodes, with numbers from b1 to bk written on them.
For every i from 1 to k: find such j (1≤j≤k, j≠i), for which (bi⊕bj) is the smallest among all such j, where ⊕ denotes the operation of bitwise XOR (https://en.wikipedia.org/wiki/Bitwise_operation#XOR). Next, draw an undirected edge between vertices with numbers bi and bj in this graph.
We say that the sequence is good if and only if the resulting graph forms a tree (is connected and doesn't have any simple cycles).
It is possible that for some numbers bi and bj, you will try to add the edge between them twice. Nevertheless, you will add this edge only once.

You can find an example below (the picture corresponding to the first test case).

Sequence (0,1,5,2,6) is not good as we cannot reach 1 from 5.

However, sequence (0,1,5,2) is good.

![pic](https://user-images.githubusercontent.com/44316768/190644391-aa9c0646-f3f5-40e0-bc46-e1e5171271a0.png)

You are given a sequence (a1,a2,…,an) of distinct non-negative integers. You would like to remove some of the elements (possibly none) to make the remaining sequence good. What is the minimum possible number of removals required to achieve this goal?

It can be shown that for any sequence, we can remove some number of elements, leaving at least 2, so that the remaining sequence is good.

Input
The first line contains a single integer n (2≤n≤200,000) — length of the sequence.

The second line contains n distinct non-negative integers a1,a2,…,an (0≤ai≤109) — the elements of the sequence.

Output
You should output exactly one integer — the minimum possible number of elements to remove in order to make the remaining sequence good.

## input
```
5
0 1 5 2 6
```

## output
```
1
```


## input
```
7
6 9 8 7 3 5 2
```

## output
```
2
```

## Note
Note that numbers which you remove don't impact the procedure of telling whether the resulting sequence is good.

It is possible that for some numbers bi and bj, you will try to add the edge between them twice. Nevertheless, you will add this edge only once.

