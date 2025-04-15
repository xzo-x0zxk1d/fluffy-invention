<!DOCTYPE html>
<html>
<head>
  <title>WARNING: SYSTEM HACK</title>
  <style>
    body {
      background-color: black;
      color: red;
      font-family: 'Courier New', Courier, monospace;
      text-align: center;
      padding-top: 50px;
      margin: 0;
      height: 100vh;
      overflow: hidden;
    }

    .blood {
      font-size: 40px;
      color: red;
      text-shadow: 0 0 10px red, 0 0 20px red, 0 0 30px red;
    }

    h1 {
      font-size: 48px;
      color: red;
      text-transform: uppercase;
      letter-spacing: 10px;
      text-shadow: 0 0 10px red, 0 0 20px red;
    }

    .button {
      margin-top: 40px;
      padding: 20px 50px;
      font-size: 20px;
      background-color: red;
      color: white;
      border: 3px solid red;
      cursor: pointer;
      border-radius: 10px;
      font-weight: bold;
      text-transform: uppercase;
      box-shadow: 0 0 10px red;
    }

    .button:hover {
      background-color: darkred;
    }

    .no-button {
      margin-top: 40px;
      padding: 20px 50px;
      font-size: 20px;
      background-color: black;
      color: red;
      border: 3px solid red;
      cursor: pointer;
      border-radius: 10px;
      font-weight: bold;
      text-transform: uppercase;
      box-shadow: 0 0 10px red;
    }

    .no-button:hover {
      background-color: darkred;
    }

    #scaryImage {
      display: none;
      width: 100%;
      height: 100vh;
      object-fit: cover;
    }

  </style>
</head>
<body>

  <h1 class="blood">SYSTEM HACK DETECTED!</h1>
  <p class="blood">Are you sure you want to proceed?</p>

  <button class="button" onclick="proceed()">Yes</button>
  <button class="no-button" onclick="decline()">No</button>

  <!-- Scary Sound -->
  <audio id="scarySound" src="https://www.soundjay.com/button/beep-07.wav" preload="auto"></audio>

  <!-- Scary Image -->
  <img id="scaryImage" src="https://example.com/scary-image.jpg" alt="Scary Image" />

  <script>
    function proceed() {
      // Play scary sound
      var sound = document.getElementById('scarySound');
      sound.play();

      // Show scary image
      var image = document.getElementById('scaryImage');
      image.style.display = 'block';

      // Add a scary message after some time
      setTimeout(function() {
        document.body.innerHTML = "<h1 style='color: red;'>YOU'RE IN DANGER! SYSTEM BREACH DETECTED!</h1>";
        document.body.style.backgroundColor = 'black';
      }, 3000); // Show after 3 seconds
    }

    function decline() {
      alert("Nice try! But you can't escape the hack.");
    }
  </script>
</body>
</html>
