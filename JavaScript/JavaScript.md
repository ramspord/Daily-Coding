### JavaScript 



자바스크립트는 사용자와 상호작용하는 언어이다.



개발자 모드에서 elements 는 태그 라는 뜻 



#### 1장 낮과 밤 

`<input type="button" value="night" onclick=""?`

타입은 버튼, 해당 버튼의 제목은 night, 온클릭은 누르면 반응이 오는 



#### 2장 자바스크립트 넣는 방법 

`<script></script>`  

이것이 자바스크립트 라는 것을 웹브라우저에게 알려주기 위한 태그 



HTML은 정적이고 

Javascript는 동적인 이유인 이유로 1+1를 예시로 들 수 있다. 

html은 1+1이 그대로 표시되지만 자바스크립트는 1+1 이 2로 계산되어 출력된다 

`<script>`

document.write(1+1);

`</script>`  



`<h1>html</h1>`

1+1



#### 3장 HTML와 Javascript 가 만나는 방법  (event)

onclick 뒤에는 반드시 Javascript가 와야 한다 

onclick="alert('hi')"

`<input type="button">` 버튼

`<input type="text">`   글 입력창

onchange

onkeydown 



#### 4장 콘솔 

개발자모드에서의 console 창에서도 자바스크립트를 실행할 수 있다. 

`alert('  '.length)`

.length 는 범위 안에있는 글자가 몇개인지 세주는 명령어 



#### 5장 데이터 타입 (자료형)

숫자는 그냥 숫자만 써도 되지만  1+1  =  2 

문자(열)는 "  " 따옴표를 붙여줘야한다.  "1"+"1"  = "11"

'Hello world'.toUpperCase()  하면 소문자였던것이 대문자가 되어 출력된다 "HELLO WORLD"

'Hello world'.indexOf('d')  사이에 d를 치면 d가 몇번째인지 숫자로 나타내준다 "10"

'Hello world'.trim() 하면 따옴표 사이에 있는 공백을 없애준다 "Helloworld"



#### 6장 변수와 대입 연산자 

변수라는 것은 바뀔 수 있는 어떤 값 

x = 1; 

x 는 =(대입 연산자)를 통해 값이 변할 수 있는 변수 / 값이 변하지 않는건 상수 



변수를 왜 쓰는가?

enter 를 치면 실행이 되지만 shift + enter를 치면 실행이 유보된다 



변수를 치기전에 앞에 var 라고 쳐주는 것이 좋은 습관이다 

var name = '  ';

variable 



#### 7장 CSS 기초 (패쓰)



#### 8장 제어할 태그 선택하기 (주간모드 야간모드)

`<body>

`<input type="button" value="night" onclick=" 

document.querySelector('body').style.backgroundColor='black';

document.querySelector('body').style.color='white';

">`

`<input type="button" value="day" onclick=" 

document.querySelector('body').style.backgroundColor='white';

document.querySelector('body').style.color='black';

">`

</body>`

- 이 문서에서 웹 브라우저에게 질의한다  CSS의 셀렉터 ('body') 

  query 는 질의하다의 의미 

  .color 는 텍스트 (글자)의 색 변환을 담당

  또한 

  CSS에서는 바탕색 명령어가 background-color인 반면 

  자바스크립트에선 backgroundColor   C 가 대문자로 온다 



#### 9장 프로그램, 프로그래밍, 프로그래머

프로그램 = 순서 

프로그래밍 = 순서를 만드는 행위 

프로그래머 = 순서를 만드는 사람 

HTML은 순서에 따라 진행되지 않지만 

아래 (주간모드/야간모드) 코드처럼 

`<input type="button" value="night" onclick=" 

document.querySelector('body').style.backgroundColor='black';

document.querySelector('body').style.color='white';

">`

버튼을 누르면 까매지고 글자가 하얘진다 처럼 

자바스크립트는 순서에 따라 작업이 진행된다. 



#### 10장 조건문 (if)

하나의 프로그램이 하나의 흐름으로 가는 것이 아니라 조건에 따라서 다른 순서의 기능들이 실행되도록 하는 것 

토글 = 낮과 밤을 바꾸는 것처럼 상반된 결과를 가져다 주는 기능의 명칭 



#### 11장 비교 연산자와 블리언 

비교 연산자  ===  Comparison operators

블리언 true  false  Boolean 

`document.write(1===1);`

true 

`document.write(1===2);`

false



`<h3>1&lt;2</h3>`

`<script>document.write(1<2);</script>`

1&lt2  는  1< 2 와 의미가 같다    & 엔퍼센트 less than ;



#### 12장 조건문 (Conditional statements)

`<script>`

document.write();

if (true/false) {

document.write(); (true면 실행 그리고 3번이 패쓰되고)

}else {

document.write(); (false면 실행 2번이 패쓰된다)

}

document.write();

`</script>`



if 뒤 () 안에는 boolean 데이터 타입(true/false)이 온다. 

따라서 조건에 따라 true가 오고 false가 오게끔 하면 된다. 



#### 13장   조건문 주간/야간모드 



`<input id="night_day" type="button" value="night" onclick="`

if(document.querySelector('#night_day').value === 'night'){

document.querySelector('body').style.backgroundColor= 'black';

document.querySelector('body').style.color='white';

document.querySelector('#night_day').value ='day';

}else{

document.querySelector('body').style.backgroundColor= 'white';

document.querySelector('body').style.color='black';

document.querySelector('#night_day').value ='night';

}

`">`



#### 14장 리팩토링 (중복의 제거)

틈틈히 해야 좋은 프로그래밍을 할 수 있다 

비효율적인 것들을 제거하는 것 



`<input type="button" value="night" onclick="`

if(this.value === 'night'){

document.querySelector('body').style.backgroundColor= 'black';

document.querySelector('body').style.color='white';

this.value ='day';

}else{

document.querySelector('body').style.backgroundColor= 'white';

document.querySelector('body').style.color='black';

this.value ='night';

}

`">`

- 위는 중복된 document.querySelector('#night_day') 해당 명령어를 this 로 바꾼 것이다 
- this는 자기 자신을 가리킨다 따라서 자기 자신을 가리키는 위 명령어는 this로 바꾸어 사용할 수 있는 것이다.



`<input type="button" value="night" onclick="`

var target = document.querySelector('body'); 

if(this.value === 'night'){

target.style.backgroundColor= 'black';

target.style.color='white';

this.value ='day';

}else{

target.style.backgroundColor= 'white';

target.style.color='black';

this.value ='night';

}

`">`



- 또한 위는 중복된 document.querySelector('body') 명령어를 target이라는 변수에 대입해 코드의 중복을 제거한 예시이다. 



#### 15장 반복문 (배열)



var coworkers = ["egoing", "leezche"];

document.write(coworkers[0]);   0번째 배열 추출 / 배열은 항상 0부터 수를 센다.

document.write(coworkers.length);  배열안에 단어가 몇 개가 있는지 확인하는 명령어 /  2 / length는 1부터 

coworkers.push('duru');

coworkers.push('taeho');  배열에 단어 추가하는 명령어 



#### 16장 반복문  

반복문의 영문명은 Loop 

`<script>`

document.write('<li>1<li>');

var i =0;   ( i 가 0이라면)

while(i < 3){   (0<3, 1<3, 2<3, 3=3)

document.write('<li>2<li>');

document.write('<li>3<li>');

i = i  + 1; (0+1, 1+1, 2+1)

}

document.write('<li>4<li>');

`</script>`



- 반복문의 기본문법은 while (){}

  if 문은 if(){}   if 뒤 () 괄호에 true or false (boolean)데이터 타입이 들어간다 

  while문은 if문과 비슷하지만 

  while 괄호 안이 (true)이면 {} 중괄호 안 데이터는 반복적으로 실행된다.

  그리고 괄호 안이 (false)가 되면 그 다음 명령어로 넘어간다 

  위 코드는 i 가 반복해서 3이 된 후 숫자 4로 넘어간 예시이다



#### 17장 배열과 반복문 

22/38





 















































 









 

 
