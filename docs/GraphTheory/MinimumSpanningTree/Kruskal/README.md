* [Upper Folder - 上一级目录](../../)
* [Source Code - 源码](https://github.com/zhaochenyou/Way-to-Algorithm/blob/master/src/GraphTheory/MinimumSpanningTree/Kruskal.hpp)
* [Test Code - 测试](https://github.com/zhaochenyou/Way-to-Algorithm/blob/master/src/GraphTheory/MinimumSpanningTree/Kruskal.cpp)

--------

### Kruskal
### Kruskal算法
<div>
问题：
<p id="i">用Kruskal算法求无向图\(G\)的最小生成树。</p>
解法：
<p id="i">Kruskal算法是一种贪心算法。初始时将图\(G\)的边集\(E\)按照权值，从小到大进行排序，并且生成树。从最小权值的边开始，依次考虑每一条边，对于边\(e_i\)来说，若将它加入生成树集合\(S\)中，\(e_i\)不会与\(S\)中已有的边形成环，那么选取边\(e_i\)作为生成树中的一条边，将其加入集合\(S\)；反之若将\(e_i\)加入\(S\)中会与已有的边形成环，则跳过\(e_i\)考虑下一个。</p>
<p id="i">这里对于环的判断，比较像<并查集>的算法思路：判断一条边\(e_i\)加入生成树集合\(S\)是否会出现回路，不需要在生成树集合\(S\)中判断回路是否存在（太过麻烦）。判断边\(e_i\)的两个端点\(v_1\)和\(v_2\)是否都属于集合\(S\)。若两个端点都属于集合\(S\)，则添加边\(e_i\)会使生成树中增加环，因此需要跳过该边。下图中红色的边已经加入生成树集合\(S\)中，节点\(v_2\)和\(v_3\)属于生成树集合\(S\)，因此边\(e_{2-3}\)加入生成树中会产生环：</p>
<p id="c"><></p>
</div>

<br>
