---
title: "(algorithm) maze BFS"
tags:
- algorithm
---

BFS의 최단거리 탐색을 이용한 미로찾기

```
n,m=map(int,input().split())
l= [[] for i in range(n)]
for i in range(n):
    l[i] = list(input())
stk=[]
stk.append((0,0,1))
done=set()
case=[]
while stk:
    t=stk.pop(0)
    x=t[0]
    y=t[1]
    if x==n-1 and y==m-1:
        case.append(t[2])
        continue
    elif x>=0 and y>=0 and x<=n-1 and y<=m-1:
        if l[x][y]=='1' and (x,y) not in done:
            done.add((x, y))
            stk.append((x + 1, y, t[2] + 1))
            stk.append((x - 1, y, t[2] + 1))
            stk.append((x, y + 1, t[2] + 1))
            stk.append((x, y - 1, t[2] + 1))

print(min(case))
```
