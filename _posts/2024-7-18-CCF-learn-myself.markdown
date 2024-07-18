---
layout:     post
title:      "CCF自学日记"
date:       2024-07-13
author:     "黄昏"
catalog: true
tags:
  - c++
  - 被夹
---

#1.1模块化编程
---
'''cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    int x1, y1, x2, y2;
    cin>>x1>>y1>>x2>>y2;
    printf("%d\n", abs(x1-x2)+abs(y1-y2));
    return 0;
} 

//计算两点的曼哈顿距离
'''
这是一个通过外置函数计算曼哈顿距离的代码，那么，我们要怎么知道其中的原理呢？
首先，我们知道，曼哈顿函数其实就是|x1-x2|+|y1-y2|，那么自定义模块函数就好写了！
'''cpp
#include <iostream>
using namespace std;

int abs(int x) {
    return x > 0? x : -x;
}

int main() {
    int x1, y1, x2, y2;
    scanf("%d%d%d%d", &x1, &y1, &x2, &y2);
    printf("%d\n", abs(x1-x2)+abs(y1-y2));
    return 0;
} 

'''
---
总结：自定义模块化函数
