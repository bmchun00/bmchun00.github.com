---
title: One-way BFS
---

백준의 '특정 거리의 도시 찾기'문제.
각 노드가 단뱡향으로 연결되어있습니다.

```
from sys import stdin as s
from _collections import deque as d
n, m, k, x = map(int,s.readline().split())
l = {i:[] for i in range(1,n+1)}
for i in range(m):
    a,b = map(int, s.readline().split())
    l[a].append(b)
r=d()
done=set()
r.append((x,0))
c=0
res=[]
while r:
    p,dist=r.popleft()
    if dist>k:
        break
    if p not in done and dist==k:
        res.append(p)
    for i in l[p]:
        if i in done:
            continue
        r.append((i,dist+1))
    done.add(p)
if res:
    res.sort()
    for i in res:
        print(i)
else:
    print(-1)
```
