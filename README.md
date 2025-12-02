# 퀀트 투자를 위한 머신러닝 실습 저장소

이 저장소는 **「퀀트 투자를 위한 머신러닝」(기욤 코케렛 저)** 를 따라가며  
책의 내용을 코드로 직접 구현·응용하기 위한 개인 실습용 프로젝트입니다.

> 목표: 책의 예제와 아이디어를 그대로 따라 치는 데서 끝나지 않고,  
> **내 데이터 / 내 전략으로 확장**하는 것을 최종 목표로 합니다.

---

## 1. 환경 설정

### Python & 가상환경

```bash
# (선택) 가상환경 생성
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate

# 기본 패키지 설치
pip install -r requirements.txt
```

### requirements.txt 예시
```text
numpy
pandas
scikit-learn
matplotlib
seaborn
jupyter
statsmodels
```

---

## 2. 폴더 구조
```bash
.
├── README.md                 # 이 파일
├── requirements.txt          # 패키지 목록
├── data/
│   ├── raw/                  # 원천 데이터 (다운로드 그대로)
│   ├── processed/            # 전처리된 데이터
│   └── external/             # 책 외부에서 가져온 추가 데이터
├── notebooks/
│   ├── ch01_data.ipynb       # 1장 표기법과 데이터
│   ├── ch02_intro.ipynb      # 2장 개요
│   └── ...                   # 장/주제별 노트북
├── src/
│   ├── utils/                # 공통 함수(로딩, 시각화 등)
│   ├── features/             # 피처 생성 관련 코드
│   ├── models/               # 모델 학습·평가 코드
│   └── backtest/             # 간단한 백테스트/전략 평가
└── reports/
    └── figures/              # 그래프, 결과 이미지
```

---

## 3. 실습 방식

### 1. 장별 노트북 생성

- 데이터 다운로드 경로: [shokru 깃허브 페이지](https://github.com/shokru/mlfactor.github.io/tree/master/material)
- `notebooks/ch0X_제목.ipynb` 형태로 만들기
- 책의 수식·그림·표를 코드로 직접 재현해 보기

### 2. 책 그대로 구현 → 변형

- 그대로 구현: 책 코드/아이디어를 최대한 충실히 따라 하기
- 변형:
    - 다른 종목/지수 데이터로 실험
    - 파라미터 바꾸기 (윈도우 길이, 테스트 구간 등)
    - 평가지표 추가 (샤프, MDD, 승률 등)

### 3. 결과 정리

- 중요한 인사이트는 노트북 마지막에 텍스트 셀로 요약
- 의미 있었던 실험·그래프는 `reports/`에 저장

---

## 4. 진행상황 체크

- [x] 1. 표기법과 데이터
- [ ] 2. 개요
- [ ] 3. 팩터 투자와 자산 가격 결정 이상 현상
- [ ] 4. 데이터 전처리
- [ ] 5. 페널티 회귀와 최소 분산 포트폴리오를 위한 희소 헤징
- [ ] 6. 트리 기반 기법
- [ ] 7. 신경망
- [ ] 8. 서포트 벡터 머신
- [ ] 9. 베이지안 기법
- [ ] 10. 검증 및 튜닝
- [ ] 11. 앙상블 모델
- [ ] 12. 포트폴리오 백테스팅
- [ ] 13. 해석성
- [ ] 14. 두 가지 주요 개념: 인과성과 비정상성
- [ ] 15. 비지도 학습
- [ ] 16. 강화학습

---

## 5. 참고

원서: *Machine Learning for Factor Investing / Machine Learning for Quantitative Trading* (저자: Guillaume Coqueret 등, 번역본 기준 도서)