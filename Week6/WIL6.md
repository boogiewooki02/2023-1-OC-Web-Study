*Gdsc 웹 6주차 강의정리
주제: Box model

박스의 테두리 = border
모든 요소는 박스 안에 있었다.

박스의 2가지 종류
1. 블록 레벨 요소 -> 한 줄을 차지하는 박스 (부모요소 전체 공간 차지)
2. 인라인 레벨 요소 -> 자신만을 감싸는 박스


content -> padding -> border -> margin (안쪽부터 순서대로)

border : 테두리
content : 걍 안에 있는 내용
padding : 컨텐츠와 border 사이의 간격
ex) padding: 20px -> 컨텐츠와 border 사이의 간격을 20px로 설정
margin : border로부터 다른 컨텐츠 사이의 여백 (컨텐츠와 컨텐츠 사이의 여백)

top -> right -> bottom -> left (시계방향 순으로)
ex) margin: 10px, 20px, 0, 30px -> 순서대로 적용됨

tip: 창에서 f12 누르고 스타일에서 가장 아래로 내리면 box style의 구성을 볼 수 있다.



Flex BoxLayout
-> Flexible Layout

아이템이 배열될 방향인 ‘주축’을 정할 수 있다.
ex) 나열된 요소를 가로로 배열하거나 할 수 있음

justify-content : main axis (주축)
align-item : cross axis (아이템을 넣는 순서..?)

무작정 외우기보다는 직접 사용해보는 것이 좋다. (많이 써보는 게 답이다)

더 알아보면 좋을 것들
1. css grid layouts
2. can I use?


6주차 과제를 하며 배운 css 문법들 정리
*속성(각 속성들은 지정된 값으로 사용할 수 있다):
justify-conent: 플렉스 요소의 수평 정렬 방식
align-items: 플렉스 요소의 수직 정렬 방식
flex-direction: 플렉스 컨테이너(flex container)안의 플렉스 요소(flex item)가 위치할 방향을 설정함.
flex-wrap: 플렉스 라인에 더 이상의 여유 공간이 없을 때, 플렉스 요소의 위치를 다음 줄로 넘길지를 설정함.
flex-flow: flex-direction 속성과 flex-wrap 속성을 이용한 스타일을 한 줄에 설정할 수 있음.