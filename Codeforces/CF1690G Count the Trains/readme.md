# [CF1690G](https://codeforces.com/contest/1690/problem/G)

## tags
`binary search` `data structures` `greedy` `sortings` `*2000`

## description
There are n of independent carriages on the rails. The carriages are numbered from left to right from 1 to n. The carriages are not connected to each other. The carriages move to the left, so that the carriage with number 1 moves ahead of all of them.

The i-th carriage has its own engine, which can accelerate the carriage to ai km/h, but the carriage cannot go faster than the carriage in front of it. See example for explanation.

All carriages start moving to the left at the same time, and they naturally form trains. We will call trains — consecutive moving carriages having the same speed.

For example, we have n=5 carriages and array a=[10,13,5,2,6]. Then the final speeds of the carriages will be [10,10,5,2,2]. Respectively, 3 of the train will be formed.

There are also messages saying that some engine has been corrupted:

message "k d" means that the speed of the k-th carriage has decreased by d (that is, there has been a change in the maximum speed of the carriage ak=ak−d).
Messages arrive sequentially, the processing of the next message takes into account the changes from all previous messages.

After each message determine the number of formed trains.

Input
The first line of input data contains a single integer t (1≤t≤104) —the number of input test cases.

This is followed by descriptions of the test cases.

The first line of each test case is empty.

The second line of the test case contains two integers n and m (1≤n,m≤105) —the number of carriages and the number of messages to slow down the carriage, respectively.

The third line contains n integers: a1,a2,…,an (0≤ai≤109) — the number ai means that the carriage with number i can reach a speed of ai km/h.

The next m lines contain two integers kj and dj (1≤kj≤n, 0≤dj≤akj) —this is the message that the speed of the carriage with number kj has decreased by dj. In other words, there has been a change in its maximum speed akj=akj−dj. Note that at any time the speed of each carriage is non-negative. In other words, ai≥si, where si —is the sum of such dj that kj=i.

It is guaranteed that the sum of n over all test cases does not exceed 105. Similarly, it is guaranteed that the sum of m over all test cases does not exceed 105.

Output
Print t lines. On each line print the answer for the corresponding test case.

For each test case print m numbers: the number of trains formed after each message.

## input
```
3

4 2
6 2 3 7
3 2
4 7

5 4
10 13 5 2 6
2 4
5 2
1 5
3 2

13 4
769 514 336 173 181 373 519 338 985 709 729 702 168
12 581
6 222
7 233
5 117
```

## output
```
3 4 
4 4 2 3 
5 6 6 5 
```

## Note
For the first test case:

Initially array a=[6,2,3,7].
After the first message, the array a=[6,2,1,7]. Accordingly, the speeds of the carriages are [6,2,1,1] and will form 3 of the train.
After the second message the array a=[6,2,1,0]. Accordingly, the speeds of the carriages are [6,2,1,0], and 4 of the train will be formed.
For the second test case:

Initially, the array a=[10,13,5,2,6].
After the first message, the array a=[10,9,5,2,6]. Accordingly, the speeds of the carriages are equal: [10,9,5,2,2], and 4 of the train will be formed.
After the second message the array a=[10,9,5,2,4]. Accordingly, the speeds of the carriages are [10,9,5,2,2], and 4 of the train will be formed.
After the third message the array a=[5,9,5,2,4]. Accordingly, the speeds of the carriages are [5,5,5,2,2], and 2 of the train will be formed.
After the fourth message the array a=[5,9,3,2,4]. Accordingly, the speeds of the carriages are [5,5,3,2,2], and 3 of the train will be formed.



