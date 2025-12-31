# 🕷️ WebScraper Studio

**Visual Web Scraping Tool - No Code Required**

코딩 없이 웹 데이터를 수집할 수 있는 비주얼 웹 스크래핑 도구입니다.

![Python](https://img.shields.io/badge/Python-3.12+-blue.svg)
![PyQt6](https://img.shields.io/badge/PyQt6-6.6+-green.svg)
![Playwright](https://img.shields.io/badge/Playwright-1.40+-orange.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

<img width="1274" height="829" alt="image" src="https://github.com/user-attachments/assets/5dc0d800-bd5f-46da-a689-868a4d43698e" />



---

## ✨ 주요 기능

- **🎯 비주얼 셀렉터**: 클릭만으로 CSS/XPath 자동 생성
- **🌐 동적 웹 지원**: JavaScript 렌더링, SPA 완벽 지원
- **📊 다양한 출력**: CSV, JSON, Excel, SQLite 내보내기
- **⏰ 페이지네이션**: 다음 버튼, 무한 스크롤, URL 패턴 지원
- **🔄 데이터 변환**: Trim, Regex, 숫자/날짜 변환 파이프라인
- **💾 로컬 저장**: SQLite 기반 프로젝트 및 데이터 관리

---

## 🚀 설치 방법

### 요구사항

- Python 3.12 이상
- pip 또는 uv

### 설치

```bash
# 1. 저장소 클론 또는 압축 해제
cd webscraper-studio

# 가상환경 생성 및 활성화, 비활성화
C:\Python311\python.exe -m venv venv

venv\Scripts\activate

venv\Scripts\deactivate

# 2. 의존성 설치
C:\Python311\python.exe -m pip install -r requirements.txt

# 3. Playwright 브라우저 설치
playwright install chromium

# 4. 실행
C:\Python311\python.exe -m src.main
```

---

## 📖 사용 방법

### 1. 프로젝트 생성

1. **File > New Project** 또는 `Ctrl+N`
2. 프로젝트 이름과 시작 URL 입력
3. **Create** 클릭

### 2. 페이지 로드

1. URL 바에 웹사이트 주소 입력
2. **Go** 클릭 또는 `Enter`

### 3. 요소 선택

1. **🎯 Pick Element** 버튼 클릭
2. 브라우저에서 수집할 요소 클릭
3. CSS 셀렉터 자동 생성 확인

### 4. 필드 정의

1. **Fields** 탭에서 **+ Add Field** 클릭
2. 필드명, 셀렉터, 타입 설정
3. 필요시 데이터 변환 추가

### 5. 스크래핑 실행

1. **▶ Run** 버튼 클릭 또는 `F5`
2. 진행 상황 모니터링
3. 완료 후 **Data** 탭에서 결과 확인

### 6. 데이터 내보내기

1. **File > Export** 또는 `Ctrl+E`
2. 형식 선택 (CSV, JSON, Excel, SQLite)
3. 저장 위치 지정

---

## ⌨️ 단축키

| 동작 | 단축키 |
|------|--------|
| 새 프로젝트 | `Ctrl+N` |
| 프로젝트 열기 | `Ctrl+O` |
| 저장 | `Ctrl+S` |
| 스크래핑 실행 | `F5` |
| 스크래핑 중지 | `Shift+F5` |
| 요소 선택 모드 | `Ctrl+Shift+C` |
| 내보내기 | `Ctrl+E` |
| URL 포커스 | `Ctrl+L` |
| 종료 | `Ctrl+Q` |

---

## 🏗️ 프로젝트 구조

```
webscraper-studio/
├── src/
│   ├── main.py                 # 진입점
│   ├── core/                   # 핵심 로직
│   │   ├── browser_manager.py  # Playwright 브라우저 관리
│   │   ├── scraping_engine.py  # 스크래핑 엔진
│   │   └── data_transformer.py # 데이터 변환
│   ├── data/                   # 데이터 계층
│   │   ├── models.py           # SQLAlchemy 모델
│   │   ├── database.py         # DB 관리
│   │   └── exporters.py        # 내보내기
│   └── ui/                     # UI 계층
│       ├── main_window.py      # 메인 윈도우
│       ├── widgets/            # UI 위젯
│       └── styles/             # 스타일시트
├── resources/
│   ├── icons/
│   └── templates/
├── requirements.txt
└── pyproject.toml
```

---

## 📦 의존성

| 패키지 | 버전 | 용도 |
|--------|------|------|
| PyQt6 | 6.6+ | GUI 프레임워크 |
| qasync | 0.27+ | Qt-asyncio 통합 |
| playwright | 1.40+ | 브라우저 자동화 |
| SQLAlchemy | 2.0+ | ORM |
| beautifulsoup4 | 4.12+ | HTML 파싱 |
| lxml | 5.0+ | 빠른 XML/HTML 파싱 |
| pandas | 2.0+ | 데이터 처리 |
| openpyxl | 3.1+ | Excel 내보내기 |
| orjson | 3.9+ | 빠른 JSON 처리 |

---

## 🔧 데이터 변환 타입

| 변환 | 설명 | 예시 |
|------|------|------|
| `trim` | 공백 제거 | `"  hello  "` → `"hello"` |
| `regex` | 정규식 추출 | 패턴에서 값 추출 |
| `replace` | 문자열 치환 | 특정 문자 교체 |
| `number` | 숫자 변환 | `"₩1,290,000"` → `1290000` |
| `date` | 날짜 변환 | 포맷 변경 |
| `url` | URL 변환 | 상대→절대 URL |
| `mapping` | 값 매핑 | `{"Y": "Yes", "N": "No"}` |

---

## 🤝 기여

이슈 및 풀 리퀘스트를 환영합니다!

---

## 📄 라이선스

MIT License

---

## 🙏 감사의 말

- [Playwright](https://playwright.dev/) - 브라우저 자동화
- [PyQt6](https://www.riverbankcomputing.com/software/pyqt/) - GUI 프레임워크
- [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/) - HTML 파싱
