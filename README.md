# Doctoral Dissertations on Modern Korean Literature (DDMKL)
[박사학위 논문(2000~2019) 데이터 분석을 통해 본 한국 현대문학 연구의 변화와 전망 (상허학보 60, 202010)](https://www.kci.go.kr/kciportal/ci/sereArticleSearch/ciSereArtiView.kci?sereArticleSearchBean.artiId=ART002647202)

저자
* 김병준(성균관대학교 인터랙션사이언스학과 박사과정)
* 천정환(성균관대학교 국어국문학과 교수)

## 0. 서지정보 데이터 다운로드
[data 폴더](https://github.com/ByungjunKim/DDMKL/tree/main/data)

## 1. 데이터 수집 및 개괄
#### Selenium 을 활용한 RISS 서지정보 자동 내려받기
* 00RissCrawling.ipynb (RISS 서지정보 자동수집, [코드 활용안내 튜토리얼](https://youtu.be/3A7EKg9XyMU))
* 01RissParsing.ipynb (RISS에서 다운로드 받은 서지정보 엑셀파일 합치기)

## 2. 데이터 전처리 & 형태소 분석
#### Pandas를 활용한 데이터 전처리
#### 사용자 사전 구축
#### Khaiii 형태소 분석기
#### 불용어 처리
#### ngram 처리

## 3. 키워드 추출
#### TF, TF-IDF 기준 키워드 추출
#### 시기별 키워드 추출

## 4. 시계열 토픽 모델링

## 5. 토픽 모델링 시각화
#### 시간에 따른 토픽별 주요단어 변화
#### 토픽-토픽 네트워크
