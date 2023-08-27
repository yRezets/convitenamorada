# TE amo vida!!!

<html>
<head>
<style>
  body {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    font-family: Arial, sans-serif;
  }

  #message {
    font-size: 24px;
    text-align: center;
    margin-bottom: 20px;
  }

  .button {
    padding: 10px 20px;
    background-color: #3498db;
    color: white;
    border: none;
    cursor: pointer;
    transition: 0.3s;
  }

  .button:hover {
    background-color: #2980b9;
  }
</style>
</head>
<body>
<div id="message">Vem dormir comigo vidinha?</div>
<button class="button" onclick="showResponse('Sim')">Sim</button>
<button class="button" onclick="moveButton()">Não</button>

<script>
function showResponse(response) {
  const messageDiv = document.getElementById('message');
  messageDiv.textContent = response === 'Sim' ? 'Te amo pra poha!' : 'Awww, pensa melhor 😢';
}

function moveButton() {
  const buttons = document.querySelectorAll('.button');
  buttons.forEach(button => {
    const maxX = window.innerWidth - button.offsetWidth;
    const maxY = window.innerHeight - button.offsetHeight;
    const newX = Math.random() * maxX;
    const newY = Math.random() * maxY;
    button.style.position = 'absolute';
    button.style.left = newX + 'px';
    button.style.top = newY + 'px';
  });
}
</script>
</body>
</html>
