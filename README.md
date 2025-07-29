<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Countdown Timer</title>
  <style>
    body {
      background: #2c3e50;
      color: #ecf0f1;
      font-family: Arial, sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }

    h2 {
      margin-bottom: 10px;
    }

    input {
      padding: 10px;
      font-size: 16px;
      width: 150px;
      text-align: center;
      border-radius: 5px;
      border: none;
      margin-bottom: 15px;
    }

    button {
      padding: 10px 20px;
      font-size: 16px;
      background: #e67e22;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    .countdown {
      font-size: 48px;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <h2>Countdown Timer</h2>
  <input type="number" id="timeInput" placeholder="Enter seconds" />
  <button onclick="startCountdown()">Start</button>
  <div class="countdown" id="countdownDisplay">00</div>

  <script>
    let interval;

    function startCountdown() {
      clearInterval(interval);
      let time = parseInt(document.getElementById("timeInput").value);
      const display = document.getElementById("countdownDisplay");

      if (isNaN(time) || time < 1) {# Countdown-timer-
