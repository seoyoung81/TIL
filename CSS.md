### CSS

**Box model**

> CSS 원칙 1

- 모든 요소는 네모(박스모델)
- 위에서부터 아래로, 왼쪽에서 오른쪽으로 쌓인다(좌측 상단에 배치)

> Box model

- 모든 HTML 요소는 box 형태
- 하나의 박스는 네부분(영역)
  - content 글이나 이미지 등 요소의 실제 내용
  - _padding_ 테두리 안쪽의 내부 여백. **요소에 적용된 배경색, 이미지는 padding까지 적용**
  - border 테두리 영역
  - _margin_ 테두리 바깥의 외부 여백. 배경색을 지정할 수 없다

> Box model 구성
> margin

```CSS
.margin { margin-top: 10px; margin-right: 20px; margin-bottom: 30px;
margin-left: 40px; }
```

> padding
> margin/padding

- shorthand로 표현
  ```CSS
  .margin-1{ margint: 10px; }
  ```
  > border

> 박스 만들어보기

```CSS
.box1 { width: 500px; border-width: 2px; border-style: dashed; border-color:
black; padding-left: 50px; margin-bottom: 30px; }
```

> Box-sizing

- 기본적으로 모든 요소의 box-sizing은 content-box
  - padding을 제외한 순수 contents 영역만을 box로 지정
- 우리가 일반적으로 영역을 볼 때는 border까지의 너비를 100px 보는 것을 원함
  - 그 경우 box-sizing을 border-box으로 설정(border를 padding까지 보고 싶은 경우)

### 개발자 도구

> 크롬 개발자 도구

- 웹 브라우저 크롬에서 제공하는 개발과 관련된 다양한 기능을 제공
- 주요 기능
  - Elements - DOM 탐색 및 CSS 확인 및 변경
    - Styles 요소에 적용된 CSS 확인
    - Computed 스타일이 계산된 최종 결과
    - Event Listeners 해당 요소에 적용된 이벤트(JS)

> HTML

1. elements 해당 요소의 HTML 태그
2. DOM 조작하기
3. CSS - styles, computed(계산이 되어있는 모델을 볼 수 있음)
   1. styles 해당 요소에 선언된 모든 CSS
   2. computed 해당 요소에 최종 계산된 CSS
4. CSS 조작하기

### CSS Display

> CSS 원칙2

- display에 따라 크기와 배치가 달라진다

**인라인/블록 요소**

> 대표적으로 활용되는 display

- display: block
  - 줄 바꿈이 일어나는 요소(다른 elem를 밀어냄)
  - 화면 크기 전체의 가로 폭을 차지
  - 블록 레벨 요소 안에 인라인 레벨 요소가 들어갈 수 있음
  - div/ ul, oi, li / p / hr / form
- display: inline
  - 줄 바꿈이 일어나지 않는 행의 일부 요소
  - content를 마크업 하고 있는 만큼만 가로 폭을 차지
  - width, height, margin-topm, margin-bottom을 지정할 수 없음
  - 상하 여백은 line-height로 지정
  - span / a / img / input, label / b, em, i, strong

**CSS Position**

> CSS Position

- 문서 상에서 요소의 위치를 지정(공식문서를 찾아보자)
- static: 모든 태그의 기본 값(기준 위치)

  - 일반적인 요소의 배치 순서에 따름(좌측 상단)
  - 부모 요소 내에서 배치될 때는 부모 요소의 위치에 따름

  ```CSS
  div {
    height: 100px;
    width: 100px;
    background-color: #9775fa;
    color: black;
    line-height: 100px;
    text-align: center;
  }

  ```

  딱히 안 건들면 static

- **좌표 프로퍼티를 사용하여 이동 가능한 것들**

  - realative: 상대 위치

    - 자기 자신의 static 위치를 기준으로 이동(normal flow 유지)
    - 레이아웃에서 요소가 차지하는 공간은 static일 때와 같음(normal position 대비 offset)
    - ```CSS

      ```

  - absoulte: 절대 위치
    - 요소를 일반적인 문서 흐름에서 제거 후 레이아웃에 공간을 차지하지 않음(normal flow에서 벗어남)
    - static이 아닌 가장 가까이 있는 부모/조상 요소를 기준으로 이동(없는 경우 body)
  - fixed: 고정 위치
    - 요소를 일반적인 문서 흐름에서 제거 후 레이아웃에 공간을 차지하지 않음(normal flow에서 벗어남)
    - 부모 요소와 관계없이 viewpart를 기준으로 이동
      - 스크롤 시에도 항상 같은 곳에 위치함
  - sticky
