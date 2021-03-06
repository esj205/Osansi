# COMPAS 주관 오산시 어린이 교통사고 위험지역 예측 프로젝트
도로정보, 인구 통계량, 어린이 관련 양적 변수 등을 통해 오산시의 어린이 교통사고 위험지역을 예측하는 프로젝트를 진행하였다.
## 분석 목적
- 다양한 데이터를 융합 및 활용하여 어린이 교통사고 위험 지역 예측
- 이를 통해 주정차 단속 강화 등 어린이 보호를 위한 다양한 정책 수립 및 추진

------------

## 해결 과제
1. 어린이 보호구역 외 어린이 교통사고 위험지역 20개소 제시
2. 기존 어린이 보호구역 중 교통사고 안전시설물 우선 설치 지역 20개소 제시

------------

## 분석 과정
### 1. 데이터 전처리
1. 데이터 선정
2. 결측치 및 무관한 정보 처리
3. 격자에 정보 할당
4. 데이터 통합
5. 추가 정제

### 2. EDA
1. 정제된 데이터를 이용하여 시각화
2. 어린이 보호구역 / 어린이 보호구역 외 비교
3. 분석 Insight 도출


### 3. 모델 선정 및 분석
1. 분석 모델 선정 및 모델링
- Geographically Weighted Regression
- Random Forest
- Light GBM
2. 위험도 지수 산출
3. 위험지역 선정

------------
## 결과

위험도 지수를 기준으로 어린이 보호구역과 외 구역 상위 20개 지역 선정

### 위험도 지도 제작
![위험지역_nochild](https://user-images.githubusercontent.com/55840722/116553323-f7758600-a934-11eb-94d1-3a78316af3a9.png)


### 어린이 보호구역 내 20개소
![child_risk](https://user-images.githubusercontent.com/55840722/116553053-abc2dc80-a934-11eb-8bb3-92c9134e2373.png)

### 어린이 보호구역 외 20개소
<img width="582" alt="no_school" src="https://user-images.githubusercontent.com/55840722/116553234-df9e0200-a934-11eb-943b-6fcb90f2d2cb.png">

------------

## 의의
### 결과적 유의성
어린이 보호구역과 어린이 보호구역 외의 위험도 지수가 높은 지역을 살펴본 결과 일반적으로 생각하는 교통사고 위험요인(추정 교통량, 유동인구)들 또한 높은 것을 확인할 수 있었고, 배경지식에서 예상했던 바와 같이 중앙동과 대원동 근처에 위험지역이 많은 것을 확인할 수 있었다.
### 독창성
통계 모델을 사용하여 오산시 만의 특성을 반영할 수 있는 위험도 지수를 산출하였다.
### 시각적 활용
지도를 제작하였기 때문에 한눈에 위험 지역을 파악할 수 있었다. 또한 검색 기능을 이용하여 해당 격자를 찾을 수 있도록 하였다.
### 경제성 및 공공성
모든 자료는 기본 제공 자료와 공공자료, 오픈 소스들을 활용하였으며, 데이터 추가를 제외하면 모델을 발전시키는 데에 비용이 들지 않음.
### 추후 발전 가능성
추후 데이터를 추가하여 모델에 반영하면 더 정확한 위험도 지수를 산출할 수 있다.

------------

## 한계
### 데이터의 부족 및 불완전성
필요한 곳의 데이터가 없거나 불완전한 경우들이 있었다.
예를 들어 도로가 있음에도 도로 정보가 없는 지역들이 존재 → 분석을 위해 대체값을 사용 → 분석의 부정확성
### 적은 어린이 보호구역 수
어린이 보호구역의 경우 원래 숫자가 적기 대문에 어린이 보호구역 외에 비해 비교적 분석의 정확도가 떨어졌음.

------------

## 제언 및 활용방안 제시
### 데이터 보완
정기적으로 데이터를 갱신 또는 추가하는 경우 더욱 정확한 분석 결과를 얻을 수 있을 것.
### 오산시 외의 데이터와 결합하여 분석
오산시와 비슷한 특징을 가진 도시와의 데이터와 결합하여 분석을 진행한다면 충분한 수의 어린이 보호구역 데이터 수를 얻을 수 있을 것
### 활용방안
위험지역으로 표시된 곳에 안전시설물이 부족한 경우 안전시설물 설치 우선지역으로 선정할 수 있으며, 이를 통해 어린이 교통사고를 방지할 수 있다.
