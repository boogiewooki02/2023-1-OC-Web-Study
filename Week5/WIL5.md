<HTML5 정리>
1.2 HTML5 기본문법

1.3 시맨틱 요소와 검색 엔진
시맨틱 태그란 브라우저, 검색엔진, 개발자 모두에게 콘텐츠의 의미를 명확히 설명하는 역할을 한다. 시멘틱 웹이란 웹에 존재하는 수많은 데이터에 의미와 관련성을 부여하는 것이다. 

1.4 웹페이지의 구성하는 기본 태그
모든 요소는 html요소의 자식 요소이다. lang 글로벌 어트리뷰트(ex: <html lang -="ko">)를 통해서 주언어를 설정할 수 있다. 메타데이터에는 검색키워드, 웹페이지 설명, 저자, refresh에 관한 내용을 적을 수 있다. 메타데이터를 제외한 웹페이즈를 구성하는 대부분의 요소가 body 요소 내에 기술된다.

1.5 텍스트 관련 태그
시맨틱 웹의 의미를 살려서 제목 태그는 제목 이외에는 사용하지 않는 것이 좋다. 태그를 사용하면 의미론적(Semantic) 중요성에 영향을 미친다. 


<CSS 정리>
2.1 CSS 기본 문법
HTML과 CSS는 각자의 문법을 갖는 별개의 언어이다. 그러나 HTML없이 단독으로 존재하는 CSS는 의미가 없다. 
*셀렉터: 스타일을 적용하고자 하는 HTML 요소를 선택한다. 
(ex: h1 {color:red;})
*프로퍼티: 셀렉터로 요소를 선택하고 {} 내에 프로퍼터와 '값'을 지정하는 것으로 다양한 스타일을 정의할 수 있다.
ex: p {
        color: orange;
        font-size: 16px;
    }
*HTML과 CSS의 연동
Link style: HTML에서 외부에 있는 CSS 파일을 로드하는 방식이다. 가장 일반적.
Embedding style: HTML 내부에 CSS를 포함하는 방식. 사용 지양.
Inline style: HTML요소의 style 프로퍼티에 CSS를 기술하는 방식. 사용 지양.

*Reset CSS: 브라우저 별로 제각각인 디폴트 스타일을 하나로 통일시키는 역할.

2.2 셀렉터
*전체 셀렉터: 모든 요소를 선택. 
*태그 셀렉터: 지정된 태그명을 가지는 요소를 선택.
*ID 셀렉터: id 어트리뷰트 값을 지정하여 일치하는 요소를 선택해서 적용.
*클래스 셀렉터: class 어트리뷰트 값을 지정하여 일치하는 요소를 선택해서 적용
*어트리뷰트 셀렉터: 지정된 어트리뷰트를 갖는 모든 요소를 선택.

복합 셀렉터(Combinatior)
*후손 셀렉터
*자식 셀렉터
*형제(동위) 셀렉터

가상 클래스 셀렉터: 요소의 특정 상태에 따라 스타일을 정의할 때 사용.
ex: 마우스가 올라와 있을때, 링크를 방문했을 때 등등

2.3 CSS 프로퍼티 값의 단위
2.4 박스 모델
2.7 폰트와 텍스트
2.8 요소의 위치 정의
2.9 요소 정렬