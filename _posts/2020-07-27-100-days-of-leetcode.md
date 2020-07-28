---
title: "100 Days of LeetCode"
date: 2020-07-27
categories: en

header:
  image: /assets/img/2020-07-27-100-days-of-leetcode/1.png
classes:
  - wide
---

Writing down this article while listening to some Mandopop 「夜長夢少」 by 傻子與白癡.

On Feb 25, 2020, I gave myself a challenge: doing 100 days of LeetCode questions. It's not like I'm preparing for an interview to get me a new job, I just wanted to refresh my memories (both brain and muscle) solving algorithm questions. You know, working as a software engineer, no matter how many years of experience you may have resolving actual engineering problems, you may get rejected if you don't know how to invert a binary tree or reverse a linked list. So... always good to know how to solve at least the basic algorithm questions.

To formalize this challenge (at least for myself), I made myself several rules:

- everyday, solve 1-3 easy problem(s), or 1-2 medium problem(s), or 1 hard problem;
- a LeetCode weekly contest counts as one day, if I'm unable to solve any of the problems in a contest, that day is marked as fail;
- the real important thing is about understanding the solution of a problem, even an easy one, not memorizing the code that solves the problem;

And to keep a record of the problem(s) I solve everyday, I created a Google Sheet (the one in the header), I try to categorize the problems and keep some notes, which turned out to be no more than something that boosts my confidence: "Hey, look at this long list, I've solved so many problems so many times!" Oh, also speaking from a former data scientist's perspective, that's some rich data I can perform some analysis of myself later.

So I started my first day with a hard problem - [Word Break II](https://leetcode.com/problems/word-break-ii/). I couldn't really remember how long it took me to solve the problem, I ended up reading the discussions and learned the DP solution in one of the most upvoted thread. Oh, and why a hard DP to kick off the challenge? I don't know, just feel like solving a lot of DPs. I heard a lot that you have to solve a lot of DPs before you really understanding how DP works, which I learned after the 100 days challenge, that is true, a constant boolean `true`. Even as today, having solved dozens of DP problems, I still can't solve half of them giving my first try.

There were many types of problems, I tried to solve as many types of problems while trying to get a rather deep understanding of them as much as possible. There are a lot of DPs, then comes many tree / graph problems, then maybe string / array / linked list problems. Out of all categories of problems, I really enjoy the tree / graph problems, they may seem difficult and complex at first, but usually ends up with a really elegant and concise solution in the form of recursion. For example, [Linked List in Binary Tree](https://leetcode.com/problems/linked-list-in-binary-tree/):

```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def isSubPath(self, head: ListNode, root: TreeNode) -> bool:
        if not head:
            return True
        if not root:
            return False

        return self.dfs(head, root) or\
               self.isSubPath(head, root.left) or\
               self.isSubPath(head, root.right)

    def dfs(self, head: ListNode, root: TreeNode) -> bool:
        if not head:
            return True
        if not root:
            return False

        return (head.val == root.val) and\
               (
                    self.dfs(head.next, root.left) or\
                    self.dfs(head.next, root.right)
               )
```

Oh I love them, so beautiful in any language.

Also, gotta admire [lee215](https://www.youtube.com/channel/UCUBt1TDQTl1atYsscVoUzoQ) and [花花酱](https://www.youtube.com/channel/UC5xDNEcvb1vgw3lE21Ack2Q) for their awesome solutions and videos, helped me a looooooooooooooooooot.

Besides the regular daily problems, I also did quite a few weekly contests. Contest can be reaaaaally interesting sometimes, as it forces you to do your best in 90 minutes solving typically 1 easy, 2 medium, and 1 hard problems. I usually solve 3 problems and get a top 20% - 40% score. Hard problems can be extra hard if it's the first time you see it. I've only solved hard problems 2 or 3 times. Here are some screenshot of my best scores.

![2](/assets/img/2020-07-27-100-days-of-leetcode/2.png)

![3](/assets/img/2020-07-27-100-days-of-leetcode/3.png)

And finally, did I complete the challenge?

No, I failed.

I had a fight with my wife and I couldn't get myself to LeetCode for 2 days, so 98/100, not bad! I'm satisfied.

I may have this challenge again sometime and the end of this year or next year. Before that, I want to write some actual engineering code, lol.

BTW, typing on my MSI GP62MVR feels so much better than on the MBP15 2018, even though I have 3 keys broken and remapped...
