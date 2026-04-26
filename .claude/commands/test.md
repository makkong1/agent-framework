# Test (`/test`)

## 목적

최근 변경에 맞춰 **테스트를 추가·수정·실행**한다. (TDD는 `CLAUDE.md` CRITICAL 준수.)

## 이 저장소 (harness_framework)

| 구분 | 경로·명령 (기본) |
|------|------------------|
| 하네스 | `scripts/execute.py` |
| 테스트 | `scripts/test_execute.py` |
| 실행 | `python3 -m pytest scripts/test_execute.py` |

`package.json`이 없으면 `npm test` 등 npm 기반 검증은 **문서·hooks와 불일치**일 수 있음 — 실제 존재하는 커맨드로 대체.

## 전략

1. 변경된 모듈·함수에 대한 단위 테스트 우선
2. 통합이 필요하면 임시 디렉터리·픽스처 패턴 기존 테스트에 맞출 것
3. 실패 시 원인 → 최소 수정 → 재실행

## 출력

- 실행한 명령
- 통과/실패 요약
- 추가한 테스트 파일·케이스 목록
