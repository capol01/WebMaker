# WebMaker
<!DOCTYPE html>
<html lang="cs">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Web na objednávku</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f4f4f4;
        }
        .container {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .form-group {
            margin-bottom: 15px;
        }
        .form-group label {
            display: block;
            margin-bottom: 5px;
        }
        .form-group input {
            width: 100%;
            padding: 8px;
            box-sizing: border-box;
        }
        .form-group button {
            padding: 10px 15px;
            background-color: #007BFF;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        .form-group button:hover {
            background-color: #0056b3;
        }
        .info {
            display: none;
            margin-top: 20px;
        }
        .title {
            margin-bottom: 20px;
            font-size: 24px;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="title">Registrace</div>
        <div class="form-group">
            <label for="username">Jméno</label>
            <input type="text" id="username" name="username">
        </div>
        <div class="form-group">
            <label for="password">Heslo</label>
            <input type="password" id="password" name="password">
        </div>
        <div class="form-group">
            <button onclick="showInfo()">Přihlásit se</button>
        </div>
        <div class="info" id="info">
            <h2>O tomto webu</h2>
            <p>Tento web je určen pro objednávání webových stránek. Vytvořím vám web na zakázku za peníze.</p>
            <h2>O mně</h2>
            <p>Narodil jsem se 10. ledna 2013.</p>
            <h2>Kontakt</h2>
            <p>Email: <a href="mailto:capolvoking@gmail.com">capolvoking@gmail.com</a></p>
        </div>
    </div>

    <script>
        function showInfo() {
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;

            if (username && password) {
                document.getElementById('info').style.display = 'block';
            } else {
                alert('Prosím, zadejte jméno a heslo.');
            }
        }
    </script>
</body>
</html>
