# 의약 CSO 솔루션 홈페이지

의약 CSO 영업·정산·컴플라이언스 통합 관리 솔루션 공식 홈페이지

## 프로젝트 개요

- **목적**: 의약품 계약영업조직(CSO) 대상 B2B SaaS 솔루션 마케팅
- **구조**: 단일 페이지 애플리케이션 (SPA)
- **기술**: HTML5, CSS3, Vanilla JavaScript
- **반응형**: Mobile, Tablet, Desktop 지원

## 파일 구조

```
project/
├── index.html          # 메인 HTML 파일
├── styles.css          # 스타일시트
├── script.js           # JavaScript 인터랙션
├── sitemap.xml         # SEO 사이트맵
├── robots.txt          # 검색엔진 크롤러 설정
├── netlify.toml        # Netlify 배포 설정
├── vercel.json         # Vercel 배포 설정
├── 배포가이드.md        # 상세 배포 가이드
└── README.md           # 본 파일
```

## 주요 섹션

1. **Hero Section** - 메인 가치 제안
2. **Problem Section** - CSO 운영 문제점 제시
3. **Solution Overview** - 솔루션 개요
4. **Features Section** - 4대 핵심 기능
5. **Compliance Section** - 컴플라이언스 대응
6. **Benefits Section** - 도입 효과
7. **Target Section** - 타겟 고객
8. **Implementation Section** - 도입 방식
9. **Pricing Section** - 요금 안내
10. **Contact Section** - 문의 폼

## 빠른 시작

### 로컬 개발 환경

```bash
# 프로젝트 디렉토리로 이동
cd cso-solution

# 간단한 HTTP 서버 실행 (Python)
python -m http.server 8000

# 또는 Node.js 사용
npx http-server

# 브라우저에서 접속
# http://localhost:8000
```

### Netlify 배포 (권장)

**방법 1: 드래그 앤 드롭**
1. https://netlify.com 접속 및 가입
2. "Add new site" → "Deploy manually"
3. 프로젝트 폴더 드래그 앤 드롭
4. 배포 완료

**방법 2: CLI**
```bash
npm install -g netlify-cli
netlify login
netlify deploy --prod
```

### Vercel 배포

```bash
npm install -g vercel
vercel login
vercel --prod
```

### GitHub Pages 배포

```bash
# Git 초기화
git init
git add .
git commit -m "Initial commit"

# GitHub 저장소 연결
git remote add origin [YOUR_REPO_URL]
git push -u origin main

# Settings → Pages에서 활성화
```

## 기능

### 사용자 경험
- ✅ 스무스 스크롤 네비게이션
- ✅ Intersection Observer 기반 애니메이션
- ✅ 반응형 디자인 (모든 디바이스)
- ✅ 접근성 고려 (Semantic HTML)

### 폼 기능
- ✅ 실시간 유효성 검증
- ✅ 이메일 형식 검증
- ✅ 전화번호 형식 검증
- ✅ 알림 시스템

### 성능
- ✅ 경량화 (외부 라이브러리 미사용)
- ✅ 이미지 Lazy Loading 지원
- ✅ CSS/JS 최소화 준비 완료

## 브라우저 지원

- Chrome (최신)
- Firefox (최신)
- Safari (최신)
- Edge (최신)
- Mobile Safari (iOS 12+)
- Chrome Mobile (Android 8+)

## 성능 지표 (목표)

- Lighthouse Performance: 90+
- First Contentful Paint: < 1.5s
- Largest Contentful Paint: < 2.5s
- Time to Interactive: < 3.0s

## 커스터마이징

### 색상 변경

`styles.css`의 CSS 변수 수정:

```css
:root {
    --primary-color: #2563eb;    /* 메인 컬러 */
    --secondary-color: #1e40af;  /* 보조 컬러 */
    --accent-color: #60a5fa;     /* 강조 컬러 */
}
```

### 콘텐츠 수정

`index.html`에서 직접 텍스트 수정 가능

### 이미지 추가

```html
<!-- placeholder-image 클래스를 실제 이미지로 교체 -->
<div class="hero-image">
    <img src="images/dashboard.png" alt="Dashboard Preview">
</div>
```

## 보안 설정

### 헤더 설정 (이미 적용됨)
- X-Frame-Options: DENY
- X-Content-Type-Options: nosniff
- X-XSS-Protection: 1; mode=block

### HTTPS
- Netlify/Vercel: 자동 SSL
- AWS S3: CloudFront에서 SSL 설정
- 전통적 서버: Let's Encrypt 사용

## SEO 최적화

### 메타 태그 (이미 적용됨)
```html
<meta name="description" content="...">
<meta name="keywords" content="...">
```

### 사이트맵
- `sitemap.xml` 포함
- Google Search Console 등록 권장

### 구조화된 데이터
추후 추가 가능:
- Organization Schema
- WebSite Schema
- BreadcrumbList Schema

## 분석 도구 통합

### Google Analytics (추가 예정)

`index.html`의 `<head>` 내 추가:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## 문제 해결

### CSS가 적용되지 않음
```bash
# 파일 경로 확인
ls -la

# 권한 확인
chmod 644 styles.css
```

### JavaScript 오류
브라우저 개발자 도구(F12) → Console 탭에서 오류 확인

### 폼이 작동하지 않음
- `script.js`가 로드되었는지 확인
- 브라우저 Console에서 오류 확인
- 백엔드 API 연결 필요 시 별도 구현

## 다음 단계

### Phase 1: 콘텐츠 보완
- [ ] 실제 대시보드 스크린샷 추가
- [ ] 고객 사례(Case Study) 섹션
- [ ] FAQ 섹션 추가
- [ ] 팀 소개 페이지

### Phase 2: 기능 확장
- [ ] 백엔드 API 연동 (폼 제출)
- [ ] 챗봇 통합 (채널톡, 인터콤)
- [ ] 블로그 연동
- [ ] 다국어 지원 (영어)

### Phase 3: 마케팅 최적화
- [ ] A/B 테스트 설정
- [ ] 전환율 추적
- [ ] 히트맵 분석 (Hotjar)
- [ ] 광고 픽셀 통합

## 라이선스

Copyright © 2026 CSO Solution. All rights reserved.

## 지원

- 이메일: info@cso-solution.com
- 전화: 02-XXXX-XXXX

## 버전 히스토리

- **v1.0.0** (2026-02-04)
  - 초기 릴리스
  - 단일 페이지 구조
  - 반응형 디자인
  - 기본 SEO 설정
