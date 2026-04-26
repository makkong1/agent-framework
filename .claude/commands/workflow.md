# 워크플로 (메타)

이 파일은 **기능**이라기보다 **권장 순서**를 고정한다. 다른 `.claude/commands/*.md`의 「연계」는 아래 순서를 따른다.

## 전체 맵

| 파일 | 슬래시 | 역할 한 줄 |
|------|--------|------------|
| `workflow.md` | (메타) | 파이프라인 총정리 — 아래 순서의 기준 |
| `review.md` | `/review` | 변경분을 `CLAUDE.md`·`docs/*`로 체크리스트 리뷰 |
| `fix.md` | `/fix` | Troubleshooting — 버그·에러·재현 실패 시 흐름 |
| `refactor.md` | `/refactor` | 구조·성능·가독성 리팩터, 보통 `/review` 다음 |
| `test.md` | `/test` | 변경 기준 테스트 생성·실행 전략 |
| `commit.md` | `/commit` | 스테이징, conventional commit, 민감파일 제외 |
| `docs-sync.md` | `/docs-sync` | 코드 변경 → 영향 받는 `docs/` 매핑·갱신 |
| `harness.md` | `/harness` | `phases/` step — **메인 파이프라인과 별 트랙** |

## 권장 순서

```
코드 수정
  → ① /review
  → ② /fix (버그) 또는 /refactor (설계·성능·가독성)
  → ③ /test
  → ④ /commit
  → ⑤ /docs-sync
```

- `/fix`·`/refactor` 직후에는 **가능하면** `/test`.
- `/review`에서 **Critical ≥ 1**이면 먼저 `/fix` 또는 `/refactor`로 정리.

## `/commit` 시 주의 (요약)

- `--force` push, 민감 파일(`.env`, 키, 토큰) 커밋 금지.
- 스테이징 전 `git status`로 의도한 파일만 포함했는지 확인.
