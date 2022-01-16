<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>爱心动画</title>
    <style>
        body {
            margin: 0;
            animation: colorChange 6s linear infinite alternate;
        }

        .heart {
            width: 400px;
            height: 400px;
            margin: 100px auto;
        }

        .yue {
            float: left;
            width: 200px;
            height: 200px;
        }

        .left,
        .right {
            float: left;
            width: 100px;
            height: 160px;
            background-color: pink;
            border-radius: 50px 50px 0 0;
        }

        .left {
            transform: translateX(-28px) rotate(45deg);
            /* transform:translateX位移，以x轴为准; */
        }

        .right {
            transform: translateX(30px) rotate(-45deg);
        }

        /* 选择heart下的第二个you 【子元素】*/
        .you:nth-child(2) {
            animation: move 6s linear infinite alternate;
            /* 播放/绑定动画 绑定函数 时间 速度【匀速】 次数【循环【反向】】 */
        }

        .you:nth-child(2) .left,
        .you:nth-child(2) .right {
            animation: colorChange 6s linear infinite alternate;
        }

        @keyframes move {
            0% {
                /* 动画开始的画面 */
                transform: translate(0px);
            }

            100% {
                /* 动画结束的画面 */
                transform: translate(-400px);
            }
        }

        @keyframes colorChange {
            0% {
                background-color: skyblue;
            }

            50% {
                background-color: black;
            }

            100% {
                background-color: skyblue;
            }

        }
    </style>
</head>

<body>
    <div class="heart">
        <div class="you">
            <div class="right"></div>
            <div class="left"></div>
        </div>
        <div class="you">
            <div class="right"></div>
            <div class="left"></div>
        </div>
    </div>
</body>

</html>
