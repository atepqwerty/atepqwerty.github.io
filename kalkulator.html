<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no" />
<title>Modern Kalkulator</title>
<style>
  /* Reset and base */
  * {
    box-sizing: border-box;
  }
  body {
    margin: 0;
    background: #121212;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    color: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    padding: 10px;
  }
  #calculator {
    background: #212121;
    border-radius: 15px;
    box-shadow: 0 8px 20px rgba(0,0,0,0.6);
    width: 350px;
    max-width: 100%;
    height: 600px;
    display: flex;
    flex-direction: column;
    padding: 20px;
  }
  #display {
    background: #000;
    color: #0f0;
    font-size: 3rem;
    text-align: right;
    padding: 20px 15px;
    border-radius: 12px;
    margin-bottom: 20px;
    user-select: none;
    overflow-wrap: break-word;
    min-height: 70px;
    line-height: 1.1;
    font-weight: 700;
    font-family: 'Consolas', 'Courier New', monospace;
  }
  .button-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-gap: 15px;
    flex-grow: 1;
  }
  button {
    background: #333;
    color: #eee;
    font-size: 1.8rem;
    border: none;
    border-radius: 12px;
    box-shadow: 0 4px #111;
    transition: background 0.2s;
    cursor: pointer;
    user-select: none;
    touch-action: manipulation;
  }
  button:active {
    box-shadow: none;
    transform: translateY(2px);
  }
  button.operator {
    background: #ff9500;
    color: #fff;
    font-weight: 700;
    box-shadow: 0 4px #cc7a00;
  }
  button.operator:active {
    box-shadow: none;
    background: #cc7a00;
  }
  button.span-two {
    grid-column: span 2;
  }
  @media (max-width: 380px) {
    #calculator {
      width: 100%;
      height: 100%;
      padding: 15px;
    }
    #display {
      font-size: 2.4rem;
      padding: 15px 10px;
      min-height: 55px;
    }
    button {
      font-size: 1.4rem;
    }
  }
</style>
</head>
<body>
<div id="calculator" role="application" aria-label="Calculator">
  <div id="display" aria-live="polite" aria-atomic="true">0</div>
  <div class="button-grid">
    <button type="button" class="operator" data-action="clear" aria-label="Clear">C</button>
    <button type="button" class="operator" data-action="delete" aria-label="Delete">⌫</button>
    <button type="button" class="operator" data-action="percent" aria-label="Percent">%</button>
    <button type="button" class="operator" data-action="divide" aria-label="Divide">÷</button>

    <button type="button" data-number="7">7</button>
    <button type="button" data-number="8">8</button>
    <button type="button" data-number="9">9</button>
    <button type="button" class="operator" data-action="multiply" aria-label="Multiply">×</button>

    <button type="button" data-number="4">4</button>
    <button type="button" data-number="5">5</button>
    <button type="button" data-number="6">6</button>
    <button type="button" class="operator" data-action="subtract" aria-label="Subtract">−</button>

    <button type="button" data-number="1">1</button>
    <button type="button" data-number="2">2</button>
    <button type="button" data-number="3">3</button>
    <button type="button" class="operator" data-action="add" aria-label="Add">+</button>

    <button type="button" data-number="0" class="span-two">0</button>
    <button type="button" data-number=".">.</button>
    <button type="button" class="operator" data-action="equals" aria-label="Equals">=</button>
  </div>
</div>
<script>
  (() => {
    const display = document.getElementById('display');
    let currentInput = '0';
    let previousInput = null;
    let operation = null;
    let resetNext = false;

    function updateDisplay() {
      display.textContent = currentInput;
    }

    function clearAll() {
      currentInput = '0';
      previousInput = null;
      operation = null;
      resetNext = false;
      updateDisplay();
    }

    function deleteLast() {
      if (resetNext) {
        clearAll();
        return;
      }
      if (currentInput.length === 1 || (currentInput.length === 2 && currentInput.startsWith('-'))) {
        currentInput = '0';
      } else {
        currentInput = currentInput.slice(0, -1);
      }
      updateDisplay();
    }

    function appendNumber(num) {
      if (resetNext) {
        currentInput = '0';
        resetNext = false;
      }
      if (num === '.' && currentInput.includes('.')) return;
      if (currentInput === '0' && num !== '.') {
        currentInput = num;
      } else {
        currentInput += num;
      }
      updateDisplay();
    }

    function chooseOperation(op) {
      if (operation !== null) {
        compute();
      }
      previousInput = currentInput;
      operation = op;
      resetNext = true;
    }

    function compute() {
      let prev = parseFloat(previousInput);
      let current = parseFloat(currentInput);
      if (isNaN(prev) || isNaN(current)) return;
      let result = 0;
      switch(operation) {
        case 'add':
          result = prev + current;
          break;
        case 'subtract':
          result = prev - current;
          break;
        case 'multiply':
          result = prev * current;
          break;
        case 'divide':
          if (current === 0) {
            alert('Error: Division by zero');
            clearAll();
            return;
          }
          result = prev / current;
          break;
        case 'percent':
          // Percent of previous input: previous * (current / 100)
          result = prev * (current / 100);
          break;
        default:
          return;
      }
      currentInput = result.toString();
      operation = null;
      previousInput = null;
      resetNext = true;
      updateDisplay();
    }

    function handleButton(e) {
      const target = e.target;
      if (!target.matches('button')) return;

      if (target.dataset.number !== undefined) {
        appendNumber(target.dataset.number);
      } else if (target.dataset.action) {
        switch(target.dataset.action) {
          case 'clear': clearAll(); break;
          case 'delete': deleteLast(); break;
          case 'add': chooseOperation('add'); break;
          case 'subtract': chooseOperation('subtract'); break;
          case 'multiply': chooseOperation('multiply'); break;
          case 'divide': chooseOperation('divide'); break;
          case 'percent':
            // Apply percent operation immediately on current input by itself
            currentInput = (parseFloat(currentInput) / 100).toString();
            updateDisplay();
            break;
          case 'equals': compute(); break;
        }
      }
    }

    function handleKey(e) {
      const key = e.key;
      if ((/[0-9.]/).test(key)) {
        appendNumber(key);
      } else if (key === '+' || key === 'Add') {
        chooseOperation('add');
      } else if (key === '-' || key === 'Subtract') {
        chooseOperation('subtract');
      } else if (key === '*' || key === 'Multiply' || key === 'x' || key === 'X') {
        chooseOperation('multiply');
      } else if (key === '/' || key === 'Divide') {
        chooseOperation('divide');
      } else if (key === 'Enter' || key === '=') {
        e.preventDefault();
        compute();
      } else if (key === 'Backspace') {
        deleteLast();
      } else if (key === 'Escape') {
        clearAll();
      }
    }

    document.querySelector('.button-grid').addEventListener('click', handleButton);
    window.addEventListener('keydown', handleKey);

    clearAll();
  })();
</script>
</body>
</html>
</content>
</create_file>
