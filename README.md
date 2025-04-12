<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Cookie Clicker</title>
  <style>
    body {
      background-color: #f3e5ab;
      font-family: 'Arial', sans-serif;
      text-align: center;
      padding: 50px;
    }
    h1 {
      color: #5d4037;
    }
    #cookie {
      width: 200px;
      cursor: pointer;
      transition: transform 0.1s;
    }
    #cookie:active {
      transform: scale(0.95);
    }
    #counter {
      font-size: 2em;
      margin: 20px 0;
    }
    .upgrade {
      background-color: #8d6e63;
      color: white;
      padding: 10px 20px;
      border: none;
      margin-top: 20px;
      cursor: pointer;
      border-radius: 5px;
    }
    .upgrade:hover {
      background-color: #a1887f;
    }
  </style>
</head>
<body>
  <h1>Cookie Clicker</h1>
  <img id="cookie" src="https://upload.wikimedia.org/wikipedia/commons/6/69/Chocolate_Chip_Cookie.png" alt="Cookie" />
  <div id="counter">Cookies: 0</div>
  <button class="upgrade" onclick="buyUpgrade()">Buy Auto-Click (Cost: 50)</button>

  <script>
    let cookies = 0;
    let autoClickers = 0;
    let upgradeCost = 50;

    const counter = document.getElementById("counter");
    const cookie = document.getElementById("cookie");

    cookie.onclick = () => {
      cookies++;
      updateCounter();
    };

    function updateCounter() {
      counter.textContent = `Cookies: ${cookies}`;
    }

    function buyUpgrade() {
      if (cookies >= upgradeCost) {
        cookies -= upgradeCost;
        autoClickers++;
        upgradeCost = Math.floor(upgradeCost * 1.5);
        setInterval(() => {
          cookies += autoClickers;
          updateCounter();
        }, 1000);
        updateCounter();
      } else {
        alert("Not enough cookies!");
      }
    }
  </script>
</body>
</html>
