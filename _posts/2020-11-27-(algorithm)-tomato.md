---
title: "(algorithm) tomato"
tags:
- algorithm
---

백준의 '토마토'문제
```
from _collections import deque

def findto():
    for i in range(n):
        for j in range(m):
            if l[i][j]==1:
                onelist.append((i,j))
    return False
def isalltwo():
    for i in range(n):
        if 0 in l[i]:
            return True
    return False

m,n=map(int,input().split())
l= [[] for i in range(n)]
for i in range(n):
    l[i] = list(map(int,input().split()))
stk=deque([])
onelist=[]
findto()
case=[]
for i in onelist:
    stk.append(i)
    l[i[0]][i[1]]=0
cnt=-1
while isalltwo():
    cnt += 1
    ck=True
    for i in range(len(stk)):
        t = stk.popleft()
        x = t[0]
        y = t[1]
        if not ((x >= 0 and y >= 0) and (x <= n - 1 and y <= m - 1)):
            continue
        elif l[x][y] == -1 or l[x][y] == 2:
            continue
        else:
            l[x][y] = 2
            ck=False
            stk.append((x + 1, y))
            stk.append((x - 1, y))
            stk.append((x, y + 1))
            stk.append((x, y - 1))
    if ck:
        cnt=-1
        break
print(cnt)
```
