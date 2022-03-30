# SVG

### 설명
SVG는 좌표를 그리는 시스템을 사용하여 점을 그려서 선, 도형 또는 경로를 그리는 데 연결한다.<br>
벡터 그래픽은 수학을 사용하여 그려져있어 선명하며 다른 이미지 형식처럼 픽셀 화되지 않아 로고, 아이콘 및 일러스트레이션에 적합하다. 
<br>브라우저 내부의 SVG에는 고유 한 DOM이 있다. <br> 
SVG는 브라우저에 의해 별도의 문서로 취급 된 다음 페이지의 일반 DOM 내부에 배치된다.<br>
SVG 내부의 속성을 업데이트하지 않고도 모든 크기의 캔버스에 이미지를 그려 넣을 수 있지만 다른 곳에서는 이미지를 브라우저에 표시 할 수 있으므로이 속성은 'viewBox'속성이 중요하다.<br>
이 별도의 탐색 가능한 DOM은 CSS와 Javascript를 사용하여 SVG 내부 요소와 상호 작용하는 방법이기도하다.<br>
SVG의 벡터 특성으로 인해 이미지는 해상도에 독립적이다. 모든 디스플레이에서 이미지가 선명하게 보인다.
<br>
애니메이션을 만들 수 있다.
<br>
모든 부분은 path로 이루어져있기 때문에 시간차를 두고 path를 바꿔 선을 이동시키는 원리이다.  
<br><br>
[https://app.svgator.com](https://app.svgator.com/) 
<br>
초보자도 손쉽게 움직이는 SVG를 만들 수 있는 사이트이다.

-------------------------------------------------------------------
### 사용방법
SVG 코드는 다음의 HTML 요소를 사용해 문서에서 활용할 수 있다.
```
<img>
<embed>
<object>
<iframe>
<svg>
```
1.이미지 태그
<br><br>
HTML 이미지 태그를 사용하여 다른 이미지를 만드는 것과 같은 방법으로 SVG 이미지를 페이지에 포함 할 수 있다.<br>
alt속성으로 이미지의 의미를 포함한 경우 적절한 대체 텍스트를 제공한다.

```
<img src="myAwesomeSVG.svg" alt="My Awesome SVG">
```
이 방법으로 이미지를 페이지에 삽입하면 HTML 또는 CSS를 통해 width 및 height 속성을 지정하지 않으면 원본 SVG 파일의 크기가된다. 
<br>
이미지 태그를 사용하면 화면 판독기에서 alt 속성에 액세스해야하는 경우 로고 및 기타 내용에 유용하다.
<br>
 Modernizr을 사용하여 SVG가 지원되지 않는 경우 PNG로 교체 할 수있는 대체 기능을 제공 할 수 있다.
<br><br>

2.CSS 배경 이미지
<br>
다른 종류의 이미지를 요소에 부착하는 것과 같은 방법을 사용하여 CSS의 페이지에 SVG 이미지를 포함시킬 수도 있다.

```
.hero {
background-image: url('myAwesomeSVG.svg');
}
```
이런 식으로 SVG를 사용하면 다른 CSS 배경 속성을 활용하여 이미지를 요소 배경으로 크기 조정, 위치 지정 및 반복 할 수 있다.

```
background-repeat:no-repeat;
background-position:centercenter;
background-size:contain;
```
지원을 제공하기 위해 브라우저에서 CSS를 구문 분석하고 SVG를 포함하기 전에 폴백 PNG를 제공하는 방식에 트릭을 사용할 수 있다.

```
.hero {
background-image: url('myAwesomeSVGfallback.png');
background-image: url('myAwesomeSVG.svg');
}
```
3.임베드(embed)<br>
임베드 요소를 사용해 SVG 요소를 HTML 문서에 포함하는 방법은 <embed> 요소의 src 속성에 파일의 경로를 설정하는 것이다.<br>
이미지를 설명해야 할 필요가 있다면 적절한 대체 텍스트를 aria-label 속성을 통해 제공한다.
```
<embed src="king.svg" type="image/svg+xml" aria-label="킹 (체스 말)">
```
4.오브젝트(object)
<br>
오브젝트 요소를 사용해 SVG 요소를 HTML 문서에 포함하는 방법은 <object> 요소의 data 속성에 파일의 경로를 설정하는 것이다.<br>
이미지를 설명해야 할 필요가 있다면 적절한 대체 텍스트를 aria-label 속성을 통해 제공한다.
```
<object data="king.svg" type="image/svg+xml" aria-label="킹 (체스 말)"></object>
```
5.아이프레임(iframe)
<br>
아이프레임 요소를 사용해 SVG 요소를 HTML 문서에 포함하는 방법은 <iframe> 요소의 src 속성에 파일의 경로를 설정하는 것이다.<br>
이미지를 설명해야 할 필요가 있다면 적절한 대체 텍스트를 aria-label 속성을 통해 제공한다.
```
<iframe src="king.svg" aria-label="킹 (체스 말)"></iframe>
```
6.인라인 SVG
<br>
<br>
SVG는 SVG 태그를 사용하여 문서에 곧바로 작성할 수 있다.
```
<svg width="100px" height="100px"viewBox="0 0 100 100" version="1.1"xmlns="..."><title>My Awesome SVG</title<circle class="circle"cx="50" cy="50" r="50"fill="#FFFF00"></circle></svg>
```
SVG가 확장 가능하기 때문에 폭과 높이 속성없이 태그를 제공하면 SVG는 컨테이너의 크기로 커진다.
<br>
페이지에 SVG를 작성하여 인라인 SVG에서 채우기를 제거하고 CSS에서 스타일을 지정할 수 있다.

```
.circle {
fill: #FFFF00;
}
```
이 방법을 다시 사용하는 데있어 폴백은 PNG 폴백을 제공하고 Modernizr을 사용하여 지원을 검색하는 데 의존한다. 
<br>유일한 다른 단점은 브라우저에서 인라인 SVG - 마크 업이 아닌 - 캐싱되지 않는다는 것이다.

--------------------------------------------------------------------------------------------------
더 자세한 SVG 설명 사이트:

[https://ldrerin.tistory.com/398?category=772248](https://ldrerin.tistory.com/398?category=772248)<br>
https://a11y.gitbook.io/graphics-aria/svg-graphics/html+svg
