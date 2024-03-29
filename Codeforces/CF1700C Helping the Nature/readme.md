# [CF1700C](https://codeforces.com/contest/1700/problem/C)

## tags
`constructive algorithms` `data structures` `greedy` `*1700`

## description
Little Leon lives in the forest. He has recently noticed that some trees near his favourite path are withering, while the other ones are overhydrated so he decided to learn how to control the level of the soil moisture to save the trees.

There are n trees growing near the path, the current levels of moisture of each tree are denoted by the array a1,a2,…,an. Leon has learned three abilities which will help him to dry and water the soil.

Choose a position i and decrease the level of moisture of the trees 1,2,…,i by 1.
Choose a position i and decrease the level of moisture of the trees i,i+1,…,n by 1.
Increase the level of moisture of all trees by 1.
Leon wants to know the minimum number of actions he needs to perform to make the moisture of each tree equal to 0.

Input
The first line contains a single integer t (1≤t≤2⋅104)  — the number of test cases. The description of t test cases follows.

The first line of each test case contains a single integer n (1≤n≤200000).

The second line of each test case contains n integers a1,a2,…,an (−109≤ai≤109) — the initial levels of trees moisture.

It is guaranteed that the sum of n over all test cases doesn't exceed 200000.

Output
For each test case output a single integer — the minimum number of actions. It can be shown that the answer exists.

## input
```
4
3
-2 -2 -2
3
10 4 7
4
4 -4 4 -4
5
1 -2 3 -4 5
```

## output
```
2
13
36
33
```

## Note
In the first test case it's enough to apply the operation of adding 1 to the whole array 2 times.

In the second test case you can apply the operation of decreasing 4 times on the prefix of length 3 and get an array 6,0,3.

After that apply the operation of decreasing 6 times on the prefix of length 1 and 3 times on the suffix of length 1. In total, the number of actions will be 4+6+3=13. It can be shown that it's impossible to perform less actions to get the required array, so the answer is 13.
