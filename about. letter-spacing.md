# letter-spacing

letter-spacing 속성은 글자 사이의 간격을 조절한다.

```
/* 키워드 값 */
letter-spacing: normal;

/* <length> 값 */
letter-spacing: 0.3em;
letter-spacing: 3px;
letter-spacing: .3px;

/* 전역 값 */
letter-spacing: inherit;
letter-spacing: initial;
letter-spacing: unset;
```  
(normal)<br>
현재 글꼴의 기본 간격. 0과 달리, auto는 사용자 에이전트가 양쪽 정렬을 위해 간격을 임의로 조절할 수 있다.
<br>(length)<br>
기본 간격에 추가할 글자간 간격. 음수 값을 지정할 수 있지만 구현에 따라 한계가 있을 수 있다.
<br><br>
(고려사항)<br>
letter-spacing 값의 절댓값이 너무 크면 스타일을 적용한 글을 읽기 힘들다. 반대로 지나친 음숫값은 글자가 서로 겹쳐 알아볼 수 없게된다.
