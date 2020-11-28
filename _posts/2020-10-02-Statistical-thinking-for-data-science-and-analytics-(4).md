---
title: Statistical thinking for data science and analytics (4)
tag: 데이터와분석적사고
---

# 벡터의 방향
norm이 1인 벡터를 **unit vector**라고 합니다. 만약 ei가 유닛벡터라고 한다면, i번째 축에 대해 양수인 방향을 가지고 있습니다.        
모든 벡터는 ei의 선형 결합으로 나타낼 수 있는데, 이렇게 표현한다면 각 축이 벡터의 방향에 얼마나 기여하고 있는지 쉽게 볼 수 있습니다.   
예를 들면, v1 = (2, 1, 3)을 우리는 v1 = 2* e1 + e2 + 3* e3로 표현할 수 있고, v2 = (4, 2, 6)을 v2 = 4* e1 + 2* e2 + 6* e3로 표현할 수 있고, **2v1 = v2**임을 알 수 있습니다. 그러니까, 두 벡터는 같은 direction을 갖고, magnitude가 다르다는 것을 알 수 있습니다.

# 선형 결합(Linear Combination)
필드 F에 존재하는 벡터 공간 V가 있다고 가정합니다. v1, v2, v3 ... vn ∈ V 와 a1, a2, a3 ... an ∈ F가 있다면,  계수 an과 벡터 vn을 결합할 수 있습니다.    
**a1v1 + a2v2 + ... + anvn** 과 같은 꼴이 됩니다. 앞의 벡터 방향에서 단위벡터로 표현하는 방식도 마찬가지로 선형 결합입니다.

# 선형 독립
{v1, ... ,vn}의 벡터공간 V에 있는 벡터 집합과 요소에 0이 없는 스칼라 집합 {a1, ... ,an}을 선형 결합해    
 a1v1 + a2v2 + ... + anvn = 0을 만들 수 있다면, **선형 종속**이라고 합니다. 반대로 0을 만들 수 없다면 **선형 독립**입니다. 정의 자체는 이렇지만, 이해하는 데에는 어렵지 않습니다.    
 **예제**
 * {(1,1),(3,3)} 은 선형 종속입니다. 왜냐하면 (3,3) = 3(1,1)이기 때문입니다.
 * {(2,1,3),(1,0,0),(0,1,0),(0,0,1)}은 선형 종속입니다. 왜냐하면 (2,1,3)을 나머지 벡터로 표현할 수 있기 때문입니다.
 * {(0.5,3),(1,3),(1,-1)} 역시 선형 종속입니다. **2차원인데 반해 벡터집합의 요소는 3개나 있기 때문입니다.**

# 집합 요소가 선형 독립인지 확인
{ e1, e2, e3 }은 선형 독립입니다. 따라서 a1e1 + a2e2 + a3e3 = (0, 0, 0) 인 a1, a2, a3가 **(0, 0, 0)밖에 존재하지 않습니다.**    
(1, -1), (3, 2) 도 선형 독립입니다. a1(1, -1) + a2(3, 2) = (0, 0) 을 만족하는 (a1, a2)가 (0, 0)뿐입니다.        
(a1 + 3a2, -a1 + 2a2) = (0, 0)     
**a1 = -3a2 , a1 = 2a2. 0이 아닌 a1, a2는 모순입니다.**