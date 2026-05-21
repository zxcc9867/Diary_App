# 📔 Diary App

감정을 기록하고 돌아볼 수 있는 **React + Vite 기반 다이어리 웹 애플리케이션**입니다.  
하루의 감정과 생각을 간편하게 작성하고, 월별로 모아보며 나의 일상을 관리할 수 있습니다.

## 🔗 배포 링크

- https://emotion-project-xi.vercel.app/

## 📌 프로젝트 개요

Diary App은 일기 작성/조회/수정/삭제(CRUD)를 중심으로 구성된 감정 기록 서비스입니다.

- 날짜, 감정 상태, 일기 내용을 함께 저장
- 월별 목록 탐색 및 정렬 지원
- 브라우저 `localStorage` 기반 데이터 유지

## ✨ 주요 기능

- **일기 CRUD**
  - 새 일기 작성
  - 일기 상세 조회
  - 기존 일기 수정
  - 일기 삭제

- **감정 선택 UI**
  - 감정(1~5단계) 선택
  - 감정 상태를 시각적으로 확인

- **월 단위 탐색**
  - 이전/다음 월 이동
  - 선택한 월 기준 목록 조회

- **정렬 기능**
  - 최신순 / 오래된순 정렬

- **로컬 저장소 연동**
  - 새로고침 이후에도 작성 데이터 유지

## 🛠 기술 스택

- **Frontend**: React 18
- **Build Tool**: Vite 6
- **Routing**: React Router DOM 7
- **State Management**: Context API + `useReducer`
- **Storage**: Browser `localStorage`
- **Styling**: CSS

## 📁 프로젝트 구조

```bash
src/
 ┣ components/         # 공통 UI 컴포넌트
 ┃ ┣ Editor.jsx        # 일기 작성/수정 폼
 ┃ ┣ DiaryList.jsx     # 일기 목록/정렬
 ┃ ┣ DiaryItem.jsx     # 일기 카드
 ┃ ┣ View.jsx          # 일기 상세 보기
 ┃ ┣ Header.jsx        # 상단 헤더
 ┃ ┣ Button.jsx        # 공용 버튼
 ┃ ┗ EmotionItem.jsx   # 감정 선택 아이템
 ┣ hooks/
 ┃ ┣ useDiary.jsx      # id 기반 일기 조회
 ┃ ┗ usePagetitle.jsx  # 페이지 타이틀 설정
 ┣ pages/
 ┃ ┣ Home.jsx          # 홈(목록/월 이동)
 ┃ ┣ New.jsx           # 새 일기 작성
 ┃ ┣ Edit.jsx          # 일기 수정
 ┃ ┣ Diary.jsx         # 일기 상세
 ┃ ┗ Notfound.jsx      # 404 페이지
 ┣ util/
 ┃ ┣ constants.js      # 감정 상수
 ┃ ┣ get-emtion-images.js
 ┃ ┗ getStringDate.js
 ┣ App.jsx             # 라우팅 + 전역 상태 관리
 ┗ main.jsx            # 앱 진입점
```

## 🚀 실행 방법

### 1) 저장소 클론

```bash
git clone <REPOSITORY_URL>
cd Diary_App
```

### 2) 패키지 설치

```bash
npm install
```

### 3) 개발 서버 실행

```bash
npm run dev
```

### 4) 브라우저 접속

```bash
http://localhost:5173
```

## 📦 빌드 및 미리보기

### 프로덕션 빌드

```bash
npm run build
```

### 빌드 결과 미리보기

```bash
npm run preview
```

## 🧭 화면 예시

### Home
<img src="image.png" width="800" alt="Diary App Home 화면" />

### Edit
<img src="image-1.png" width="800" alt="Diary App Edit 화면" />

## 🔮 향후 개선 아이디어

- 감정/키워드 검색 기능
- 월별 감정 통계 시각화
- 다크 모드
- 클라우드 동기화 및 계정 연동
- 모바일 UX 개선
