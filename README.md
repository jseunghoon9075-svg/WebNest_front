프로젝트개요
  프론트엔드 부분은 React 기반으로 구성된 SPA로, 백엔드와의 명확한 인터페이스와 재사용 가능한 컴포넌트·훅 중심 설계를 목표로 합니다. 
  사용자 경험 향상을 위해 동적 스타일링과 상태 관리를 체계적으로 적용했습니다.

기술 스택

- 프레임워크: React
- 상태 관리: Redux (Redux Toolkit 권장)
- HTTP 통신: fetch 기반의 REST API 호출 (에러/로딩 처리 일관화)
- 스타일링: styled-components로 동적 스타일링 및 테마 적용
- 훅: React 훅과 커스텀 훅으로 로직 재사용성 확보
- 개발 도구: VSCode

프로젝트 구조

- src/
- components/: 재사용 가능한 UI 컴포넌트
- pages/: 라우트별 페이지 컴포넌트
- routes/: 라우팅 설정
- modules/: Redux 슬라이스 또는 도메인별 로직
- hooks/: 커스텀 훅 모음 (API 호출, 폼, 인증 등)
- context/: 전역 Context가 필요한 경우 사용
- styles/: 전역 스타일, 테마, keyframes
- utils/: 유틸 함수 및 상수

주요 기능 및 구현

- REST API 호출 표준화
  fetch를 래핑한 공통 유틸을 만들어 에러 처리, 토큰 갱신, 공통 헤더, 타임아웃을 중앙에서 관리합니다.
  응답 포맷(예: { message, data })에 맞춘 파싱 로직을 공통화했습니다.
  
- 상태 관리
- Redux를 사용해 전역 상태(인증, 사용자, UI 상태 등)를 관리합니다.

- 동적 스타일링
  styled-components로 상태 기반 스타일(로딩, 활성화 등)을 구현해 UI 일관성과 접근성을 개선했습니다.
