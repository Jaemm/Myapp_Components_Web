# MY-APP

Next.js 기반의 사내/대시보드형 웹 애플리케이션입니다.  
회원가입, 로그인, 마이페이지 같은 인증 흐름과 함께 카카오 지도, 날씨 위젯 같은 외부 서비스 연동을 포함한 프론트엔드 프로젝트입니다.

## 프로젝트 개요

- 프레임워크: `Next.js 12`
- 언어: `TypeScript`
- UI: `Ant Design`, `Emotion`
- 상태 관리: `React Query`, `Recoil`
- 통신: `Axios`
- 외부 연동: `Kakao Maps`, `OpenWeatherMap`, `Daum Postcode`

이 프로젝트는 `pages router` 기반으로 구성되어 있으며, 공통 레이아웃과 페이지 컴포넌트를 분리해 관리합니다.  
전역 상태는 `Recoil`로, 서버 상태는 `React Query`로 다루는 구조입니다.

## 주요 기능

- 로그인 / 로그아웃
- 회원가입
- 마이페이지 조회
- 회원정보 수정 / 삭제
- 카카오 지도 화면 연동
- 날씨 정보 위젯
- 공통 헤더 / 네비게이션 / 푸터 레이아웃

## 기술 스택

### Frontend

- `Next.js`
- `React`
- `TypeScript`
- `Emotion`
- `Ant Design`
- `Recoil`
- `@tanstack/react-query`

### Network / Integration

- `Axios`
- `Kakao Maps JavaScript API`
- `OpenWeatherMap API`
- `Daum Postcode API`

### Tooling

- `ESLint`
- `Prettier`
- `Next.js`

## 아키텍처

이 프로젝트는 완전한 MSA나 DDD 구조보다는, 화면 중심의 기능별 분리 구조에 가깝습니다.

- `src/pages`: 라우팅과 페이지 진입점
- `src/layouts`: 공통 레이아웃
- `src/components`: 공통 UI 및 기능 컴포넌트
- `src/components/apis`: 서버 통신 및 외부 API 연동
- `src/recoil`: 전역 상태 관리
- `src/config`: 환경 및 서버 설정

## 폴더 구조

```bash
src
├─ components
│  ├─ Headers
│  ├─ Navbars
│  ├─ Footers
│  ├─ antd
│  └─ apis
├─ config
├─ layouts
├─ pages
│  └─ auth
├─ recoil
├─ styles
└─ types
```

## 실행 방법

```bash
npm install
npm run dev
```

개발 서버는 기본적으로 `http://localhost:3090`에서 실행됩니다.

## 빌드 / 실행

```bash
npm run build
npm run start
```

## 참고 사항

- 백엔드 주소는 `src/config/config.ts`에서 관리합니다.
- 카카오 지도 스크립트와 다음 우편번호 스크립트는 `_document.tsx`에서 주입합니다.
- 로그인 후 사용자 정보는 `sessionStorage`와 `Recoil`을 함께 사용합니다.

## 포트폴리오 설명용 한 줄

> Next.js와 React Query, Recoil을 활용해 인증, 마이페이지, 외부 API 연동을 구현한 프론트엔드 대시보드형 웹 애플리케이션입니다.
