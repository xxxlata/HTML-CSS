# 기본 선택자
### 전체 선택자(Universal selector)
asterisk ``` * ``` 모든 요소를 선택한다. <br>

구문: ``` * ```<br>
예제: ``` *{color:tomato;}```<br>
예제링크:
https://codesandbox.io/s/serverless-morning-unjoz?file=/style.css

### 유형 선택자(type selector)
노드이름을 사용해 요소를 선택한다. 즉 문서 내에서 주어진 유형의 모든 요소를 선택한다.<br>

구문: ```element {style properties}```<br>
예제:``` span {font-size: 10px;}```<br>
예제링크:
https://codesandbox.io/s/gallant-mirzakhani-vxr8n?file=/index.html

### 클래스 선택자(class selector)
css 클래스 선택자는 요소의 class 특성에 기반해 요소를 선택한다.<br>

구문: ``` .class_name{style properties}```<br>
예제: ``` .class_selector{margin:10px;}```<br>
예제링크:
https://codesandbox.io/s/mystifying-paper-z7l7o?file=/style.css

### ID 선택자(id selector)
CSS ID 선택자는 요소의 id 특성 값을 비교하여, 완전히 동일한 id를 가진 요소를 선택한다.<br>

구문:```#id_name{style properties}```<br>
예제:```#id_selector{margin:10px;}```<br>
예제링크:
https://codesandbox.io/s/laughing-swanson-ckces?file=/style.css

### 특성 선택자(Attribute Selector)
CSS 특성 선택자는 주어진 특성의 존재 여부나 그 값에 따라 요소를 선택한다.<br>

구문:```[attr^=value]```접두사로 특성값을 가지는 모든 요소를 선택한다.<br>
예제:```.toy[category^="Swim"]``` toy 클래스 요소 중에서 카테고리가 "Swimwear" 이거나 "Swimming"인 장난감을 선택할 수 있다.<br>

구문:```[attr$=value]```접미사로 특성값을 가지는 모든 요소를 선택한다.<br>
예제:```img[src$=".jpg"]``` .jpg 형식의 모든 이미지를 선택한다.<br>

구문:```[attr*=value]```특성값을 가지는 모든 요소를 선택한다.<br>
예제:```img[src*="/thumbnails/"]``` thumbnails 폴더에 있는 모든 이미지 요소를 선택한다.<br>

