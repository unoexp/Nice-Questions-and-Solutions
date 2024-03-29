有n个节点, 每个节点为一个数字, 每个节点向其他所有节点中xor值最小的节点连一条边, 问最少去掉多少个节点就可以形成一棵树.

首先, 每个点都必会往外连一条边, 但是不可能形成环, 因为a如果向b连边, b又向c连边, 说明a^b>b^c, 如果c向a连边, 说明b^c>c^a, 此时有a^b>c^a, 那a为什么一开始不向c连边呢, 于是产生了矛盾. 

所以所有n个点的边数就是<n的, 运气好的话直接就是一棵树. 如果不是一棵树, 那么剩下的可能是很多棵树, 树与树是不连通的, 什么样的数字会产生这种情况呢? 

首先, 只有两个二进制位一样, 他们的xor才会最小(0), 假设我们考虑最高的一位二进制, n个数中有n-2个该位都是0, 有2个该位为1, 我们分别把他们放入集合a和集合b, 我们可以发现, a集合的元素不可能向b集合连边, 为什么呢? 因为要保证xor最小, 那么该位最好的情况肯定是0, 我们发现集合a和集合b的元素都可以和自身集合中的其他元素异或来得到0, 所以每个集合只可能与自身集合中的元素连边. 但如果a集合只有一个元素, 那么他就只能与b集合的元素连边了, 因为a集合没有其他元素了. 所以当我们按第i位二进制的0/1分出两个集合时, 我们可以从任意一个集合保留一个元素, 然后求另一个集合中能保留的最多元素就好了. 

当一个集合为空时, 我们直接选择下一个i继续划分就好了.

