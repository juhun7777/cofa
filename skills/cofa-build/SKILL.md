---
name: cofa-build
description: Build a minimal working result for a time-limited workplace task using its existing environment. Use for apps, data deliverables, or automation after scope is understood.
---

# 작동하는 최소 결과부터 구현

사용자가 제공한 실제 과제, 현재 단계, 남은 시간, 허용 도구와 제출 조건을 따른다. AI 금지 단계에서는 지원하지 않는다. 요구사항이 이미 정리돼 있으면 기획을 반복하지 않는다.

기존 런타임·파일·테스트·실행 방법을 우선 확인한다. 제공 스택을 유지하고 최소한의 변경으로 입력→처리→출력을 먼저 연결한다. 과제가 요구하지 않는 인증·DB·배포·멀티 에이전트·MCP·프레임워크 교체를 추가하지 않는다. 별도 모델 호출이나 외부 서비스는 명시적 허용·사용 방법이 확인돼야 한다. 결과물 자체의 AI API 요구는 코딩 보조 AI 허용과 별도다.

과제에 해당하는 참고문서 하나만 읽고, 혼합 과제일 때만 필요한 부분을 추가한다.
- 웹 화면·업무 앱: [references/web-app.md](references/web-app.md)
- CSV·수치·추천·보고서: [references/data-report.md](references/data-report.md)
- 반복 업무·파일 처리·워크플로우: [references/automation.md](references/automation.md)

기능 단위로 구현→실행→출력 확인을 반복한다. 외부 연동을 목업으로 대체했다면 그 상태를 명확히 표시한다. 실제 연동이 필수인 과제에서 목업을 완성으로 보고하지 않는다. 실패해도 정상 성공처럼 보이지 않게 처리하고 마지막 유효 결과와 새로 실패한 결과를 구분한다.

핵심 흐름이 작동한 뒤 필수 조건의 누락을 먼저 보완한다. 선택 기능은 남은 시간과 검증 비용을 고려해 추가한다. 짧은 마감 직전에는 구조 전면 교체나 새로운 의존성 설치를 피하고 필수 오류 수정·검증·제출에 집중한다.

사용자에게 실제 실행 방법, 지금 확인할 대표 입력과 예상 출력, 변경한 핵심 위치, 입력→처리→출력과 실패 시 동작을 간결하게 알려준다. 확인하지 않은 결과를 확인했다고 쓰지 않는다. 작업 로그는 허용된 공간에만 남기며 자동조작·외부 전송·업데이트 제한을 우회하지 않는다.
