<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Markdown in HTML</title>
    <script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
    <style>
        body {
            display: flex;
            margin: 0;
            height: 100vh;
        }
        .column {
            flex: 1;
            padding: 20px;
            border: 1px solid #ccc;
            box-sizing: border-box;
            overflow-y: auto;
        }
        .left {
            border-right: none;
        }
    </style>
</head>
<body>
    <div id="left-column" class="column left">
        <!-- 왼쪽 열에 마크다운 내용이 들어갈 곳 -->
    </div>
    <div id="right-column" class="column right">
        <!-- 오른쪽 열에 마크다운 내용이 들어갈 곳 -->
    </div>

    <script>
        // 마크다운 내용 (--- 기준으로 분리된 두 부분)
        var markdownContentLeft = `
![header](https://capsule-render.vercel.app/api?type=waving&color=0:c5c8fa,100:9095ee&text=chaewon%20KIM&fontColor=4d518e&fontSize=50)

### Who am I?
- Born, raised and based in Korea / Lived in France   
- Graduated from Pusan National University (South Korea)
- Studied at INALCO (France) as an exchange student
- Majored in **French Language and Literature**   
- Double majored in **Computer Science Engineering**   
   
### I speak
- Korean : native   
- English : fluent (OPIc IH)
- French : intermediate (DELF B2)    
 　   
　   
`;

        var markdownContentRight = `
### Project
1.  Large-scale Language Model specialized in Patent Field   
2.  Auto-sanitizing machine for door handle due to COVID-19

### Tech
![Static Badge](https://img.shields.io/badge/C++-badge?logo=C%2B%2B&labelColor=00599C&color=00599C)
![Static Badge](https://img.shields.io/badge/Java-badge?color=purple)
![Static Badge](https://img.shields.io/badge/C-badge?logo=C&logoColor=white&labelColor=A8B9CC&color=A8B9CC)
![Static Badge](https://img.shields.io/badge/Python-badge?logo=Python&logoColor=white&labelColor=3776AB&color=3776AB)

### Baekjoon [![Solved.ac프로필](http://mazassumnida.wtf/api/mini/generate_badge?boj=bbubbune)](https://solved.ac/bbubbune)
`;

        // 마크다운 내용을 HTML로 변환하여 각 열에 삽입
        document.getElementById('left-column').innerHTML = marked(markdownContentLeft);
        document.getElementById('right-column').innerHTML = marked(markdownContentRight);
    </script>
</body>
</html>
