# Docs sync (`/docs-sync`)

## 원칙

**코드·실제 설정이 진실.** 문서는 그에 맞게 갱신한다.

## 이 저장소의 `docs/` (flat)

| 문서 | 용도 (대략) |
|------|-------------|
| `docs/ARCHITECTURE.md` | 디렉터리·흐름 |
| `docs/ADR.md` | 기술 결정 |
| `docs/PRD.md` | 제품·MVP |
| `docs/UI_GUIDE.md` | UI 토큰·안티패턴 |

`API_CONVENTIONS.md` 등은 **없으면** 만들지 않아도 됨 — 변경이 API 계약을 도입할 때만 추가 검토.

## 변경 유형 → 볼 문서 (가이드)

| 코드 변경 | 우선 볼 문서 |
|-----------|----------------|
| `scripts/` 실행·CLI | `ARCHITECTURE.md`, `CLAUDE.md` 명령 섹션 |
| 의존성·런타임 결정 | `ADR.md` |
| 사용자 기능·범위 | `PRD.md` |
| UI/스타일 (해당 시) | `UI_GUIDE.md` |

## 출력

- 갱신한 `docs/*.md` 경로
- "코드만 맞고 문서는 옛날" 이슈가 있으면 항목별로 정리
