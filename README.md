
   <!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pagina în construcție</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(45deg, #f06, #4a90e2);
            background-size: 400% 400%;
            animation: gradientAnimation 5s ease infinite;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            color: #fff;
        }
        
        @keyframes gradientAnimation {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .container {
            text-align: center;
            background-color: rgba(255, 255, 255, 0.1);
            padding: 50px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            transform: translateY(-50px);
            animation: fadeIn 1.5s ease-out forwards;
        }

        h1 {
            font-size: 3em;
            margin: 0;
            animation: textAnimation 1s ease-out forwards;
        }

        p {
            font-size: 1.5em;
            margin-top: 20px;
            opacity: 0;
            animation: fadeInText 2s ease-out 1s forwards;
        }

        .loader {
            border: 8px solid #f3f3f3;
            border-top: 8px solid #3498db;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            animation: spin 2s linear infinite;
            margin: 20px auto;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        @keyframes fadeIn {
            0% { opacity: 0; transform: translateY(-50px); }
            100% { opacity: 1; transform: translateY(0); }
        }

        @keyframes textAnimation {
            0% { opacity: 0; transform: scale(0.5); }
            100% { opacity: 1; transform: scale(1); }
        }

        @keyframes fadeInText {
            0% { opacity: 0; }
            100% { opacity: 1; }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Pagina este în construcție</h1>
        <p>Îți mulțumim pentru răbdare! Vom reveni în curând cu mai multe informații.</p>
        <div class="loader"></div>
    </div>
</body>
</html>
