# [CF1478E Nezzar and Binary String](https://codeforces.com/contest/1478/problem/E)

## tags
`data structures` `greedy` `*1900`

## description

Nezzar has a binary string s of length n that he wants to share with his best friend, Nanako. Nanako will spend q days inspecting the binary string. At the same time, Nezzar wants to change the string s into string f during these q days, because it looks better.

It is known that Nanako loves consistency so much. On the i-th day, Nanako will inspect a segment of string s from position li to position ri inclusive. If the segment contains both characters '0' and '1', Nanako becomes unhappy and throws away the string.

After this inspection, at the i-th night, Nezzar can secretly change strictly less than half of the characters in the segment from li to ri inclusive, otherwise the change will be too obvious.

Now Nezzar wonders, if it is possible to avoid Nanako being unhappy and at the same time have the string become equal to the string f at the end of these q days and nights.

Input
The first line contains a single integer t (1≤t≤2⋅105) — the number of test cases.

The first line of each test case contains two integers n,q (1≤n≤2⋅105, 0≤q≤2⋅105).

The second line of each test case contains a binary string s of length n.

The third line of each test case contains a binary string f of length n.

Then q lines follow, i-th of them contains two integers li,ri (1≤li≤ri≤n)  — bounds of the segment, that Nanako will inspect on the i-th day.

It is guaranteed that the sum of n for all test cases doesn't exceed 2⋅105, and the sum of q for all test cases doesn't exceed 2⋅105.

Output
For each test case, print "YES" on the single line if it is possible to avoid Nanako being unhappy and have the string f at the end of q days and nights. Otherwise, print "NO".

You can print each letter in any case (upper or lower).

## input
```
4
5 2
00000
00111
1 5
1 3
2 1
00
01
1 2
10 6
1111111111
0110001110
1 10
5 9
7 10
1 7
3 5
6 10
5 2
10000
11000
2 5
1 3
```

## output
```
YES
NO
YES
NO
```


## Note
In the first test case, 00000––––––→000––––11→00111 is one of the possible sequences of string changes.

In the second test case, it can be shown that it is impossible to have the string f at the end.

