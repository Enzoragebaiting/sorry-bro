<!DOCTYPE html>
<html>
<head>
  <title>Ultimate Click Challenge</title>
  <style>
    body {
      background: black;
      color: white;
      font-family: Arial, sans-serif;
      text-align: center;
      overflow: hidden;
    }

    button {
      padding: 20px 40px;
      font-size: 20px;
      cursor: pointer;
      border: none;
      border-radius: 10px;
      transition: all 0.3s ease;
      position: absolute;
    }

    #mainBtn {
      background-color: #555;
      color: white;
      top: 40%;
      left: 45%;
    }

    #popup {
      position: fixed;
      top: 40%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 50px;
      display: none;
      text-align: center;
    }
  </style>
</head>
<body>

<button id="mainBtn">Click Me</button>
<div id="popup"></div>

<script>
  const btn = document.getElementById("mainBtn");
  const popup = document.getElementById("popup");

  let stage = 0;
  let growthClicks = 0;

  function randomPosition(button) {
    const x = Math.random() * (window.innerWidth - button.offsetWidth);
    const y = Math.random() * (window.innerHeight - button.offsetHeight);
    button.style.left = x + "px";
    button.style.top = y + "px";
  }

  btn.addEventListener("click", () => {

    if (stage === 0) {
      btn.innerText = "Click Harder";
      randomPosition(btn);
      stage++;
    } 
    
    else if (stage === 1) {
      btn.innerText = "You call that a click? Click again.";
      randomPosition(btn);
      stage++;
    } 
    
    else if (stage === 2) {
      btn.innerText = "Okay... that one had some effort.";
      btn.style.backgroundColor = "rgb(255,150,150)"; // light red
      btn.style.color = "white";
      randomPosition(btn);
      stage++;
    } 
    
    else if (stage === 3) {
      growthClicks++;

      // Grow size
      let size = 20 + growthClicks * 20;
      btn.style.padding = size + "px " + (size * 2) + "px";
      btn.style.fontSize = (20 + growthClicks * 8) + "px";

      // Phase messages + color progression
      if (growthClicks === 1) {
        btn.innerText = "Ohhh now we're warming up.";
        btn.style.backgroundColor = "rgb(255,90,90)"; // normal red
      } 
      else if (growthClicks === 2) {
        btn.innerText = "Bro is locked in for real.";
        btn.style.backgroundColor = "rgb(220,40,40)";
      } 
      else if (growthClicks === 3) {
        btn.innerText = "Why are you trying so hard 😭";
        btn.style.backgroundColor = "rgb(180,0,0)";
      } 
      else if (growthClicks >= 4) {
        btn.innerText = "IT'S NOT THAT DEEP 💀";
        btn.style.backgroundColor = "rgb(120,0,0)"; // aggressive red
        setTimeout(() => {
          btn.style.display = "none";
          startCountdown();
        }, 800);
      }

      randomPosition(btn);
    }
  });

  function startCountdown() {
    popup.style.display = "block";

    let messages = [
      "6...",
      "7...",
      "All that rage clicking just to prove absolutely nothing 💀"
    ];

    let index = 0;

    function nextMessage() {
      if (index < messages.length) {
        popup.innerText = messages[index];
        index++;
        setTimeout(nextMessage, 1000);
      }
    }

    nextMessage();
  }
</script>

</body>
</html>
