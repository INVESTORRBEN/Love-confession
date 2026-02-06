<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>💖 For My Love 💖</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: linear-gradient(120deg, #ff9a9e, #fad0c4);
      margin: 0;
      overflow: hidden;
      text-align: center;
    }

    h1 {
      font-size: 3rem;
      color: #fff;
      text-shadow: 2px 2px 8px #ff6f91;
    }

    .heart-button {
      font-size: 2rem;
      background: #ff6f91;
      color: white;
      border: none;
      padding: 15px 30px;
      border-radius: 50px;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 5px 15px rgba(0,0,0,0.2);
    }

    .heart-button:hover {
      transform: scale(1.2);
      background: #ff4d6d;
    }

    .message {
      margin-top: 20px;
      font-size: 1.5rem;
      color: #fff;
      opacity: 0;
      transition: opacity 0.5s ease;
    }

    /* Floating hearts animation */
    .floating-heart {
      position: absolute;
      font-size: 2rem;
      animation: floatUp 2s ease forwards;
    }

    @keyframes floatUp {
      0% { transform: translateY(0) scale(1); opacity: 1; }
      100% { transform: translateY(-200px) scale(0.5); opacity: 0; }
    }
  </style>
</head>
<body>

  <div>
    <h1>💖 Click the Heart 💖</h1>
    <button class="heart-button">❤️</button>
    <div class="message" id="message">I love you more than words can say! 💕</div>
  </div>

  <script>
    const button = document.querySelector('.heart-button');
    const message = document.getElementById('message');

    button.addEventListener('click', () => {
      // Show message
      message.style.opacity = 1;

      // Create floating heart
      const heart = document.createElement('div');
      heart.classList.add('floating-heart');
      heart.textContent = '💖';
      heart.style.left = Math.random() * window.innerWidth + 'px';
      heart.style.color = `hsl(${Math.random() * 360}, 100%, 70%)`;
      document.body.appendChild(heart);

      // Remove heart after animation
      setTimeout(() => heart.remove(), 2000);
    });
  </script>

</body>
</html>
