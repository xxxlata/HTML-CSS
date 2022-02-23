## backgroound-clip 이용하여 글씨에 그라데이션 입히기
index.html
```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="./sample.css">
    <title>Document</title>
</head>

<body>
    <h1>HELLO, WORLD!</h1>
    <div class="gradcircle"></div>
</body>

</html>
```
sample.css
```
body {
    display: flex;
    height: 100vh;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}

h1 {
    font-size: 60px;
}

.gradcircle {
    width: 100px;
    height: 100px;
    border-radius: 5rem;
    background: linear-gradient(to right top, #861657, #ffa69e);
}
```
1. gradcircle에 적용된 색을 h1에도 background로 넣어준다.
```
h1 {
    font-size: 60px;
    background: linear-gradient(to right top, #861657, #ffa69e);
}
```
*그라디언트 내 to right top은 색상을 오른쪽 위를 향해 퍼지도록 한다.<br>

2. 아래 코드를 넣어준다.

h1 {
    font-size: 60px;
    background: linear-gradient(to right top, #861657, #ffa69e);
    color: transparent;
    -webkit-background-clip: text;
}
 

background-clip은 background 를 어디까지 적용시키는지에 대한 것이다.<br>

텍스트에 배경색을 채워야 하므로, text를 적어주자.<br>

background-clip만 적으면 텍스트 원래 색인 검은색 배경에 그라디언트가 적용 된다.<br>

이를 보여주게 하려면 텍스트 원래의 색을 투명하게 만들어야 하기 때문에

color: transparent를 적용시킨다. <br>

*지원의 한계로, 크롬을 위해 앞에 -webkit-을 붙여주었다.

