## HTML

**웹사이트**

웹 브라우저를 통해서 접속하는 웹 페이지들의 모음

링크를 통해 여러 웹 페이지를 연결한 것이 웹 사이트

**구성요소**

- HTML 구조(레이아웃)
- CSS 표현(스타일링)
- JavaScript 동작(인터렉션)

**Hyper Text Markup Language**

- Hyper Text

  > 참조(하이퍼링크)를 통해 사용자가 한 문서에서 다른 문서로 즉시 접근할 수 있는 텍스트

- Markup Language

  > 태그 등을 이용하여 문서나 데이터의 구조를 명시하는 언어

- 웹 페이지를 작성(구조화)하기 위한 언어

_MDN_, _W3Schools_ 이용하기

**HTML 기본 구조**

```html
<!DOCTYPE html>
<html lang="ko">
  <head>
    ...
  </head>
  <body>
    ...
  </body>
</html>
```

- html: 문서의 최상위(root)요소
- head: 문서 메타데이터 요소

  - 문서 제목, 인코딩, 스타일, 외부 파일 로딩
  - 일반적으로 브라우저에 나타나지 않는 내용
  - `<title>` 브라우저 상단 타이틀
  - `<link>` 외부 리소스 연결 요소(CSS 파일)
  - `<style>` CSS 직접 작성
  - ```html
    <head>
      <title>HTML 수업</title>
      <meta charset="UTF-8" />
      <link href="style.css" rel="stylesheet" />
      <script src="javascript.js"></script>
      <style>
        p {
          color: black;
        }
      </style>
    </head>
    ```

- body: 문서 본문 요소

  - 실제 화면 구성과 관련된 내용

**요소**

`<h1>contents</h1>`

- 여는/시작 태그
- 내용
- 닫는/종료 태그

- HTML 요소는 시작 태그와 종료 태그 그리고 태그 사이에 위치한 내용으로 구성

  - 태그(Element, 요소)는 컨텐츠(내용)를 감싸는 것으로 그 정보의 성격과 의미를 정의

- 내용이 없는 태그들

  - `br` 줄바꿈
  - `hr`
  - `img`
  - `input`
  - `link`
  - `meta`

- 요소는 중첩(nested)될 수 있음

  - 요소의 중첩을 통해 하나의 문서를 구조화
  - 여는 태그와 닫는 태그의 쌍을 잘 확인해야함

    - 오류를 반환하는 것이 아닌 그냥 레이아웃이 깨진 상태로 출력되기 때문에 디버깅이 힘들어질 수 있음

**속성**

`<a href="https://google.com"></a>`

- 속성명
- 속성값
- 공백 없이 쌍따옴표 사용

- 속성을 통해 태그의 부가적인 정보를 설정할 수 있음
- 요소는 속성을 가질 수 있으며, 경로나 크기와 같은 추가적인 정보를 제공
- 요소의 시작 태그에 작성하며 보통 이름과 값이 하나의 쌍으로 존재
- 태그와 상관없이 사용 가능한 속성(HTML Global Attribute)들도 있음

  - 모든 HTML 요소가 공통으로 사용할 수 있는 대표적인 속성(몇몇 요소에는 아무 효과가 없을 수 있음)
  - `id` 문서 전체에서 유일한 고유 식별자 지정
  - `class` 공백으로 구분된 해당 요소의 클래스의 목록
  - `style` inline 스타일

**코드 예시**

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Hello, HTML</title>
  </head>
  <body>
    <!-- 이것은 주석입니다. -->
    <h1>나의 첫번째 HTML</h1>
    <p>이것은 본문입니다.</p>
    <span>이것은 인라인요소</span>
    <a href="https://www.naver.com">네이버로 이동!!</a>
  </body>
</html>
```

**HTML 문서 구조화**

> 텍스트 요소

- <a></a> href 속성을 활용하여 다른 URL로 연결하는 하이퍼링크 생성
- <b></b> 굵은 글씨 요소
- <strong></strong> 중요한 강조하고자 하는 요소(보통 굵은 글씨로 표현)
- <i></i> 기울임 글씨 요소
- <em></em> 중요한 강조하고자 하는 요소(보통 기울임 글시로 표현)
- <br> 텍스트 내에 줄 바꿈 생성
- <img> src 속성을 활용하여 이미지 표현
- <span></span> 의미 없는 인라인 컨테이너

> 그룹 컨텐츠 -

<p></p>
하나의 문단 -
<hr>
주제를 분리하기 위한 수평선 -
<div></div>
의미 없는 블록 레벨 컨테이너

> form

<form>
  <form>은 사용자의 정보를 제출하기 위한 영역
  
  
> input
  다양한 타입을 가지는 입력 데이터 유형과 위젯이 제공됨

> input label

- label을 클릭하여 input 자체의 초점을 맞추거나 활성화시킬 수 있음
- 사용자는 선택할 수 있는 영역이 늘어나 웹/ 모바일(터치)환경에서 편하게 사용할 수 있음
- label 과 input 입력의 관계가 시각적 뿐만 아니라 화면리더기에서도 label을 읽어 쉽게 내용을 확인할 수 있도록 함
- **<input />에 id 속성을, <label>에는 for 속성**을 활용하여 상호 연관을 시킴

```html
<label for="agreement">개인정보 수집에 동의합니다.</label>
<input type="checkbox" name="agreement" id="agreement"/></label>
```

> input 유형 - 일반

- 일반적으로 입력을 받기 위하여 제공되며 `type`으로 HTML기본 검증 혹은 추가 속성을 활용할 수 있음
  - text: 일반 텍스트 입력
  - password: 입력 시 값이 보이지 않고 문자를 특수기호(\*)로 표현
  - email: 이메일 형식이 아닌 경우 form 제출 불가
  - number: min,max, step 속성을 활용하여 숫자 범위 설정 가능
  - file: accept 속성을 활용하여 파일 타입 지정 가능

> input 유형 - 항목 중 선택

- label로 선택에 대한 내용을 작성하고, 항목으로 선택할 수 있는 input을 제공
- 동일한 범주에 속하는 항목들은 name을 통일하고 선택된 항목의 값은 value로 지정함
  - checkbox 다중선택
  - radio 단일선택

> input 유형 - 종합

- <input> 요소의 동작은 type에 따라 달라지므로, 각각의 내용을 숙지할 것

## CSS

> Cascading Style Sheets
> 스타일을 지정하기 위한 언어
> 선택하고, 스타일을 지정한다

> CSS 구문

```html
h1 { color:blue; font-size: 15px; }
```

- h1 선택자
- color: blue; 선언
- font-size 속성
- 15 px 값

* CSS 구문은 선택자를 통해 스타일을 지정할 HTML 요소를 선택
* **중괄호 안에서는 속성과 값** 하나의 쌍으로 이루어진 선언을 진행
* 각 쌍은 선택한 요소의 속성, 속성에 부여할 값을 의미
  - 속성: 어떤 스타일 기능을 변경할지 결정
  - 값: 어떻게 스타일 기능을 변경할지 결정

> CSS 정의 방법

- 인라인(inline)
  - 해당 태그에 직접 style 속성을 활용
  - `<h1 style="color: blue; font-size: 100px;">Hello</h1>`
- 내부참조(embedding) -<style>
  - <head> 태그 내에 <style>에 지정
  - ```html
    h1 { color: blue; font-size: 100px; }
    ```
- 외부참조(link file) - 분리된 CSS 파일

> CSS 개발자 구조

**CSS Selectors**

> 선택자(Selector) 유형

- 기본 선택자

  - 전체 선택자(\*), 요소(tag) 선택자

  ```html
  <style>
    <!--/* 전체 선택자 */-->
      * {
      color: red;
    }

    <!--/* 요소 선택자 */-->
      h2 {
      color: orange;
    }

    <!--/* 클래스 선택자 */-->
      .green {
      color: green;
    }

    <!-- /* 자식 결합자 */>
      .box > p {
      font-size: 30px;
    }

    <!--/* 자손 결합자 */ -->
      .box p {
      color: blue;
    }
  </style>
  ```

  - 클래스(class) 선택자, 아이디(id) 선택자, 속성(attr) 선택자

- 결합자(Combinators)
  - 자손 결합자, 자식 결합자

> **CSS 적용 우선순위(cascading order)**

- CSS 우선순위를 아래와 같이 그룹을 지어볼 수 있다
  - 1. 중요도(importance) - 사용시 주이
    - `!important` (우선순위 무시하고 적용)
  - 2. 우선순위(Specificity)
    - 인라인 > id > calss, 속성 > 요소

* Quiz (!시험!)
  orange
  blue
  green(CSS 파일에 나중 값이 green)
  green
  red
  darkviolet
  yellow
  darkviolet

**CSS 상속**

> CSS 상속

- CSS는 상속을 통해 부모 요소의 속성을 자식에게 상속한다.

  - 속성(프로퍼티) 중에서는 상속이 되는 것과 되지 않는 것들이 있다.

  ```html
  <body>
    <p>안녕하세요 <span>김싸피</span> 입니다.</p>
  </body>

  <style>
    p {
      <!-- 상속됨 -->
      color: red;
      <!-- 상속 안됨 -->
      border: 1px solid black;
    }
    span {
      border: 1px solid blue;
    }
  </style>
  ```

```html
<style>
  <!--/* 클래스 선택자 */>
  .green {
    color: green;
  }
  <!--/* id 선택자 */>
  #purple {
    color: purple;
  }
  <!--/* 자식 결합자 */>
  .box > p {
    font-size: 30px;
  }

  <!--/* 자손 결합자 */>
  .box p {
    color: blue;
  }
</style>
```
