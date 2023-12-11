<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8">
    <title>我的主页</title>
    <style>
        body {
            background-color: #f0f0f0;
            font-family: Arial, sans-serif;
            padding: 20px;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            background-color: #fff;
            border-radius: 5px;
            padding: 20px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        h1 {
            text-align: center;
            color: #333;
            margin-top: 20px;
        }

        .link-list {
            list-style: none;
            padding: 0;
            margin-top: 20px;
        }

        .link-list li {
            margin-bottom: 10px;
        }

        .link-list li a {
            display: block;
            padding: 10px 20px;
            background-color: #e0e0e0;
            border: 1px solid #999;
            text-decoration: none;
            color: #333;
            border-radius: 5px;
            transition: background-color 0.3s ease-in-out;
        }

        .link-list li a:hover {
            background-color: #ccc;
            box-shadow: 0 1px 2px rgba(0, 0, 0, 0.1);
        }

        /* 新增样式 */
        .intro {
            margin-top: 30px;
            text-align: center;
            color: #666;
            font-size: 16px;
            line-height: 1.5;
        }
    </style>
</head>

<body>
    <!-- 添加一个顶部容器，放置日期时间 -->
    <div class="top-container">
        <span id="datetime"></span>

    </div>
    <div class="container">
        <h1>欢迎访问我的主页</h1>

        <ul class="link-list">
            <li><a href="20213649-20230905.txt">第一次作业</a></li>
            <li><a href="20213649-20230912.html">第二次作业</a></li>
            <li><a href="20213649-2023919.html">第三次作业</a></li>
            <li><a href="#">第四次作业</a></li>
            <li><a href="#">第五次作业</a></li>
            <li><a href="#">第六次作业</a></li>
            <li><a href="#">第七次作业</a></li>
            <li><a href="#">第八次作业</a></li>
            <li><a href="#">第九次作业</a></li>
        </ul>

        <!-- 新增个人简介 -->
        <div class="intro">
            <h3>个人简介</h3>
            <p>这是我的主页</p>
        </div>
    </div>
    <script>
        function updateDateTime() {
            var now = new Date();
            var year = now.getFullYear();
            var month = now.getMonth() + 1;
            var date = now.getDate();
            var hour = now.getHours();
            var minute = now.getMinutes();
            var second = now.getSeconds();

            // 格式化时间，例如：2023-10-07 11:25:30
            var formattedDateTime = year + "-"
                + (month > 9 ? month : "0" + month) + "-"
                + (date > 9 ? date : "0" + date) + " "
                + (hour > 9 ? hour : "0" + hour) + ":"
                + (minute > 9 ? minute : "0" + minute) + ":"
                + (second > 9 ? second : "0" + second);

            // 更新页面内容
            document.getElementById("datetime").innerHTML = formattedDateTime;
        }

        // 每秒更新一次时间
        setInterval(updateDateTime, 1000);
    </script>
</body>

</html>
