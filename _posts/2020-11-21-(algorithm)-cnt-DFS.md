---
title: "(algorithm) cnt DFS"
tag: algorithm
---

백준의 '단지번호붙이기' 문제

```
import sys
sys.setrecursionlimit(10000)
def makezero():
    global cc
    while stk:
        pp = stk.pop()
        if int(mp[pp[0]][pp[1]])==0:
            return None
        else:
            cc+=1
            mp[pp[0]][pp[1]]=0
            if pp[0]<m-1:
                stk.append((pp[0]+1,pp[1]))
                makezero()
            if pp[1]<m-1:
                stk.append((pp[0],pp[1]+1))
                makezero()
            if pp[0]>0:
                stk.append((pp[0] - 1,pp[1]))
                makezero()
            if pp[1]>0:
                stk.append((pp[0],pp[1] - 1))
                makezero()
def checker():
    for i in mp:
        if '1' in i:
            return True
    return False
l=list()
m=int(input())
stk=list()
cc=0
cnt=0
mp=[0]*m
for j in range(m):
    mp[j]=list(input())
while checker():
    for q in range(m):
        for p in range(m):
            if int(mp[q][p])==1:
                stk.append((q, p))
                makezero()
                l.append(cc)
                cc=0
                cnt+=1
                break
print(cnt)
for i in sorted(l):
    print(i)

```
