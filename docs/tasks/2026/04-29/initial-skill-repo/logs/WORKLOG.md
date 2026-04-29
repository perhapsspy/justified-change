**2026-04-29**
- 한국어/영어 README, MIT 라이선스, 영문/한국어 스킬 문서, 재개 가능한 최소 project-context 표면으로 독립 스킬 저장소 구조를 만들었다. 애플리케이션 코드가 없어서 검증은 Markdown 확인 중심이다.
- 저장소 노트용 AGENTS.md, 스킬 방향, 기본 ignore 규칙을 추가했다. 과한 검사/테스트 레이어는 제거했고, README는 sibling skill 저장소 형태의 사용자 진입점으로 유지했다.
- sibling skill README 형태에 맞춰 지원/라이선스 푸터를 유지하고, AGENTS.md의 README 역할 경계에도 이 기본 안내를 포함했다.
- 저장소에 노출되는 표면을 sibling `interactive-state-flow` skill의 핵심 흐름에 맞췄다. README는 요약/빠른 시작/사용 사례/프로젝트 가치/지원/라이선스 구조를 쓰고, AGENTS.md는 배포 스킬 경계를 명시하며, `skills/justified-change/agents/openai.yaml`은 OpenAI interface metadata를 제공한다.
- 리뷰 도그푸딩을 시작해 배포 스킬에 작은 실행 흐름을 추가하고, UI 메타데이터의 `scoped` 표현을 `proportional`로 맞췄다.
- repo-local 예시 문서는 스킬 사용자 런타임에 의미가 약해 제거했다.
- 2차 리뷰를 반영해 저장소 로컬 reference/task 문서를 한국어 기본으로 맞추고, BRIEF의 작업 경계를 현재 리뷰 범위까지 갱신했다.
