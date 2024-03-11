**You:**

1을 누르면 고양이 그림을 다음주소에서 가져와 보여주고(https://cdn.pixabay.com/photo/2015/11/16/14/43/cat-1045782_1280.jpg), 
2를 누르면  강아지 그림을 다음주소에서 가져오는 (https://cdn.pixabay.com/photo/2016/12/13/05/15/puppy-1903313_1280.jpg) HTML 소스를 만들어줘


* * *

**ChatGPT:**

아래는 간단한 HTML 코드입니다. 사용자가 1 또는 2를 누르면 해당하는 이미지가 나타납니다.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pet Images</title>
</head>
<body>

<h1>동물 사진</h1>
<p>1을 누르면 고양이, 2를 누르면 강아지 사진을 보여줍니다.</p>

<script>
    function showImage(option) {
        var imageElement = document.getElementById('petImage');
        if (option === 1) {
            imageElement.src = 'https://cdn.pixabay.com/photo/2015/11/16/14/43/cat-1045782_1280.jpg';
        } else if (option === 2) {
            imageElement.src = 'https://cdn.pixabay.com/photo/2016/12/13/05/15/puppy-1903313_1280.jpg';
        }
    }
</script>

<button onclick="showImage(1)">1. 고양이</button>
<button onclick="showImage(2)">2. 강아지</button>

<img id="petImage" src="" alt="동물 이미지">

</body>
</html>
```

이 코드는 버튼을 클릭할 때 `showImage` 함수가 호출되어 선택한 동물 이미지를 보여줍니다. `img` 태그에 `id`를 부여하여 JavaScript에서 해당 이미지를 조작할 수 있도록 했습니다.