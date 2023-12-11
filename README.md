# css style sheet
----
## css 작성위치 
* 내부스타일시트 `<head><style>여기 작성</style></head>`
* 외부스타일시트 style/파일명.css 별도 생성 후 
    `<link rel="stylesheet" href="./style/파일명.css">`
--
## font-family 글꼴 설정
* `선택자 {font-family:`대표글꼴`, `보조글꼴`}`
* 모든 사용자에게 동일한 글꼴을 보여줄 수 있도록 웹 글꼴을 사용하는 것이 좋다.! fonts.google.com 추천
------------------------------
<스스로 공부한 것 정리하는 용도>
## font-size
* px 단위는 절대 크기값으로 사용자별 글자크기를 지원 x 
* px가 아닌 em rem % 상대적 단위를 사용해야한다.

## font size 글자크기 
* 웹브라우저 평균 글자 크기는 16px(100%)이다.
* px은 절대크기이므로 모바일 디바이스에 적합하지 않아 em 또는 rem 단위를 사용한다.(%가능)
* `선택자 {font-size:1.0em;}`
* `선택자 {font-size:1.0rem;}`
* `선택자 {font-size:100%;}`
* 글자크기값은 부모에 상속받게 하지 않고 적용 대상 자체한테 작성하는 것이 좋다!(이유: 부모한테 줄 경우 우선순위에 가로 막혀서 적용안됨.)
* ★★개발자도구(F12) 우선순위 CSS를 자주 확인해야한다.!!

---
## color 글자색상 
* 글자색상은 단순 테스트 용도로 사용할때는 영문으로 사용한다 . ex)aqua,blue
* 실제 디자인 용도로 사용할 때는 rgba, #헥사코어 6자리, 3자리를 사용한다.
* `선택자 {color:#ff0000}`
* `선택자 {color:rgba(255,0,0,0.5);}`
-----------------------------------------------
## line-height 행간
* 행간 값은 1.0(100%) 또는 50px 방식으로 작성한다.
* `본문 12 ~ 18px 내용 글자 크기 기준 1.3 ~ 1.7 값을 많이 사용한다. (평균1.5)`
* 제목 글자의 경우 글자크기에 따라 행간값은 상대적으로 다르기 때문에 자주 체크하며 수정해야한다.
------------------------------------------------------------
## float (CSS 2.0) 1207
* left right 좌우 방향으로만 정렬하는 레이아웃 속성
* float 해제하고 싶은 대상엔 clear:both 이용해서 해제가능 
* 정렬되는 형제 대상에 float 명령을 주고 부모엔 height 또는 
* overflow:hidden 을 적용해서 float 오류 해결 가능  
-----------------------------------------------------------------------
## flex (CSS3)
* 메인축, 교차축의 방향 기준으로 다양한 정렬을 설정할 수 있는 새로운 CSS3의 레이아웃 속성
### flex 적용 순서 및 주의사항 
1. 메인축으로 정렬하고 싶은 item 대상 선정 
2. 1번 item의 부모 container에게 `display:flex` 입력
3. 부모 container에게 item 정렬 방향과 줄바꿈의 속성을 `flex-flow:derection wrap`입력 
4. 부모 컨테이너에게 flex-flow에서 정한 방향(direction)에 따라 
정렬 방법을 `justify-content: 정렬방법` 입력
5. (교차축 설정 - 교차축 대상이 1줄, 2줄인지 check! )
5-1. 1줄일 경우 부모에게 `align-items:값`
5-2  2줄일 경우 부모에게  `align-content:값`
6. 특정 item만 교차축을 다르게 설정하고 싶다면? 자식(item)에게 `align-self:값`
7. (선택) item의 태그순서와 다르게 화면에서 보이는 순서를 다르게 하고 싶다면 `order:값`
8. (선택) item의 너비값을 전체 부모 기준으로 일정하게 ㅅㄹ정하고 싶다면? `flex:값`
--------------------------------------------------------------------------------

# project blog 23/12/08 
## title : 작은 가든 만들기 
* index.html(main)
* plants_kind.html(어울리는 식물소개)
* plants_supplies.html(화분&용품)
* plants_raise.html(내가키우는식물)
* ※ 모든 html은 서로 '뒤로/앞으로' 기능없이 이동할 수 있어야한다.
------------
## 공통영역 HTML, CSS 
* 모든 HTML 공통으로 존재해야하는 HTML = > header , main(내용만 제거), footer
* CSS 공통영역 == > reset, common.css(Header , main, footer)
* CSS 개별영역 == > index.html, plants_kind.html(어울리는 식물소개), plants_supplies.html(화분&용품) plants_raise.html(내가키우는식물) 메인의 내용영역 
---------
