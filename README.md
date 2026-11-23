# 여행 계획표 웹 뷰어

플래너가 노션에 입력한 여행 계획표를 클라이언트가 **공유 링크 하나로 웹에서 확인**하고 **PDF로 다운로드**할 수 있는 서비스입니다. (MVP)

## 주요 기능

- **여행 개요 표시** - 제목, 고객명, 목적지, 기간, 플래너 메모
- **Day별 일정 표시** - 날짜별 타임라인 (시간·장소·활동·메모)
- **PDF 다운로드** - 화면과 동일한 구성의 A4 PDF (한글 폰트 포함)
- **공유 링크 접근 제어** - 랜덤 공유 토큰 + '발행' 상태만 공개
- **노션 데이터 연동** - 노션 데이터베이스가 CMS 역할

자세한 요구사항은 [`docs/PRD.md`](docs/PRD.md)를 참고하세요.

## 기술 스택

- Next.js 15.5.3 (App Router + Turbopack), React 19, TypeScript 5
- TailwindCSS v4, shadcn/ui, Lucide Icons
- Notion API (`@notionhq/client`), `@react-pdf/renderer`, Zod
- ESLint, Prettier, Husky, lint-staged

## 시작하기

```bash
npm install
npm run dev
```

브라우저에서 http://localhost:3000 을 엽니다.

### 환경변수

`.env` 파일을 만들어 설정합니다. (저장소에는 포함되지 않습니다.)

```bash
NOTION_API_KEY=
NOTION_TRIPS_DATA_SOURCE_ID=
NOTION_ITEMS_DATA_SOURCE_ID=
```

## 주요 명령어

```bash
npm run dev         # 개발 서버 (Turbopack)
npm run build       # 프로덕션 빌드
npm run check-all   # 타입체크 + 린트 + 포맷 검사
```

## 문서

- [PRD](docs/PRD.md)
- [프로젝트 구조](docs/guides/project-structure.md)
- [스타일링 가이드](docs/guides/styling-guide.md)
- [컴포넌트 패턴](docs/guides/component-patterns.md)
