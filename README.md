<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Omke Gams Generator 666</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-image: url('gambar/bekgron.jpg');
            background-size: cover;
            background-position: center;
        }

        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 20px;
            background-color: rgba(255, 255, 255, 0.3);
            backdrop-filter: blur(10px);
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.5);
        }

        .title, .footer {
            font-size: 24px;
            color: black;
            text-shadow: 1px 1px 2px rgba(255, 255, 255, 0.7);
        }

        .footer {
            font-size: 14px;
            margin-top: 10px;
        }

        .textarea-container {
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .input-area, .output-area {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        textarea {
            width: 300px;
            height: 100px;
            padding: 10px;
            border-radius: 5px;
            border: 1px solid #ccc;
            resize: none;
            font-size: 16px;
            backdrop-filter: blur(5px);
        }

        button {
            padding: 10px 20px;
            font-size: 16px;
            border-radius: 5px;
            border: none;
            background-color: #007bff;
            color: white;
            cursor: pointer;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.3);
        }

        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="title">Omke Gams Generator 666</div>
        
        <div class="textarea-container">
            <div class="input-area">
                <textarea id="inputText" placeholder="Masukkan teks di sini..." oninput="modifyText()"></textarea>
            </div>
            <div class="output-area">
               
                <textarea id="outputText" placeholder="Hasil akan muncul di sini..." readonly></textarea>
            </div>
             <button onclick="copyText()">Salin</button>
             
        </div>

        <div class="footer">made by fufufufu</div>
    </div>

    <script>
        function modifyText() {
            let inputText = document.getElementById('inputText').value;
            
            // Hilangkan huruf ganda yang berurutan
            let outputText = inputText.replace(/([a-zA-Z])\1+/g, '$1');

            // Menyisipkan huruf "m" setelah vokal diikuti oleh konsonan
            outputText = outputText.replace(/([aeiou])(\w)/gi, '$1m$2');

            // Mengganti huruf "p" atau "b" dengan "v"
            outputText = outputText.replace(/[pb]/gi, 'v');

            document.getElementById('outputText').value = outputText;
        }

        function copyText() {
            const outputText = document.getElementById('outputText');
            outputText.select();
            document.execCommand('copy');
            alert('Teks hasil berhasil disalin!');
        }
    </script>
</body>
</html>
