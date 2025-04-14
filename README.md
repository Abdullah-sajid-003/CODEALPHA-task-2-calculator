# CODEALPHA-task-2-calculator
task 2-calculator
<!-- calculator.html -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #333;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .calculator {
      background: #222;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 20px #000;
    }
    input {
      width: 100%;
      font-size: 2em;
      padding: 10px;
      text-align: right;
      margin-bottom: 10px;
    }
    button {
      width: 23%;
      padding: 15px;
      font-size: 1.2em;
      margin: 5px 1%;
      border: none;
      border-radius: 5px;
      background: #555;
      color: #fff;
      cursor: pointer;
    }
    button:hover {
      background: #777;
    }
  </style>
</head>
<body>
  <div class="calculator">
    <input type="text" id="result" readonly>
    <div>
      <button onclick="appendValue('7')">7</button>
      <button onclick="appendValue('8')">8</button>
      <button onclick="appendValue('9')">9</button>
      <button onclick="appendValue('/')">/</button>
      <br>
      <button onclick="appendValue('4')">4</button>
      <button onclick="appendValue('5')">5</button>
      <button onclick="appendValue('6')">6</button>
      <button onclick="appendValue('*')">*</button>
      <br>
      <button onclick="appendValue('1')">1</button>
      <button onclick="appendValue('2')">2</button>
      <button onclick="appendValue('3')">3</button>
      <button onclick="appendValue('-')">-</button>
      <br>
      <button onclick="appendValue('0')">0</button>
      <button onclick="appendValue('.')">.</button>
      <button onclick="calculate()">=</button>
      <button onclick="appendValue('+')">+</button>
      <br>
      <button onclick="clearResult()" style="width: 98%;">Clear</button>
    </div>
  </div>

  <script>
    function appendValue(value) {
      document.getElementById('result').value += value;
    }

    function calculate() {
      const resultField = document.getElementById('result');
      try {
        resultField.value = eval(resultField.value);
      } catch {
        resultField.value = 'Error';
      }
    }

    function clearResult() {
      document.getElementById('result').value = '';
    }
  </script>
</body>
</html>
