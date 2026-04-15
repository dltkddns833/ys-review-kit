# ys-log 스킬

ys-review 스킬의 페르소나 데이터(`references/`)를 일관된 형태로 등록하기 위한 관리 도구. ys-review와 같은 트리 안(`~/Desktop/personal/cto/log-skill/`)에 배치된 **자매 스킬**이다.

## 사용법

| 항목 | 내용 |
|------|------|
| 수동 호출 | `/ys-log` |
| 자동 트리거 | "영수님 코멘트 기록해줘", "이 사례 references에 등록", "새 리뷰 로그 추가" 등 — SKILL.md `description` 기반 |
| 응답 모드 | **도구(assistant) 모드.** 영수님 페르소나를 재현하지 않는다. |

## 참조 파일 구조

```
log-skill/
  SKILL.md    절차·템플릿·규칙
  README.md   본 파일
```

이 스킬은 자기 폴더 밖의 파일도 쓴다 — 대상 경로는 모두 `SKILL.md` 상단에 절대 경로로 명시.

| 쓰기 대상 | 역할 |
|---|---|
| `/Users/isang-un/Desktop/personal/cto/references/YYYY-MM-DD-<slug>.md` | 신규 사례 파일 |
| `/Users/isang-un/Desktop/personal/cto/SKILL.md` | `## 참조 문서 안내` 테이블에 행 추가 |
| `/Users/isang-un/Desktop/personal/cto/README.md` | `## 참조 파일 구조` 블록에 줄 추가 |
| `/Users/isang-un/Desktop/personal/cto/CLAUDE.md` | `## 파일 구조` → `references/` 목록에 줄 추가 |

## 유지보수

- **템플릿 변경 시**: 기존 `references/*.md` 도 같은 구조로 맞춰야 영수님이 짚음. SKILL.md 템플릿만 고치면 불일치.
- **증거 등급 체계 변경 시** (예: "반직접" 추가): SKILL.md `## 절대 규칙` 2번과 템플릿·응답 포맷 모두 업데이트.
- **ys-review 파일 구조 변경 시** (예: `references/` → 다른 경로): 이 스킬의 절대 경로들(SKILL.md 상단 쓰기 대상 목록·실행 절차 단계)을 모두 함께 수정.
- **심링크 확인**: `~/.claude/skills/ys-log` 가 실제로 이 폴더를 가리키는지 로드 안 될 때 점검.

## 출처

- 상위 스킬: [ys-review](../SKILL.md) · [CLAUDE.md](../CLAUDE.md) `## 새 사례를 추가할 때`
- 사례 템플릿 원형: [2026-04-15-pr-1215-design-system-bw-app.md](../references/2026-04-15-pr-1215-design-system-bw-app.md)
- mydata 스킬 구조(README·SKILL.md 섹션 구성): 영수님 본인이 반복 인용하는 표준. `~/better-wealth-pb/skills/mydata/`

## TODO

- [ ] **일괄 등록 모드**: 여러 사례를 한꺼번에 입력할 때의 흐름 정의 (현재는 1건 단위).
- [ ] **직접/간접 자동 판별 힌트**: 출처 문자열에 "상운 사전 리뷰"가 들어있으면 간접으로 기본 세팅 등. 현재는 사용자가 명시.
