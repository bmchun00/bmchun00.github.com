---
title: GIS1 정의
---

**1. GIS**   
컴퓨터를 이용하여 지표상에 다양한 지리정보를 종합적으로 처리하는 시스템.   
지표면에 다양한 지리 자료들을 그들 특성에 따른 공간적 위치에 맞추어 수집, 입력, 저장, 관리, 조작, 분석, 모형화를 표시할 수 있는 종합정보처리 시스템이다.

**2. Data vs. Information**   
Data : 직접적인 관찰이나 측량을 통해 얻은 자료   
Information : Data가 어떠한 의미 있는 과정에 의해 해석될 때 Information이 된다. 이 과정은 사람이나 목적에 따라 달라질 수 있다.

**3. Spatial Resolution**  
공간 해상도는 디지털 이미지 구축에 사용되는 픽셀 수를 가리키는 용어입니다. Spatial Resolution이 높은 영상은 Spatial Resolution이 낮은 영상보다 픽셀 수가 더 많습니다.

**4. Discrete Object View**   
기본적으로 세계는 비어 있다고 가정합니다. 뚜렷한 경계를 가진 객체를 포함합니다.      
각 개체는 셀 수 있습니다.     
개체에는 차원이 있고, 0차원 (점) 1차원(선) 2차원(면) 입니다.   

**5. Continuous Field View**   
한정적인 개수의 변수로 실세계를 표현합니다. 변수들은 각각의 위치에 정의되어 있습니다.    
값의 변화에 따라 구별될 수 있고, 얼마나 부드럽게 변하는지에 따라서도 구별될 수 있습니다.   

**6. Five methods to classify quantitative values in Continuous Fields**   
Nominal : 도면의 요소를 식별합니다. 산술 연산이 없습니다.   
Ordinal : 순서를 가집니다. 평균과 덧셈 등의 연산은 없지만, 중간값을 구할 수 있습니다.   
Interval : 값의 차이가 존재합니다.   
Ratio : 값 간의 비율이 존재합니다. 0은 없음을 뜻합니다.   
Cyclic : 순환하는 값입니다.   

**7. Raster vs. Vector Data**   
Raster : 정사각형인 셀(픽셀)의 배열로 표현합니다. 속성들에 대한 값을 각 셀에 직접 넣습니다.    
Vector : 점, 선, 면의 형태로 표현합니다.   
Raster는 셀의 크기가 작아질수록 용량은 커집니다.   
Raster는 주로 원격 탐사를 통한 영상으로부터 얻어지고,   
Vector는 인구 등의 행정 데이터를 이용합니다.   

**8. Paper Map vs. Digital Map**   
Digital Map은 디지털화나 스캔을 통해 데이터로 변화합니다. 종이 지도에 비해 데이터의 수정이 용이하며, 2차원으로 제한된 종이지도에 비해 3차원으로도 표현할 수 있습니다.

**9. Orthometric Height**   
"정표고(Orthometric Height)"는 일반적으로 평균해수면 고도로 나타내는 지오이드를 기준으로 한 특정 지점의 높이를 말합니다.

**10. Map Projection**   
지도를 만들기 위해서는 지구를 2차원으로 투영해야 합니다. 이러한 투영 과정을 Map Projection이라고 합니다. 지도 투영에는 여러 방법이 있고, 각각 모양, 면적, 거리, 방향의 왜곡을 최소화하는 방향으로 지도를 만듭니다.

**11. Map Scale**   
지도와 실제 세계 사이의 비율입니다. Map Scale을 나타내는 방법은 여러가지가 있습니다. Bar Scale을 출력할 때에는 오차가 바뀌는 경우가 없습니다.

**12. Large scale vs. small scale map**   
축척이 1:10000보다 크면 대축척, 1:300000보다 작으면 소축척입니다. 대축척 지도는 좁은 지역을 자세히 표현할 수 있고, 소축척은 넓은 지역을 간단히 표현할 수 있습니다.

**13. Reference map vs. Thematic map**   

**14. Unique Identifier**   
GIS data의 각 테이블에는 각 투플을 고유하게 식별할 수 있는 필드가 있어야 지리 데이터와 속성 데이터를 연결할 수 있습니다. 지리 데이터를 속성 데이터에 할당 및 연결해주는 것을 Unique Identifier라고 합니다.

**15. Simple Join**

**16. Summarized Join**

추가)

**17. Representation**   
정보를 전달하기 위해 필요합니다. 정보를 표준 양식에 맞추는 과정을 의미합니다.

**18. Generalization**   
데이터의 모든 것을 표현하는 것은 한계가 있기 때문에, 데이터를 간단하게 표현해 정보를 더 효율적으로 얻을 수 있도록 합니다.
