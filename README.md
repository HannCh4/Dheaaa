<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no" />
<title>I Love You, Adekkkkk </title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');

  * {
    box-sizing: border-box;
  }
  body, html {
    margin: 0; padding: 0;
    height: 100%;
    width: 100%;
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #ff758c 0%, #ff7eb3 100%);
    color: #fff;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }

  .container {
    background: rgba(255, 255, 255, 0.15);
    border-radius: 20px;
    width: 90vw;
    max-width: 350px;
    padding: 25px 20px 35px;
    box-shadow: 0 8px 20px rgba(255 255 255 / 0.2);
    backdrop-filter: blur(10px);
    user-select: none;
  }

  h1 {
    font-size: 2.5rem;
    margin-bottom: 10px;
    text-shadow: 0 0 12px rgba(255,255,255,0.6);
  }

  h2 {
    font-weight: 400;
    font-size: 1.25rem;
    margin-bottom: 25px;
    letter-spacing: 0.07em;
    color: #ffe7f0cc;
    text-shadow: 0 0 6px rgba(255, 255, 255, 0.6);
  }

  .heart {
    width: 90px;
    height: 80px;
    position: relative;
    margin: 0 auto 25px auto;
    cursor: pointer;
    filter: drop-shadow(0 0 6px #ffcade);
    transition: transform 0.3s ease;
  }

  .heart:before,
  .heart:after {
    content: "";
    position: absolute;
    left: 45px;
    top: 0;
    width: 45px;
    height: 70px;
    background: #ff1867;
    border-radius: 45px 45px 0 0;
    transform-origin: bottom left;
    animation-name: heartbeat;
    animation-duration: 1.2s;
    animation-iteration-count: infinite;
    animation-timing-function: ease-in-out;
  }

  .heart:after {
    left: 0;
    transform-origin: bottom right;
  }

  @keyframes heartbeat {
    0%, 100% {
      transform: rotate(45deg);
      background: #ff1867;
      filter: drop-shadow(0 0 12px #ff1867);
    }
    50% {
      transform: rotate(50deg) scale(1.1);
      background: #ff3d7a;
      filter: drop-shadow(0 0 20px #ff3d7a);
    }
  }

  .heart.pulse {
    transform: scale(1.15);
  }

  button {
    font-size: 1.1rem;
    padding: 14px 35px;
    background: #ff2d68;
    border: none;
    border-radius: 50px;
    color: #fff;
    cursor: pointer;
    font-weight: 600;
    text-shadow: 0 0 8px rgba(255, 255, 255, 0.7);
    transition: background 0.3s ease;
    box-shadow: 0 6px 15px rgba(255, 45, 104, 0.6);
    user-select: none;
  }

  button:hover, button:focus {
    background: #ff4a8a;
    outline: none;
  }

  .message {
    margin-top: 25px;
    font-size: 1.2rem;
    color: #fff4f8;
    text-shadow: 0 0 6px #ff7ba9;
    min-height: 60px;
    opacity: 0;
    transition: opacity 1.2s ease;
  }

  .message.visible {
    opacity: 1;
  }

  @media (max-width: 350px) {
    h1 {
      font-size: 2rem;
    }
    h2 {
      font-size: 1rem;
    }
    .heart {
      width: 70px;
      height: 64px;
    }
    button {
      padding: 12px 25px;
      font-size: 1rem;
    }
  }
</style>
</head>
<body>
  <div class="container" role="main" aria-label="Love message to girlfriend">
    <div class="heart" tabindex="0" aria-label="Heart icon"></div>
    <h1>I Love You</h1>
    <h2>Adekkkkk</h2>
    <button id="revealBtn" aria-pressed="false" aria-controls="secretMessage">Show Secret Message</button>
    <p id="secretMessage" class="message" aria-live="polite"></p>
  </div>

<script>
  const heart = document.querySelector('.heart');
  const button = document.getElementById('revealBtn');
  const message = document.getElementById('secretMessage');

  heart.addEventListener('click', () => {
    heart.classList.add('pulse');
    setTimeout(() => heart.classList.remove('pulse'), 600);
    revealMessage();
  });

  heart.addEventListener('keydown', (e) => {
    if (e.key === 'Enter' || e.key === ' ') {
      e.preventDefault();
      heart.classList.add('pulse');
      setTimeout(() => heart.classList.remove('pulse'), 600);
      revealMessage();
    }
  });

  function revealMessage() {
    if (!message.classList.contains('visible')) {
      message.textContent = "ABANG SAYANGGG ADEKKKK, WOP YU BANYAK BANYAKKK SAYANGGGG ❤️";
      message.classList.add('visible');
      button.setAttribute('aria-pressed', 'true');
    }
  }

  button.addEventListener('click', () => {
    revealMessage();
  });
</script>
</body>
</html>
</content>
</create_file>
