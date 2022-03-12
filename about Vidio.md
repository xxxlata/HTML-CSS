# HTML5
```<vidio>``` 의 autoplay 속성
<br>
정의 및 특징<br>
```<video>``` 태그의 autoplay 속성은 비디오가 실행될 준비가 끝나는 대로 자동으로 실행됨을 명시한다.
<br>
<br>
autoplay 속성은 불리언(boolean) 속성이다.<br>
불리언 속성은 해당 속성을 명시하지 않으면 속성값이 자동으로 false 값을 가지게 되며, 명시하면 자동으로 true 값을 가지게 된다.

#### 문법
```<video autoplay>```
 
```  
<video height="180" width="288" controls autoplay>
    <source src="/examples/media/sample_video_ogg.ogg" type="video/ogg">
    <source src="/examples/media/sample_video_mp4.mp4" type="video/mp4">
    //이 문장은 브라우저가 video 태그를 지원하지 않을 때 화면에 표시된다.
</video>
```
----------------------------------------  
HTML과 XHTML에서의 차이점<br>
XHTML에서는 속성값을 생략할 수 없으므로, 다음과 같이 속성명과 속성값을 모두 명시해야만 합니다.

```<video autoplay="autoplay">```
