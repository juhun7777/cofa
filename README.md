# COFA 과제 준비용 운영 안내

실제 문제를 본 뒤 역할과 작업 범위를 정하는 개인 준비 자료입니다. 공식 시험 지침이나 기출문제가 아닙니다. **사용할 지침은 operating/ 폴더에 모았습니다.**

## 시작하기

- [빠른 시작: 내려받기·터미널·역할 프롬프트](operating/QUICKSTART.md)
- [현재 운영 문서 ZIP](cofa-operating-kit.zip): 이 README와 operating/만 포함합니다.
- [공통 원칙](operating/COMMON.md), [운영안 선택](operating/MODES.md), [실무자 질문](operating/QUESTIONS.md)

| 역할 | 지침 |
| --- | --- |
| T1 — 이해·출처 표·실무자 질문·변경 관리 | [T1.md](operating/roles/T1.md) |
| T2 — 주 구현 A·뼈대·기술 통합·담당 검증 | [T2.md](operating/roles/T2.md) |
| T3 — 독립 구현 B·담당 검증·수정 | [T3.md](operating/roles/T3.md) |
| T4 — 실제 구현의 위치·원리·선택 이유 설명 | [T4.md](operating/roles/T4.md) |

기록의 빈 양식은 operating/templates/에 있습니다. 작업량에 따라 설명을 T1이 겸하거나 작은 과제의 구현자를 줄일 수 있습니다. 불필요한 세션·문서를 강제하지 않습니다.

## 받는 방법

반입과 공개 저장소 다운로드가 허용된 경우 실제 프로젝트 루트의 일반 터미널에서 한 번 실행합니다.

```sh
git clone --depth 1 https://github.com/juhun7777/cofa.git cofa-prep
```

이 명령이 cofa-prep 폴더를 만듭니다. 이후 같은 실제 프로젝트 위치에서 제공된 Codex를 실행하고 COMMON.md와 자기 역할 파일을 읽으라고 요청합니다. 역할 문서는 일반 Markdown이며 별도 등록·설치가 필요하지 않습니다. 세션 간 대화·파일 갱신이 자동으로 전달되지는 않습니다.

## 사용 범위

실제 과제·환경·최신 운영 안내가 우선입니다. 기존 시험 지침을 덮어쓰지 않습니다. 실제 문제·데이터·실무자 대화·작업 기록·제출물을 이 저장소에 작성하거나 Push하지 않습니다. AI 금지 단계에서는 설명·파일 읽기·도구 사용을 포함한 지원을 중단합니다.

2026-11-05 정리: 사용하지 않는 기존 스킬·중복 템플릿·이전 스킬 ZIP을 현재 배포에서 제거했습니다. 현재 자료는 README, operating/, 운영 ZIP으로 구성됩니다.
