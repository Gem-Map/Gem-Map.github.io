# Gemmap: Team Blog & Project Documentation

이 문서는 **Gemmap** 팀 블로그 프로젝트의 핵심 정보와 설계 원칙을 담고 있습니다. 다른 AI 모델이나 개발자가 프로젝트의 문맥을 빠르게 파악할 수 있도록 돕기 위해 작성되었습니다.

## 💎 Project Overview
- **Service Name**: Gemmap (젬맵)
- **Core Vision**: 숨겨진 보석 같은 사진 스팟을 찾는 서비스.
- **Content Space**: "Gem있는 Writing" - 팀의 여정, 기술 인사이트, 기록을 담는 블로그 공간.

## 🛠 Tech Stack
- **Framework**: Astro (v6+)
- **Styling**: Tailwind CSS v4 (Modern, Clean, High-Contrast)
- **Content**: Markdown-based local files (`src/content/blog/`)
- **SEO**: `astro-seo` integration for dynamic meta tags.
- **Deployment**: GitHub Pages (via GitHub Actions)

## 🎨 Design System (Gemmap Brand Colors)
제공된 Flutter `AppColors` 시스템을 CSS 테마로 이식했습니다.

### Core Colors
- **Background (Light)**: `#FFFFFF` (Pure White)
- **Background (Dark)**: `#101014` (GrayScale0)
- **Primary (Key Color)**: `#00BFC2` (Teal/Mint) - 보석의 청량함을 상징.
- **Secondary (Accent)**: `#00DB9D` (Green/Mint) - 다크 모드 및 포인트 강조용.
- **Card Background**: `#F2F3F8` (GrayScale99) - 화이트 배경과의 대조를 위해 사용.

### UI Components
- **gem-card**: 게시글 목록에 사용되는 카드 UI. 호버 시 `-translate-y-2` 및 그림자 효과.
- **gem-gradient-text**: 브랜드의 정체성을 보여주는 Primary to Secondary 그라데이션 텍스트.
- **gem-tag**: 게시글 카테고리/태그 표시용 뱃지 스타일.

## 📂 Project Structure
- `/src/components/`: 공통 UI 요소 (Header, Footer, ThemeToggle 등)
- `/src/layouts/`: 페이지 레이아웃 (BlogPost 전용 레이아웃 포함)
- `/src/pages/`: 메인 페이지, 블로그 목록, 팀 소개 페이지
- `/src/content/`: 블로그 포스트 데이터 및 스키마 정의 (`content.config.ts`)
- `/src/styles/`: Tailwind v4 설정이 포함된 `global.css`

## 🚀 Key Features
- **Dark Mode**: `class` 전략 기반. 시스템 설정 감지 및 수동 토글 지원. (FOUC 방지 스크립트 포함)
- **Analytics**: GA4 환경 변수(`PUBLIC_GA_ID`) 연동 구조.
- **HITS Badge**: 각 포스트 하단에 실시간 방문자 수 배지 자동 생성.
- **Localization**: 한국어 로케일 적용 (`FormattedDate.astro` - `ko-kr`).

---
*Created by Gemini CLI for Gemmap Project Continuity.*
