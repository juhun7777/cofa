# COFA 준비용 선택형 스킬

제한 시간 안에 과제를 해결할 때 필요한 지침만 선택해서 사용하기 위한 개인 준비 자료입니다. 공식·제휴 스킬이나 기출문제가 아닙니다.

외부 플러그인, MCP, 외부 AI 연결, 실행 스크립트를 포함하지 않습니다. 네 스킬은 자동으로 모두 실행하는 묶음이 아닙니다.

## 파일 받기

- [준비 파일 ZIP](cofa-skills-public-candidate.zip)
- [공통 작업 원칙 템플릿](AGENTS.template.md)
- [시작 프롬프트](START.template.md)
- [검증 기록 양식](WORKLOG.template.md)

| 스킬 | 필요할 때 | 지침 파일 |
|---|---|---|
| cofa-scope | 요구사항·우선순위·완료 기준을 정리할 때 | [SKILL.md](skills/cofa-scope/SKILL.md) |
| cofa-build | 제공 환경에서 작은 전체 흐름부터 구현할 때 | [SKILL.md](skills/cofa-build/SKILL.md) |
| cofa-verify | 예상 결과와 실제 결과를 비교할 때 | [SKILL.md](skills/cofa-verify/SKILL.md) |
| cofa-debug | 실제 오류를 재현·수정·재검증할 때 | [SKILL.md](skills/cofa-debug/SKILL.md) |

## Codex에서 사용

파일 반입·공개 저장소 다운로드·로컬 검사 등이 허용된 환경에서만 사용합니다. 실제 과제 지침과 최신 운영 안내가 이 준비 자료보다 우선합니다.

일반 Codex의 프로젝트 단위 스킬 위치는 다음과 같습니다. 필요한 폴더를 선택해서 가져오고, cofa-build는 references도 함께 유지합니다.

```text
작업 프로젝트/
├─ 기존 파일들
└─ .agents/
   └─ skills/
      └─ cofa-verify/
         ├─ SKILL.md
         └─ agents/openai.yaml
```

이 저장소의 skills/는 보관용 구조입니다. 저장소를 내려받는 것만으로 시험 프로젝트의 .agents/skills에 자동 설치되지는 않습니다. AGENTS.template.md도 자동 적용되는 AGENTS.md와 다릅니다. 기존 시험 AGENTS.md를 덮어쓰지 않습니다.

스킬 선택을 지원하는 Codex 채팅창에서 다음처럼 요청합니다. 터미널 명령이 아닙니다.

```text
$cofa-verify

현재 구현의 필수 요구사항만 검증해 줘.
예상값의 근거와 실제 결과를 대조하고,
내가 화면에서 직접 확인할 절차를 알려줘.
```

자동 발견이 지원되지 않아도, 허용된 작업공간에 파일이 있다면 채팅에서 해당 지침만 읽도록 요청할 수 있습니다.

```text
내려받은 cofa 저장소의 skills/cofa-verify/SKILL.md를 읽고
현재 결과물 검증에만 적용해 줘.
다른 스킬은 읽거나 자동 적용하지 마.
```

각 agents/openai.yaml에는 allow_implicit_invocation: false를 설정했습니다. 해당 설정을 지원하는 Codex에서 명시적 호출로 사용합니다. Cofa의 구체적인 반입·메뉴·발견 지원 여부는 별도 확인이 필요합니다.

## 사용 범위

시험 문제·입력파일·결과물·실제 작업 기록·개별 안내·접속 링크를 이 저장소에 추가하거나 Push하지 않습니다. AI 사용 금지 단계에서는 이 자료를 통한 AI 지원도 중단합니다. 도구를 가져올 수 있다는 사실은 그 도구의 모든 기능을 사용할 수 있다는 뜻이 아닙니다.

형식·참조 경로를 확인한 준비용 초안이며 실제 Cofa 환경에서의 호환성이나 점수 개선을 보장하지 않습니다. 필요하지 않은 스킬은 사용하지 않아도 됩니다.
