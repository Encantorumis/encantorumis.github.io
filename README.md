<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Encantorumis - Loja de Amigurumis</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #fff7fc;
      color: #333;
    }
    header {
      background: #ff8ac9;
      padding: 20px;
      text-align: center;
      color: white;
      font-size: 24px;
      font-weight: bold;
    }
    .container {
      padding: 20px;
      max-width: 1000px;
      margin: auto;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 20px;
    }
    .card {
      background: white;
      padding: 15px;
      border-radius: 12px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
      text-align: center;
      transition: 0.3s;
    }
    .card:hover {
      transform: translateY(-5px);
      box-shadow: 0 4px 18px rgba(0,0,0,0.15);
    }
    .card img {
      width: 100%;
      border-radius: 10px;
    }
    .btn {
      display: inline-block;
      margin-top: 10px;
      padding: 10px 15px;
      background: #ff66b3;
      color: white;
      border-radius: 8px;
      text-decoration: none;
      font-weight: bold;
      transition: 0.3s;
    }
    .btn:hover {
      background: #ff3d9e;
    }
  </style>
</head>
<body>

<header>Encantorumis ✨</header>

<div class="container">
  <h2>Nossos Amigurumis</h2>
  <div id="produtos" class="grid"></div>
</div>

<script>
  const produtos = [
    {
      nome: "Hogi Amigurumi",
      preço: "R$ 85,00",
      img: "https://encantorumis.github.io/imagens/hogi.jpg",
      mensagem: "Olá! Tenho interesse no amigurumi Hogi."
    },
    {
      nome: "Baby Shark",
      preço: "R$ 75,00",
      img: "https://encantorumis.github.io/imagens/shark.jpg",
      mensagem: "Quero saber mais sobre o Baby Shark amigurumi."
    }
  ];

  const lista = document.getElementById("produtos");

  produtos.forEach(p => {
    const card = document.createElement("div");
    card.className = "card";

    card.innerHTML = `
      <img src="${p.img}" alt="${p.nome}" />
      <h3>${p.nome}</h3>
      <p><strong>${p.preco}</strong></p>
      <a class="btn" href="https://wa.me/55SEUNUMERO?text=${encodeURIComponent(p.mensagem)}" target="_blank">Comprar pelo WhatsApp</a>
    `;

    lista.appendChild(card);
  });
</script>

</body>
</html>
