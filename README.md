<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lacuher Personalizado</title>
<style>
  body {
    font-family: Arial, sans-serif;
    text-align: center;
  }
  .container {
    background-image: url('https://i.imgur.com/X03ikPQ.png'); /* Substitua pelo caminho da sua imagem */
    background-size: cover;
    background-position: center;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: #fff;
  }
  .welcome-text {
    font-size: 2em;
    margin-bottom: 20px;
  }
  .site-button {
    display: block;
    margin: 10px auto;
    padding: 10px 20px;
    font-size: 1em;
    text-decoration: none;
    color: #fff;
    border-radius: 5px;
  }
</style>
</head>
<body>
<div class="container">
  <h1 class="welcome-text">Seja Bem vindo Gabs</h1>
  <a href="https:computecnica.desk.ms" class="site-button" style="background-color: rgb(255, 0, 0)">Desk</a>
  <a href="https://computecnica.callbox.com.br" class="site-button" style="background-color: rgb(0, 255, 0)">Callbox</a>
  <a href="https://utils-n1.netlify.app" class="site-button" style="background-color: rgb(0, 0, 255)">Utils</a>
  <div id="clock"></div>
</div>

<script>
function updateClock() {
  var now = new Date();
  var brasiliaTime = new Date(now.toLocaleString('en-US', {timeZone: 'America/Sao_Paulo'}));

  var hours = brasiliaTime.getHours().toString().padStart(2, '0');
  var minutes = brasiliaTime.getMinutes().toString().padStart(2, '0');
  var seconds = brasiliaTime.getSeconds().toString().padStart(2, '0');

  var timeString = hours + ':' + minutes + ':' + seconds;
  document.getElementById('clock').innerHTML = 'Horário de Brasília: ' + timeString;

  setTimeout(updateClock, 1000);
}

setTimeout(function() {
  updateClock();
  document.body.style.transition = 'background 2s';
  document.body.style.background = 'rgba(0, 0, 0, 0.5)';
}, 2000);
</script>
</body>
</html>
