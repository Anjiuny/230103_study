# Chapter 03 총정리 문제풀이

1. 😐(50%) 물건 구매가를 입력받아 할인율에 따라 지불 금액을 계산하는   
프로그램을 작성하시오.
```html
<script>
        var price;
        var dis;     //할인율
        var disp;   //할인 금액
        var pay;    //지불 금액

        var price = Number(prompt("구매 금액을 입력해 주세요."));
        if(price >= 10000 && price < 50000){
            dis = 5;
        }
        else if(price >= 50000 && price < 300000){
            dis = 7.5;
        }
        else if(price >= 300000){
            dis = 10;
        }
        else {
            dis = 0;
        }
        disp = price * (dis / 100);
        pay = price - disp;

        document.write("- 구매 금액 : " + price + "원<br>");
        document.write("- 할인율 : "+ dis + "% <br>");
        document.write("- 할인 금액 : " + disp + "원<br>");
        document.write("지불 금액은 : " + pay + "원입니다.")
    </script>
```

<br>

2. ❌❌❌ 물의 온도를 나타내는 단위(섭씨 또는 화씨)와 온도를 입력받아    
섭씨 온도에 따라 물 상태를 판별하는 프로그램을 작성하시오.

    ※ 화씨/섭씨 온도 환산식 : 섭씨 = (화씨 -32) * 5 / 9   
    ※ 물의상태   
        - 섭씨 온도 100도 이상 : 기체   
        - 섭씨 온도 0도 초과 ~ 100도 미만 : 액체   
        - 섭씨 온도 0도 이하 : 고체   

<br>


_여긴 정답.._
```html
<script>    
    var unit;           // 물의 온도 단위
    var temp;           // 물의 온도
    var state;          // 물의 상태(고체, 액체, 기체)

    unit = Number(prompt("온도 단위를 입력해 주세요(1:섭씨, 2:화씨)."));
    temp = Number(prompt("온도를 입력해 주세요."));

    if (unit == 2) {
        temp = (temp - 32) * 5 / 9;     // 화씨 => 섭씨 변환
    }
        
    if (temp < 0) {
        state = "고체";
    }
    else if (temp < 100) {
        state = "액체";
    }
    else {
        state = "기체";
    }
    
    document.write("물의 섭씨 온도 : " + temp + "도<br>");
    document.write("물의 상태는 " + state + "입니다.");
</script>
```
첫번째로 나는 변수 섭씨 화씨를 따로 정하려고함.   
위의 답에서 알수있듯이 unit이 2와 같다면 섭씨로 변환시키는 식을 수행시켜주고,   
첫번째 조건문 (unit == 2)이 아니라면 다음 조건문으로 바로 이동하는 식을 이용함...   
굳이 두개를 나눌 필요가 전혀 없는...   
<b>if문의 중첩에 대한 이해도가 부족한거 같다</b>   

<br>

3. ⭕⭕⭕ 키와 몸무게를 입력받아 다이어트 유무를 판정하는 프로그램을 작성하시오.   

    ※ 판정 기준    
    std = (몸무게 - 100) * 0.9      

    ※ 출력 메세지    
    - 뭄무게가 std 보다 큰 경우   
        다이어트가 필요할 수 있습니다 를 화면에 출력   
    - 그렇지 않은 경우   
        표준(또는 마른)체형입니다 를 화면에 출력     

```html
<script>
    var height;
    var weight;
    var std;

    height = Number(prompt("키를 입력해 주세요."));
    weight = Number(prompt("몸무게를 입력해 주세요."));
    std = (weight -100) * 0.9;
    document.write("키 : " + height + "cm" + "<br>");
    document.write("몸무게 : " + weight + "kg" + "<br>");
    if(weight > std){
        document.write("다이어트가 필요할 수 있습니다.");
    }
    else{
        document.write("표준(또는 마른) 체형입니다.");
    }
    
</script>
```


