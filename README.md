# Chinese_chess_AI
人工智能，中国象棋，人际博弈

# 第一次提交：
实现基本的象棋功能
# 第二次提交：
实现一步象棋人工智能。

方式：
计算局面分，认为
将：2000分
车：100分
炮：50分
马：50分
兵：20分
士：10分
象：10分

（电脑走黑棋）
等到电脑走时，电脑尝试这一步的所有可能的走法。每一种走法，电脑记录
自己黑棋的分数 blackTotalScore=所有活着的黑棋分数的和，
红棋的分数 redTotalScore=所有活着的红棋分数的和
那么局面分 score = blackTotalScore - redTotalScore
然后选取所有走法中，局面分最大的那种走法。

```cpp
if(score>maxScore)
{
    maxScore=score;
    ret=step;
}
return ret;
```
![enter description here][1]
# 第三次提交：
1. 修改程序中bug，防止<Step*> steps内存泄漏，所以使用完steps中的某一元素时，如果不在使用，就将其delete掉。
2. 用最大最小值算法，实现两步的象棋人工智能
比如小偷偷了一堆东西，你要和他分赃，小偷让你选一个袋子，然后小偷从这个袋子中选择一个东西给你。现在有3个袋子，每个袋子有两件物品，价格分别为
![enter description here][2]
很显然，因为为了防止小偷坑你，你应该选择第二个袋子。得到的最好的结果为20. 这就是最大最小值算法。
推广到象棋博弈中：
电脑走一步后，就是人来走。为了防止在人走的时候坑电脑。
    
![enter description here][3]


  [1]: ./images/1.png "1.png"
  [2]: ./images/2.png "2.png"
  [3]: ./images/3.png "3.png"