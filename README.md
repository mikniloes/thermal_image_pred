# thermal_image_pred
### 열화상 이미지를 이용한 체온 예측
![image](https://user-images.githubusercontent.com/84064361/120269715-5424e180-c2e3-11eb-8e6f-ec1e314d3e1a.png)

#### 1. json 데이터 전처리
* nested json 파일을 데이터프레임(csv) 형식으로 변형
* unicode 포함 데이터 디코딩 
#### 2. scikitlearn random forest 회귀 모델을 사용한 예측
* 범주형 데이터 one-hot 인코딩
* 결측/중복 제거
* scikitlearn의 random forest regressor로 학습


![스크린샷 2021-06-01 오후 12 23 15](https://user-images.githubusercontent.com/84064361/120262114-3b60ff80-c2d4-11eb-8116-098d2b65fe91.png)
