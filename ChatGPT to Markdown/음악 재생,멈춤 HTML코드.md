**You:**

HTML 페이지에서 버튼이 2개 있다.

[시작], [멈춤]
[시작]을 누르면

https://vgmsite.com/soundtracks/samurai-aces-arcade/cmqeaknx/01_Player%20Select.mp3

플레이한다.

[멈춤]을 누르면 음악을 멈춘다.

소스를 만들어줘



* * *

**ChatGPT:**

아래는 HTML과 JavaScript를 사용하여 버튼으로 음악을 재생하고 멈추는 간단한 예제입니다. 이 코드를 HTML 파일에 추가하면 됩니다.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>음악 플레이어</title>
</head>
<body>

<button onclick="playMusic()">시작</button>
<button onclick="stopMusic()">멈춤</button>

<script>
let audio;

function playMusic() {
    // 이미 재생 중인 경우 중복 재생을 방지하기 위해 음악을 중지
    if (audio) {
        audio.pause();
        audio.currentTime = 0;
    }

    // 새로운 음악 재생
    audio = new Audio('https://vgmsite.com/soundtracks/samurai-aces-arcade/cmqeaknx/01_Player%20Select.mp3');
    audio.play();
}

function stopMusic() {
    // 음악을 멈추고 재생 위치를 초기화
    if (audio) {
        audio.pause();
        audio.currentTime = 0;
    }
}
</script>

</body>
</html>
```

이 코드는 [시작] 버튼을 누르면 주어진 URL의 음악을 재생하고, [멈춤] 버튼을 누르면 재생 중인 음악을 멈추는 간단한 음악 플레이어를 만듭니다.