<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <title>Taschenrechner</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #222;
      color: white;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .calculator {
      background: #333;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px #000;
    }
    .display {
      background: black;
      color: lime;
      font-size: 2em;
      padding: 10px;
      margin-bottom: 10px;
      text-align: right;
      border-radius: 5px;
    }
    .buttons {
      display: grid;
      grid-template-columns: repeat(4, 60px);
      gap: 10px;
    }
    button {
      padding: 15px;
      font-size: 1.2em;
      background: #555;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background: #777;
    }
  </style>
</head>
<body>
  <div class="calculator">
    <div class="display" id="display">0</div>
    <div class="buttons">
      <button onclick="clearDisplay()">C</button>
      <button onclick="appendValue('/')">/</button>
      <button onclick="appendValue('*')">*</button>
      <button onclick="deleteLast()">⌫</button>

      <button onclick="appendValue('7')">7</button>
      <button onclick="appendValue('8')">8</button>
      <button onclick="appendValue('9')">9</button>
      <button onclick="appendValue('-')">-</button>

      <button onclick="appendValue('4')">4</button>
      <button onclick="appendValue('5')">5</button>
      <button onclick="appendValue('6')">6</button>
      <button onclick="appendValue('+')">+</button>

      <button onclick="appendValue('1')">1</button>
      <button onclick="appendValue('2')">2</button>
      <button onclick="appendValue('3')">3</button>
      <button onclick="calculate()">=</button>

      <button onclick="appendValue('0')" style="grid-column: span 2">0</button>
      <button onclick="appendValue('.')">.</button>
    </div>
  </div>

  <script>
    const display = document.getElementById('display');

    function appendValue(value) {
      if (display.textContent === "0") display.textContent = "";
      display.textContent += value;
    }

    function clearDisplay() {
      display.textContent = "0";
    }

    function deleteLast() {
      display.textContent = display.textContent.slice(0, -1) || "0";
    }

    function calculate() {
      try {
        display.textContent = eval(display.textContent);
      } catch {
        display.textContent = "Fehler";
      }
    }
  </script>
</body>
</html>
