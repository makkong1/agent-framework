# Commit (`/commit`)

## 절차

1. `git status` — 의도한 파일만 스테이징
2. **제외**: `.env`, 키, `*.pem`, 대용량 비의도 산출물, `phases/**/phase*-output.json` 등 (`.gitignore` 준수)
3. **메시지**: Conventional Commits + 한국어 본문 허용

## 형식 (예)

```
feat(scripts): phase 실행 시 에러 메시지 보강

fix: …
docs: …
refactor: …
test: …
```

- `type`: `feat` | `fix` | `docs` | `refactor` | `test` | `chore` …
- `scope`(선택): `scripts` | `docs` | `phases` | `claude` 등 이 프로젝트에 맞게

## Push (선택)

- 기본은 로컬 커밋만.
- `git push`가 필요하면 사용자가 명시할 때만.
