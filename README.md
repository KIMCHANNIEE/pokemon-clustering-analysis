# 🧬 포켓몬 도감 데이터 분석 및 클러스터링

이 프로젝트는 포켓몬 관련 데이터를 웹 크롤링하여  
데이터를 전처리하고, 시각화 및 클러스터링 분석을 수행하는 Python 기반의 데이터 분석 프로젝트입니다.

---

## 📌 주요 내용

- 영어/한국어 포켓몬 도감 데이터 수집 (BeautifulSoup 활용)
- `전국도감 번호`, `이름`, `지방` 정보 병합
- 텍스트 전처리 및 중복 제거
- 향후 특성 기반 클러스터링 적용 예정

---

## 🛠 사용된 기술 스택

- Python 3
- pandas, BeautifulSoup, re
- matplotlib / seaborn (시각화)
- scikit-learn (군집화)

---

## 📊 클러스터링 분석

이 프로젝트에서는 포켓몬 데이터를 기반으로 두 가지 방식의 군집화를 수행했습니다:

1. **DBSCAN (밀도 기반 클러스터링)**  
   - 포켓몬 데이터를 거리 기반으로 분할하여, 밀도에 따라 클러스터를 구분했습니다.  
   - 클러스터 개수를 미리 설정하지 않아도 되며, 노이즈(잡음) 데이터도 감지 가능합니다.

2. **KMeans (중심 기반 클러스터링)**  
   - X, Y 피처(추정: 특성 점수 or 차원 축소 결과)를 기준으로 8개의 군집으로 분할했습니다.  
   - 각 포켓몬이 속한 클러스터를 색상으로 시각화하여 분포를 확인했습니다.

> 두 모델을 비교하여 포켓몬 유형이나 지역별 특성의 분포를 이해하고자 하였습니다.
