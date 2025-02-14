# Jobish

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
