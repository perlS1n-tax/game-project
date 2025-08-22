<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Rock Paper Scissors Game</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background: #f0f8ff;
      padding: 50px;
    }
    h1 {
      color: #333;
    }
    .choices {
      margin: 20px;
    }
    button {
      padding: 15px 25px;
      margin: 10px;
      font-size: 18px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      background: #87ceeb;
      transition: 0.2s;
    }
    button:hover {
      background: #4682b4;
      color: #fff;
    }
    #result {
      margin-top: 30px;
      font-size: 22px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>Rock ✊ Paper ✋ Scissors ✌️</h1>
  <div class="choices">
    <button onclick="play('rock')">✊ Rock</button>
    <button onclick="play('paper')">✋ Paper</button>
    <button onclick="play('scissors')">✌️ Scissors</button>
  </div>
  <div id="result">Make your choice!</div>

  <script>
    function play(userChoice) {
      const choices = ["rock", "paper", "scissors"];
      const computerChoice = choices[Math.floor(Math.random() * 3)];
      let result = "";

      if (userChoice === computerChoice) {
        result = "It's a draw! 🤝 (Computer chose " + computerChoice + ")";
      } else if (
        (userChoice === "rock" && computerChoice === "scissors") ||
        (userChoice === "paper" && computerChoice === "rock") ||
        (userChoice === "scissors" && computerChoice === "paper")
      ) {
        result = "You win! 🎉 (Computer chose " + computerChoice + ")";
      } else {
        result = "You lose! 😭 (Computer chose " + computerChoice + ")";
      }

      document.getElementById("result").innerHTML = result;
    }
  </script>
</body>
</html>
