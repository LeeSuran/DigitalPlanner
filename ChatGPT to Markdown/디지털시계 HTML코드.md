**You:**


HTML과 Javascript  
    기능:  
    2024.12.31을 기준으로 현재시간을 뺀 남은 시간을 표시한다  
    화면:  
    중앙에 디지털 시계를 표시한다.  
    디지털 시계는 남은 시간을 표시한다.

디지털 시계화면 상세:  
글자크기: 32pt  
그림자 : True  
글자색: 붉은색

소스를 만들어줘



* * *

**ChatGPT:**

아래는 HTML과 JavaScript를 사용하여 설명한 요구사항에 맞는 코드 예제입니다.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>디지털 시계</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
        }

        #digitalClock {
            font-size: 32pt;
            text-shadow: 2px 2px 5px #ff0000;
            color: #ff0000;
        }
    </style>
</head>
<body>
    <div id="digitalClock"></div>

    <script>
        function updateDigitalClock() {
            // 현재 날짜 및 시간 가져오기
            var currentDate = new Date();
            var targetDate = new Date("2024-12-31T00:00:00");

            // 남은 시간 계산
            var timeDiff = targetDate - currentDate;
            var days = Math.floor(timeDiff / (1000 * 60 * 60 * 24));
            var hours = Math.floor((timeDiff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            var minutes = Math.floor((timeDiff % (1000 * 60 * 60)) / (1000 * 60));
            var seconds = Math.floor((timeDiff % (1000 * 60)) / 1000);

            // 디지털 시계 업데이트
            var digitalClock = document.getElementById("digitalClock");
            digitalClock.innerHTML = days + "일 " + hours + "시간 " + minutes + "분 " + seconds + "초";
        }

        // 초기화 및 주기적으로 업데이트
        updateDigitalClock(); // 초기화
        setInterval(updateDigitalClock, 1000); // 1초마다 업데이트
    </script>
</body>
</html>
```

이 코드는 현재 날짜와 2024년 12월 31일의 차이를 계산하여 디지털 시계로 표시하는 예제입니다. 화면에는 빨간색으로 그림자가 적용된 32pt 크기의 디지털 시계가 중앙에 표시됩니다.