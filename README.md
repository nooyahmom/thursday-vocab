# 목요일 영어 단어장 · Thursday Vocab

목요일 영어 시험 대비용 단어 학습 웹앱입니다. 이름·가족·위치 등 개인정보는 넣지 않은 익명 버전입니다.

## 폴더 구성

| 파일 | 설명 |
|---|---|
| `index.html` | 단어장 웹앱 (이 파일 하나만 열어도 그림·영영 뜻·음성 모두 동작) |
| `assets/*.webp` | 단어 10개 2D 그림 (384×384). `index.html` 안에도 같은 그림이 base64로 들어 있어서 없어도 화면은 똑같이 나옵니다. 나중에 그림을 바꿀 때 쓰는 원본입니다. |
| `robots.txt` | 검색엔진 수집 차단 (`Disallow: /`) |
| `.nojekyll` | GitHub Pages에서 Jekyll 처리를 건너뛰게 하는 빈 파일 |

- 앱 기능: 📖 단어 카드(그림·영어 단어·영영 뜻·예문) / 🧩 스펠링 블록 / ✏️ 실전 받아쓰기
- 단어 10개: reindeer, trustworthy, brilliant, antler, graceful, strength, steady, sleigh, muscle, elegance
- 카드의 영영 뜻과 예문은 같은 모양의 파스텔 박스(영영 뜻=보라, 예문=민트)로 묶여 있고, 각 박스 오른쪽 위 `🔊 듣기` 버튼으로 그 내용을 읽어 줍니다. 한글 발음·음절 표기·한글 뜻은 넣지 않았습니다.
- 그림은 단어 카드와 스펠링 힌트에서 보이고, 받아쓰기 문제 화면에서는 숨겨져 있습니다. 받아쓰기 **정답 확인** 화면에서만 다시 보입니다.

## 개인정보 보호

- 아이 이름, 가족 이름, 집 주소, 계정 핸들 등 개인을 알아볼 수 있는 문자열을 파일·파일명·HTML 제목·주석·변수·`localStorage` 키 어디에도 넣지 않았습니다.
- `<head>`에 `<meta name="robots" content="noindex, nofollow">`를 넣고 `robots.txt`로 검색엔진 수집을 막아 두었습니다.

## GitHub Pages 로 올리는 방법

1. github.com 에서 새 저장소(Repository)를 만듭니다. 이름: `thursday-vocab`, 공개 범위: Public
2. 이 폴더 안의 파일들(`index.html`, `assets` 폴더, `README.md`, `robots.txt`, `.nojekyll`)을 저장소 `main` 브랜치에 올립니다.
   - 이미 로컬에서 커밋해 두었다면: `git push -u origin main`
   - 웹페이지에서 올릴 때는 `Add file → Upload files` 로 끌어다 놓으면 됩니다. (`.nojekyll`처럼 점으로 시작하는 파일은 업로드가 안 될 수 있으니 `git push`를 권장합니다.)
3. 저장소의 `Settings → Pages` 로 갑니다.
4. `Build and deployment` 의 Source 를 **Deploy from a branch**, Branch 를 **main / (root)** 로 고르고 저장합니다.
5. 1~2분 뒤 `https://<아이디>.github.io/thursday-vocab/` 주소로 열립니다. (아이패드 사파리에서 열고 "홈 화면에 추가" 하면 앱처럼 쓸 수 있어요.)

## 참고

- 음성은 기기(아이패드/아이폰)에 들어 있는 영어 음성(Siri 목소리)을 씁니다. 소리가 안 나면 음량을 올리고 화면을 한 번 눌러 주세요.
- 외운 단어 체크와 최고 기록은 브라우저에 저장됩니다. (사생활 보호 모드에서는 저장되지 않을 수 있어요.)
- 시험 날짜는 `index.html` 안 `var EXAM = new Date(2026, 10, 26);` 한 줄만 고치면 됩니다. (월은 0부터 시작하므로 10 = 11월)
