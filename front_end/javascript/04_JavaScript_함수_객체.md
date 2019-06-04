## JavaScript - 함수/객체



2019-06-04

------

< 생활코딩 Web2 - Javascript >



* #### 함수 

  * 유지보수가 편해짐
  * 웹페이지의 크기가 확 줄어짐
  * 똑같은 로직을 가질 때 사용
  * 함수 이름을 붙일 수 있기 때문에 사용처나 기능을 분명히 알 수 있게 됨



* #### 실습 - day_and_night.html 에서 함수만들기

```html
<head>
  <title>WEB1 - JavaScript</title>
  <meta charset="utf-8">
  <script>
    // 함수 생성
    function nightDayHandler(self){
    var target = document.querySelector('body');
        if(self.value === 'night'){
            target.style.backgroundColor = 'black';
            target.style.color = 'white';
            self.value ='day';
 
            var alist = document.querySelectorAll('a');
            var i = 0;
            while(i < alist.length){
                alist[i].style.color = 'powderblue';
                i = i + 1;
            }

        } else {
            target.style.backgroundColor = 'white';
            target.style.color = 'black';
            self.value ='night';

            var alist = document.querySelectorAll('a');
            var i = 0;
            while(i < alist.length){
                alist[i].style.color = 'blue';
                i = i + 1;
            }
        }
    } 
  </script>
</head>
<body>
    <h1><a href="ex3.web_day_and_night4.html">WEB</a></h1>
    <input this type="button" value="night" onclick="
        nightDayHandler(this);
    ">
    <input this type="button" value="night" onclick="
        nightDayHandler(this);
    ">
</body>
```

