---
layout: posts
categories: python
title: Matplotlib画图
tags: python
---

{% hightlight python3 %}
#!/usr/bin/python3

import matplotlib.pyplot as plt


x = []

y = []


ReadFile = open('data.txt','r')

SepFile = ReadFile.read().split('\n')

ReadFile.close()



del SepFile[-1]  #不知道为什么列表末尾多了一个空格，删去



for Pairs in SepFile:

    XandY = Pairs.split(',')

    x.append(int(XandY[0]))

    y.append(int(XandY[1]))


plt.plot(x,y)


plt.title('date.file')

plt.xlabel('xlabel')

plt.ylabel('ylabel')


plt.show()

{% endhoghtlight %}
