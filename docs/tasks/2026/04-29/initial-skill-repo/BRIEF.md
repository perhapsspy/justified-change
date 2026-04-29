# 초기 스킬 저장소

## 목표

- 첫 독립 `justified-change` 스킬 저장소를 만든다.

## 범위

- 요청된 README, 라이선스, 설치 가능한 스킬 파일을 만든다.
- 스킬은 간결하고 독립적이며 변경 비례성에 집중하게 유지한다.
- 다음 세션이 저장소 파일만으로 이어갈 수 있도록 최소한의 project-context를 남긴다.

## 현재 사실

- 기본 README 언어는 한국어이고, 영어는 `README.en.md`에 둔다.
- 설치 가능한 스킬 경로는 `skills/justified-change/`다.
- `SKILL.md`는 영문 frontmatter를 가지며, `SKILL.ko.md`는 frontmatter 없는 한국어 페어다.
- README는 sibling `interactive-state-flow` 저장소 형태를 따르되, 프로젝트 가치 보존 시리즈 블록과 짧은 지원/라이선스 안내를 포함한다.
- 현재 저장소는 Markdown 중심이므로 애플리케이션 테스트는 범위에 없다.

## 현재 상태

- 초기 저장소 내용이 있고, README와 저장소 지침은 sibling skill 저장소 구조에 맞춰져 있다.
- 리뷰 도그푸딩을 통해 shipped skill에 실행 흐름과 직접 영향 범위 기준을 보강했다.
- repo-local 예시 문서는 스킬 사용자 런타임에 의미가 약해 제거했다.
- README footer는 공개 저장소의 기본 지원/라이선스 안내로 유지하고, `AGENTS.md`의 README 역할 경계에도 포함했다.

## 다음 단계

- 현재 문구를 최종 검토한 뒤 커밋/배포 여부를 결정한다.

## 작업 경계

- `README.md`
- `README.en.md`
- `docs/skill-direction.md`
- `docs/reference/skill-repository.md`
- `docs/tasks/2026/04-29/initial-skill-repo/`
- `skills/justified-change/SKILL.md`
- `skills/justified-change/SKILL.ko.md`
- `skills/justified-change/agents/openai.yaml`
