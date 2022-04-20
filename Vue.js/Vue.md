## Vue.js
- 자바스크립트 프레임워크
- 간단하게 웹 페이지에 다양한 기능을 추가하는 것이 가능한 라이브러리

## SPA(Single Page Application)

웹 페이지 하나에 여러 가지 기능을 넣어 한 페이지로 다양한 기능을 동작하는 것

## Vue 주요 기능

|기능|서식|
|:---:|:---:|
|데이터를 있는 그대로 표시|{{데이터}}|
|요소의 속성을 데이터로 지정|v-bind|
|입력폼과 데이터를 연동|v-model|
|이벤트|v-on|
|조건문|v-if|
|반복문|v-for|
|데이터 계산 관련|computed|
|데이터 변화 감지|watch|
|애니메이션 처리|transition|
|컴포넌트|component|

## Vue.js의 특징

###  MVVM(Model-View-ViewModel) 패턴 사용

- 화면에 해당하는 View와 프로그래밍 로직을 분리하기 위해 사용

- View와 Model중간에 Viewmodel을 통해 데이터 바인딩 처리 가상 DOM을 통한 성능 및 개발의 편의성을 제공한다.


|View|ViewModel|Model|
|:---:|:---:|:---:|
|화면|연결 방식|데이터|
### 컴포넌트(Component)

- 특정 기능을 처리하는 화면(View)를 이루고 있는 작은 단위의 여러 개의 View 중에는 다른 화면에서도 사용되는 View가 있다 이런 단위를 재사용 할 수 있는 구조로 개발 하는 걸 컴포넌트(Component)라고 한다.

- vue로 개발된 파일이 모두 컴포넌트이다. 
