# 오늘 뭐 먹지? 🍱 — 자취생 메뉴 랜덤 추천

자취생을 위한 메뉴 랜덤 추천 웹앱입니다. 카테고리를 고르면 슬롯머신 스타일 애니메이션과 함께 메뉴를 무작위로 뽑아줍니다.

## 주요 기능

- **3가지 카테고리** — 종합메뉴 / 재료별메뉴 / 상황별메뉴 중 골라서 시작
- **슬롯/빙고 스타일 애니메이션** — 점점 느려지다 멈추는 추첨 연출
- **다시 뽑기** — 결과가 마음에 안 들면 즉시 재추출
- **공유·복사** — 모바일에선 공유 시트, PC에선 클립보드 복사
- **최근 추천 기록** — 직전 추천 메뉴들을 칩으로 표시
- **모바일 최적화** — 반응형 레이아웃, 큰 터치 버튼, 안전영역(노치) 대응

총 207종(카테고리별 종합 72 · 재료별 71 · 상황별 64)의 메뉴가 내장되어 있습니다.

## 기술

- 순수 HTML + CSS + JavaScript **단일 파일** (`index.html`)
- 외부 라이브러리·빌드 과정 없음 → 파일 하나로 어디서든 동작
- 메뉴 데이터는 `index.html` 내 `MENU_DATA` 객체에 내장

## 로컬 실행

`index.html`을 브라우저로 열기만 하면 됩니다. (더블클릭 또는 브라우저에 드래그)

## GitHub Pages 배포 방법

1. GitHub에서 새 저장소(repository)를 만듭니다. (예: `pick-menu`)
2. 이 폴더의 `index.html`과 `README.md`를 저장소에 업로드(또는 push)합니다.
3. 저장소 페이지에서 **Settings → Pages** 로 이동합니다.
4. **Source**를 `Deploy from a branch`로 두고, **Branch**를 `main` / 폴더는 `/ (root)`로 선택 후 **Save**.
5. 잠시 기다리면 `https://<your-id>.github.io/pick-menu/` 주소로 공개됩니다.

> `index.html`이 저장소 최상위(root)에 있어야 바로 열립니다.

### 명령어로 올리는 경우

```bash
git init
git add index.html README.md
git commit -m "오늘 뭐 먹지 메뉴 추천 앱"
git branch -M main
git remote add origin https://github.com/<your-id>/pick-menu.git
git push -u origin main
```

이후 위 4~5단계(Settings → Pages)를 진행하면 됩니다.

## 메뉴 추가/수정

`index.html`을 열고 `MENU_DATA` 객체에서 원하는 카테고리의 서브그룹 배열에 메뉴를 추가하거나 수정하면 됩니다. 별도 빌드 없이 저장 후 새로고침하면 바로 반영됩니다.
