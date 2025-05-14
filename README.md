# Fortune-teller
a simple click to decide what your future entails, do you dare to click? 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Fortune Teller</title>
  <style>
    body {
      background-color: #000000;
      color: #FFD700;
      font-family: 'Arial', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      text-align: center;
    }
    #fortune-btn {
      background-color: #FFD700;
      color: black;
      border: none;
      padding: 15px 30px;
      font-size: 1.2em;
      cursor: pointer;
      border-radius: 8px;
      transition: background 0.3s ease;
    }
    #fortune-btn:hover {
      background-color: #e6c200;
    }
  </style>
</head>
<body>
  <div>
    <button id="fortune-btn">Reveal Your Fortune</button>
    <p id="fortune-text" style="margin-top: 20px; display: none;"></p>
  </div>

  <script>
    const fortunes = [
      "You will find what you're not looking for.",
      "A mysterious stranger will change your day.",
      "Today is a good day to try something new.",
      "Avoid decisions made in the moonlight.",
      "Wealth is coming — but it’s not money.",
      "You are the glitch in someone else's simulation.",
      "Your pet knows more than they let on.",
      "Soon, you'll overhear something meant just for you.",
      "Laugh now. The universe is listening.",
      "Your next thought will be important. Remember it."
    ];

    const button = document.getElementById('fortune-btn');
    const fortuneText = document.getElementById('fortune-text');

    button.addEventListener('click', () => {
      const randomFortune = fortunes[Math.floor(Math.random() * fortunes.length)];
      fortuneText.textContent = randomFortune;
      fortuneText.style.display = 'block';
      button.style.display = 'none';
    });
  </script>
</body>
</html>
