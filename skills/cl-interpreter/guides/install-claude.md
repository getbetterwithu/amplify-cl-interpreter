# 설치 안내 — Claude

> **확인 상태**: 아래 방법은 Anthropic 문서와 설명 글을 검색해 정리한 것이다. 이 ZIP을 실제로 올려 본 것은 아니다. 메뉴 이름이 문서마다 다르게 나온다(Settings → Capabilities → Skills, 또는 Settings → Features).

## 가장 간단한 방법: ZIP 올리기 (claude.ai 웹·데스크톱)
1. 받은 배포용 ZIP을 **풀지 않은 채로** 준비한다. (ZIP 안에 `cl-interpreter/` 폴더가 있고 그 안에 `SKILL.md`가 있어야 한다. 이 ZIP은 그렇게 만들어져 있다.)
2. claude.ai에서 설정(Settings)의 Skills(스킬) 항목을 연다. → `Upload skill`(스킬 올리기)에 ZIP을 올린다.
3. 스킬을 켜고 새 대화에서 CL 코드를 붙여넣어 확인한다.

조건: 유료 요금제(Pro, Max, Team, Enterprise)에서, 코드 실행(Code execution) 기능이 켜져 있어야 한다고 문서에 나온다. 스킬이 안 보이면 이 두 가지를 먼저 확인한다.

## Claude Code (터미널·VS Code)
`cl-interpreter` 폴더를 `C:\Users\<사용자>\.claude\skills\` 안에 복사하고 Claude Code를 새로 시작한다. (프로젝트에서만 쓰려면 `<프로젝트>\.claude\skills\`)

## 안 될 때
- "SKILL.md가 없다"는 오류: ZIP 안에 파일이 바로 들어 있는 경우다. 폴더째 압축해야 한다.
- 스킬이 안 읽히면: 폴더 이름과 SKILL.md의 `name`(cl-interpreter)이 같은지 확인한다.
- 스킬 기능이 없는 계정이면: Claude 프로젝트(Projects)의 지침에 `guides/instructions-short.md`를, 프로젝트 지식에 파일들을 넣는다.

## 코드 올리는 방법 (사용자 안내)
- 기본은 **캡처**입니다. 편집기에서 **줄 번호가 보이게** 캡처해 올려 주세요.
- 긴 코드는 **캡처와 텍스트를 함께** 올려 주세요.
- 텍스트만 붙여넣을 때는 **첫 줄에 `컴포넌트: 이름`** 을 적어 주세요. (예: `컴포넌트: input1`)
- 다른 컴포넌트의 값이나 그래프 변수를 읽는 코드라면 그 컴포넌트의 CL도 함께 보내 주세요. 풀이 끝에 필요한 자료를 알려 드립니다.
