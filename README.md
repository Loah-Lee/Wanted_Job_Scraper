# Wanted Job Scraper (Study Project)

## 📌 프로젝트 개요
본 프로젝트는 **구직 목적 + 웹 스크래핑 학습**을 위해 진행한 개인 학습 프로젝트입니다.

- 채용 플랫폼 **원티드(Wanted)**의 채용 공고 데이터를
  - **공식 OpenAPI 방식**
  - **HTML 스크래핑 방식**
  두 가지로 수집하며,
- 두 접근 방식의 **안정성, 한계, 학습 포인트**를 비교하는 것을 목표로 합니다.

> ⚠️ 본 프로젝트는 개인 학습 및 구직 목적이며,  
> 수집한 데이터는 재배포·상업적 활용을 하지 않습니다.

---

## 🎯 목표
- 실제 구직에 활용 가능한 채용 공고 데이터 정리
- OpenAPI 기반 데이터 수집 경험
- HTML 기반 웹 스크래핑의 구조적 이해
- 두 방식의 차이를 직접 비교하며 장단점 체득

---

## 🛠 사용 기술
- Python 3.10
- requests
- BeautifulSoup4
- SQLite
- Jupyter Notebook (분석용)

---

## 📂 프로젝트 구조
```
wanted-job-scraper/
├── api/
│   └── fetch_jobs_api.py        # Wanted OpenAPI 기반 수집
├── html/
│   └── scrape_list_html.py      # HTML 스크래핑 (검색 결과 리스트)
├── normalize/
│   └── clean_jobs.py            # 데이터 정규화
├── db/
│   └── jobs.sqlite              # 수집 데이터 저장
├── analysis/
│   └── keyword_analysis.ipynb   # 기술 스택/키워드 분석
└── README.md
```

---

## 🔌 수집 방식 1: Wanted OpenAPI
### 특징
- 공식 제공 API 사용
- 안정적인 JSON 구조
- 구조 변경에 강함
- 실제 서비스/현업 환경에 가까움

### 학습 포인트
- REST API 구조 이해
- Pagination 처리
- JSON 데이터 정규화
- Rate limit 고려한 요청 설계

---

## 🕸 수집 방식 2: HTML Scraping
### 특징
- 검색 결과 페이지의 공개 HTML만 수집
- 로그인 필요 없는 범위에서 제한적으로 사용
- DOM 구조 변경에 취약

### 학습 포인트
- HTML / DOM 구조 분석
- CSS Selector 활용
- 정적 페이지 vs 동적 페이지 구분
- 웹 스크래핑의 구조적 한계 체감

---

## ⚖ OpenAPI vs HTML Scraping 비교
| 항목 | OpenAPI | HTML Scraping |
|----|----|----|
| 안정성 | 높음 | 낮음 |
| 구조 변경 영향 | 적음 | 큼 |
| 학습 난이도 | 중 | 중~상 |
| 실무 활용도 | 매우 높음 | 보조적 |

---

## 📝 한계 및 주의사항
- 본 프로젝트는 **학습 목적**으로만 진행됨
- 대량 수집, 빈번한 요청은 지양
- 사이트 정책 및 robots.txt 범위를 존중

---

## 🔍 느낀 점
- OpenAPI는 “실전용”
- HTML 스크래핑은 “구조 이해용”
- 두 방식을 함께 써보며 **왜 현업에서 API를 선호하는지**를 체감할 수 있었음

---

## 📅 향후 계획
- 키워드 기반 구직 알림 자동화
- 기술 스택 트렌드 분석 고도화
- 다른 채용 플랫폼과 구조 비교

