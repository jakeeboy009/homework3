# NuanceBridge - AI 듀얼 영한 번역기 🎧📰
> **"직역"과 "문화적 맥락/슬랭 해설이 포함된 뉘앙스 번역"을 한눈에 비교하는 웹 애플리케이션**

OpenRouter API의 `google/gemma-4-26b-a4b-it:free` 모델을 활용하여, 단순 번역기로는 알 수 없는 미국/영국의 서브컬처 은어, 힙합/팝 가사 슬랭, 실리콘밸리 비즈니스 관용구(Idiom) 및 행간의 뉘앙스를 정밀하게 해설합니다.

---

## ✨ 주요 기능

1. **OpenRouter API Key 관리**
   - 상단 헤더에서 언제든지 API 키를 등록/수정/삭제 가능합니다.
   - 브라우저의 `localStorage`에만 저장되어 보안상 안전합니다.
   - 키 숨김/보임(마스킹) 토글 기능을 지원합니다.

2. **이중 번역 모드 (Lyrics vs Article)**
   - **🎵 가사(Lyrics) 모드**: 운율(Rhyme), 힙합/팝 문화 은어(Slang), 더블 앙탕드르(이중적 의미), 펀치라인의 숨은 의도를 살려 감성적으로 해설합니다.
   - **📰 아티클(Article) 모드**: 테크/비즈니스 관용구, 논리적 흐름, 글쓴이의 비판적/냉소적 뉘앙스를 매끄럽게 번역하고 배경 지식을 풀어줍니다.

3. **2단(Dual View) 비교 레이아웃**
   - **좌측 (직역)**: 원문의 문장 구조와 단어 뜻에 충실한 1:1 매칭 번역.
   - **우측 (뉘앙스 & 슬랭 해설)**: 문화적 맥락, 핵심 슬랭 사전식 정리, 초월번역 및 심층 해설 (마크다운 포맷팅 적용).

4. **사용자 경험(UX) 극대화**
   - 프리셋 예시 버튼 (클릭 한 번으로 슬랭 가사 / 테크 칼럼 예시 입력).
   - 단축키 지원 (`Ctrl + Enter` 또는 `Cmd + Enter`).
   - 번역 중 감성적인 진행 상태 애니메이션 및 메시지 순환.
   - 각 영역별 개별 복사 버튼 및 전체 결과 통합 복사 지원.
   - 다크 모드 기반의 글래스모피즘 & 세련된 퍼플/인디고 그라데이션 디자인.
   - 필요 시 다른 OpenRouter 모델(`meta-llama/llama-3.3-70b-instruct:free` 등)로 교체 가능한 모델 설정 모달.

---

## 🚀 빠른 시작 가이드 (실행 방법)

### 방법 1: 웹 브라우저에서 바로 열기 (가장 간단한 방법)
`index.html` 파일은 외부 빌드 도구(Node.js, npm 등)가 전혀 필요 없는 **단일 파일(Standalone HTML)** 구조입니다.
- 탐색기에서 `index.html` 파일을 더블 클릭하여 크롬(Chrome), 엣지(Edge), 사파리(Safari) 등 웹 브라우저로 엽니다.

### 방법 2: 로컬 웹 서버로 열기 (선택 사항)
Python이나 VS Code Live Server 등을 이용할 수 있습니다.
```bash
# Python 내장 웹 서버 실행 (터미널에서 실행)
python -m http.server 8000
```
브라우저에서 `http://localhost:8000`에 접속합니다.

---

## 🔑 OpenRouter API Key 발급 방법
1. [OpenRouter](https://openrouter.ai/)에 접속하여 구글 계정 등으로 로그인합니다.
2. [Keys 페이지](https://openrouter.ai/keys)로 이동하여 `Create Key`를 클릭합니다.
3. 생성된 키(`sk-or-v1-...`)를 복사하여 사이트 상단의 `API 키 설정` 영역에 입력하고 **저장**을 누릅니다.
4. 기본 모델인 `google/gemma-4-26b-a4b-it:free`는 무료 크레딧 한도 내에서 무료로 사용 가능합니다.

---

## 🛠️ 기술 스택
- **프론트엔드**: HTML5, Vanilla JavaScript (ES6+), Tailwind CSS (Typography CDN), Lucide Icons, Marked.js
- **백엔드/AI**: OpenRouter API (`https://openrouter.ai/api/v1/chat/completions`)
- **기본 모델**: `google/gemma-4-26b-a4b-it:free`
