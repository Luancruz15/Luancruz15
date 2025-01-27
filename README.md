<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Apresentação do Luan</title>
  <style>
    body {
      background-color: #121212;
      color: #fff;
      font-family: Arial, sans-serif;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
      text-align: center;
      padding: 10px;
    }
    #text {
      font-size: 2rem;
      white-space: pre-wrap;
      overflow: hidden;
      border-right: 2px solid #fff;
      width: 100%; /* Ajustei para ocupar toda a largura */
      max-width: 600px;
      margin-bottom: 20px;
      animation: typing 4s steps(40, end), blink 0.7s step-end infinite;
    }
    #stats {
      margin-top: 20px;
      width: 100%;
      max-width: 600px;
    }
    table {
      width: 100%;
      border-collapse: collapse;
      margin: 20px 0;
    }
    table, th, td {
      border: 1px solid #fff;
    }
    th, td {
      padding: 10px;
      text-align: left;
    }
    .badge {
      display: inline-block;
      padding: 5px 10px;
      border-radius: 5px;
      margin: 5px;
      font-size: 1rem;
    }
    hr {
      border: 1px solid #fff;
      width: 80%;
      margin: 20px auto;
    }
    @keyframes typing {
      from {
        width: 0;
      }
      to {
        width: 100%;
      }
    }
    @keyframes blink {
      from {
        border-color: transparent;
      }
      to {
        border-color: white;
      }
    }
  </style>
</head>
<body>
  <div id="text"></div>
  <script>
    const text = `Eu sou o Luan
Apaixonado por programação e cibersegurança
Adoro resolver problemas e aprender novas tecnologias!`;
    let i = 0;

    function typeWriter() {
      if (i < text.length) {
        document.getElementById("text").innerHTML += text.charAt(i);
        i++;
        setTimeout(typeWriter, 50);
      }
    }

    typeWriter();
  </script>

  <div id="stats">
    <h3>🌐 Apaixonado por programação e cibersegurança</h3>
    <hr>
    <h3>🔍 Luan's GitHub Stats</h3>
    <table>
      <tr>
        <th>Métrica</th>
        <th>Valor</th>
      </tr>
      <tr>
        <td>Total de Stars</td>
        <td>203</td>
      </tr>
      <tr>
        <td>Total de Commits (2025)</td>
        <td>925</td>
      </tr>
      <tr>
        <td>Total de PRs</td>
        <td>2</td>
      </tr>
      <tr>
        <td>Total de Issues</td>
        <td>1</td>
      </tr>
      <tr>
        <td>Contribuições (último ano)</td>
        <td>0</td>
      </tr>
    </table>

    <h3>🛠️ Linguagens Mais Usadas</h3>
    <div>
      <span class="badge" style="background-color: red;">Java: 40%</span>
      <span class="badge" style="background-color: yellow;">JavaScript: 27.41%</span>
      <span class="badge" style="background-color: orange;">HTML: 23.01%</span>
      <span class="badge" style="background-color: blue;">Python: 19.56%</span>
      <span class="badge" style="background-color: purple;">CSS: 15.46%</span>
      <span class="badge" style="background-color: darkgreen;">Cibersegurança: 20%</span>
    </div>
  </div>

  <div>
    <h3>🚀 Vamos conectar?</h3>
    <a href="https://github.com/seu-username" target="_blank">
      <img src="https://img.shields.io/badge/-GitHub-black?style=for-the-badge&logo=github" alt="GitHub">
    </a>
    <a href="https://www.linkedin.com/in/seu-linkedin" target="_blank">
      <img src="https://img.shields.io/badge/-LinkedIn-blue?style=for-the-badge&logo=linkedin" alt="LinkedIn">
    </a>
  </div>
</body>
</html>
