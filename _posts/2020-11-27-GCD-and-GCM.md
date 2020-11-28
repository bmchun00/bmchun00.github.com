---
title: GCD and GCM
---

```
def GCD(x,y):
    while y!=0:
        x,y=y,x%y
    return x

def GCM(x,y):
    res=(x*y)//GCD(x,y)
    return res

print(GCD(12,16))
print(GCM(12,16))
```
