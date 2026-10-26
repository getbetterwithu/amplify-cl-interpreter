# 설치 안내 — GPT (ChatGPT)

> **확인 상태**: 아래 방법은 검색으로 찾은 설명 글(대부분 제3자 블로그)을 정리한 것이다. OpenAI 공식 도움말로 직접 확인하지 못했고, 이 ZIP을 올려 보지도 못했다. 메뉴 이름과 사용 가능한 요금제는 공식 도움말에서 확인한다.

## 가장 간단한 방법: ZIP 올리기 (Skills)
검색 결과 기준으로 ChatGPT도 같은 SKILL.md 형식의 스킬 업로드를 지원한다.
1. 받은 배포용 ZIP을 풀지 않은 채로 준비한다.
2. ChatGPT에서 Plugins(플러그인) → Skills(스킬) 탭 → Create(만들기) → Upload from your computer(컴퓨터에서 올리기)에서 ZIP을 올린다.
3. 새 대화에서 CL 코드를 붙여넣어 확인한다.

**조건**: 이 기능은 요금제에 따라 다르다. 설명 글에는 Business, Enterprise, Healthcare, Edu 요금제가 나오고, 관리자가 업로드를 꺼 둘 수 있다고 한다. 개인 무료·Plus 계정에서 되는지는 확인하지 못했다.

## 스킬 메뉴가 없을 때: 맞춤 GPT로 구성
1. GPT 탐색 → 만들기 → 구성(Configure)을 연다.
2. 지침(Instructions)에 `guides/instructions-short.md` 내용을 붙여넣는다.
3. 지식(Knowledge)에 `INDEX.md`, `knowledge/` 안의 8개 파일(`official-index.md`, `official-docs.md`, `site-core.md`, `grammar-defs.md`, `examples-A.md`, `examples-B.md`, `examples-CD.md`, `grammar-index.md`), `reference/hypotheses.md`, `reference/conflicts.md`를 올린다(모두 11개. 맞춤 GPT 한도는 20개로 알려져 있으나 공식 도움말로 확인하지 못했다). (`conflicts.md`가 빠지면 SKILL.md가 따르라고 하는 충돌 처리 기준이 없어져 readOnly 대시보드 표시와 differenceFunction 부호를 단정할 수 있다.)

## 알려진 한계
- 지식 파일이 큰 경우(예제 파일 각 약 80~100KB) 질문마다 일부만 읽힐 수 있다. 답이 "자료에 없습니다"로 나오는데 파일에는 있는 경우다. 질문에 컴포넌트 이름과 sink 이름을 함께 적어 본다.

## 코드 올리는 방법 (사용자 안내)
- 기본은 **캡처**입니다. 편집기에서 **줄 번호가 보이게** 캡처해 올려 주세요.
- 긴 코드는 **캡처와 텍스트를 함께** 올려 주세요.
- 텍스트만 붙여넣을 때는 **첫 줄에 `컴포넌트: 이름`** 을 적어 주세요. (예: `컴포넌트: input1`)
- 다른 컴포넌트의 값이나 그래프 변수를 읽는 코드라면 그 컴포넌트의 CL도 함께 보내 주세요. 풀이 끝에 필요한 자료를 알려 드립니다.
