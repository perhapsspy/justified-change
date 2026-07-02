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

## 지원

[![Buy Me A Coffee](https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png)](https://www.buymeacoffee.com/perhapsspy)

## 라이선스

[MIT](LICENSE)
