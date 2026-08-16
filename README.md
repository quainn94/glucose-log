# glucose-log v0.1 — GitHub Pages

아빠가 휴대폰에서 간단히 쓰는 1인용 혈당 기록 웹앱입니다.

## 기능
- Supabase 이메일/비밀번호 로그인 및 로그인 유지
- 월간 달력형 화면
- 날짜 클릭 → 아침 식전 / 저녁 식전 혈당 입력
- 입력된 날짜 재클릭 → 기존 수치 수정
- 아침 식전 목표 80~120 mg/dL
- 저녁 식전 목표 100~150 mg/dL
- 목표 범위 내 초록 / 범위 밖 빨강 / 미측정 회색
- 이전 달 / 다음 달 이동
- Supabase `glucose_records` 테이블에 데이터 저장

## GitHub Desktop에 넣는 방법
압축을 푼 뒤, 아래 파일들을 `glucose-log` 저장소 폴더의 최상위에 그대로 넣습니다.

```text
glucose-log/
├─ index.html
├─ README.md
├─ supabase.sql
└─ .nojekyll
```

GitHub Desktop에서 변경 파일이 보이면:
1. Summary에 `v0.1` 입력
2. `Commit to main`
3. `Publish repository` 또는 `Push origin`

그 다음 GitHub 웹에서:
`Settings → Pages → Deploy from a branch → main / (root) → Save`

Netlify는 사용하지 않습니다.

## Supabase
앱에는 Publishable key만 들어 있습니다. `sb_secret_...` Secret key는 절대 프론트엔드 코드에 넣지 마세요.
