---
title: "Goodbye, PyCharm"
date: 2019-04-19
categories: code

classes:
  - wide
---

I've used PyCharm as my daily IDE extensively for quite some time, and now finally I can say goodbye to it.

To begin with, I like PyCharm, it's a fantastic IDE for Python developers. It was one of the most popular and powerful IDEs in the past and it still is, if not the best. Its simple user interface and powerful reference, debugger tools make writing Python codes so smooth. And since all JetBrain's IDEs share basically the same interface, it is easy to adopt JB's IDEs of other languages. I've also used GoLand and IntelliJ IDEA, and they are fantastic as well.

However, despite how powerful PyCharm is, it has one major drawback for me: the start-up time is too slow! Every time I start the IDE, the background tasks would seem to run forever to index. And while it's indexing, a lot of RAM will be consumed, and I can hear my fans making noise. It is fine for a workstation or a powerful laptop (although still takes some time and RAM), but probably a bit too much for older ones. I have a 2011 Macbook Air that is still perfect for lightweight tasks and general usage, but every time I boot up PyCharm it's actually like opening XCode, the laptop becomes slower and battery running out faster. There are also other problems I encountered but not as critical, e.g. running program in PyCharm is a bit slower than running in terminal. I don't know if it is because of PyCharms running on JVM.

![pycharm-indexing](/assets/img/2019-04-19-goodbye-pycharm/pycharm-indexing.png)

Though the problem is there, I didn't have any other alternatives that are as simple and powerful as PyCharm, until I meet VSCode... It is powerful, lightweight, cross-platform, almost-all-language-supported, free... So many great stuff... Anyway, figuring out all the settings and configurations in VSCode can be painful, especially if doing it the first time, but once figured out, it'd be hard to go back. I can do almost anything I can do in PyCharm and it doesn't need to index at start-up! And there are so many extensions to make your life easier. One extension actually made me decide to write this article, which is:

![dracula-python](/assets/img/2019-04-19-goodbye-pycharm/dracula.png)

Personally, PyCharm's Dracula theme is one of my favorite things of PyCharm, much better than the default code theme in VSCode. Now I can have PyCharm's color theme working in VSCode, isn't that awesome? The binary search code below is showing in VSCode.

![sample-code](/assets/img/2019-04-19-goodbye-pycharm/sample-code.png)

Now I basically use VSCode for all my projects of all languages. Until there will be a even greater IDE than VSCode, there's no going back to PyCharm.

You have made me a better coder. Thank you, JetBrains. Thank you, PyCharm.