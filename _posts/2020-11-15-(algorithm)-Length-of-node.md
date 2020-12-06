---
title: "(algorithm) Length of node"
tag: algorithm
---

연결된 노드의 개수를 구하는 기본적인 문제

```
n=int(input())
m=int(input())
l={i:[] for i in range(1,n+1)}
for i in range(m):
    a,b=map(int,input().split())
    l[a].append(b)
    l[b].append(a)
stk=list()
stk.append(l[1])
done=set()
done.add(1)
while stk:
    t=stk.pop()
    for i in t:
        if i in done:
            continue
        stk.append(l[i])
        done.add(i)
print(len(done)-1)
```
