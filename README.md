<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>I Love You Deena</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(120deg, #ffd6e0, #ffe6f7);
      overflow: hidden;
      font-family: 'Segoe Script', cursive;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      flex-direction: column;
    }

    h1 {
      color: #ff1493;
      font-size: 3em;
      text-shadow: 0 0 10px #ff66cc;
      animation: glow 2s ease-in-out infinite alternate;
    }

    @keyframes glow {
      from {
        text-shadow: 0 0 10px #ff66cc, 0 0 20px #ff66cc;
      }
      to {
        text-shadow: 0 0 20px #ff3399, 0 0 30px #ff3399;
      }
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: #ff4d6d;
      transform: rotate(-45deg);
      animation: floatUp 6s infinite ease-in;
      opacity: 0.8;
    }

    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      width: 20px;
      height: 20px;
      background: #ff4d6d;
      border-radius: 50%;
    }

    .heart::before {
      top: -10px;
      left: 0;
    }

    .heart::after {
      left: 10px;
      top: 0;
    }

    @keyframes floatUp {
      0% {
        transform: translateY(100vh) rotate(-45deg);
        opacity: 0;
      }
      50% {
        opacity: 1;
      }
      100% {
        transform: translateY(-10vh) rotate(-45deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <h1>I Love You Deena</h1>

  <script>
    // Create hearts dynamically
    for (let i = 0; i < 40; i++) {
      const heart = document.createElement('div');
      heart.className = 'heart';
      heart.style.left = `${Math.random() * 100}%`;
      heart.style.animationDuration = `${4 + Math.random() * 3}s`;
      heart.style.animationDelay = `${Math.random() * 5}s`;
      heart.style.opacity = `${0.5 + Math.random() * 0.5}`;
      document.body.appendChild(heart);
    }
  </script>
</body>
</html>
