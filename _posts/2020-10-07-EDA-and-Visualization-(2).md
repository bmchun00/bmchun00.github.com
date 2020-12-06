---
title: 탐색적 데이터 분석
tag: R데이터분석
---

# 유클리디안 거리 구하기 (for문 이용)
**소스 코드**
```
set.seed(1)
n = nrow(iris)
ind = sample(1:n, size = floor(0.7*n))
X = as.matrix(iris[ind,1:4])
y = iris[ind,5]
X_new = as.matrix(iris[-ind,1:4])

s <- Sys.time()
Euclidean <- function(x,y)
{
  return(sqrt(sum((x-y)^2)))
}
ind <- c()
tmp <- c()
for(i in 1:length(X_new[,1]))
{
  tmp = 0
  for(j in 1:length(X[,1]))
  {
    tmp[j] <- Euclidean(X_new[i,],X[j,])
  }
  ind[i] <- which.min(tmp)
}
ind
e <- Sys.time()
e-s
```
행렬에 있는 각 행들을 이용해 유클리디안 거리를 구하고, 가장 작은 값을 가지는 위치를 tmp 변수에 넣습니다. X_new의 차원이 45 by 4 이므로, 45개의 값이 tmp에 들어갑니다. 

**실행 결과**
```
[1]  59  59  25  33  37  28  16  41  71  44  46  44  27  28  33  93  55  82  74  96  12
[22]  60  93   6  86 102  55  55  22  19  53  85  18   6   2  32  65  17  34  39   2  32
[43]  65 103  95

Time difference of 0.4783821 secs
```
# 유클리디안 거리 구하기 (apply 이용)
**소스 코드**
```
set.seed(1)
n = nrow(iris)
ind = sample(1:n, size = floor(0.7*n))
X = as.matrix(iris[ind,1:4])
y = iris[ind,5]
X_new = as.matrix(iris[-ind,1:4])

s <- Sys.time()
tmp <- c()
for(i in 1:length(X_new[,1]))
  tmp[i] <- which.min(sqrt(apply(t(t(X)-X_new[i,])^2,1,sum)))
tmp
e <- Sys.time()
e-s
```
동일한 문제를 apply를 이용해 구현했습니다. 직관적이지는 않지만 실행 속도가 유의미하게 빠르고, 차지하는 공간도 줄었을 뿐더러 코드의 길이도 짧습니다.

**실행 결과**
```
 [1]  59  59  25  33  37  28  16  41  71  44  46  44  27  28  33  93  55  82  74  96  12
[22]  60  93   6  86 102  55  55  22  19  53  85  18   6   2  32  65  17  34  39   2  32
[43]  65 103  95

Time difference of 0.1595731 secs
```
