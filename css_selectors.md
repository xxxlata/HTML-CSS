# 기본 선택자
### 전체 선택자(Universal selector)
asterisk ``` * ``` 모든 요소를 선택합니다. <br>

구문: ``` * ```<br>
예제: ``` *{color:tomato;}```<br>
예제링크:
https://codesandbox.io/s/serverless-morning-unjoz?file=/style.css

### 유형 선택자(type selector)
노드이름을 사용해 요소를 선택합니다. 즉 문서 내에서 주어진 유형의 모든 요소를 선택합니다.<br>

구문: ```element {style properties}```<br>
예제:``` span {font-size: 10px;}```<br>
예제링크:
https://codesandbox.io/s/gallant-mirzakhani-vxr8n?file=/index.html

### 클래스 선택자(class selector)
css 클래스 선택자는 요소의 class 특성에 기반해 요소를 선택합니다.<br>

구문: ``` .class_name{style properties}```<br>
예제: ``` .class_selector{margin:10px;}```<br>
예제링크:
https://codesandbox.io/s/mystifying-paper-z7l7o?file=/style.css

### ID 선택자(id selector)
CSS ID 선택자는 요소의 id 특성 값을 비교하여, 완전히 동일한 id를 가진 요소를 선택합니다.<br>

구문:```#id_name{style properties}```<br>
예제:```#id_selector{margin:10px;}```<br>
예제링크:
https://codesandbox.io/s/laughing-swanson-ckces?file=/style.css

### 특성 선택자(Attribute selector)
CSS 특성 선택자는 주어진 특성의 존재 여부나 그 값에 따라 요소를 선택합니다.<br>

구문:```[attr]```attr이라는 이름의 특성을 가진 요소를 선택합니다.<br>
예제:```/* < a>가 title이라는 속성을 가지고 있을 때 */``` ```a[title]{color: purple;}```.<br>

구문:```[attr=value]```attr이라는 이름의 특성값이 "정확히" value인 요소를 선택합니다.<br>
예제:```/*< a> 에서 href가 "https://example.org" 를 가지고 있을때 */``` ```a[href="https://example.org"] {color:green;}```<br>

구문:```[attr~=value]``` attr이라는 이름의 특성값이 value를 포함하는 요소를 선택합니다. attr 특성은 공백으로 구분한 여러 개의 값을 가지고 있을 수 있습니다.<br>
예제:```/*< a> 에서 class가 "logo" 라는 단어를 포함하고 있을때 */``` ```a[class~="logo"]{padding:20px;}```.

구문:```[attr$=value]```접미사로 특성값을 가지는 모든 요소를 선택합니다.<br>
예제:```/*< a> 에서 href가 ".org" 라는 단어로 끝날때 */``` ```a[href$=".org"]{font-style: italic;}```.<br>

구문:```[attr*=value]```특성값을 가지는 모든 요소를 선택합니다.<br>
예제:```/*< a> 에서 href가 "example" 이라는 단어를 포함하고 있을때 */``` ```a[href*="example"]{font-size:2em;}```.<br>

구문:```[attr^=value]```attr이라는 특성값을 가지고 있으며, 접두사로 value가 값에 포함되어 있으면 이 요소를 선택합니다.
예제:```/*<a> 에서 href가 #으로 시작될 때``` ```*/a[href^="#"] {background-color: gold;}```.

도합 예제링크:https://codesandbox.io/s/brave-ride-g9bhc?file=/style.css

# 그룹 선택자
### 선택자 목록(,)
CSS 선택자 목록(,)은 일치하는 모든 요소를 선택합니다.

구문:```element, element, element { style properties }```<br>
예제:```h1,h2,h3 {color:tomato;}```<br>
예제링크:https://codesandbox.io/s/loving-lumiere-dh6qf?file=/style.css

# 결합자
### 자손 결합자(Descendant selector)
결합자는 첫 번째 요소의 자손인 노드를 선택합니다.

구문: ```A B```<br>
예제: ```div span{color:black;}```은 ```<div>``` 요소 안에 위치하는 모든 ```<span>``` 요소의 글자색을 검은색으로 바꿉니다.<br>

### 자식 결합자(Child selector)
```>``` 결합자는 첫 번째 요소의 바로 아래 자식인 노드를 선택합니다.<br>
자손결합자와 다른점은 자손결합자(공백)는 손자,증손자,자식 가림없이 모든 노드를 선택하고, 자식 결합자(>)는 순수하게 자식노드만 선택합니다.<br> 

구문: ```A > B```<br>
예제: ```ul > li```는 ```<ul>``` 요소 바로 아래에 위치하는 모든 ```<li>``` 요소와 일치합니다.

### 일반 형제 결합자(General sibling selector)
```~``` 결합자는 형제들 중 매칭되는 모든 형제들을 선택합니다.

구문: ```A ~ B```<br>
예제: ```p ~ span```은 ```<p>``` 요소를 뒤따르는 모든 ```<span>``` 요소와 일치합니다.<br>

### 인접 형제 결합자(Adjacent sibling selector)
```+``` 결합자는 동등한 위치에 있는 태그(형제) 중 매칭되는 아래로 첫번째 형제 하나만 선택합니다.

구문: ```A + B```<br>
예제: ```h2 + p```는 ```<h2>``` 바로 뒤에 위치하는 ```<p>``` 요소와 일치합니다.<br>

도합 예제링크:https://codesandbox.io/s/brave-yonath-y4kt3?file=/style.css

# 의사 클래스(Pseudo-class)
CSS 의사 클래스(가상 클래스)는 선택자에 추가하는 키워드로, 선택한 요소가 특별한 상태여야 만족할 수 있습니다. <br>예를 들어 포인터를 올렸을 때에만 글씨 색을 바꾸고 싶을 때 :hover을 사용할 수 있습니다.<br>
의사 클래스를 사용하면 문서 트리 콘텐츠와 관련된 경우 뿐만 아니라 탐색기 히스토리(:visited 등),<br> 콘텐츠의 상태(특정 폼 요소에 적용한 :checked 등), 마우스의 위치(커서가 마우스 위인지 아닌지 알 수 있는 :hover 등)처럼 외부 인자와 관련된 경우에도 스타일을 적용할 수 있습니다.

도합 사용 예제링크:https://codesandbox.io/s/strange-rgb-icleq?file=/style.css
