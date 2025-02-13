<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For Piji Dewi Antikasari</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #ffebee;
            font-family: 'Courier New', Courier, monospace;
            text-align: center;
        }
        .letter {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            max-width: 500px;
        }
        .text {
            font-size: 18px;
            white-space: pre-wrap;
            word-wrap: break-word;
            text-align: left;
            min-height: 80px;
        }
        .hidden {
            display: none;
        }
        button {
            margin-top: 10px;
            padding: 10px;
            border: none;
            background-color: #e57373;
            color: white;
            font-size: 16px;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="letter">
        <p class="text" id="message">Coba pencet button dibawah</p>
        <button id="nextButton">Next</button>
    </div>

    <script>
        const messages = [
            "Bebbb, jangan lupa selalu jaga kesehatan ya. Kamu suka banget nunda makan sampe malem atau tidurmu terlalu larut malem. Aku selalu khawatir tau tentang itu",
            "Pengen tak totok rasanya kalau kamu gitu terus, melakukan hal-hal yang bisa merusak kesehatan kamu",
            "Kamu itu adalah seseorang yang sangat spesial bagiku tanpa dikareti dan Nasi goreng atau Martabak yang spesial aja masih kalah sama kamu",
            "Karna kamu se spesial itu, Tidak ada hari tanpa aku memikirkanmu dan berharap kamu selalu bahagia dan baik-baik saja disana",
            "Dan aku selalu berdoa dan berharap perasaan ini bisa tersampaikan ke kamu dan semoga kita bisa ketemu secara langsung suatu saat nanti",
            "Aku tau jarak memisahkan kita, tapi hatiku selalu terjaga untukmu. Tak peduli seberapa jauh kita, cintaku padamu tak akan berubah",
            "Happy Valentine's Day Sayangkuuuu Piji ❤️😊",
            "Dari seseorang yang selalu sayang kamu dari jarak 1,316 km"
        ];
        let index = -1;
        const messageElement = document.getElementById("message");
        const buttonElement = document.getElementById("nextButton");
        
        function typeWriter(text, i = 0) {
            if (i < text.length) {
                messageElement.innerHTML += text.charAt(i);
                setTimeout(() => typeWriter(text, i + 1), 50);
            }
        }
        
        function showMessage() {
            messageElement.innerHTML = "";
            typeWriter(messages[index]);
        }
        
        buttonElement.addEventListener("click", function() {
            if (index < messages.length - 1) {
                index++;
                showMessage();
            } else {
                buttonElement.style.display = "none";
            }
        });
    </script>
</body>
</html>
