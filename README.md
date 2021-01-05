# Doctoral Dissertations on Modern Korean Literature (DDMKL)

## 소개
2000년에서 2019년까지 출간된 전국 국어국문학과 박사 학위논문(현대문학) 1,528편의 서지정보를 수집하고 분석해  
한국 현대문학 연구 변화와 앞으로의 연구를 전망하는 연구에 필요한 파이썬 코드입니다.  
데이터 수집 및 분석의 자세한 과정은 아래 논문을 참고하십시오.  
논문이나 코드관련 문의는 아래 저자 소개에 있는 이메일로 연락주시거나 깃허브 issue 페이지를 통해 받겠습니다.  
#### [박사학위 논문(2000~2019) 데이터 분석을 통해 본 한국 현대문학 연구의 변화와 전망 (상허학보 60, 202010)](https://www.kci.go.kr/kciportal/ci/sereArticleSearch/ciSereArtiView.kci?sereArticleSearchBean.artiId=ART002647202)

## 저자
* 김병준(성균관대학교 인터랙션사이언스학과 박사과정/국어국문학과 강사, kimkunta@skku.edu)
* 천정환(성균관대학교 국어국문학과 교수, hicnunc@skku.edu)

## 코드 활용
Jupyter 코드(ipynb)를 다운받아 로컬에서 활용하거나, 

핵심 코드 3개(전처리, 키워드, 모델링)는 Google Colab으로 바로 코드 확인 및 개발 가능.

## 폴더 설명
* keywords : TF/TF-IDF 기준 시기별 키워드. 단어-단어 네트워크 매트릭스
* model : 시계열 토픽 모델링 model 파일
* plot : 토픽 內 단어변화 플롯 및 연도별 상위 20개 단어와 토픽-토픽 네트워크 매트릭스
* riss : RISS에서 다운로드 받은 서지정보 예시 파일

---

## 0. 서지정보 데이터 다운로드
#### [데이터 안내(필독)](https://github.com/ByungjunKim/DDMKL/blob/main/data/DATA.md)
#### [data 폴더](https://github.com/ByungjunKim/DDMKL/tree/main/data)

## 1. 데이터 수집 및 개괄
#### Selenium 을 활용한 RISS 서지정보 자동 내려받기
#### 00RissCrawling.ipynb (RISS 서지정보 자동수집, [코드 활용안내 튜토리얼](https://youtu.be/3A7EKg9XyMU))
#### 01RissParsing.ipynb (RISS에서 다운로드 받은 서지정보 엑셀파일 합치기)
#### [크롬 드라이버 다운로드](https://chromedriver.chromium.org/downloads)

## 2. 데이터 전처리 & 형태소 분석
#### 02Preprocess.ipynb ([구글 Colab 링크](https://colab.research.google.com/drive/1x8DIFh5LMjIC7E3Qezy9emWp_-EpMqEO?usp=sharing))
* Pandas를 활용한 데이터 전처리
* 사용자 사전 구축
* Khaiii 형태소 분석기
* 불용어 처리

## 3. 기술 통계량 & 키워드 추출
#### 03Keywords.ipynb ([구글 Colab 링크](https://colab.research.google.com/drive/1bGebwCdiwY1g-0aMEUqQbZ1QMptSkDc7?usp=sharing))
* 기술 통계량
* TF, TF-IDF 기준 키워드 추출
* 시기별 키워드 추출

## 4. 시계열 토픽 모델링
#### 04Model.ipynb ([구글 Colab 링크](https://colab.research.google.com/drive/15A9sNGjogSm23yYmT_KVkwWd6YHxfvur?usp=sharing))
##### [Dynamic Topic Model 바이너리 Github](https://github.com/magsilva/dtm)
##### [Dynamic Topic Model 바이너리 다운로드(윈도우64)](https://github.com/magsilva/dtm/raw/master/bin/dtm-win64.exe)
##### [Dynamic Topic Model 바이너리 다운로드(리눅스64)](https://github.com/magsilva/dtm/raw/master/bin/dtm-linux64)
* 모델링
* 시간에 따른 토픽별 주요단어 변화
* 모델링 결과 시각화
* 토픽-토픽 네트워크

