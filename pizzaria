<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pizzaria Saborosa</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #fff5e6;
    }
    header {
      background-color: #d35400;
      color: white;
      padding: 20px;
      text-align: center;
    }
    main {
      padding: 20px;
    }
    .menu, .carrinho {
      margin-bottom: 30px;
    }
    .pizza {
      background-color: #ffe0b3;
      margin-bottom: 15px;
      padding: 15px;
      border-radius: 10px;
    }
    button {
      background-color: #e67e22;
      border: none;
      color: white;
      padding: 10px;
      margin-top: 10px;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background-color: #cf711f;
    }
    ul {
      list-style: none;
      padding: 0;
    }
  </style>
</head>
<body>

  <header>
    <h1>🍕 Pizzaria Saborosa</h1>
    <p>O melhor da pizza na sua casa!</p>
  </header>

  <main>
    <section class="menu">
      <h2>Cardápio</h2>
      <div class="pizza">
        <strong>Calabresa</strong><br>
        R$ 35,00<br>
        <button onclick="adicionarAoCarrinho('Calabresa', 35)">Adicionar</button>
      </div>
      <div class="pizza">
        <strong>Frango com Catupiry</strong><br>
        R$ 40,00<br>
        <button onclick="adicionarAoCarrinho('Frango com Catupiry', 40)">Adicionar</button>
      </div>
      <div class="pizza">
        <strong>Marguerita</strong><br>
        R$ 38,00<br>
        <button onclick="adicionarAoCarrinho('Marguerita', 38)">Adicionar</button>
      </div>
    </section>

    <section class="carrinho">
      <h2>Carrinho de Compras</h2>
      <ul id="lista-carrinho"></ul>
      <p><strong>Total:</strong> R$ <span id="total">0</span></p>
      <button onclick="finalizarPedido()">Finalizar Pedido</button>
      <p id="mensagem-pedido"></p>
    </section>
  </main>

  <script>
    let carrinho = [];
    let total = 0;

    function adicionarAoCarrinho(nome, preco) {
      carrinho.push({ nome, preco });
      total += preco;
      atualizarCarrinho();
    }

    function atualizarCarrinho() {
      const lista = document.getElementById("lista-carrinho");
      lista.innerHTML = "";
      carrinho.forEach(item => {
        const li = document.createElement("li");
        li.textContent = `${item.nome} - R$ ${item.preco}`;
        lista.appendChild(li);
      });
      document.getElementById("total").textContent = total;
    }

    function finalizarPedido() {
      if (carrinho.length === 0) {
        alert("Seu carrinho está vazio!");
        return;
      }
      const tempo = Math.floor(Math.random() * 20) + 20; // entre 20 e 40 minutos
      document.getElementById("mensagem-pedido").textContent = `Pedido confirmado! Tempo estimado de entrega: ${tempo} minutos.`;
      carrinho = [];
      total = 0;
      atualizarCarrinho();
    }
  </script>

</body>
</html>
