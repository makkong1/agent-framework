이 프로젝트의 변경 사항을 리뷰하라.

## 먼저 읽을 문서

- `/CLAUDE.md`
- `/docs/ARCHITECTURE.md`
- `/docs/ADR.md`
- (웹/UI 이슈가 있으면) `/docs/UI_GUIDE.md`

`API_CONVENTIONS.md` 등 이 저장소에 **없는 파일**은 건너뛴다.

## 변경분 확인

`git diff`, `git status` 또는 사용자가 지정한 파일로 변경 범위를 파악한다.

## 체크리스트

1. **아키텍처 준수**: `ARCHITECTURE.md`에 정의된 구조·흐름과 맞는가? (템플릿 그대로면 그 사실을 비고에 쓴다.)
2. **기술 스택 준수**: `ADR.md`의 결정을 벗어나지 않았는가?
3. **테스트**: 새/변경된 동작에 테스트가 있는가? (`scripts/test_execute.py` 등)
4. **CRITICAL**: `CLAUDE.md`의 CRITICAL(TDD·규칙) 위반이 없는가?
5. **빌드/검증**: 실제 존재하는 커맨드로 통과하는가? (예: `python3 -m pytest scripts/test_execute.py` — `package.json` 없으면 `npm` 전제는 불일치로 표시)

## 출력 형식

### 요약

한 단락.

### 이슈 표 (Critical / Warning / Info)

| 심각도 | 제목 | 위치/파일 | 설명 | 제안 |
|--------|------|-----------|------|------|
| Critical / Warning / Info | | | | |

### 체크리스트

| 항목 | 결과 | 비고 |
|------|------|------|
| 아키텍처 준수 | ✅/❌/N/A | |
| 기술 스택 준수 | ✅/❌/N/A | |
| 테스트 | ✅/❌/N/A | |
| CRITICAL 규칙 | ✅/❌/N/A | |
| 빌드·검증 | ✅/❌/N/A | |

**Critical ≥ 1**이면 `/fix` 또는 `/refactor`로 정리한 뒤 `/test` → `/commit` → `/docs-sync` (상세는 `/workflow`).

위반·개선이 있으면 **구체적 수정 방안**을 쓴다.
