<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Scary Website</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: black;
      overflow: hidden;
      font-family: 'Courier New', Courier, monospace;
    }

    /* Blood Overlay */
    .blood-overlay {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: url('https://cdn.pixabay.com/photo/2015/12/08/00/26/blood-1081814_1280.png') no-repeat center center; /* New blood splatter image */
      background-size: cover;
      opacity: 0.85;
      z-index: 1;
    }

    /* Main container */
    .container {
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      text-align: center;
      z-index: 3;
    }

    .container h1 {
      font-size: 4em;
      color: red;
      text-shadow: 0 0 10px red, 0 0 20px darkred, 0 0 30px black;
      animation: glow 1.5s infinite alternate;
    }

    @keyframes glow {
      0% {
        text-shadow: 0 0 10px red, 0 0 20px darkred;
      }
      100% {
        text-shadow: 0 0 20px red, 0 0 40px darkred, 0 0 50px black;
      }
    }

    button {
      background: black;
      color: red;
      border: 2px solid red;
      padding: 15px 30px;
      font-size: 1.5em;
      cursor: pointer;
      margin: 20px;
      text-shadow: 0 0 5px red;
      transition: all 0.3s ease;
    }

    button:hover {
      background: red;
      color: black;
      border: 2px solid black;
    }

    /* Scary Content */
    #scary-content {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: black;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      z-index: 5;
    }

    #scary-image {
      max-width: 100%;
      max-height: 100%;
    }
  </style>
</head>
<body>
  <!-- Blood overlay -->
  <div class="blood-overlay"></div>

  <!-- Question and buttons -->
  <div class="container">
    <h1 id="question-text">Would you like to proceed?</h1>
    <button id="yes-button">Yes</button>
    <button id="no-button">No</button>
  </div>

  <!-- Scary content -->
  <div id="scary-content">
    <img id="scary-image" src="https://preview.redd.it/i-need-help-i-accidentally-installed-a-virus-and-now-every-v0-bn5u1uq761ma1.jpg?width=1080&crop=smart&auto=webp&s=4fd20f4cb6b0ae01cf2c26d798f0797d702ebaef" alt="Scary Screamer">
    <audio id="scary-audio" src="https://www.soundjay.com/button/beep-07.wav"></audio>
  </div>

  <script>
    const yesButton = document.getElementById('yes-button');
    const noButton = document.getElementById('no-button');
    const scaryContent = document.getElementById('scary-content');
    const scaryAudio = document.getElementById('scary-audio');

    yesButton.addEventListener('click', () => {
      scaryContent.style.display = 'flex';
      scaryAudio.play();
    });

    noButton.addEventListener('click', () => {
      alert('Good choice!');
    });
  </script>
</body>
</html>
