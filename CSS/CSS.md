### CSS



초창기의 색 표현 방법 

`<font color="red">HTML</font>` 

--------

웹브라우저가 처음 등장했을때는 HTML 언어만 해석되도록 설정되어 있어 모든 코드를 HTML이라고만 생각했다.

`<style></style>`  

위 CSS 태그는 HTML밖에 모르는 웹브라우저에게 이제부터 CSS 문법에 따라 꾸미기 방법을 적용하라고 알려주는 태그이다. 

----------------

 `<a href="2.html">`CSS`</a>`  CSS 글을 빨간색으로 바꾸고 싶다면

1. 첫번째 방법, style 태그를 이용하는 방법 

```<head>
<head>

<style>
a {
  color:red;
}

</style>  

</head>  이런식으로 헤드 태그 안쪽에 집어넣는다. 
```



 `<a></a> `  a 태그의 글을 빨간색으로 바꾸고 싶다면 위와 같이 

a {} 중괄호 안에 color : red ;  이런식으로 적어주면 된다. 

------

a 는 선택자라고 부른다 (누구를 선택해서 바꿀것이냐 해서 선택자)

{}는 효과 혹은 선언이라고 한다. 

color:red;

속성(효과):값 

property:value 



2. 속성을 이용하는 방법

위 방법과 다른 또 하나의 방법이 있다 

이는 body 태그안에 직접넣는 법으로 이러한  style 방식은 style 속성이라 한다. 

 `<a href="2.html" style="color:red">`CSS`</a>` 



; 는 구분자 

밑줄을 없애고 싶다면 

 `<a href="2.html" style="color:red; text-decoration:none;">`CSS`</a>` 

----------

`<h1></h1>` 태그를 이용했는데 글자를 더 크게 하고 싶다면 

style 태그 안에 



h1 {

font-size:45px; 

}



이런식으로 사이즈를 px 단위로 지정해주면 된다. 

혹은 구글에 css text size property 라고 검색하면 방법이 나온다. 



text-align: center;  가운데 정렬 



----------



id 선택자가 힘이 가장 강하고 > class 선택자가 그 다음 > a {}  태그 선택자가 가장 힘이 약하다 

그러므로 style 태그에서 순서를 지정할때 잘 고려해야한다.   

`<a href="index.html"class="saw">HTML</a>`

`<a href="1.html"class="saw">CSS </a>` 

`<a href="2.html">JavaScript</a>` 

이렇게 세 줄이 있을 때 HTML과  CSS만 색갈을 바꾸고 싶다면 

둘을 하나의 class 로 묶어서 

`<style>`

.saw {

color:gray;

}

`</style>`

이런식으로 적으면 된다  saw 앞에 . (점) 이 class를 뜻한다. 

----------------

`<a href="1.html"class="saw" id="active">CSS </a>`



`<style>`

#active {

color:gray;

}

`</style>`



id는 #으로 표현  또한 한번밖에 못 쓴다 



더 알고 싶다면 CSS selector  검색 

-------

### CSS BOX MODEL



border 는 테두리  border: 5px solid red;

padding 은 글자와 테두리 사이의 간격 (여백)  20px;

margin 테두리와 테두리 사의 간격 0으로 하면 없어지고 20px 등 크게하면 커진다 

width 는 폭이라는 뜻 

height 는 높이 



![boxmodel](C:\Users\zwzw9\Downloads\boxmodel.png)



개발자모드로 들어가면 상태 확인이 가능하다 .  (매우중요)

-----------

border 하면 테두리가 그려지고 

border-bottom  하면 테두리의 아랫부분만 남는다 

-------------------

10/16 그리드 

 `<div>` 태그는 division(분할) 의 약자 

아무런 의미도 없고 단지 디자인의 용도로 쓰는 무색무취의 태그 

화면 전체를 쓰는 태그이기 때문에 줄 바꿈 안 써도 다음줄로 넘어감 



`<div>NAVIGATION</div>` 

`<div>ARTICLE</div> `  



`<div>` 태그 안에 `<div>` 태그를 또 쓸 수 있다 



`<span>` 태그는 똑같은 태그이나 인라인 태그로 

줄바꿈이 자동으로 되는 `<div>` 태그와 상반되게 다음 내용이 한 줄에 이어진다. 



`<div id="grid"></div>`



#grid{

display:grid;

grid-template-colums: 150px 1fr;

} 



fr은 화면 전체를 쓰겠다는 뜻 

grid 를 쓰면 가운데 줄  두 파트로 나눌 수 있다. 

colums 는 한 줄로 표현하겠다는 의미. 

rows 는 행 

cols 는 열 



----------------------------------------------------------------------

