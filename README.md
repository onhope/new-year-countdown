# new-year-countdown
<img src="./New%20Year%20Countdown.gif">

<br>

## 기능
2024년 새해 카운트 다운 시계  

<br>

## 학습
### 1. css : 가상요소 ::before ::after  
HTML을 통해 생성된 요소 앞뒤에 새로운 요소를 추가하는 기능을 제공하는 가상 요소  

**가상 요소 :before :after 특징**

- inline 요소 이므로 너비(width), 높이(height) 값을 가질 수 없다. 크기 값을 바꾸려면 inline-block 옵션을 주어야 한다.
- content: '들어갈 컨텐츠 내용'; 형식으로 시작한다.
- margin 값의 left, right는 가질 수 있으나 top, bottom은 가질 수 없다.
- padding 값은 상하좌우 모든 방향에 대해서 값을 가질 수 있다.

<br>

가상 요소는 컨텐츠의 앞뒤에 기호, 도형, 수식어 등을 사용하여 컨텐츠를 장식할 필요가 있을 때 많이 사용   

**: : before( )와 : : after( )**  
보통 'content' 속성과 함께 사용됩니다.   
'content' 속성에 정의된 값을, 선택된 요소의 첫 번째 자식 요소로 추가합니다.  

```
p::after {
  content: " - Remember this";
  background-color: yellow;
  color: red;
  font-weight: bold;
}

p::before {
  content: "Read this -";
  background-color: yellow;
  color: red;
  font-weight: bold;
}
```

<br>

### 2. css : css 변수 
변수를 선언해 두면 <u>유지보수</u>에 용이하다. 

**CSS 변수 선언 및 호출**  
CSS에서 변수의 이름을 지정할 때는 변수 맨 앞에 -- 를 붙여주어야 한다. 그리고 변수를 호출해 사용할 때는 var(변수명)형식을 사용한다.
```
:root {
	--main-font-color: #000f22;  /* CSS 전역 변수 선언 */
}

div {
	color: var(--main-font-color);   /* CSS 변수 사용 */
}
```

<br>

### 3. js : Date
Date 객체를 사용하여 매 순간 변화하는 시간과 날짜에 관한 정보를 손 쉽게 얻을 수 있음  

Date 객체를 활용하면 <u>생성 및 수정 시간을 저장하거나 시간을 측정할 수 있고, 현재 날짜를 출력하는 용도</u> 등으로도 활용할 수 있음  

**Date 객체 생성하기**   
인수 없이 호출하면 현재 날짜와 시간이 저장된 Date 객체가 반환
```
let now = new Date(); // 객체 Date 생성
alert( now ); // 현재 날짜 및 시간이 출력됨
```

<br>

**날짜 구성 요소 얻기**
|메서드|의미|
|---|---|
|getFullYear()|연도(네 자릿수)를 반환합니다.|
|getMonth()|월을 반환합니다(0 이상 11 이하)|
|getDate()|일을 반환합니다(1 이상 31 이하)|
|getHours(), getMinutes(), getSeconds(), getMilliseconds()|시, 분, 초, 밀리초를 반환합니다.|
|getDay()|일요일을 나타내는 0부터 토요일을 나타내는 6까지의 숫자 중 하나를 반환. getDay에선 항상 0이 일요일을 나타냅니다. 이를 변경할 방법은 없습니다.
|getTime()|주어진 일시와 1970년 1월 1일 00시 00분 00초 사이의 간격(밀리초 단위)인 타임스탬프를 반환합니다.
|getTimezoneOffset()|현지 시간과 표준 시간의 차이(분)를 반환합니다.
 
<br>

**날짜 구성요소 설정하기**  
|메서드|의미|
|---|---|
|setFullYear(year, [month], [date])|현지 시간 기준으로 연도(네 자리 연도면 네 자리로)를 설정합니다.
|setMonth(month, [date])|현지 시간 기준으로 월을 설정합니다.
|setDate(date)|현지 시간 기준으로 일을 설정합니다.
|setHours(hour, [min], [sec], [ms])|현지 시간 기준으로 시를 설정합니다.
|setMinutes(min, [sec], [ms])|현지 시간 기준으로 분을 설정합니다.
|setSeconds(sec, [ms])|현지 시간 기준으로 초를 설정합니다.
|setMilliseconds(ms)|현지 시간 기준으로 밀리초를 설정합니다.
|setTime(milliseconds)|Date가 나타낼 시간을 1970년 1월 1일 00:00:00 UTC로부터의 경과시간(밀리초)으로 설정합니다. 기준 이전의 시간은 음수 값을 사용해 설정할 수 있습니다.

<br>

### 4. js :setTimeout()  
일정 시간이 지난 후 정해진 코드를 실행하게 합니다.   

```
setTimeout(function () {
  console.log("Hello World");
}, 2000);

console.log("setTimeout() example...");

// 2초가 지나면 javascript가 "Hello World"를 출력
```

<br>

## 학습출처
**유튜브**  
https://www.youtube.com/@JavaScriptKing

**css**  
https://developer.mozilla.org/  
https://www.w3schools.com/  

**css : 가상요소**  
https://hianna.tistory.com/726  


**css : css 변수 선언**  
https://inpa.tistory.com/entry/CSS-%F0%9F%93%9A-CSS%EC%9A%A9-%EB%B3%80%EC%88%98-variable-%EC%A0%95%EB%A6%AC

**js : Date**  
https://ko.javascript.info/date