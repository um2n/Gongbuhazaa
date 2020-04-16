## CSS (Cascading Style Sheets)
  
 ***
  
#### * 구조  

```
article{
    fontfamily:'맑음 고딕';  
    font-size: 16px;
    color:blue;
}
```

##### 1. 선택자(Selector)  
: HTML의 ```<article>``` 태그를 가리키고 있는 article을 말한다. 스타일을 지정할 특정 HTML 요소를 선택하는 역할을 수행한다. 
> ','로 여러 개의 스타일을 한꺼번에 지정할 수 있다.
```
h1, p {
    color:red;
}
```

##### 2. 속성(Property)  
: ```font-family```, ```font-size```에 해당하는 부분이며 지정, 변경하고 싶은 스타일 속성의 이름이다.  
> _font-size, color, background, position 등 다양한 요소를 사용할 수 있다._  
  
##### 3. 값(Value)  
: ```16px```, ```blue```에 해당하는 부분이며 값은 일반적으로 CSS에 정의된 특정 키워드(blue, block 등)과 수치와 특정 단위(px, %, em, rem, vh, vw 등)으로 나뉜다.  
> _값은 프로퍼티와 짝을 이루어 사용한다.(<b>선언</b>) 각 프로퍼티에 허용되는 값의 종류가 정해져 있다._
  
##### 4. 선언 블록(Declaratio Block)  
: {} 안의 한 덩어리를 말한다. 각각 적혀 있는 선택자에 한해 스타일이 적용된다. 선언 블록 내부의 다른 선언과 ;로 구분한다.  



#### * 기본 단위  

##### 1. 고정 크기 단위  
* ```px``` : pixel, 디스플레이를 구성하는 최소 단위  
* ```pt``` : point  
* ```in``` : inch  
* ```cm```, ```mm```  
  
##### 2. 가변 크기 단위  
* ```em``` : 현재 스타일이 지정되는 요소의 폰트 크기를 기준으로 설정한다.  
* ```rem``` : 최상위 요소의 폰트 크기를 기준으로 설정한다.  
>  _습관적으로 rem을 사용할 것_  
* ```%``` : 이미지나 레이아웃의 너비나 높이를 지정할 때 자주 쓰인다.  
  

#### * 색상  

##### 1. 키워드  
내부적으로 지정되어 있는 키워드를 쓴다. 다른 방식에 비해 수가 제한적이다.  

##### 2. RGB  
빛의 3원색인 빨,초,파를 혼합하여 색을 표현한다. 0~255값으로 나타낸다.  

##### 3. HEX Code  
16진수 6자리 코드로 색상을 표현한다.  
``` 
#FF0000 = 빨간색, #800080 = 보라색  
```
##### 4. Alpha  
투명도를 말한다.  
```
RGB에서
rgba(23,41,13,0.5)  
  
HEX Code에서  
#23fe4e55 
```  


#### * 선택자  
  
##### 1. 단순 선택자  

* ```타임 선택자``` : 해당 태그를 가지는 모든 요소에 스타일을 적용한다. 
```
<h1> 저는 h1 태그입니다. </h1>  
<p> 저는 p 태그입니다. </p>  
```

* ```아이디 선택자``` : 아이디 이름으로 스타일을 적용한다.  
```
<p id="goorm"> 저는 p 태그입니다. </p>
  
#goorm{
    background-color: blue;
}
```

* ```클래스 선택자``` : 비슷한 특징을 갖는 요소를 지정하여 묶어 그룹으로 만들 수 있다.  
```
<p class="student"> 학생</p>
<p class="teacher"> 선생님</p> 
  
.student{
    color:white;
}
.teacher{
    color:black;
}
```

* ```전체 선택자``` : 모든 요소에 스타일을 적용한다. 모든 요소에 적용시키기 때문에 속도가 저하될 수 있다. 선택자 자리에 *를 입력하면 된다.  

```
*{
    color:yellow;
}
```
  
* ```속성 선택자``` : 특정 HTML 속성을 가지고 있는 모든 요소에 스타일을 적용한다. 선택자 오른쪽에 []로 속성과 속성값을 넣으면 된다.  

```
선택자[속성명="속성값"]{
    color:pink;
}
```
  
##### 2. 복합 선택자  

* ``` 부모 - 자식 - 후손 요소```  : 관계는 상대적이다. 상위 태그가 부모태그, 하위 태그가 자식태그가 된다.  
*  ```자식 선택자``` : 선택자 A의 모든 자식 중 선택자 B와 일치하는 요소를 선택한다. 자식 선택자는 복합 선택자이기 때문에 선택자를 두 개 사용하며 '>'를 써준다. 바로 하위에 해당하는 자식 요소에만 스타일을 적용하고 싶을 때 사용한다.  
```
div > p {
    color:green;
}
``` 

* ``` 후손 선택자``` : 선택자 A의 모든 후손 중 선택자 B와 일치하는 요소를 선택한다. 중간에 띄어쓰기를 사용한다. #me 밑의 모든 태그가 선택됨
```
div p {
    color:yellow;
}
```  

* ```가상 클래스 선택자```  
가상 클래스 : 직접 정의할 수 없고 실제 HTML에 보이지 않는다.  
```
선택자:pseudo-class{
    color:red;
}
```
가장 대표적인 가상 클래스는 <font color="red">링크 태그</font>와 관련됐다.  

>   - a:link : 방문하지 않은 링크일 때
>   - a:visited : 방문한 링크일 때  
>   - a:hover : 링크에 마우스를 올렸을 때  
>   - a:active : 선택된 링크일 때  


#### * 박스 모델  
: 박스 형태를 만들 때 쓴다. 내용(Content), 패딩(Padding), 경계선(Border), 마진(Margin)으로 구성된다.  

##### 1. 내용(Content) : 실제로 내용을 담고 있는 부분

보통 요소의 크기를 정할 때 width나 height를 많이 사용한다. 이런 너비와 크기는 content의 크기에 해당한다.
>   _개발자 도구 > inspect > #inner로 크기 확인_ 
```
#inner{
    background-color:pink;
    width:200px;
    height:100px;
} 
```

##### 2. 경계선(Border) : 컨텐츠를 감싸고 있는 테두리   

경계선은 세 프로퍼티인 border-style, border-width, border-color를 사용한다.  
```
<div id="main">
	<div class="inner">
		TOP
	</div>
	<div class="inner" id="target">
		DOWN
	</div>
</div>  

body { background-color: skyblue; }
.inner {
    background-color: pink;
    width: 200px;
    height: 100px;
}
#target {
	border-color: black;
	border-style: solid;
	border-width: 8px;
}
```
_#target에 검은 테두리가 생김_  

* ```border-style``` : 선의 종류를 지정하는 프로퍼티.  
```none```, ```hidden```, ```dotteed```, ```dashed```, ```solid```, ```double```, ```groove```, ```ridge```, ```inset```, ```outset```, ```initial```, ```inherit```  
  
```
#target{
    border-style : solid dashed dotted double;
}
```
_top, right, bottom, left 순서로 스타일이 지정됨_  

>   1개 : 상하좌우, 2개 : 상하/좌우, 3개 : 상/좌우/하, 4개 : 상/우/하/좌  

* ```border-width```, ```border-color``` : 선의 두께와 색 지정하는 프로퍼티. border-style 없이 지정했을 때에는 적용되지 않는다.  

>   ```shortcut``` : 한 번에 지정할 수 있다.  
```border:red solid 1px;```  

* ```border-radius``` : 경계선을 둥글게 표현할 때 사용한다.   
```
<div id="main">
	<div class="box radius">border-radius</div>
</div>
```  
_border-radius의 값은 모서리의 반지름의 값_  
_border-radius는 테두리 존재 여부와 별개로 전체 백그라운드에 적용된다._  

_```shortcut``` : 한 번에 지정하거나 네 방향으로 나눠 부분적으로 적용가능.  
4등분으로 나눠서 top-left, top-right, bottom-right, bottom-left 순서로 적용된다._  
 _타원형의 radius를 적용할 때에는 가로 반지름, 세로 반지름 순서로 적용된다_  

##### 3. 패딩(Padding) : 컨텐츠와 경계선 사이의 여백  
_top, right, bottom, left 순서로 스타일이 지정됨_  

##### 4. 마진(Margin) : 경계선 밖의 여백  
_top, right, bottom, left 순서로 스타일이 지정됨_

* ```마진 상쇄``` : 위아래로 맞닿은 두 요소 사이의 마진은 더 큰 쪽을 기준으로 결정된다. 각각 마진을 따로 적용하더라도 서로 맞닿아 있다면 마진이 따로 존재하지 않는다는 말이다.  

##### 5. box-sizing  
box-sizng: content-box; 는 컨텐츠박스를 기준으로 크기를 정하지만, box-sizing: border-box;의 크기는 border 바로 전 padding까지를 기준으로 정해진다.  
  
```box-sizing:content-box;``` : width(height) = content size  
```box-sizing:border-box;``` : width(height) = content size + padding + border size  

#### * 글자 관련 스타일  

##### 1. 폰트 종류와 웹 폰트  

* ```font-family```

한 단어로 구성된 폰트명은 따옴표 없이 사용할 수 있지만, 띄어쓰기나 '-'가 들어간 폰트명은 따옴표를 사용해야 한다.  
```
font-family : '폰트이름1' '폰트이름2';
```  
_모든 이용자의 기기에 동일한 폰트가 없을 수도 있기 때문에 폰트를 여러 개 지정하여 앞 순서에 위치한 폰트부터 차례로 적용한다._
> 가장 보편적으로 사용하는 글꼴 : Sans-serif, Serif, Cursive, Fantasy, Monospace  

* ```Web Font``` : 링크를 통해 폰트를 불러오는 방식  

##### 2. 폰트의 크기와 형태  

* ```font-style``` : normal, italic, oblique 등이 있다.  
* ```font-weight``` : 폰트 굵기를 지정할 때 사용한다.  
>   bold나 100~900까지의 숫자 중 100 단위의 숫자값을 사용할 수 있다. _normal은 400, bold는 700_  
```
font 프로퍼티를 사용하면 모든 과정을 한 번에 사용 가능하다.  
  
font-style, font-weight, font-size, font-family를 순서대로 띄어쓰기로 구분하여 사용해야 함  
```  

##### 3. 텍스트 정렬  

* text-align : 좌, 우, 중앙 정렬할 때 사용한다.  
```
<h1>텍스트 정렬</h1>
<p id="right">오른쪽 정렬</p>
<p id="middle">가운데 정렬</p>
<p id="left">왼쪽 정렬</p>
```  
>   _```justify``` : 좌우로 띄어쓰기를 늘려 붙인다._  

* ```line-height``` : 문장 사이의 간격을 조정한다. 단위가 존재하는 값 또는 단위가 없는 숫자 값으로 높이를 조정한다. 단위 없는 숫자 값은 해당 요소의 font-size를 기준으로 한 배수로 높이를 조정한다. 
```
.line-height : 2;
```
```
.line-height : 30px;  
``` 

> _글자의 하단부 사이의 거리가 아닌 그 글자 라인의 높이를 말한다_  

* ```letter-spacing``` : 자간(각 글자 사이의 간격)을 조정한다.  
```
letter-spacing : 5px;
```  

*``` text-indent``` : 문단의 시작부에 들여쓰기를 지정한다.  
```
text-indent : 16px;
```  

#### * 위치 정렬  
  
##### 1. block과 inline  

* ```display``` : 요소가 보여지는 방식을 지정하는 프로퍼티.  

* ```display:block``` : 항상 새로운 줄에서 시작하며, 따로 너비를 지정하지 않아도 width:100%을 기본 값으로 가진다.
_div, h1~h6, p, header, footer, section 등이 해당된다._  

* ```display:inline``` : block과 달리 새로운 줄에서 시작하지 않으며 필요한 만큼의 너비만 가진다. = 요소의 컨텐츠 크기만큼만 너비를 가진다.  
_span, a, img 등이 해당된다._  

>   block은 전체 문단과 같이 큰 맥락을 가질 때 사용하는 반면, inline은 그 안에 들어가는 단어, 링크, 이미지 등에 쓰인다.  ```block은 width, height, margin, padding 등을 모두 사용할 수 있지만, inline은 지정할 수 없다.```  
  
##### 2. inline-block  
  
```display:inline```에서 width, height, margin-top, margin-bottom 프로퍼티가 적용되지 않아 불편한 것을 해결하기 위해 ```display: inline-block```을 사용한다.  
  
* ```display: lnline-block``` : block과 inline 요소의 특징을 모두 가진다. 쓰임은 inlie과 동일하지만, 사용할 수 없었던 width, height, margin-left, margin-right을 지정할 수 있다.  

* ```display:none``` : 브라우저에 해당 요소가 출력되지 않는다.  

##### 3. position  
: 요소를 배치하는 방법을 정하는 프로퍼티  

* ```position:static``` : 요소의 position 값은 static이 기본이다. static에서는 좌표 프로퍼티를 사용할 수 없다.  
_좌표 프로퍼티 : top, right, botto, left_  

* ```position:relative``` : 상대 위치. 좌표 프로퍼티를 사용할 수 있는 점만 static과 다르다.  

* ```position:absolute``` : 절대 위치. 부모 요소나 조상 요소 중 relative, absolut, fixed가 선언된 곳을 기준으로 좌표 프로퍼티가 작동한다.  

* ```position:fixed``` : 보이는 화면을 기준으로 좌표 프로퍼티를 이용하여 위치를 고정시킨다.
>   _스크롤할 때 따라다니는 메뉴_  

* ```z-index``` : 수직으로 어떻게 쌓이는지를 정하는 프로퍼티로 값은 숫자로 표현된다. 숫자가 클수록 전면에 출력된다. static을 제외한 요소에서만 적용된다.  

##### 4. float  
: 요소를 어떻게 띄울지 결정한다. 요소를 디자인의 흐름에서 벗어나게 한 뒤, 사용자가 지정한 방향에 배치하도록 하는 프로퍼티다.  


#### * 위치 정렬 - flexbox  
: flexbox는 부모요소인 flex container와 자식요소인 flex item으로 구성되어 있는데, 부모요소와 자식요소는 사용할 수 있는 프로퍼티가 다르다.  
 
>   flexbox를 사용하려면 정렬하고자 하는 요소의 부모요소인 flex container에 ```display: flex;```를 추가하면 된다.  

>   ```flexbox``` : 가로 혹은 세로로 정해둔 방향을 기준으로 프로퍼티를 정렬, 줄을 세운다는 것이 핵심이다.  

##### 1. flex container : 방향과 흐름  

* ```flex-direction``` : flex container 안에서 flex item이 배치될 기본 방향을 정할 수 있다. 이 프로퍼티를 따로 지정하지 않으면 ```row```라는 값으로 기본 설정되며 ```item```은 왼쪽에서 오른쪽으로 정렬한다.  
>   _row는 가로방향, column은 세로방향_  
```
.container {
	background-color: skyblue;
	padding: 16px;
	display: flex;
	flex-direction: column; /* column은 세로방향, row는 가로방향 */
}
```  

>   row, column 이외에 ```row-reverse```와 ```column-reverse```도 사용가능한데, 이는 각각 row와 column의 역순으로 item을 정렬한다.  

* ```flex-wrap``` : flex item이 여러 줄에 걸쳐지지 않고 한 줄에 들어가도록 정렬된다. 위의 예시에서 .container의 width를 줄이면, 기존에 .item에 정의되어 있던 width는 무시되고 부모 요소인 .container의 너비에 맞춰 줄어든다.  

>   flex item들을 여러 줄에 나열하고 싶다면 ```flex-wrap```프로퍼티를 사용하면 된다.  
  
* ```flex-flow``` : ```flex-direction```과 ```flex-wrap```을 한번에 지정할 수 있다. ```flex-flow```의 값으로 direction과 wrap을 순서대로 써주면 된다.  


##### 2. flex container : 정렬1  

```justify-content``` : flex-direction으로 정해진 방향에 flex item들을 어떻게 정렬할 것인지를 결정한다.  

```
flex-direction : row;

flex-direction : column;
```

* ```flex-start```, ```center```, ```flex-end```  
: flex-direction이 row일 때는 각각 왼쪽 끝, 가운데, 오른쪽 끝을 기준으로 정렬한다. column일 때는 각각 위 끝, 가운데, 아래 끝을 기준으로 정렬한다.  

* ```space-between``` : 시작과 끝을 기준으로 하여 item들을 동일한 간격으로 배치한다.  

* ```space-around``` : 시작과 끝에 item을 하나씩 두고 그 사이 남은 공간을 동일한 간격으로 나눠 나머지 item을 배치한다.  


##### 3. flex container : 정렬2  

```align-items```는 ```justify-content```와 달리 item을 ```flex-direction```에서 정해진 방향의 <br>수직방향<br>으로 정렬한다.  

* stretch : ```align-items```가 기본 값으로 가진다. 별다른 크기가 지정되지 않았을 때 flex 아이템을 늘려서 맞춰준다.  

>   _```align-itmes: flex-start```를 추가하면 높이가 콘텐츠의 크기만큼으로 바뀐다.  

* ```flex-start``` : 수직이 시작하는 부분부터 정렬한다.  

* ```center``` : 가운데 위치에 정렬한다.  

*  ```flex-end``` : 수직이 끝나는 부분부터 정렬한다.  

* ```baseline``` : ```justify-content```와 ```align-items``` 모두에서 사용할 수 있는 값이다. 글꼴의 기준선인 baseline을 기준으로 flex item들을 정렬한다. 만약 서로 다른 크기의 글자들에 적용해야 할 경우 baseline을 기준으로 맞춘다.  

##### 4. flex container : 정렬3  

```align-content```는 flex item들이 여러 줄일 경우 ```flex-direction```방향을 기준으로 수직 정렬 방법을 결정한다.  

* ```stretch``` : 기본값. 
* ```flex-start``` : 시작 부분에 맞춰서 정렬  
* ```center``` : 가운데 정렬  
* ```flex-end``` : 끝 부분에 맞춰서 정렬  
   
![b430a583955c4b129e3aa25285d27d37142eea704e89e36731096fb8cc1e2173](https://user-images.githubusercontent.com/58182440/79418789-6b761200-7ff0-11ea-9edc-2a87fab5b4d7.png)
 
![e4bdfb5b1350631110bdba4a5d78506602851382e7f4c96c92bf8a83902b369e](https://user-images.githubusercontent.com/58182440/79418885-9f513780-7ff0-11ea-917d-9f86999d5c2c.png)

>   코드에서 align-content를 쓰기 위해서는 ```flex-wrap:wrap```이 꼭 포함되어야 한다.  
>   >   ```align-content```는 여러 줄에 걸친 item들이 한 몸처럼 움직이고, ```align-items```는 각 줄이 따로 나누어져 정렬된다.  

* ```space-between``` : 수직 방향으로 끝과 끝에 하나씩 기준을 두고 그 사이에 배치한다.  

* ```space-around``` : 모든 간격을 동일하게 배치한다.  

##### 5. flex item  
  
flex item의 프로퍼티는 ```display:flex```가 적용된 부모 요소의 자식 요소에만 사용할 수 있다.  
  
* ```flex-grow``` : flex item의 확장과 관련된다.  단위 없는 숫자 값(비율)을 사용하며 기본값은 0이다.
>  값이 0일 경우에 flex container가 커져도 flex item의 크기는 커지지 않고 원래 크기를 유지한다.  
>  값이 1 이상일 경우에 flex item의 원래 크기와 상관 없이 flex container를 채우기 위해 flex item도 커지게 된다.  
  
![fe7de951af0f4094fbc3a427599222db7bee9924a9b7917044c53d131213a2f8](https://user-images.githubusercontent.com/58182440/79418971-cf98d600-7ff0-11ea-9e46-77ce6933a7f2.png)

_```flex-grow```크기는 비율이기 때문에 flex container의 크기가 커지거나 줄어들면 동일한 비율로 크기가 커지거나 줄어든다._  

* ```flex-shrink``` : flex item의 축소와 관련있다. 0과 정수(비율)를 사용하며 기본값은 1이다.  
>  속성값이 0일 경우 flex container 크기가 flex item의 크기보다 작아져도 flex item의 크기가 줄어들지 않고 원래 크기를 유지한다.  
>  속성값이 1 이상이면 flex container 크기가 작아질 때 flex item의 크기가 flex container 크기에 맞춰 줄어든다.  

![111add767aa3c6087f8d1eafafb79f4c272eb875fe68281df53e03f7c6560aa5](https://user-images.githubusercontent.com/58182440/79419180-446c1000-7ff1-11ea-97c8-880699eda255.png)


> ```flex-shrink:0```인 경우 flex item은 작아지지 않기 때문에 flex container를 벗어나게 된다.  

> ```flex-shrink:1```인 경우 flex item은 flex container에 맞춰 줄어든다.  

_```flex-shrink``` 값은 비율이기 때문에 flex container가 줄어들면 각 flex item에 적용한 값을 기준으로 비율에 맞춰 줄어든다._  

* ```flex-basis``` : flex item의 기본 크기를 결정하며, 기본값은 auto이다. 모든 크기 단위를 사용할 수 있다. 
>   ```flex-basis:auto``` : 각 flex item의 크기가 flex-basis로 할당된다. 그리고 남은 크기를 flex-grow에 따라 2:1의 비율로 나눠가진다. 

![0c0bcdffbc2bf986a20b56847cc3e9eaceafdb8b3feb047ab7b4e56b5b8cc83d](https://user-images.githubusercontent.com/58182440/79419726-57331480-7ff2-11ea-9499-62520846dd5e.png)


>   ```flex-basis:0``` : flex-grow에 따라 각 flex item의 크기가 2:1:1 비율로 나눠진다.  

![2558ad547848d2ee39bdd178916cb03304f328784828722a65141c07d0751dfa](https://user-images.githubusercontent.com/58182440/79419782-72058900-7ff2-11ea-9aaa-e5aa2165a889.png)


>   ```flex-basis:100px``` : 각 컨텐츠마다 100px을 제외, 즉 총 300px에 해당하는 값을 제외한 크기(테두리)를 2:1:1의 비율로 나눠가진다.  

![75fbdec7605a53b346cbb6cdf0c514230f786e08449c71e9de29cb58f34b5431](https://user-images.githubusercontent.com/58182440/79419863-9a8d8300-7ff2-11ea-9003-775014dfb08a.png)

* ```flex``` : ```flex-grow```,```flex-shrink```,```flex-basis```를 한 번에 설정할 수 있는 축약형.  
>   _순서 지키기_  


#### * 위치 정렬 - grid 1  

Grid : 격자 혹은 눈금을 말한다.  
_Flexbox가 줄에 대한 정렬이었다면 Grid는 격자, 행렬을 통해 좀 더 정교하고 복잡하게 정렬 및 배치할 수 있다._  

```
Lines, Track, Area, Gap이라는 영역으로 이루어져있다.
```  

##### 1. Grid 요소  
* Grid Lines : 격자를 이루는 선의 집합. Grid를 이루는 행과 열의 선들을 모두 일컫는다.  
>   행 : Grid column, 열 : Grid row  

* Grid Track : 평행한 Grid Line 두 줄 사이의 공간을 말한다.  

* Grid Area : Grid Line 네 줄로 둘러싸인 공간을 말한다. 

* Grid Gap : Grid Lines의 두께를 말한다. 

##### 2. Grid 구성  
Grid Container와 Grid items로 구성되어 있다.  
_Grid item ⊂ Grid Container_  

##### 3. grid container:template  

* ```display:grid/inline-grid``` : Grid Container를 사용하고 싶다면 display를 통해 선언해야 한다. 값으로는 grid 또는 inline-grid를 설정할 수 있다.  
>   grid : display:block의 특성을 갖는 Grid Container를 정의  
>   inline-grid : display:inline의 특성을 갖는 Grid Container를 정의  

* ```grid-template-rows/columns``` : Grid Track의 크기를 정의한다.
>   grid-template-rows : 행에 해당하는 grid track의 크기  
>   grid-template-columns : 열에 해당하는 grid track의 크기  

![b9b5000232373b85106a8b399030f0bf995e4eccfe2658b143cd5cc5a7c0b665](https://user-images.githubusercontent.com/58182440/79421021-f78a3880-7ff4-11ea-9bfd-1c3d721001a5.png)

_```gird-template-rows: 40px 40px 40px```와 같이 반복되는 값을 쉽게 할당하려면 ```repeat()```함수를 사용하면 된다._  
```
grid-template-rows: repeat(10, 40px);
```
>   repeat함수는 grid-template-rows와 grid-template-columns에서만 사용할 수 있다.  

```
.main {
	display: grid;
	grid-template-rows: 128px auto 240px;
	grid-template-columns: 1fr 3fr 1fr;
}
``` 
![178e4b7d723b8703624a05e1832cb1e7796a58d307fc580019b7ed812d48e043](https://user-images.githubusercontent.com/58182440/79421285-72ebea00-7ff5-11ea-8936-6de91a7b0d22.png)

>   fr : fraction의 약자로 파편, 분수를 뜻한다. Grid Container에 남은 공간의 비율을 나타내는 유연한 단위다. _fr은 비율이기 때문에 Grid Container의 너비가 변하더라도 해당 비율을 유지한다_  

* ```grid-template-areas``` : Grid Area의 이름을 할당한다.  
>   같은 이름을 가진 Grid Area끼리 셀병합된다.  

![d9ee2df8f031d3c14cd783756a1d43200c16b7c60dfda127f72d56483cfca4c4](https://user-images.githubusercontent.com/58182440/79421618-294fcf00-7ff6-11ea-949e-f660d98761ea.png)

> gird-template-areas의 값은 ""로 한 행을 표현하며, 여러 행을 띄어쓰기로 구분한다.  

```
grid-template-areas: /* ㄴ 모양 ❌ */
		"hd hd hd"
		"nav content ad"
		"nav nav ft";

grid-template-areas: /* ㅗ 모양 ❌ */
		"hd hd hd"
		"nav ft ad"
		"ft ft ft";
``` 

_직사각형 모양이 되어야 레이아웃이 무너지지 않는다._  

> 공간을 비우고 싶다면 . 또는 none을 입력한다.  
```
grid-template-areas: 
		"hd hd hd"
		"nav content ad"
		". ft none";
```
![b952702ed010fcfc47dfdde8ceba7df773c67c006f4bd6b9490b5063ecc87717](https://user-images.githubusercontent.com/58182440/79421829-9cf1dc00-7ff6-11ea-829b-e1cb4a709561.png)

_grid-template-areas의 값은 전체 grid area 수와 동일해야 한다._  

* ```grid-template``` : grid-template-xxx에 해당하는 모든 프로퍼티의 단축 프로퍼티다.  

```.main {
	display: grid;
	grid-template-rows: 128px auto 240px;
	grid-template-columns: 1fr 3fr 1fr;
	grid-template-areas: 
		"hd hd hd"
		"nav content ad"
		"ft ft ft";
}
```
는 아래와 같다.  
```
.main {
	display: grid;
	grid-template: 
		"hd hd hd" 128px
		"nav content ad" auto
		"ft ft ft" 240px
		/ 1fr 3fr 1fr;
}
```  

##### 4. gird container:gap  

* ```grid-row/column-gap``` : 각 행과 열 사이의 간격을 지정할 수 있다.  

![2b1738a258d59a79b7c09525afe37be4c50ac78c89a29f82cca0fbe9c97120ff](https://user-images.githubusercontent.com/58182440/79422150-49cc5900-7ff7-11ea-988d-e0d2b41fc74d.png)

↓ Grid Gap이 0일 경우  

![ba827c2640834e7a855d9e2285235f7f1c55a091795ea36d2c91f6b5c158a768](https://user-images.githubusercontent.com/58182440/79422193-649ecd80-7ff7-11ea-86cb-07b6957b98a4.png)

* ```grid-gap``` : 단축 프로퍼티. row, column 순서로 입력한다. 값을 하나만 작성하면 동일한 값으로 지정된다.  

```
grid-row-gap: 16px;
grid-column-gap: 16px;
/* 위와 아래의 코드는 동일합니다. */
grid-gap: 16px 16px;
/* 모두 동일한 코드입니다. */
grid-gap: 16px;
```

##### 5. grid container:auto  

* ```grid-auto-rows/columns``` : 크기가 지정되지 않은 Grid Track의 크기를 지정할 수 있는 프로퍼티다.  

>   각 행의 높이를 200px로 설정하고 싶다면,  
```
.photos {
	display: grid;
	grid-gap: 8px;
	grid-template-columns: repeat(3, 1fr);
	grid-template-rows: repeat(3, 200px);
}
```
이렇게 설정하면 된다.  
내용이 칸 밖으로 빠져나갈 경우  ```minmax()```라는 grid함수를 이용하면 된다.  

>   ```minmax(최솟값, 최댓값)``` : 첫 번째 매개변수로 최솟값을, 두 번째 매개변수로 최댓값을 받는다.  

```
.photos {
	display: grid;
	grid-gap: 8px;
	grid-template-columns: repeat(3, 1fr);
	grid-template-rows: repeat(3, minmax(200px, auto));
}
```  
이와 같이 설정하면 <b>내용에 따라 자동으로 크기가 늘어나는 카드</b>가 완성된다.  

>   추가 카드가 계속 들어오게 되면, 3번째 카드까지만 크기를 설정했기 때문에, 4번째 줄부터는 크기가 지정되지 않은 상태로 바뀐다. 이 때 ```grid-auto```를 쓴다.  
```
.photos {
	display: grid;
	grid-gap: 8px;
	grid-template-columns: repeat(3, 1fr);
	grid-auto-rows: minmax(200px, auto);
}
```  
-> 행의 갯수에 상관없이 크기를 지정할 수 있다.  

* ```grid-auto-flow``` : Grid가 자동으로 배치되는 방향을 결정한다.  
>   ```row```, ```column```, ```row dense```, ```column dense```를 값으로 가질 수 있다.  
>   >   dense : 밀집된 형태로 정렬한다.  

-grid-auto-flow:row일 때  

![5df170cb4f63ba5d3d8ed5019bd546bb44803f4645de2bd56fb7887437a24bc0](https://user-images.githubusercontent.com/58182440/79423970-75047780-7ffa-11ea-837b-a810a62bcb47.png)

-gird auto-flow:row dense일 때

![ece19fece107410b3bc7ae657e55f4f03b5916f8cec027be3050a750ae28ebc4](https://user-images.githubusercontent.com/58182440/79424097-92d1dc80-7ffa-11ea-8134-1b5cf4d9482c.png)


##### 6. grid container:grid  

grid는 grid-template와 grid-auto의 단축형 프로퍼티다.  
  
* ```grid-template``` : grid, grid-template-rows, grid-template-columns 값을 한 번에 적용할 수 있다.  
  
```
.main {
	display: grid;
	grid-template: 128px auto 240px / 1fr 3fr 1fr;
	grid-template-areas: 
		"hd hd hd"
		"nav content ad"
		"ft ft ft";
}
```  

* ```auto-flow <grid-auto-rows>/<grid-template-columns>``` : ```grid```로 ```grid-template-rows```와 ```grid-auto```를 동시에 적용할 수 있다.  

```
.photos {
	display: grid;
	grid-gap: 8px;
	grid-template-columns: repeat(2, 100px);
	grid-auto-rows: 100px;
	grid-auto-flow: row;
}
```  
```
.photos {
	display: grid;
	grid-gap: 8px;
	grid: auto-flow 100px / repeat(2, 100px);
}
```
>   grid의 ```auto-flow```는 ```gird-auto-flow:row```와 동일하다.  
>   auto-flow의 위치에 의해 결정되는데, / 앞에 있는 경우 row를, / 뒤에 있는 경우는 column을 적용한다.  
>   ```auto-flow```키워드가 있어야만 ```grid-auto-flow```가 적용된다. _```auto-flow```가 없다면 ```grid-template```의 형식으로 인식된다._  

> dense도 비슷하게 사용한다.  
```
.photos {
	display: grid;
	grid-gap: 8px;
	grid: auto-flow dense 100px / repeat(2, 100px);
}
```  
```
.photos {
	display: grid;
	grid-gap: 8px;
	grid-template-columns: repeat(2, 100px);
	grid-auto-rows: 100px;
	grid-auto-flow: row dense;
}
```  
* ```grid-template-rows>/auto-flow<grid-auto-columns>```  
: ```auto-flow```를 /뒤에 사용하기 때문에 ```grid-auto-flow:column```의 값을 가진다.  
```
.photos {
	display: grid;
	grid-gap: 8px;
	grid: repeat(2, 100px) / auto-flow 100px;
/* 	grid: repeat(2,100px)  / auto-flow dense; */
}
```  
```
.photos {
	display: grid;
	grid-gap: 8px;
	grid-template-rows: repeat(2, 100px);
	grid-auto-columns: 100px;
	grid-auto-flow: column;
	/* grid-auto-flow: column dense; */
}
``` 
>   grid에는 값을 주는 순서와 ```auto-flow```키워드의 유무에 따라 값이 적용되는 방식이 다르므로 프로퍼티를 사용할 때 신경써야한다.  

##### 7. gird container:align&justify  

* ```align``` : 수직 방향 정렬  
* ```justify``` : 수평 방향 정렬  
* ```place``` : align과 justify의 축약형  
</br>

* ```content``` : Grid Container를 기준으로 Grid Cell을 정렬한다.  
* ```items``` : Grid Cell 혹은 Grid Area를 기준으로 Grid Item을 정렬한다.  
</br>

* 프로퍼티의 값 : 앞부분인 ```align```와 ```justify```에 영향을 받지 않고, 오로지 ```content```와 ```items```에만 영향을 받는 값이 있다.  

|```content```와 ```items```에서 모두 가능한 값 | ```content```에서만 가능한 값 |  
|:---:|:---:|:---:|
start | sapce-around |  
center | space-between |  
end | space-evenly |  
stretch | |
    

  




