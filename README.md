# 🥗 칼로리 비서 (Calorie Secretary)

**칼로리 비서**는 사용자 맞춤형 일일 칼로리 및 3대 영양소(탄수화물·단백질·지방) 관리를 도와주는 스마트 식단 기록 및 분석 웹 애플리케이션입니다.  
별도의 백엔드 서버 없이 단일 HTML 파일 형태로 동작하며, OpenAI API(GPT-4o-mini)를 활용한 **음식 사진 자동 인식 기능**과 **실시간 맞춤 영양 조언**을 제공합니다.

---

## 📸 주요 기능 (Key Features)

### 1. 📊 스마트 대시보드
- **실시간 칼로리 트래킹:** 하루 목표 칼로리 대비 섭취량 및 잔여 칼로리 시각화 (프로그레스 바 & 게이지 표시)
- **탄단지(Macronutrients) 분석:** Chart.js 도넛 차트를 통한 탄수화물, 단백질, 지방 섭취 비율 및 목표 대비 달성률 한눈에 확인
- **시간대별 끼니 타임라인:** 아침, 점심, 저녁, 간식 별 섭취 칼로리 구분 요약

### 2. 🤖 AI 식단 조언 및 사진 자동 인식 (OpenAI GPT-4o-mini 연동)
- **실시간 영양 조언 시스템:** 현재 시각과 섭취한 탄·단·지 비율을 계산하여 부족한 영양소와 추천 음식을 맞춤형 텍스트로 제안
- **📷 사진 업로드 음식 인식:** 식사 사진을 올리면 AI가 음식을 자동 분석하여 트레이(장바구니)에 담아주는 스마트 기능 제공
- **개인 API 키 보안 저장:** OpenAI API 키를 브라우저 `localStorage`에만 안전하게 저장하여 외부 유출 방지

### 3. 📝 간편 식단 기록 및 검색
- **음식 검색 & 트레이 시스템:** 내장된 한식/외식 음식 DB를 기반으로 실시간 연관 검색 및 수량 조절 후 한 번에 기록
- **대화형 기록 인터페이스:** 카카오톡/메신저 스타일의 UI로 끼니 시간대와 섭취 시간을 자연스럽게 수집
- **기록 수정 및 삭제:** 칼로리, 끼니 유형, 시간 정보를 손쉽게 변경 가능

### 4. 📐 BMR / TDEE 기반 자동 목표 설정
- **미플린-센트 지오어(Mifflin-St Jeor) 공식 적용:** 체중, 키, 나이, 성별, 활동량을 기반으로 기초대사량(BMR) 및 일일 권장 칼로리(TDEE) 자동 계산

### 5. 💾 데이터 관리 & CSV 내보내기
- **로컬 스토리지 데이터 보존:** 브라우저에 식단 및 설정 데이터가 자동 저장되어 서버 없이 지속적인 사용 가능
- **CSV 내보내기:** 기록된 식단 데이터를 엑셀 등에서 활용할 수 있도록 CSV 파일로 다운로드 지원

---

## 🛠 기술 스택 (Tech Stack)

| 구분 | 기술 / 라이브러리 |
| :--- | :--- |
| **Frontend** | HTML5, JavaScript (ES6+), CSS3 |
| **Styling** | [Tailwind CSS CDN](https://tailwindcss.com/) |
| **Visualization** | [Chart.js (v4.4.3)](https://www.chartjs.org/) |
| **AI Integration** | [OpenAI API (GPT-4o-mini)](https://platform.openai.com/) |
| **Design System** | Mobile-first Responsive App Layout (Noto Sans KR Font) |

---

## 🚀 시작하기 (Getting Started)

별도의 라이브러리 설치나 빌드 과정(`npm install` 등)이 필요 없는 **Single Page Application (SPA)** 입니다.

1. 본 리포지토리를 클론하거나 `index.html` 파일을 다운로드합니다.
   ```bash
   git clone https://github.com/YOUR_USERNAME/calorie-secretary.git
   ```
2. `index.html` (또는 해당 html 파일)을 브라우저(Chrome, Safari, Edge 등)로 열어 즉시 실행합니다.
3. (선택 사항) **기록** 탭 하단의 `API 키 설정`을 클릭하여 본인의 [OpenAI API Key](https://platform.openai.com/api-keys)를 등록하면 사진 인식 기능을 사용할 수 있습니다.

---

## 📱 앱 화면 구조

- **대시보드 탭 (🏠):** 일일 칼로리 프로그레스, 탄단지 도넛 차트, 끼니별 섭취 요약 및 AI 영양 조언 카드
- **기록 탭 (📝):** 타임라인 기반 채팅 인터페이스, 음식 검색/수량 조절 트레이, 사진 업로드, CSV 다운로드
- **설정 모달 (⚙️):** 신체 정보 입력, BMR/TDEE 자동 계산, 일일 목표 칼로리 설정 및 데이터 초기화

---

## 🔒 개인정보 및 보안

- 본 프로그램은 서버 백엔드를 사용하지 않습니다.
- 사용자가 입력한 신체 정보, 식단 기록, OpenAI API 키는 모두 **사용자의 웹 브라우저(`localStorage`)에만 저장**됩니다.

---

## 📄 라이선스 (License)

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
