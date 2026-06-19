<!DOCTYPE html>
<html lang="sv">
<head>
  <meta charset="UTF-8">
  <title>VM Tipset</title>
  <style>
    body {
      font-family: Arial;
      background: #0b1d3a;
      color: white;
      text-align: center;
      margin: 0;
      padding: 20px;
    }

    h1 {
      margin-top: 20px;
    }

    .match {
      background: #16335c;
      padding: 15px;
      margin: 10px auto;
      width: 90%;
      max-width: 500px;
      border-radius: 10px;
    }

    input {
      width: 60px;
      padding: 5px;
      text-align: center;
      margin: 5px;
      font-size: 16px;
    }

    button {
      margin-top: 20px;
      padding: 10px 20px;
      border: none;
      background: #ffcc00;
      font-weight: bold;
      cursor: pointer;
      border-radius: 8px;
    }

    #result {
      margin-top: 20px;
      font-size: 20px;
    }
  </style>
</head>

<body>

  <h1>⚽ VM Tipset</h1>
  <p>Tippa resultat med dina vänner</p>

  <div class="match">
    <p>Sverige vs Brasilien</p>
    <input type="number" id="swe1"> - 
    <input type="number" id="bra1">
  </div>

  <div class="match">
    <p>Frankrike vs Argentina</p>
    <input type="number" id="fra1"> - 
    <input type="number" id="arg1">
  </div>

  <div class="match">
    <p>Tyskland vs Spanien</p>
    <input type="number" id="ger1"> - 
    <input type="number" id="spa1">
  </div>

  <button onclick="checkTips()">Räkna poäng</button>

  <div id="result"></div>

  <script>
    function checkTips() {
      let score = 0;

      // Rätt svar (kan ändras)
      if (document.getElementById("swe1").value == 2 &&
          document.getElementById("bra1").value == 1) {
        score++;
      }

      if (document.getElementById("fra1").value == 1 &&
          document.getElementById("arg1").value == 1) {
        score++;
      }

      if (document.getElementById("ger1").value == 3 &&
          document.getElementById("spa1").value == 2) {
        score++;
      }

      document.getElementById("result").innerHTML =
        "Du fick " + score + " rätt!";
    }
  </script>

</body>
</html>
