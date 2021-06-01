# thermal_image_pred
### 열화상 이미지를 이용한 체온 예측
![image](https://user-images.githubusercontent.com/84064361/120269715-5424e180-c2e3-11eb-8e6f-ec1e314d3e1a.png)

#### 1. json 데이터 전처리
* nested json 파일을 데이터프레임(csv) 형식으로 변형
```
from pandas.io.json import json_normalize

pandas.io.json.json_normalize(data, record_path=None, meta=None,...)
```
* unicode 포함 문자열 데이터 디코딩 

![image](https://user-images.githubusercontent.com/84064361/120269912-a534d580-c2e3-11eb-8696-96aadaed091b.png)

#### 2. scikitlearn random forest 회귀 모델을 사용한 예측
* 범주형 데이터 one-hot 인코딩
* 결측/중복 제거
* scikitlearn의 random forest regressor로 학습
* 모델의 feature 중요도 확인
```
featureImportance = model.feature_importances_
```

![image](https://user-images.githubusercontent.com/84064361/120270921-4cfed300-c2e5-11eb-8c80-0f4239014a2f.png)


