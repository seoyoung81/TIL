### Layout

### Float

> CSS 원칙 1

- Normal Flow
  - 모든 요소는 네모(박스모델), 위 -> 아래 / 왼 -> 오 (좌측 상단에 배치)

> Folat

- 박스를 왼쪽 혹은 오른쪽으로 이동시켜 텍스트를 포함 인라인요소들이 주변을 wrapping하도록 함
- 요소가 Normal flow를 벗어나도록 함
- 속성
  - none 기본값
  - left 요소를 왼쪽으로 띄움
  - right 요소를 오른쪽으로 띄움

```CSS
.box {
  width: 100px;
  height: 100px;
  background-color: blue;

  float: left;
  margin-right: 20px;
}
```

- layout 잡는데 많이 사용
- ```html
  <body>
      <div class="container">

        <div class="box1 left"></div>
        <div class="box1 box2 left"></div>
        </div>
      </div>

    </body>
  ```

  ```CSS
    .box1 {
    width: 100px;
    height: 100px;
    background-color: orangered;
    border: 1px solid black;
  }

  .box2 {
    /* height: 200px; */
    background-color: aquamarine;
  }

  .left {
    float: left;
  ```

  **정리**

  - Float는 레이아웃을 구성하기 위해 필수적으로 활용되었으나, 최근 Flexbox, Grid 등장과 함께 사용도가 낮아짐
  - Float 활용 전략 - Normal Flow에서 벗어난 레이아웃 구성
    - 원하는 요소들을 Float로 지정하여 배치

### Flexbox

> Layout을 위해 탄생한 Flexbox
> CSS Flexible Box Layout

    - Float
    - Position

    - absoulte를 주면 normal flow를 줄 수 있음
    * 수동 값 부여 없이
      * 수직 정렬
      * 아이템의 너비와 높이 혹은 간격을 동일하게 배치

- 행과 열 형태로 아이템들을 배치하는 1차원 레이아웃 모델
- 축
  - main axis 메인 축
  - cross axis 교차 축
- 구성 요소
  - Flex Container 부모 요소
  - Flex Item 자식 요소

* 컨테이너 안에 아이템이 담겨 있다
* 컨테이너를 조작해서 아이템을 이리저리 배치하자

> Flexbox 축

- flexbox-direction: row

> Flexbox 구성요소

- Flex Container 부모요소
  - flexbox 레이아웃을 형성하는 가장 기본적인 모델
  - flex item들이 놓여있는 영역
  - display 속성을 flex 혹은 inline-flex로 지정
- Flex Item 자식 요소
  - 컨테이터에 속해 있는 컨텐츠(박스)
  -

```CSS
.flex-container {
  disply: flex;
}
```

> Flex 속성

- 배치 설정
  - flex-direction
  - flex-wrap
- 공간 나누기
  - justify-content(main axis)
    **메인 축**
  - align-content(cross axis)
    **교차 축**
    ```CSS
    .container {
    background-color: cadetblue;
    height: 300px;
    display: flex;
    align-items: center; /* 가운데 정렬 무조건 많이 씀*/
    /*align-items: stretch; 기본 값*/
    /* align-items: flex-start; */
    ```

}

- 정렬
  - align-items 모든 아이템을 cross axis 기준으로
  - align-self 개별 아이템
