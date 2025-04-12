<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Estimated Counter</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #111;
      color: #0f0;
      text-align: center;
      padding-top: 100px;
    }

    .counter {
      font-size: 4rem;
      margin: 20px;
    }

    .label {
      font-size: 1.2rem;
      color: #ccc;
    }
  </style>
</head>
<body>

  <div class="counter" id="counter">0</div>
  <div class="label">Estimated Views</div>

  <script>
    let currentCount = 1837100; // Starting number
    const counter = document.getElementById('counter');

    function updateCounter() {
      const increase = Math.floor(Math.random() * 4); // Random small increase
      currentCount += increase;
      counter.textContent = currentCount.toLocaleString();
    }

    // Update every 2 seconds
    setInterval(updateCounter, 2000);
  </script>

</body>
</html>
