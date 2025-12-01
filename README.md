<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>慈青活動介紹</title>

    <style>
        body {
            font-family: 'Arial', 'Microsoft JhengHei', sans-serif;
            background-color: #f4f4f9;
            color: #333;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        .container {
            background-color: #fff;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            text-align: center;
            width: 80%;
            max-width: 650px;
        }

        h1 {
            color: #2c3e50;
            margin-bottom: 20px;
        }

        .btn {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 12px 25px;
            font-size: 16px;
            border-radius: 5px;
            cursor: pointer;
            margin: 10px auto;
            display: block;
            width: 280px;
            transition: 0.3s;
        }

        .btn:hover {
            background-color: #2980b9;
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 10;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.6);
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            background-color: #fff;
            width: 90%;
            max-width: 600px;
            padding: 20px;
            border-radius: 10px;
            text-align: left;
            animation: fadeIn 0.3s ease;
        }

        .modal img {
            width: 100%;
            border-radius: 8px;
            margin-bottom: 15px;
        }

        .close-btn {
            background-color: #e74c3c;
            color: white;
            float: right;
            padding: 5px 12px;
            cursor: pointer;
            border-radius: 4px;
        }

        .close-btn:hover {
            background-color: #c0392b;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        footer {
            margin-top: 30px;
            font-size: 0.9em;
            color: #7f8c8d;
        }

    </style>
</head>
<body>

    <div class="container">
        <h1>慈青活動介紹</h1>
        <h3>什麼是慈青呢?</h3>
        <p>慈青全稱為「慈濟大專青年聯誼會」，由全球大專院校學生所組成，秉持走入人群、付出自我的理念，成為校園中一股清流。</p>

        <h3>慈青的營隊介紹</h3>
        <p>請選擇任一活動，查看詳細介紹：</p>

        <button class="btn" onclick="showCamp('lifeMaker')">LifeMaker 人生創客大專青年營</button>
        <button class="btn" onclick="showCamp('overseas')">全球慈青幹部研習營</button>
        <button class="btn" onclick="showCamp('summerCamp')">暑期海外志工成長營</button>
        <button class="btn" onclick="showCamp('leadCamp')">慈青幹部培訓營</button>

        <footer>
            <p>&copy; 2025 網頁設計範例</p>
        </footer>
    </div>

    <div id="campModal" class="modal">
        <div class="modal-content">
            <span class="close-btn" onclick="closeModal()">關閉</span>
            <h2 id="campTitle"></h2>
            <img id="campImg" src="">
            <p id="campText"></p>
        </div>
    </div>

    <script>
        const campData = {
            lifeMaker: {
                title: "LifeMaker 人生創客大專青年營",
                img: "大學.jpg",
                text: "透過設計思考、團隊合作、生命探索，引導青年打造屬於自己的『人生藍圖』。"
            },
            overseas: {
                title: "全球慈青幹部研習營",
                img: "大學.jpg",
                text: "以靜思語、人文課程、團隊活動為核心，培養青年的人文素養與團隊默契。"
            },
            summerCamp: {
                title: "慈青人文教育交流",
                img: "大學.jpg",
                text: "結合海外服務與文化交流，引導青年走出舒適圈，看見世界的需要。"
            },
            leadCamp: {
                title: "慈濟青年營",
                img: "大學.jpg",
                text: "強化領導能力、帶隊技巧與溝通協作，提供幹部實務訓練。"
            }
        };

        function showCamp(campKey) {
            const camp = campData[campKey];
            document.getElementById('campTitle').textContent = camp.title;
            document.getElementById('campImg').src = camp.img;
            document.getElementById('campText').textContent = camp.text;

            document.getElementById('campModal').style.display = "flex";
        }

        function closeModal() {
            document.getElementById('campModal').style.display = "none";
        }
    </script>

</body>
</html>
