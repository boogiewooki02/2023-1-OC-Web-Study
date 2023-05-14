<웹스터디 7주차 강의 정리>
주제: 클론 코딩을 이용한 사이트 만들기

*클론 코딩을 위한 단계
1. 구현 페이지 분석
  유튜브 영상 재생 페이지를 예시로 분석해보자. 화면에는 헤더, 영상 재생부, 영상 게시자 정보, 영상 댓글, 추천 영상 목록 등이 있다.

2. 구획 나누기
  전체: view
    헤더: header
    헤더 외 아래 부분: container

      container 안에서 메인이 되는 부분: main-container
      사이드 부분: aside-container

        영상 재생부: video-container
        영상 게시자 정보: video-info-container
        영상 댓글: comment-container
  
  flex를 이용해 어떻게 배치할지 분석해본다.
    1. view : view 안에 header와 container가 flex-direction : columns 방향으로 배치 되어 있습니다.
    2. header : header안에 각종 버튼들이 row 방향으로 배치 되어 있습니다.
    3. container 안엔 main-container와 aside-container가 row 방향으로 배치 되어 있습니다.
    4. main-container 안엔 3개의 container가 columns 방향으로 배치 되어 있습니다.
    5. video-info-container 안엔 video의 제목, 게시자 정보 등이 columns 방향으로 배치 되어 있습니다.
    6. comment-container 안엔 댓글들이 columns 방향으로 배치 되어 있습니다.

  각각의 구획에서는 어떠한 기능이 들어갈지 결정한다.

3. CSS 초기화
  코딩에 들어가기 전에 CSS를 초기화 해준다. 필수는 아니지만, 모든 브라우저에 동일한 스타일을 적용하기 위한 단계이다.
  초기화하는 코드는 구글링을 통해서 얻으면 될 것 같다.
  초기화한 CSS 파일은 reset.css로 폴더에 저장한다. 이후 스타일을 적용할 style.css 파일을 만든 후 첫 줄에 @import 'reset.css' 코드를 삽입한다. 이로써 스타일 코드를 짤 준비를 마쳤다.

  *기본 html 틀
  <!doctype html> 을 통해 HTML5로 작성된 문서임을 알려준다
  <html lang="en"> language가 english임을 알려준다
  <head>
    <meta charset="utf-8"> 인코딩이 UTF-8로 되어 있다
    <meta name="viewport" content="width=device-width, initial-scale=1"> 
    <link rel="stylesheet" href="style.css"> link 태그를 통해 css 파일을 참조한다
    <title>유튜브 클론 HTML</title> 타이틀을 지정한다
  </head>
  <body>
  </body>
  </html> 

4. 앞에서 나눴던 구획대로 코드를 작성
  이때, 동일한 크기단위인 구획들을 묶어주는 것이 중요하다. 예를 들어, header와 main-container은 같은 위상을 가지고 있고 main-container 안에 있는 video-container, video-info-container, comment-container은 동일한 위상을 갖는다.

  style.css 파일에서는 html에서 사용될 스타일들을 작성한다. 이때, 한번만 사용되는 스타일은 id로, 재사용이 되는 스타일은 class로 작성한다. 참고로 class와 id가 중복되는 경우는 id가 우선순위에 있다. 

  각 class와 id는 display를 flex로 가지며, 배치 방향(row, column), justify-content, align-items, margin, padding, cursor, background-color 등을 필요에 맞게 설정해준다
  예시)
  1. 요소끼리 너무 붙어있지 않아야 합니다. → margin
     GDSC 웹 스터디 7주차 클론 코딩 9
  2. 요소의 테두리와 요소 안의 글씨나 이모티콘이
     너무 딱 붙어 있으면 안 됩니다. → padding
  3. 마우스를 올리면 회색으로 변합니다. → hover,
     background color gray
  4. 마우스를 올렸을 때 회색이 되는 부분이
     동글동글합니다.
  5. 마우스를 올리면 마우스 화살표가 손가락 모양으로 변합니다.

  html에서 코드를 작성한다. <div> 태그로 구획을 나누고 스타일을 지정하며 코드를 작성한다. 