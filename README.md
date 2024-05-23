
# R 프로그래밍

## 소개
R은 통계 계산과 그래픽을 위한 무료 소프트웨어 환경입니다. 뉴질랜드의 통계학자 로스 이하카(Ross Ihaka)와 로버트 젠틀맨(Robert Gentleman)이 개발한 R은 현재 R 재단에 의해 유지 관리되고 있으며, 오픈 소스 커뮤니티의 기여로 꾸준히 발전하고 있습니다.

## 특징
R은 강력한 데이터 분석 도구로서 다음과 같은 주요 특징을 가지고 있습니다:

1. **통계 분석 기능**: R은 다양한 통계 모델링 기법을 지원합니다. 선형 및 비선형 모델, 시계열 분석, 분류 및 클러스터링 등 다양한 통계 분석을 수행할 수 있습니다.
2. **그래픽 기능**: 고품질의 데이터 시각화를 지원합니다. 기본 그래픽 시스템 외에도 `ggplot2`와 같은 패키지를 통해 더욱 정교한 그래픽을 생성할 수 있습니다.
3. **확장성**: CRAN (Comprehensive R Archive Network)을 통해 수천 개의 패키지를 제공하여, 다양한 분석 작업을 지원합니다.
4. **오픈 소스**: R은 무료로 사용할 수 있으며, 누구나 소스 코드를 열람하고 수정할 수 있습니다.
5. **커뮤니티 지원**: 방대한 사용자 커뮤니티와 활발한 개발자 그룹이 존재하여, 다양한 온라인 자료와 포럼을 통해 지원을 받을 수 있습니다.

## 주요 용도
R은 다양한 분야에서 데이터 분석과 시각화를 위해 사용됩니다:

- **학계 및 연구**: 데이터 분석과 통계 모델링을 통한 연구 결과 도출.
- **금융**: 리스크 관리, 포트폴리오 최적화, 가격 모델링 등.
- **생물정보학**: 생물정보학은 유전자 및 단백질 서열 데이터를 분석하여 생물학적 문제를 해결하는 학문입니다. R은 BioConductor와 같은 강력한 패키지 모음을 제공하여, 유전자 발현 분석, 서열 정렬, 유전체 데이터 시각화 등을 지원합니다. 예를 들어, 다음과 같은 작업을 수행할 수 있습니다:
  - **유전자 발현 분석**: RNA-Seq 데이터를 사용하여 차등 유전자 발현을 분석합니다.
  - **서열 정렬**: 유전자 서열 데이터를 정렬하고 비교합니다.
  - **단백질 구조 예측**: 단백질의 3D 구조를 예측하고 시각화합니다.
  - **유전체 데이터 시각화**: 유전체 데이터를 다양한 형식으로 시각화하여 이해를 돕습니다.
   
- **마케팅**: 고객 분석, 시장 조사, 캠페인 효과 분석.
- **공공 정책**: 인구 통계 분석, 정책 평가, 사회 경제 데이터 분석.

## 시작하기
R을 시작하려면 먼저 R과 RStudio(권장)를 설치해야 합니다. RStudio는 R을 사용하는데 편리한 통합 개발 환경(IDE)입니다.

1. **R 설치**: [CRAN](https://cran.r-project.org/mirrors.html) 사이트에서 운영체제에 맞는 R 설치 파일을 다운로드하고 설치합니다.
2. **RStudio 설치**: [RStudio](https://www.rstudio.com/products/rstudio/download/) 사이트에서 무료 버전을 다운로드하여 설치합니다.

설치가 완료되면 RStudio를 열고, R 스크립트를 작성하여 실행할 수 있습니다.


## 데이터 타입 (Data Types)

R에서 사용되는 주요 데이터 타입에는 숫자형(numeric), 문자형(character), 논리형(logical) 등이 있습니다.
```markdown
x <- 10        # 숫자형
y <- "Hello"   # 문자형
z <- TRUE      # 논리형
```

벡터 (Vector)
벡터는 동일한 데이터 타입의 값들을 일렬로 저장하는 1차원 배열입니다. c() 함수를 사용하여 벡터를 생성합니다.


---
title: "Chapter 20 높은 수준의 그래프 함수"
---

# Chapter 20 높은 수준의 그래프 함수

높은 수준의 그래프 함수 (High Level Graphics facilities) 들을 표로 정리해보면 아래와 같습니다.

## 높은 수준의 그래프 함수

| 그래프 종류 | 높은 수준의 그래프 함수 |
|-------------|-------------------------|
| 히스토그램(histogram) | `hist()` |
| 박스 플롯(box and whisker plot) | `boxplot()` |
| 줄기 잎 플롯(stem and leaf plot) | `stem()` |
| 막대 그래프 | `barplot()` |
| Cleveland Dot Plot | `dotchart()` |
| 파이 차트 | `pie()` |
| 산점도 | `plot(x, y)` |

---

## 목차

1. [R과 R Studio](#r과-r-studio)
2. [R 코딩과 R 패키지](#r-코딩과-r-패키지)
3. [R 마크다운](#r-마크다운)
4. [변수와 데이터 타입](#변수와-데이터-타입)
5. [벡터(vector)](#벡터vector)
6. [요인(factor)](#요인factor)
7. [행렬(matrix)](#행렬matrix)
8. [배열(array)](#배열array)
9. [리스트(list)](#리스트list)
10. [데이터 프레임](#데이터-프레임)

