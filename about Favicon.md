# Favicon
파비콘(영어: favicon, 'favorites + icon') 또는 패비콘이란 인터넷 웹 브라우저의 주소창에 표시되는 웹사이트나 웹페이지를 대표하는 아이콘이다.<br>
아이콘 크기는 16x16, 32x32, 48x48, 64x64픽셀이 될 수 있고, 8비트, 24비트, 32비트 색상이 가능하다.<br>
다음 포맷은 브라우저에 상관없이 호환되며 인터넷 익스플로러, 파이어폭스, 크롬, 오페라에서 모두 지원한다.

----------------------------------
### favicon 만들기
1.먼저, Favicon & App icon Generator 사이트에 접속한다.<br>
https://www.favicon-generator.org/<br>
2. 정사각형 로고 이미지를 미리 준비한 후 사이트의"찾아보기"를 클릭한다.<br>
3. 이미지를 불러왔다면 "Create Favicon"버튼을 클릭해준다.<br>
4. 생성된 파비콘을 "Download the genetated favicon" 을 클릭합니다.<br>
5. 내 컴퓨터에 저장한다.<br>
6. 다운받은 알축파일을 풀면..<br>
7. 아래와 같이 파비콘과 app 아이콘들이 크기별로 생성된다.<br>
이중에서 (favicon.ico) 파일이 바로 파비콘으로 만들어진 파일이다.

----------------------------------------
### html 적용하기
    ```
    <link rel="apple-touch-icon" sizes="57x57" href="/apple-icon-57x57.png">
    <link rel="apple-touch-icon" sizes="60x60" href="/apple-icon-60x60.png">
    <link rel="apple-touch-icon" sizes="72x72" href="/apple-icon-72x72.png">
    <link rel="apple-touch-icon" sizes="76x76" href="/apple-icon-76x76.png">
    <link rel="apple-touch-icon" sizes="114x114" href="/apple-icon-114x114.png">
    <link rel="apple-touch-icon" sizes="120x120" href="/apple-icon-120x120.png">
    <link rel="apple-touch-icon" sizes="144x144" href="/apple-icon-144x144.png">
    <link rel="apple-touch-icon" sizes="152x152" href="/apple-icon-152x152.png">
    <link rel="apple-touch-icon" sizes="180x180" href="/apple-icon-180x180.png">
    <link rel="icon" type="image/png" sizes="192x192"  href="/android-icon-192x192.png">
    <link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
    <link rel="icon" type="image/png" sizes="96x96" href="img/82a8b214cf2963d88e2ea8c3054b132f.ico/favicon-16x16.png">
    <link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
    <link rel="manifest" href="/manifest.json">
    <meta name="msapplication-TileColor" content="#ffffff">
    <meta name="msapplication-TileImage" content="/ms-icon-144x144.png">
    <meta name="theme-color" content="#ffffff">
    ```
    이처럼 다양한 버전의 파비콘 설정 링크가 주어진다. 원하는 링크를 골라 이미지를 추가하면 쉽게 설정이 가능하다.
