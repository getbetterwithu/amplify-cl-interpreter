# amplify-cl-interpreter — CL 해석 스킬 (cl-interpreter) v0.3.2

Amplify Classroom의 Computation Layer(CL) 코드를 해석해 주는 스킬입니다. CL 코드를 올리면 줄별로 풀이하고, Amplify에서 실제로 실행했을 때 화면에서 보일 동작을 예측해 줍니다. CL 문법을 물어볼 수도 있습니다.

> 이 스킬의 문법 지식 중 일부는 아직 Amplify에서 실행해 확인하지 않았습니다. 답의 문장 끝에 붙는 출처 표시(*공식 문서*, *판정*, *추가검증필요*, *예상*, *코드 추론*)로 확신 정도를 구분합니다. 코드 해석은 부정확할 수 있으니 중요한 부분은 Amplify에서 직접 확인해 주세요.

## 설치 방법

스킬이 레포 루트에 있으므로 레포 주소만으로 설치합니다.

- **Claude Code:**
  ```
  claude plugin marketplace add getbetterwithu/amplify-cl-interpreter
  claude plugin install amplify-cl-interpreter@amplify-cl-interpreter
  ```
  설치 후 `claude plugin list`에서 enabled로 보이면 됩니다. 다음 세션부터 적용됩니다.
- **Gemini CLI:**
  ```
  gemini skills install https://github.com/getbetterwithu/amplify-cl-interpreter --scope user
  ```
  설치 후 `gemini skills list`에서 `cl-interpreter [Enabled]`가 보이면 됩니다.
- **그 밖의 AI 도구**(ChatGPT 웹 등): `guides/` 폴더의 안내를 따릅니다.

## 코드를 올리는 방법

**1. 기본은 캡처입니다.** 편집기에서 **줄 번호가 보이게** 캡처해 올려 주세요. 줄 번호가 있으면 어느 줄을 풀이한 것인지 정확히 짚을 수 있습니다.

**2. 긴 코드는 캡처와 텍스트를 함께** 올려 주세요. 캡처로 줄 번호를, 텍스트로 정확한 글자를 확인합니다.

**3. 텍스트만 붙여넣을 때는 첫 줄에 컴포넌트 이름을 적어 주세요.**
```
컴포넌트: input1
hidden: btn1.pressCount > 2
correct: this.numericValue > 9.99 and this.numericValue < 10.01
```
붙여넣은 텍스트는 편집기 줄 번호와 어긋나기 쉬워서, 줄 번호 대신 코드 조각을 인용해 풀이합니다.

## 더 정확한 해석을 위해
코드가 **다른 컴포넌트의 값**(예: `input1.numericValue`)이나 **그래프 안의 변수**를 읽는다면, 그 컴포넌트의 CL과 그래프 식 목록도 함께 보내 주세요. 풀이 끝에 어떤 자료가 필요한지 알려 드립니다. 자료를 모두 주셔야 더 정확한 해석이 가능합니다. 추가 자료를 보내면 전체를 다시 쓰지 않고 바뀐 부분만 정리합니다.

## 이 패키지에 들어 있는 것
`SKILL.md`(지침), `INDEX.md`(파일 지도), `knowledge/`(공식 Index·문서, 사이트 설명, 판정 86건의 정의 층, 적용 사례 226건(추가검증이 필요한 사례와 판정 항목의 보충)의 예제 층 3개 파일), `reference/`(가설, 알려진 충돌, 확인되지 않은 항목), `guides/`(설치 안내). 자세한 내용은 `INDEX.md`와 `VERSION.md`를 보세요.

## 라이선스와 출처

이 레포의 스킬 지침과 정리한 내용은 MIT 라이선스입니다(`LICENSE`). 다만 `knowledge/official-index.md`, `knowledge/official-docs.md`, `knowledge/site-core.md`에는 Amplify Classroom 공식 문서의 원문이 들어 있습니다. 그 원문의 저작권은 원 저작권자에게 있으며 MIT 라이선스 범위에 포함되지 않습니다. 원문은 공식 문서(classroom.amplify.com/computation-layer/documentation)를 확인해 주세요.
