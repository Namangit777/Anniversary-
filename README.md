# Anniversary-
anniversary-website/
├── index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Our Anniversary</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Happy Anniversary!</h1>
        <p>Celebrating [X] years together!</p>
    </header>
    <section>
        <h2>Memories</h2>
        <p>[Add a few memorable moments, photos, or quotes here]</p>
    </section>
    <footer>
        <p>Thank you for celebrating with us!</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>
<div id="countdown"></div>


├── styles.css
body {
    font-family: Arial, sans-serif;
    background-color: #f0f8ff;
    text-align: center;
    padding: 20px;
}

header {
    background-color: #ff99cc;
    padding: 20px;
    border-radius: 10px;
}

h1 {
    font-size: 3em;
    color: white;
}

p {
    font-size: 1.2em;
}

footer {
    margin-top: 30px;
    font-size: 1em;
    color: #666;
}

└── script.js
const countdownDate = new Date("2025-02-14").getTime();
const countdown = setInterval(function() {
    const now = new Date().getTime();
    const distance = countdownDate - now;

    const days = Math.floor(distance / (1000 * 60 * 60 * 24));
    const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
    const seconds = Math.floor((distance % (1000 * 60)) / 1000);

    document.getElementById("countdown").innerHTML = `${days}d ${hours}h ${minutes}m ${seconds}s`;

    if (distance < 0) {
        clearInterval(countdown);
        document.getElementById("countdown").innerHTML = "It's here! Happy Anniversary!";
    }
}, 1000);
git add .
git commit -m "Initial commit for anniversary website"
git push origin main


