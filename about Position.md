# position

relative 부모의 자식이 absolute가 되어야한다.<br>

+absolute는 가장 가까이 있는 부모relative를 따른다.  
```
<style>
    .relative{
        position: relative;
    }
    .absolute{
        position: absolute;
    }
</style>
<body>
    <div class="relative">
    부모
    </div>
    <div class="absolute">
    자식
    </div>
    <script src="app.js"></script>
</body>
```
