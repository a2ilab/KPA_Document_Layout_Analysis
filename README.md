# 📄 Public Administration Document Layout Annotation Dataset (AI-Hub 기반)

이 저장소는 **AI-Hub에서 제공하는 공공행정문서 OCR 데이터셋** 일부(총 900장)를 기반으로 **문서 레이아웃 라벨링**을 진행한 결과를 포함하고 있습니다.  
본 데이터는 **YOLO 형식**으로 구성된 라벨 파일만 포함되며, 문서 레이아웃 분석 및 관련 AI 모델 학습에 활용될 수 있습니다.

🔗 **AI-Hub 원본 데이터셋:** [공공행정문서 OCR 데이터](https://www.aihub.or.kr/aihubdata/data/view.do?currMenu=&topMenu=&aihubDataSe=data&dataSetSn=88)

---

## 📁 데이터셋 구성

| 구분             | 수량  |
|------------------|-------|
| Train Set        | 700장 |
| Validation Set   | 100장 |
| Test Set         | 100장 |
| **총합**         | **900장** (비율: 7 : 1 : 1) |

본 데이터는 AI-Hub의 **한국 공공행정문서 데이터셋(2010년~2013년)** 중 일부 문서에 대해 라벨링한 결과로, 다음의 **12개 행정 카테고리**에 해당하는 문서를 포함합니다.

- 농림·축산지원
- 도시개발
- 산업진흥
- 상·하수도관리
- 인·허가
- 일반행정
- 주민복지
- 주민생활지원
- 주민자치
- 지역문화
- 지역환경·산림
- 회계·예산

---

## 🏷️ 클래스 정의 (총 9개 클래스)

각 문서의 구성 요소는 다음과 같은 기준에 따라 총 **9개의 클래스**로 라벨링되었습니다:

| 클래스명            | 클래스 ID | 설명                                                         |
|---------------------|-----------|--------------------------------------------------------------|
| **Title**           | 0         | 문서의 제목으로, 수신자 아래 위치하며 '제목' 문구를 포함       |
| **Plain Text**      | 1         | 본문 또는 기타 일반 텍스트로, 표나 그림이 아닌 텍스트 블록     |
| **Figure**          | 2         | 그림, 로고, QR코드 등 비텍스트 시각 요소                       |
| **Table**           | 3         | 셀과 경계선으로 구성된 데이터 표                               |
| **Table Caption**   | 4         | 표의 제목 또는 설명, 표의 위 또는 아래에 위치                   |
| **Header**          | 5         | 기관명, 문서 상단 정보 등 문서의 머리말 부분                     |
| **Footer**          | 6         | 담당자 정보, 시행기관, 날짜 등 문서 하단 정보                    |
| **Signature**       | 7         | 직인이나 서명 이미지                                           |
| **Signature Block** | 8         | 서명자 이름 또는 직책이 포함된 텍스트                           |

---

## 📂 데이터 포맷

본 데이터셋은 **YOLO 포맷**으로 저장되어 있으며, 각 이미지에 대한 라벨 파일이 **`.txt` 형식**으로 제공됩니다.

## 📥 데이터 사용 방법

1. **YOLO 학습 데이터로 활용**  
   - `train`, `val`, `test` 폴더 내 `.txt` 라벨 파일과 이미지 파일을 동일한 이름으로 정리  
   - YOLO 학습 스크립트 실행

2. **문서 레이아웃 분석 연구**  
   - 특정 클래스를 기준으로 문서 구조를 분석  
   - OCR 및 문서 자동 분류 시스템과 결합

---

## 🔗 참고 자료

- 📌 **AI-Hub 원본 데이터셋**: [공공행정문서 OCR 데이터](https://www.aihub.or.kr/aihubdata/data/view.do?currMenu=&topMenu=&aihubDataSe=data&dataSetSn=88)
- 📖 **YOLO 포맷 설명**: [YOLO 공식 문서](https://github.com/AlexeyAB/darknet)

