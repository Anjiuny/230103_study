# Switch 문
switch문은 if문과 같은 류의 조건문인데 변수 값이나 표현식에 따라   
수행해야할 코드를 달리할 때 사용한다.   

    switch (변수){
        case 값1 :
            문장 1;
            문장 2;
            break;
        case 값2 :
            문장 |;
            문장 ||;
            break;
        default 값3 :
            문장 A;
            문장 B;
        ...
    }

위에서 switch 변수 값이 값1 이면 문장1,2를 수행하고 break에 의해   
switch문을 빠져나온다. 만약 변수의 값이 값2 이면 문장|,||를 수행하게 된다.   
그 외 나머지 모든 경우에는 default에 있는 문장 A,B를 수행한다.

<br>

[ switch문으로 x가 1인지 2인지 판별하기 ]
```html
<script>
    var x = 2;      //x에 2를 저장

    switch (x) {
        case 1:
            document.write("x의 값은 1입니다.");
            break;
        case 2:
            document.write("x의 값은 2입니다.");
            break;
        default:
            document.write("x의 값은 1 또는 2가 아닙니다.");
    }      
     //x=2 이므로 두번째 문장을 수행하고 switch문을 빠져나감
</script>
```

<br>

[ 숫자에 대응되는 요일 표시하기 ]
```html
<script>
    var day = 2;
    var day_name;
    switch (day) {
        case 1:
            day_name = "일요일";
            break;
        case 2:
            day_name = "월요일";
            break;
        case 3:
            day_name = "화요일";
            break;
        case 4:
            day_name = "수요일";
            break;
        case 5:
            day_name = "목요일";
            break;
        case 6:
            day_name = "금요일";
            break;
        case 7:
            day_name = "토요일";
            break;
        default:
            day_name = "입력 오류";
    }
    document.write(day_name + "입니다.");
</script>
```
- day의 값에 따라 해당 요일을 day_name에 저장한다.   
- day의 값이 1~7이 아닌 경우에는 입력 오류가 day_name에 저장된다.
