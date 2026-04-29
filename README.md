# Justified Change

[한국어](README.md) | [English](README.en.md)

## 요약

`justified-change`는 비자명한 코드 변경을 목표에 비례하고, 근거가 있으며, 검증 가능한 상태로 유지하기 위한 가벼운 코딩 스킬입니다.

이 스킬은 두 가지 반대 문제를 줄이는 데 초점을 둡니다.

- 요청보다 넓은 추측성 작업을 섞는 것
- 변경을 너무 좁게 잡아 필요한 후속 수정을 누락하는 것

목표는 가능한 가장 작은 변경이 아닙니다.

목표는 필요한 일을 필요한 만큼 수행하고, 주요 변경의 이유와 검증 기준을 설명할 수 있는 상태로 만드는 것입니다.

`스펙:` Agent Skills / SKILL.md | `라이선스:` MIT | `에이전트:` Codex, ChatGPT, Agent Skills 호환 도구

## 빠른 시작

**설치**

```bash
npx skills add perhapsspy/justified-change
```

혹은 `skills/justified-change` 폴더를 에이전트 스킬 디렉터리에 직접 복사합니다.

**바로 사용**

```text
$justified-change 를 사용해서 이 버그 수정의 목표, 필요한 범위, 검증 기준을 정리하고 구현해줘
```

## 이런 때 사용

- 비자명한 구현, 버그 수정, 리팩터링, 코드 리뷰 반영을 할 때
- 변경이 요청보다 넓은 추측성 작업이나 불필요한 정리로 번질 수 있을 때
- 변경을 너무 좁게 잡아 필요한 호출부, 타입, 테스트, 문서, 설정 수정을 누락할 위험이 있을 때
- 실패 원인을 좁히고 검증 근거를 남겨야 할 때
- 변경 범위가 왜 필요한지 리뷰어나 미래 작업자에게 설명 가능해야 할 때

## 프로젝트 가치 보존 스킬

이 스킬들은 오래 운영되는 프로젝트가 나중에도 이해되고 수정될 수 있는 상태를 유지하도록 돕습니다.

프로젝트의 가치는 코드가 늘어나서만 떨어지는 것이 아닙니다. 코드 흐름이 읽히지 않고, 결정 이유가 사라지고, 작업 맥락을 복원할 수 없고, 테스트가 실제 동작 계약을 보호하지 못하고, 변경 범위가 목표와 검증 없이 넓어지거나 좁아질 때 가치가 떨어집니다.

- [`structure-first`](https://github.com/perhapsspy/structure-first): 코드 흐름, 책임 경계, 수정 가능성, 계약 중심 테스트를 보존합니다.
- [`project-context`](https://github.com/perhapsspy/project-context): 저장소 안의 일반 문서로 프로젝트 기억, 결정 이유, 현재 작업 상태, 작업 연속성을 보존합니다.
- [`interactive-state-flow`](https://github.com/perhapsspy/interactive-state-flow): 지체 없이 기록되어야 하는 기준 상태와 비용이 큰 표현·비동기 작업·실행 경로를 분리해 사용자 반응성과 유지보수성을 보존합니다.
- `justified-change`: 변경 목표, 직접 영향 범위, 범위 근거, 검증 기준을 맞춰 불필요한 작업과 누락된 후속 수정을 함께 줄입니다.

각 스킬은 독립적으로 설치하고 사용할 수 있습니다. 이 README는 같은 철학의 스킬들을 소개할 뿐, 개별 `SKILL.md`가 서로를 호출하거나 의존하게 만들지 않습니다.

## 지원

[![Buy Me A Coffee](https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png)](https://www.buymeacoffee.com/perhapsspy)

## 라이선스

[MIT](LICENSE)
