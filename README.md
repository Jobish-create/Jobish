* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f9;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    overflow: hidden;
}

.container {
    text-align: center;
}

.content {
    background-color: #ffffff;
    padding: 40px;
    border-radius: 10px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    max-width: 400px;
    width: 100%;
}

h1, p {
    font-size: 36px;
    color: #4CAF50;
    margin: 20px 0;
    opacity: 0;
    animation: fadeIn 1s forwards;
}

p {
    font-size: 18px;
    color: #333;
}

.countdown {
    margin: 30px 0;
}

#timer {
    font-size: 24px;
    color: #FF6347;
    font-weight: bold;
    animation: countdownEffect 1s ease-out;
}

form input {
    padding: 10px;
    width: 80%;
    margin-right: 10px;
    border-radius: 5px;
    border: 1px solid #ccc;
    opacity: 0;
    animation: fadeIn 1s forwards;
}

form button {
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: all 0.3s ease-in-out;
}

form button:hover {
    background-color: #45a049;
    transform: scale(1.1);
    animation: pulseButton 1s infinite;
}

@keyframes fadeIn {
    0% {
        opacity: 0;
        transform: translateY(-20px);
    }
    100% {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes pulseButton {
    0% {
        transform: scale(1);
    }
    50% {
        transform: scale(1.1);
    }
    100% {
        transform: scale(1);
    }
}

@keyframes countdownEffect {
    0% {
        opacity: 0;
        transform: scale(0.8);
    }
    100% {
        opacity: 1;
        transform: scale(1);
    }
}


# Jobish
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f9;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    overflow: hidden;
}

.container {
    text-align: center;
}

.content {
    background-color: #ffffff;
    padding: 40px;
    border-radius: 10px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    max-width: 400px;
    width: 100%;
}

h1, p {
    font-size: 36px;
    color: #4CAF50;
    margin: 20px 0;
    opacity: 0;
    animation: fadeIn 1s forwards;
}

p {
    font-size: 18px;
    color: #333;
}

.countdown {
    margin: 30px 0;
}

#timer {
    font-size: 24px;
    color: #FF6347;
    font-weight: bold;
    animation: countdownEffect 1s ease-out;
}

form input {
    padding: 10px;
    width: 80%;
    margin-right: 10px;
    border-radius: 5px;
    border: 1px solid #ccc;
    opacity: 0;
    animation: fadeIn 1s forwards;
}

form button {
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: all 0.3s ease-in-out;
}

form button:hover {
    background-color: #45a049;
    transform: scale(1.1);
    animation: pulseButton 1s infinite;
}

@keyframes fadeIn {
    0% {
        opacity: 0;
        transform: translateY(-20px);
    }
    100% {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes pulseButton {
    0% {
        transform: scale(1);
    }
    50% {
        transform: scale(1.1);
    }
    100% {
        transform: scale(1);
    }
}

@keyframes countdownEffect {
    0% {
        opacity: 0;
        transform: scale(0.8);
    }
    100% {
        opacity: 1;
        transform: scale(1);
    }
}

// Setează data estimată pentru lansare
var launchDate = new Date("Mar 1, 2025 00:00:00").getTime();

// Actualizează contorul de timp la fiecare secundă
var x = setInterval(function() {
    var now = new Date().getTime();
    var distance = launchDate - now;

    var days = Math.floor(distance / (1000 * 60 * 60 * 24));
    var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
    var seconds = Math.floor((distance % (1000 * 60)) / 1000);

    document.getElementById("countdown").innerHTML = days + "z " + hours + "h "
    + minutes + "m " + seconds + "s ";

    // Dacă s-a ajuns la data de lansare, oprește contorul
    if (distance < 0) {
        clearInterval(x);
        document.getElementById("countdown").innerHTML = "Suntem live! 🎉";
    }
}, 1000);

<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jobish - În construcție</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <div class="content">
            <h1>Suntem aproape gata!</h1>
            <p>Lucrăm pentru a-ți aduce ceva grozav. Rămâi aproape!</p>
            <div class="countdown">
                <p>Vei fi primul care află când suntem gata!:</p>
                <div id="timer">
                    <p id="countdown"></p>
                </div>
            </div>
            <form action="#" method="POST">
                <input type="email" placeholder="Introdu emailul tău" required>
                <button type="submit">Abonează-te</button>
            </form>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
