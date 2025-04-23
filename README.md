<!DOCTYPE html>
<html lang="da">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Nedtælling til Installatøreksamen</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      background-color: #f0f0f0;
    }
    h1 {
      font-size: 2rem;
      margin-bottom: 1rem;
    }
    #countdown {
      font-size: 3rem;
      font-weight: bold;
      color: #333;
    }
  </style>
</head>
<body>
  <h1>Nedtælling til Installatøreksamen</h1>
  <div id="countdown"></div>

  <script>
    const countdownElement = document.getElementById('countdown');
    const examDate = new Date('2025-12-16T00:00:00');

    function updateCountdown() {
      const now = new Date();
      const diff = examDate - now;

      if (diff <= 0) {
        countdownElement.textContent = "Held og lykke til eksamen i dag!";
        return;
      }

      const days = Math.floor(diff / (1000 * 60 * 60 * 24));
      const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
      const minutes = Math.floor((diff / (1000 * 60)) % 60);
      const seconds = Math.floor((diff / 1000) % 60);

      countdownElement.textContent = `${days} dage, ${hours} timer, ${minutes} minutter, ${seconds} sekunder`;
    }

    updateCountdown();
    setInterval(updateCountdown, 1000);
  </script>
</body>
</html>
