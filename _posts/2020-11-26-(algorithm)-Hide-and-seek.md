---
title: "(algorithm) Hide and seek"
tag: algorithm
---

백준의 '숨바꼭질' 문제
```
from _collections import deque
n,k=map(int,input().split())
que = deque()
vis = [False]*1000001
que.append((n,0))
while que:
    t=que.popleft()
    vis[t[0]]=True
    if t[0]==k:
        print(t[1])
        break
    for i in [t[0] - 1, t[0] + 1, t[0] * 2]:
        if i<0 or i>1000000 or vis[i]:
            continue
        else:
            que.append((i, t[1] + 1))
```
