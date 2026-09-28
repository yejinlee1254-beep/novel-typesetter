# 소설 조판기

브라우저에서 원고를 A5/B6/A4 페이지로 자동 조판하고 PDF로 저장하는 정적 웹앱입니다.

## KoPub 폰트 넣기

라이선스를 확인한 뒤 허용되는 KoPub 폰트 파일을 `fonts/KoPubBatang.woff2` 경로에 두고, `index.html`의 `<style>` 맨 위에 아래를 추가하세요.

```css
@font-face {
  font-family: 'KoPubBatang';
  src: url('./fonts/KoPubBatang.woff2') format('woff2');
  font-display: swap;
}
```

폰트 파일은 이 샘플에 포함하지 않았습니다.

## GitHub Pages

1. 새 GitHub 저장소를 만듭니다.
2. `index.html`, `README.md`를 저장소 루트에 올립니다.
3. Settings → Pages → Build and deployment → Source에서 `Deploy from a branch`를 선택합니다.
4. `main` / `(root)`를 선택하고 저장합니다.

## 현재 기능

- A5/B6/A4
- 원고 자동 페이지 분할
- 글자 크기, 행간, 자간, 장평
- 첫 줄 들여쓰기, 문단 간격
- 상하/안쪽/바깥쪽 여백
- 홀짝 제본 여백
- 양쪽 정렬
- 반복 말머리
- 자동 쪽번호
- 모바일/태블릿 대응
- 브라우저 인쇄 기능을 이용한 PDF 저장
- 설정/원고 로컬 저장

## 참고

브라우저별 글꼴 렌더링과 인쇄 엔진 차이 때문에 화면 미리보기와 PDF의 줄바꿈이 아주 미세하게 달라질 수 있습니다. 출판용 PDF 수준의 완전한 재현성이 필요하면 후속 버전에서 전용 PDF 생성 엔진을 붙이는 편이 좋습니다.
