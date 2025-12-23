# 프로젝트 빌드 및 기동 가이드

이 문서는 프로젝트의 구조와 빌드, 기동 방법에 대해 설명합니다.

## 1. 프로젝트 구조

```
.
├── public/              # 정적 파일 (이미지, 아이콘 등)
├── src/                 # 소스 코드
│   ├── assets/          # 빌드 시 처리되는 에셋
│   ├── components/      # Astro 컴포넌트
│   ├── content/         # 콘텐츠 컬렉션 (블로그 포스트 등)
│   ├── data/            # 데이터 파일
│   ├── layouts/         # 레이아웃 컴포넌트
│   ├── pages/           # 페이지 라우팅
│   ├── plugins/         # 플러그인
│   ├── styles/          # 전역 스타일
│   ├── utils/           # 유틸리티 함수
│   ├── content.config.ts # 콘텐츠 설정
│   └── site.config.ts   # 사이트 설정
├── astro.config.ts      # Astro 설정 파일
├── biome.json           # Biome 설정 (Lint/Format)
├── package.json         # 프로젝트 의존성 및 스크립트
├── tailwind.config.ts   # Tailwind CSS 설정
└── tsconfig.json        # TypeScript 설정
```

## 2. 사전 요구 사항

이 프로젝트를 실행하기 위해서는 다음 도구들이 설치되어 있어야 합니다.

- **Node.js**: v18 이상 권장
- **pnpm**: 패키지 매니저

## 3. 설치 (Installation)

프로젝트 의존성을 설치합니다.

```bash
pnpm install
```

## 4. 개발 서버 실행 (Development)

로컬 개발 서버를 실행합니다.

```bash
pnpm dev
```

실행 후 브라우저에서 `http://localhost:4321` (또는 터미널에 표시된 주소)로 접속하여 확인할 수 있습니다.

## 5. 빌드 (Build)

프로덕션 배포를 위해 프로젝트를 빌드합니다.

```bash
pnpm build
```

빌드된 결과물은 `dist/` 디렉토리에 생성됩니다.

## 6. 미리보기 (Preview)

빌드된 결과물을 로컬에서 미리 확인합니다.

```bash
pnpm preview
```

## 7. 기타 명령어

- **Lint**: 코드 스타일 검사
  ```bash
  pnpm lint
  ```
- **Format**: 코드 포맷팅
  ```bash
  pnpm format
  ```
- **Check**: Astro 타입 체크
  ```bash
  pnpm check
  ```
