# ys-review 스킬

BetterWealth CTO 영수님의 리뷰 스타일을 재현하는 사전 검토 스킬. 문서·스킬·PR·코드 작성 후 실제 영수님에게 가기 전 동일 기준으로 pre-review하여 팀원의 스트레스·재작업을 줄이는 것이 목적이다.

> 작성 시작: 2026-04-15
> 정본(canonical): `~/.claude/CLAUDE.md` — 본 README는 사람용 사본. 영수님 협업 가이드 원문은 정본에 있음.

## 사용법

| 항목 | 내용 |
|------|------|
| 수동 호출 | `/ys-review` |
| 자동 트리거 | 영수님 사전 검토 요청, 스킬 PR 리뷰, mydata 기준 정합성 점검, PR 본문·문서 정합성 점검 시 |

## 참조 파일 구조

```
references/
  2026-04-15-pr-1215-design-system-bw-app.md   design-system-bw-app 스킬 PR 사전 리뷰 (간접)
  2026-04-14-readme-vs-skill-md.md             README vs SKILL.md 문서 성격 구분 (직접)
  2026-04-16-spec-md.md                        SPEC.md 작성 시 심층인터뷰 요청 필수 (직접)
  2026-04-16-spec-md-workflow-spec.md           SPEC.md 작성 시 workflow-spec 스킬 필수 사용 지시 (직접)
  2026-04-16-user-story.md                     유저스토리 상세 작성 필수 — 후속 산출물의 기초 (직접)
```

2026-04-15 기준 사례 2건 (직접 1·간접 1). 직접 증거가 들어오기 시작했다 — 해당 항목은 관찰형 인용 가능.

새 사례를 추가할 때는 **`/ys-log`** 호출을 권장 — 네 파일(references·SKILL.md·README.md·프로젝트 CLAUDE.md) 동시 업데이트를 강제한다.

## 자매 스킬

- `log-skill/` — ys-log 등록 도구. 새 사례를 `references/`에 쓰고 `SKILL.md`·`README.md`·프로젝트 `CLAUDE.md`를 동시 갱신. 상세: [`log-skill/README.md`](log-skill/README.md).

## 유지보수

- **새 사례 등록**: `references/YYYY-MM-DD-<slug>.md` 파일 생성 후 (1) `SKILL.md`의 `## 참조 문서 안내` 테이블, (2) 이 README의 `## 참조 파일 구조` 블록, (3) 프로젝트 `CLAUDE.md`의 `## 파일 구조` → `references/` 목록에 **동시 추가**. 세 곳 중 하나라도 누락되면 영수님이 바로 짚음.
- **증거 등급 유지**: 각 사례 파일은 맨 앞에 증거 등급(직접/간접)을 명시한다. **간접 증거 기반 지적은** 예측형("영수님 기준이라면 이 부분을 짚을 가능성이 높다")으로만 서술하고, **직접 증거 항목만** 관찰형("영수님은 이렇게 말한다") 인용 허용.
- **정본-사본 구분**: `~/.claude/CLAUDE.md`가 정본(canonical). 본 README는 사람용 사본 — 프로젝트 구조·운영 규칙에 한정하고, 영수님 협업 가이드 원문은 정본에만 유지한다.
- **파일명·섹션명 변경 시**: `SKILL.md`·`README.md`·프로젝트 `CLAUDE.md`·`log-skill/SKILL.md`·`log-skill/README.md`·`references/` 내부의 상호 참조를 모두 함께 수정.

## 출처

- **영수님 협업 가이드 원문 위치**: `~/.claude/CLAUDE.md` (정본). 본 사본에는 포인터만 유지.
- **스킬 구조 표준**: `better-wealth-pb/skills/mydata` (영수님 본인이 반복 인용하는 기준 — README 섹션 구성, SKILL.md description 작성 방식, 참조 문서 표 등).
- **사례 데이터**: `references/` 하위 사례 파일. 현재 직접 1·간접 1. 직접 리뷰 로그가 쌓일수록 페르소나 정확도가 올라간다.

## TODO

- [ ] **직접 증거 사례 수집**: 영수님이 실제로 남긴 리뷰 코멘트(PR 리뷰·Teams·회의록)를 `references/`에 직접 인용 형태로 등록. 현재 직접 1건(2026-04-14). 샘플 확장 필요.
- [ ] **사례 누적 후 패턴 문서화**: 사례가 3건 이상 쌓이면 공통 패턴을 별도 `references/review-style.md`로 정리(현재는 샘플 부족으로 일반화 금지).
