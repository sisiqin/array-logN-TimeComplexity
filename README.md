# 这里总结几道array通过每次减掉一般的规模来优化时间复杂度的题

这些array的题，暴力解法都是o(n) 或者o(nlogn)。那么要优化它们，就只能是：

  - 对于暴力解法是o(n)的，往o(logn)上走 ：在o(1) 的时间内，把规模为T(n)的问题变成规模为T(n/2)的问题

  - 对于暴力解法是o(nlogn)的，往o(n)上走： 在o(n)的时间内，把规模为T(n)的问题变成规模为T(n/2)的问题  <-- 注意此时时间复杂度仍然是o(n)

那要怎么变呢？ **扔一半array** 

## 相关题目

1. kth largest element/median in an unsorted array 
https://repl.it/@sisi/215m-Kth-Largest-Element-in-an-Array

  这道题用到了quick select, 每次partition完后判断target在左边还是右边还是中间，然后扔掉不要的那一半

2. kth largest element/median of 2 sorted array

  这道题的思路很牛逼，是在a,b两个array中都取index 为k/2的那个点，比一下大小，谁小扔掉谁前面那段。也达到了规模减半的目的


