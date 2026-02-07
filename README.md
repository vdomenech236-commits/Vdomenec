<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Question très importante</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: pink;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      text-align: center;
    }
    #box {
      background: white;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(0,0,0,0.2);
    }
    button {
      font-size: 20px;
      padding: 10px 25px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      background: #ff4d6d;
      color: white;
    }
    #love {
      display: none;
      font-size: 60px;
      color: red;
      font-weight: bold;
    }
  </style>
</head>
<body>

<div id="box">
  <h1>Tu veux être ma Saint-Valentin ? 💘</h1>
  <p id="message"></p>
  <button onclick="clickOui()">Oui 💖</button>
</div>

<div id="love">JE T’AIME ❤️</div>

<script>
  let clicks = 0;
  const messages = [
    "Erreur 404 : réponse trop parfaite 😅",
    "Oups… ça n’a pas marché 😳",
    "Encore un bug… bizarre 🤔",
    "Dernière tentative… 🙈"
  ];

  function clickOui() {
    clicks++;
    if (clicks < 5) {
      document.getElementById("message").innerText = messages[clicks - 1];
    } else {
      document.getElementById("box").style.display = "none";
      document.getElementById("love").style.display = "block";
    }
  }
</script>

</body>
</html>
