---
title: Statistical thinking for data science and analytics (5)
---

데이터들은 보통 stack되는 구조로 저장됩니다. 이러한 구조를 Matrix(행렬)라고 하는데, 이번에는 행렬의 특성과 연산 방법에 대해서 알아보도록 하겠습니다.

# Matrix
n row와 p columns를 가지는 행렬의 dimension(차원)은 **n × p 혹은 n by p** 라고 합니다.    
마찬가지로 데이터 행렬에서, j 번째 column은  j번째 줄의 요소를 뜻하고, i 번째 row는 i번째 줄의 요소를 뜻합니다.

n by p의 행렬인 X가 있다고 생각하면,
* 이 행렬은 np개의 요소를 가지고 있습니다.
* i번째 행, j번째 열에 해당하는 요소를 Xij 혹은 (X)ij와 같은 형태로 작성합니다.

**또한 Μn* p 라고 한다면, n by p인 모든 행렬의 집합을 의미합니다.**

# Special cases of matrices
Matrix도 벡터의 unit vector처럼, 특이한 경우가 존재합니다.
* **Square matrix(정방 행렬)** : 행렬의 row와 column의 개수가 같을 때. 2 by 2 행렬 등
*  **Column matrix(열 행렬)** : n by 1 차원을 갖는 행렬
*  **Row matrix(행 행렬)** : 1 by n 차원을 갖는 행렬
* **Diagonal matrix(대각 행렬)** : 대각선의 요소를 제외하고 모두 0을 갖는 행렬. 당연히 **정방 행렬의 일종입니다.**    
![](https://i.ibb.co/pXhFBsH/dg.jpg)
* **Identity matrix(단위 행렬)** : 대각 행렬에서 대각선의 요소가 모두 1인 행렬. **정방 행렬이면서 대각 행렬입니다.**    
![](https://i.ibb.co/cbTYfjm/id.jpg)

# Matrix Calculations
* Addition : **같은 차원의 행렬끼리 가능한 연산으로,** A + B는 다음과 같이 정의됩니다.    
![](https://i.ibb.co/x35nKkR/a-b.jpg)    
**행렬의 덧셈은 요소별로 정의됩니다.**
* Scalar multiplication : Matrix A와 scalar c가 있다고 할때, 스칼라 곱 cA는 다음과 같이 정의됩니다.    
![](https://i.ibb.co/bbZHV4R/scm.jpg)    
**스칼라 곱은 요소별로 정의됩니다.** 만약 이 두가지의 연산이 정의되었을 때, 이것은 벡터 스페이스인가요? 벡터 스페이스면 이 두가지 연산으로 8가지의 공리를 만족해야 합니다.  모든 공리를 만족하므로, 이러한 행렬로 이루어진 공간 역시 **벡터 공간이라고 할 수 있습니다.**
* Matrix multiplication : Matrix A와 B가 있을때 A와 B의 벡터곱 AB는 다음과 같이 정의합니다.    
![](https://i.ibb.co/TLzgDWT/mm.jpg)     
식으로 굉장히 어렵게 쓰여 있지만, 행렬곱은 이전에도 자주 다뤘던 내용이므로 이해하는 데 크게 어렵지 않습니다. 우리가 알 수 있듯이 행렬곱을 하면 행렬의 **차원이 변할 수 있습니다.** 만약 i by j 인 행렬 A와 k by l 인 행렬 B이 있다면 그것의 행렬곱 A * B는 i by l 차원을 가집니다.     
또한 A1, A2와 B1, B2의 행렬곱은 다음 두 가지의 법칙을 만족합니다. A1, A2와 B1, B2의 차원은 다릅니다.   
* (A1+A2)* B1 = A1B1 + A2B2
* (A1+A2)(B1+B2) = A1B1 + A2B1 + A1B2 + A2B2

그런데 **AB = BA는 성립할까요?** 그렇지 않습니다.   
만약 A가 열벡터(n by 1)이고 B가 행벡터(1 by n)이면, AB는 n by n의 행렬일 것이고, BA는 1 by 1의 행렬일 것이기 때문입니다.
