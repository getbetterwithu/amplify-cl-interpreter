# 설치 안내 — Gemini

> **확인 상태**: 아래 방법은 검색으로 찾은 설명 글(제3자 블로그)을 정리한 것이다. Google 공식 도움말로 직접 확인하지 못했고, 이 ZIP을 올려 보지도 못했다. Gems가 Skills로 바뀌는 중이라 날짜와 화면이 글마다 다르다(2026년 11월 이후 이전 계획이 있다는 글이 있다).

## 가장 간단한 방법: ZIP 올리기 (Skills)
설명 글 기준으로 Gemini 스킬은 `SKILL.md` 파일, 또는 `SKILL.md`가 있는 폴더·ZIP을 올릴 수 있다.
1. 받은 배포용 ZIP을 풀지 않은 채로 준비한다.
2. **Gemini 웹(gemini.google.com)** 에서 Skills 메뉴를 열고 올리기(Upload)로 ZIP을 올린다.
3. 새 대화에서 CL 코드를 붙여넣어 확인한다.

**조건**: 업로드는 현재 Gemini 웹 앱과 Mac 앱에서만 된다고 한다(모바일 앱은 확인하지 못함). `.docx`, `.xlsx`는 올릴 수 없다고 한다. 우리 패키지는 `.md` 파일만 들어 있다.

## Skills 메뉴가 없을 때
- 기존 Gem(맞춤 Gem)으로 구성: 지침에 `guides/instructions-short.md`를 붙여넣고 파일 10개를 첨부한다: `INDEX.md`, `knowledge/` 7개(`official-index.md`, `official-docs.md`, `site-core.md`, `grammar-defs.md`, `examples-A.md`, `examples-B.md`, `examples-CD.md`), `reference/hypotheses.md`, `reference/conflicts.md`. `conflicts.md`가 빠지면 SKILL.md가 따르라고 하는 충돌 처리 기준이 없어진다. `knowledge/grammar-index.md`는 선택 파일이라 뺐다(예제 파일 제목에 같은 정보가 있다). 첨부 한도는 10개로 알려져 있으나 Google 공식 도움말로 확인하지 못했다.
- 또는 새 대화에서 `instructions-short.md`를 첫 메시지로 붙여넣고 파일을 첨부한다. 대화마다 다시 해야 한다.

## 알려진 한계
- 큰 파일(`examples-CD.md` 약 100KB 등)은 일부만 읽힐 수 있다. 질문에 컴포넌트·sink 이름을 적어 본다.
- 이미지 속 코드를 옮겨 적는 정확도는 플랫폼마다 다르다. 스킬은 전사한 코드를 답 맨 앞에 보여 주므로, 틀린 글자가 있으면 그 부분을 알려 주고 다시 요청한다.

## 코드 올리는 방법 (사용자 안내)
- 기본은 **캡처**입니다. 편집기에서 **줄 번호가 보이게** 캡처해 올려 주세요.
- 긴 코드는 **캡처와 텍스트를 함께** 올려 주세요.
- 텍스트만 붙여넣을 때는 **첫 줄에 `컴포넌트: 이름`** 을 적어 주세요. (예: `컴포넌트: input1`)
- 다른 컴포넌트의 값이나 그래프 변수를 읽는 코드라면 그 컴포넌트의 CL도 함께 보내 주세요. 풀이 끝에 필요한 자료를 알려 드립니다.
