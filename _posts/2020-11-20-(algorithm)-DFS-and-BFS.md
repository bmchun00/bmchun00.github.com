---
title: "(algorithm) DFS and BFS"
tags:
- algorithm
---

```
def dfs(tmplist):
    for i in sorted(tmplist):
        if i in done:
            continue
        done.add(i)
        print(i, end=" ")
        dfs(l[i])

    return None
n,m,c=map(int,input().split())
l={i:[] for i in range(1,n+1)}
for i in range(m):
    a,b=map(int,input().split())
    l[a].append(b)
    l[b].append(a)
stk=list()
stk.append(l[c])
done=set()
done.add(c)
print(c,end=" ")
dfs(l[c])
print()

done=set()
done.add(c)
print(c,end=' ')
while stk:
    t=stk.pop(0)
    for i in sorted(t):
        if i in done:
            continue
        stk.append(l[i])
        print(i,end=' ')
        done.add(i)
```
