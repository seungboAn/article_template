## Markdown 기반 Article 웹서비스 개발 로드맵 (Next.js & Netlify)

### 1. 핵심 기능 (Core Features)

*   **Markdown 파싱 및 렌더링**: Markdown 문법을 HTML로 변환하여 웹 페이지에 표시
*   **Article 목록/상세 페이지**: Article 목록 페이지에서 제목/요약 미리보기 제공, 상세 페이지에서 전체 내용 표시
*   **검색 기능**: 제목, 내용 검색을 통해 원하는 Article 빠르게 접근
*   **카테고리/태그 분류**: Article을 카테고리/태그별로 분류하여 사용자 편의성 향상
*   **반응형 디자인**: 다양한 기기 (PC, 모바일, 태블릿)에서 최적화된 화면 제공
*   **SEO 최적화**: 검색 엔진 노출을 위한 meta 정보, sitemap 생성
*   **댓글 기능 (선택 사항)**: 사용자 간 커뮤니케이션 기능

### 2. 목표 및 목적 (Goals and Objectives)

*   **개인 블로그/지식 공유**: Markdown Article을 통해 개인적인 생각, 지식, 경험 등을 공유
*   **학습/개발 자료 저장**: 학습 내용, 개발 경험 등을 정리하여 체계적으로 관리
*   **커뮤니티 형성**: 댓글 기능을 통해 사용자들과 소통하고 교류 (선택 사항)

### 3. 기술 스택 (Tech Stack)

*   **프레임워크**: Next.js (React 기반) - SSR, SEO, 라우팅 용이
*   **Markdown 파서**: remark, react-markdown - 다양한 Markdown 문법 지원, 확장 가능
*   **UI 라이브러리**: Tailwind CSS, Material UI - 빠른 개발, 일관된 디자인
*   **데이터베이스**: (선택 사항) MongoDB, PostgreSQL - Article 메타데이터 저장, 사용자 관리
*   **검색**: (선택 사항) Algolia, ElasticSearch - 빠른 검색 성능
*   **배포**: Netlify - 간편한 배포, 자동 빌드
*   **기타**: Axios (HTTP 클라이언트), Moment.js (날짜/시간 처리)

### 4. 프로젝트 구조 (Project Folder Structure)

```
project-name/
├── pages/                # Next.js 페이지
│   ├── index.js          # 메인 페이지 (Article 목록)
│   ├── [slug].js         # Article 상세 페이지
│   ├── category/        # 카테고리별 Article 목록 페이지
│   └── search.js         # 검색 결과 페이지
├── components/           # 공통 컴포넌트
│   ├── Header.js
│   ├── Footer.js
│   ├── ArticleCard.js
│   └── ...
├── styles/               # 스타일 (CSS, SCSS)
├── public/               # 정적 파일 (이미지, favicon)
├── lib/                  # 유틸리티 함수, API
├── .env.local            # 환경 변수
├─── package.json
├── docs/               # 문서 폴더
```

### 5. 데이터베이스 설계 (Database Design) (선택 사항)

*   **Articles 컬렉션**:*
    *   `title` (String): 제목
    *   `slug` (String): URL slug
    *   `content` (String): Markdown 내용
    *   `excerpt` (String): 요약
    *   `category` (String): 카테고리
    *   `tags` (Array): 태그
    *   `createdAt` (Date): 생성일시
    *   `updatedAt` (Date): 수정일시

### 6. 랜딩 페이지 컴포넌트 (Landing Page Components)

*   **Hero Section**: 메인 이미지, 소개 문구, CTA 버튼
*   **Featured Articles**: 최근 Article 목록
*   **Categories/Tags**: 카테고리/태그별 Article 목록
*   **About Me**: 소개, 프로필 사진
*   **Footer**: 연락처, 소셜 미디어 링크

### 7. 색상 팔레트 및 스타일링 (Color Palette and Styling Choices)

*   **색상**:*
    *   메인: #333 (Dark Gray)
    *   보조: #EEE (Light Gray)
    *   강조: #0070F3 (Blue)
*   **스타일**:*
    *   폰트: Roboto, Open Sans
    *   레이아웃: Responsive, Boxed
    *   테마: Light/Dark 모드 지원 (선택 사항)

### 8. 랜딩 페이지 카피라이팅 (Copywriting for the Landing Page)

*   **제목**: "Welcome to My Markdown Blog"
*   **소개 문구**: "Share my knowledge, experience and thoughts"
*   **CTA 버튼**: "View Articles"
*   **About Me**: "Passionate developer sharing knowledge and experience"

## 추가 고려 사항

*   **API 연동**: 외부 API (댓글, 분석) 연동 고려
*   **테스트**: 유닛 테스트, 통합 테스트 작성
*   **보안**: XSS 공격 방어, 개인 정보 보호
*   **성능**: 이미지 최적화, 코드 최적화

## 개발 단계

1.  **기획 및 설계**: 위 로드맵 기반 상세 설계
2.  **환경 구축**: Next.js 프로젝트 생성, 필요 패키지 설치
3.  **컴포넌트 개발**: 랜딩 페이지, Article 목록/상세 페이지 컴포넌트 개발
4.  **기능 개발**: Markdown 파싱, 검색, 카테고리/태그 기능 개발
5.  **테스트**: 개발된 기능 테스트 및 버그 수정
6.  **배포**: Netlify를 이용한 배포
7.  **유지보수**: 지속적인 업데이트 및 기능 추가

## 참고 자료

*   **Next.js 공식 문서**: [https://nextjs.org/docs](https://nextjs.org/docs)
*   **remark**: [https://github.com/remarkjs/remark](https://github.com/remarkjs/remark)
*   **react-markdown**: [https://www.npmjs.com/package/react-markdown](https://www.npmjs.com/package/react-markdown)
*   **Tailwind CSS**: [https://tailwindcss.com/blog/tailwindcss-v3](https://tailwindcss.com/blog/tailwindcss-v3)