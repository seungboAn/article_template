## Markdown 기반 Article 웹서비스 개발 Task 순서

## 필수사항

*   모든 작업은 완료 시에 작업에 대한 설명과 트러블슈팅 (발생 시)을 `docs/` 폴더에 Markdown 형식으로 기록해야 합니다.
*   명령어 실행 시 `-y` 옵션은 기본으로 적용됩니다. (자동으로 '예' 응답)

### 1. 프로젝트 초기 설정 및 환경 구축

*   1.1 Next.js 프로젝트 생성 (`create-next-app`)
    *   명령어: `create-next-app -y`
    *   1.1.1 작업 문서 (`docs/1.1_next_project_setup.md`): 프로젝트 생성 과정, 사용된 템플릿 (선택 시), 설정 옵션 기록
    *   1.1.2 트러블슈팅 (`docs/1.1_next_project_setup_troubleshooting.md`): 발생 가능한 오류 (npm init 실패, 디렉토리 중복 등) 및 해결 방법 기록
*   1.2 필요한 패키지 설치: `remark`, `react-markdown`, `tailwindcss`, etc.
    *   명령어: `npm install -y remark react-markdown tailwindcss ...`
    *   1.2.1 작업 문서 (`docs/1.2_package_install.md`): 설치된 패키지 목록, 각 패키지의 역할 및 사용 이유 상세 설명, 버전 정보
    *   1.2.2 트러블슈팅 (`docs/1.2_package_install_troubleshooting.md`): 설치 오류 (패키지 충돌, 버전 문제 등) 및 해결 방법 기록
*   1.3 Tailwind CSS 설정 및 적용
    *   명령어: `npx tailwindcss init -p -y` (post css 설정 포함)
    *   1.3.1 작업 문서 (`docs/1.3_tailwind_setup.md`): Tailwind 설정 파일 (`tailwind.config.js`, `postcss.config.js`) 내용 설명, 스타일 적용 방법, 사용자 정의 스타일 규칙 기록
    *   1.3.2 트러블슈팅 (`docs/1.3_tailwind_setup_troubleshooting.md`): 스타일 충돌, 컴파일 오류, 반응형 디자인 문제 등 해결 방법 기록
*   1.4 프로젝트 구조 정리: `pages`, `components`, `styles`, `public`, `lib`, `docs` 폴더 생성 (필요에 따라 추가)
    *   1.4.1 작업 문서 (`docs/1.4_project_structure.md`): 각 폴더의 역할 및 파일 구성 상세 설명, 파일명 규칙, 프로젝트 구조 다이어그램
    *   1.4.2 트러블슈팅 (`docs/1.4_project_structure_troubleshooting.md`): 폴더 생성 오류, 파일 이동 문제 등 해결 방법 기록

### 2. 컴포넌트 개발 (각 컴포넌트별로 동일한 양식의 문서 및 트러블슈팅 파일 생성)

*   2.1 공통 컴포넌트: `Header`, `Footer` 생성 (예: `docs/2.1_header_component.md`, `docs/2.1_header_component_troubleshooting.md`)
*   2.2 랜딩 페이지 컴포넌트: `Hero Section`, `Featured Articles`, `About Me` 생성
*   2.3 Article 목록 컴포넌트: `ArticleCard` 생성
*   2.4 Article 상세 페이지 컴포넌트: Markdown 내용 렌더링, 댓글 기능 (선택 사항)

### 3. 기능 개발 (각 기능별로 동일한 양식의 문서 및 트러블슈팅 파일 생성)

*   3.1 Markdown 파싱 및 렌더링 기능 구현 (`remark`, `react-markdown`) (예: `docs/3.1_markdown_parsing.md`, `docs/3.1_markdown_parsing_troubleshooting.md`)
*   3.2 Article 목록 페이지: Article 목록 조회 및 표시 기능 구현
*   3.3 Article 상세 페이지: Article 내용 조회 및 표시 기능 구현
*   3.4 검색 기능 구현 (선택 사항)
*   3.5 카테고리/태그 분류 기능 구현
*   3.6 반응형 디자인 적용
*   3.7 SEO 최적화: meta 정보, sitemap 생성

### 4. 데이터베이스 연동 (선택 사항) (각 기능별로 동일한 양식의 문서 및 트러블슈팅 파일 생성)

*   4.1 데이터베이스 선택 및 설정 (MongoDB, PostgreSQL)
*   4.2 Article 데이터 스키마 정의
*   4.3 데이터베이스 연동 및 API 개발

### 5. API 개발 (선택 사항) (각 API별로 동일한 양식의 문서 및 트러블슈팅 파일 생성)

*   5.1 Article 목록 조회 API
*   5.2 Article 상세 정보 조회 API
*   5.3 검색 API (선택 사항)

### 6. 테스트 (각 테스트별로 동일한 양식의 문서 및 트러블슈팅 파일 생성)

*   6.1 컴포넌트 단위 테스트
*   6.2 기능 통합 테스트
*   6.3 사용자 시나리오 기반 테스트

### 7. 배포 (각 단계별로 동일한 양식의 문서 및 트러블슈팅 파일 생성)

*   7.1 Netlify 설정
*   7.2 빌드 및 배포

### 8. 유지보수 및 개선 (각 작업별로 동일한 양식의 문서 및 트러블슈팅 파일 생성)

*   8.1 버그 수정 및 기능 개선
*   8.2 사용자 피드백 반영
*   8.3 새로운 기능 추가

## 추가 Task (선택 사항) (각 기능별로 동일한 양식의 문서 및 트러블슈팅 파일 생성)

*   댓글 기능 개발
*   검색 기능 고도화
*   테마 기능 개발 (Light/Dark 모드)
*   소셜 미디어 공유 기능 개발

## Task별 우선순위

*   **필수**: 1, 2, 3, 6, 7
*   **선택**: 4, 5, 8

## 개발 단계별 Task 분류

*   **기획 및 설계**: 1.1, 1.2, 1.3, 1.4, 2.1, 5.1
*   **개발**: 2.2, 2.3, 2.4, 3.1, 3.2, 3.3, 3.4, 3.5, 3.6, 3.7, 4.1, 4.2, 4.3, 5.2, 5.3
*   **테스트**: 6.1, 6.2, 6.3
*   **배포**: 7.1, 7.2
*   **유지보수**: 8.1, 8.2, 8.3