<marquee behavior="scroll" direction="left">
  Scrolling Text
</marquee>
<div align="center">
  <h2>🎉 환영합니다! 🎉</h2>
  <img src="https://i.pinimg.com/originals/70/37/d4/7037d478852af21357f038fac2d2e9f6.gif" height="10%" width="100%">
</div>
![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![Version](https://img.shields.io/badge/version-1.0-blue)
<marquee behavior="scroll" direction="left">
  Scrolling Text
</marquee>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Text Animations</title>
  <style>
    /* 1. Color Changing Text */
    @keyframes colorChange {
      0% { color: red; }
      50% { color: blue; }
      100% { color: green; }
    }

    /* 2. Fading Text */
    @keyframes fadeInOut {
      0%, 100% { opacity: 0; }
      50% { opacity: 1; }
    }

    /* 3. Pulsing Text */
    @keyframes pulse {
      0%, 100% { font-size: 16px; }
      50% { font-size: 24px; }
    }

    /* 4. Shaking Text */
    @keyframes shake {
      0% { transform: translateX(0); }
      25% { transform: translateX(-5px); }
      50% { transform: translateX(5px); }
      75% { transform: translateX(-5px); }
      100% { transform: translateX(0); }
    }

    /* 5. Background Color Changing Box */
    @keyframes bgChange {
      0% { background-color: yellow; }
      50% { background-color: orange; }
      100% { background-color: pink; }
    }

    /* 6. Bouncing Text */
    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }

    /* 7. Rotating Text */
    @keyframes rotate {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }

    /* 8. Typing Effect */
    @keyframes typing {
      0% { width: 0; }
      100% { width: 100%; }
    }

    /* 9. Underline Blinking */
    @keyframes underlineBlink {
      0%, 100% { text-decoration-color: transparent; }
      50% { text-decoration-color: black; }
    }
  </style>
</head>
<body style="font-family: Arial, sans-serif; line-height: 2; padding: 20px;">

  <h2>1. Color Changing Text</h2>
  <span style="animation: colorChange 2s infinite; display: inline-block;">Color Changing Text</span>

  <h2>2. Fading Text</h2>
  <span style="animation: fadeInOut 3s infinite; display: inline-block;">Fading Text</span>

  <h2>3. Pulsing Text</h2>
  <span style="animation: pulse 2s infinite; display: inline-block;">Pulsing Text</span>

  <h2>4. Shaking Text</h2>
  <span style="animation: shake 0.5s infinite; display: inline-block;">Shaking Text</span>

  <h2>5. Background Color Changing Box</h2>
  <div style="animation: bgChange 2s infinite; padding: 10px; display: inline-block;">Background Changing Box</div>

  <h2>6. Bouncing Text</h2>
  <span style="animation: bounce 1.5s infinite; display: inline-block;">Bouncing Text</span>

  <h2>7. Rotating Text</h2>
  <span style="animation: rotate 2s infinite linear; display: inline-block;">Rotating Text</span>

  <h2>8. Typing Effect</h2>
  <span style="animation: typing 4s steps(10) infinite; overflow: hidden; white-space: nowrap; display: inline-block; width: 10ch; border-right: 2px solid black;">Typing Effect</span>

  <h2>9. Underline Blinking</h2>
  <span style="animation: underlineBlink 1s infinite; display: inline-block; text-decoration: underline;">Underline Blinking</span>

  <h2>10. Scrolling Text</h2>
  <marquee behavior="scroll" direction="left">Scrolling Text</marquee>

</body>
</html>
