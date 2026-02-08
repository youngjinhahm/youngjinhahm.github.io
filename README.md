# Ben Evans 스타일 블로그 사용 가이드

## 📁 파일 구조

```
youngjinhahm.github.io/
├── index.html          # 메인 페이지 (글 목록)
├── post-1.html         # 첫 번째 글
├── post-2.html         # 두 번째 글
└── README.md           # 이 파일
```

## 🚀 GitHub Pages에 업로드하는 방법

### 1. 기존 파일들 삭제 (선택사항)

minimal-mistakes 테마 파일들을 정리하고 싶다면:
- `_config.yml`, `_posts/`, `assets/` 등을 삭제해도 됩니다
- 또는 그냥 두고 새 HTML 파일만 추가해도 작동합니다

### 2. HTML 파일 업로드

1. GitHub 저장소 메인 페이지로 이동
2. **Add file** → **Upload files** 클릭
3. `index.html`, `post-1.html`, `post-2.html` 3개 파일을 드래그 앤 드롭
4. **Commit changes** 클릭

### 3. 확인

2-3분 후 `https://youngjinhahm.github.io` 접속하면 새로운 디자인이 보입니다!

---

## ✏️ 새 글 추가하는 방법

### 방법 1: post-2.html 복사해서 만들기

1. GitHub에서 `post-2.html` 파일 열기
2. 내용 전체 복사
3. **Add file** → **Create new file** 클릭
4. 파일명: `post-3.html` (숫자만 바꾸기)
5. 복사한 내용 붙여넣기
6. 내용 수정:
   - `<title>` 태그 안의 제목
   - `<h1 class="article-title">` 안의 제목
   - `<div class="article-date">` 안의 날짜
   - `<div class="article-content">` 안의 본문
7. **Commit new file** 클릭

### 방법 2: index.html에 글 추가

새 글을 만들었으면 메인 페이지에도 추가해야 합니다:

1. `index.html` 파일 열기
2. 연필 아이콘(✏️) 클릭해서 편집
3. `<ul class="essay-list">` 섹션 찾기
4. 맨 위에 새 글 항목 추가:

```html
<li class="essay-item">
    <div class="essay-date">Feb 10, 2026</div>
    <h3 class="essay-title">
        <a href="post-3.html">세 번째 글 제목</a>
    </h3>
    <p class="essay-excerpt">
        글의 간단한 요약을 여기에 작성하세요.
    </p>
</li>
```

5. **Commit changes** 클릭

---

## 🎨 디자인 커스터마이징

### 색상 변경

각 HTML 파일의 `<style>` 태그 안에서 `:root` 섹션을 찾으세요:

```css
:root {
    --bg: #ffffff;          /* 배경색 */
    --text: #1a1a1a;        /* 본문 텍스트 색상 */
    --text-light: #666666;  /* 연한 텍스트 색상 */
    --accent: #0066cc;      /* 강조 색상 (링크 등) */
    --border: #e0e0e0;      /* 테두리 색상 */
}
```

원하는 색상 코드로 변경하면 됩니다!

### 폰트 변경

현재 사용 중인 폰트:
- **제목**: Instrument Serif (세리프 폰트)
- **본문**: IBM Plex Sans (산세리프 폰트)

다른 폰트로 변경하려면:
1. [Google Fonts](https://fonts.google.com)에서 원하는 폰트 선택
2. `<link>` 태그 복사해서 `<head>` 섹션에 추가
3. CSS에서 `font-family` 값 변경

### 개인 정보 수정

`index.html`에서:
- `<div class="site-title">` - 사이트 이름
- `<section class="intro">` - 소개 문구
- `<footer>` - 푸터 정보

---

## 💡 팁

### 빠른 수정
- GitHub에서 파일을 직접 클릭해서 연필 아이콘으로 수정 가능
- 매번 업로드할 필요 없음!

### 반영 시간
- 파일 수정 후 2-3분 기다려야 사이트에 반영됨
- Actions 탭에서 빌드 상태 확인 가능

### 백업
- 중요한 변경 전에는 파일 내용을 복사해두세요
- GitHub는 자동으로 버전 관리를 해주지만, 안전하게!

---

## 🆘 문제 해결

### 사이트가 안 보여요
- Actions 탭에서 빌드가 성공(✅)했는지 확인
- 캐시 문제일 수 있으니 Ctrl + Shift + R로 강력 새로고침

### 디자인이 깨져 보여요
- HTML 태그가 제대로 닫혔는지 확인
- CSS 문법 오류가 없는지 확인
- 브라우저 개발자 도구(F12)에서 에러 확인

### 새 글이 안 나타나요
- `index.html`에 글 항목을 추가했는지 확인
- 파일명과 링크가 일치하는지 확인

---

## 📞 도움이 필요하면

문제가 생기면 언제든 저에게 물어보세요!
