---
title: Statistical thinking for data science and analytics (2)
tag: 탐색적데이터분석
---

# 집합의 연산
집합은 일반적인 연산인 사칙연산같은 연산을 사용하지는 않지만, 부분집합, 삽입, 결합 등의 방법으로 연산을 할 수 있습니다.

**부분집합 (Subset)**

![](https://i.ibb.co/rGLx3KD/subset.jpg)

그림과 같이 A집합과 B집합이 있습니다. 이러한 상황에서 A의 요소는 A의 요소이기도 하지만 **동시에 B의 요소이기도 합니다.**
그러니까, **if x ∈ B, then x ∈ A** 라는 말이죠.
이것은 **B ⊆ A로 표현합니다.**
또한, **A ⊆ A and ∅ ⊆ A**가 가능하다는 것에 유의합시다.

**합집합/교집합 (Union/Intersection)**

![](https://i.ibb.co/1rqHth5/inter.jpg)

A와 B의 합집합은 A혹은 B에 있는 모든 요소를 포함하게 됩니다.
합집합은 **A ∪ B 로 표현하고, {xlx is an element of A OR x is an element of B}** 라고 작성합니다.

A와 B의 교집합은 A와 B 모두의 요소에 해당하는 요소만을 의미합니다.
교집합은 **A ∩ B 로 표현하고, {xlx is an element of A AND x is an element of B}** 라고 작성합니다.

**여집합 (Complement)**

![](https://i.ibb.co/ckp9z7d/comple.jpg)

A의 여집합은 A가 아닌 요소들을 선택하게 됩니다.
여집합은 **Ac(지수형 꼴을 표현하기 어려움)로 표현하고, {xlx ∈/ A}**라고 작성합니다.

그런데 이때, x ∈/ A인 요소들은 어디서 오는 걸까요? 보통은 전체 집합을 기준으로 생각합니다.

**전체 집합 (Universal set)** Ω로 표현하고, U로 쓰기도 합니다.

관심있는 모든 데이터를 포함하고 있는 집합입니다. 
따라서 **A ⊆ U, Ac ⊆ U, ∅ ⊆ U** 이러한 식이 성립합니다.

**차집합 (Set subtraction)**

![](https://i.ibb.co/Q8SxkyC/substrac.jpg)

그림의 경우를 보면, A에서 A이면서 B인 요소를 제거했습니다. 또한 이것은 **A이면서 B의 여집합의 교집합**이라고 생각할 수 있습니다.
차집합은 **A − B 혹은 A ∩ Bc**로 표현할 수 있습니다.
차집합은 특이한 케이스가 있는데, 생각해보면 어렵지 않는 항목들입니다.

**특이한 케이스**
* Ω − A = Ac
* A − ∅ = A
* A − A = ∅
* A − B = A − (A ∩ B)

# 다중 집합 연산
앞에서는 단순히 한개 혹은 두 개의 집합에서의 집합 연산을 알아보았는데, 이번에는 한번에 여러 개의(혹은 무한개가 될 수도) 집합을 연산하는 방법을 알아봅시다.
