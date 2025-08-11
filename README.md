<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Coffee Família - Lanchonete</title>
  <style>
    /* Reset básico */
    * {
      margin: 0; padding: 0; box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: #fff8f0;
      color: #4a2c14;
      min-height: 100vh;
    }

    header {
      background-color: #8B4513;
      color: white;
      padding: 15px 20px;
      position: fixed;
      width: 100%;
      top: 0;
      left: 0;
      z-index: 1000;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 2px 5px rgba(0,0,0,0.3);
    }

    header h1 {
      font-size: 1.6rem;
    }

    nav button {
      background: white;
      color: #8B4513;
      border: none;
      padding: 10px 18px;
      font-weight: bold;
      border-radius: 6px;
      cursor: pointer;
      transition: background-color 0.3s ease;
      margin-left: 10px;
    }

    nav button:hover {
      background-color: #d2b48c;
    }

    main {
      padding: 100px 20px 40px;
      max-width: 900px;
      margin: 0 auto;
    }

    section {
      margin-bottom: 40px;
    }

    .intro p {
      margin-top: 10px;
      line-height: 1.4;
      font-size: 1.1rem;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fill,minmax(240px,1fr));
      gap: 20px;
    }

    .card {
      background: white;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      overflow: hidden;
      transition: transform 0.3s ease;
    }

    .card:hover {
      transform: scale(1.05);
    }

    .card img {
      width: 100%;
      height: 160px;
      object-fit: cover;
    }

    .card-content {
      padding: 15px;
    }

    .card-content h3 {
      margin-bottom: 8px;
      color: #8B4513;
    }

    .card-content p {
      font-size: 0.9rem;
      margin-bottom: 5px;
    }

    .price {
      font-weight: bold;
      color: green;
      font-size: 1.1rem;
    }

    footer {
      background-color: #8B4513;
      color: white;
      text-align: center;
      padding: 15px 20px;
      margin-top: 50px;
    }

    /* Seções controladas via JS para mostrar/esconder */
    #inicio, #cardapio {
      display: none;
    }

    #inicio.active, #cardapio.active {
      display: block;
    }
  </style>
</head>
<body>

<header>
  <h1>☕ Coffee Família</h1>
  <nav>
    <button onclick="showSection('inicio')">Início</button>
    <button onclick="showSection('cardapio')">Cardápio</button>
  </nav>
</header>

<main>
  <section id="inicio" class="active intro">
    <h2>Bem-vindo à Coffee Família!</h2>
    <p>Estamos no mercado desde 2019. Começamos pequenos, sem lugar para sentar. Hoje temos cadeiras e um espaço aconchegante para você aproveitar seus cafés e salgados com conforto.</p>
    <p>Nosso compromisso é melhorar cada dia para atender você da melhor forma!</p>
  </section>

  <section id="cardapio">
    <h2>Nosso Cardápio</h2>
    <div class="cards">

      <div class="card">
        <img src="https://upload.wikimedia.org/wikipedia/commons/f/f2/Coxinha_de_frango.jpg" alt="Coxinha" />
        <div class="card-content">
          <h3>Coxinha</h3>
          <p>A coxinha que todo mundo ama!</p>
          <p class="price">R$ 1,50</p>
        </div>
      </div>

      <div class="card">
        <img src="https://upload.wikimedia.org/wikipedia/commons/2/25/Kibe_assado.jpg" alt="Kibe" />
        <div class="card-content">
          <h3>Kibe</h3>
          <p>Salgado crocante e saboroso.</p>
          <p class="price">R$ 2,00</p>
        </div>
      </div>

      <div class="card">
        <img src="https://upload.wikimedia.org/wikipedia/commons/6/69/Ris%C3%B3is.jpg" alt="Risoles" />
        <div class="card-content">
          <h3>Risoles</h3>
          <p>Delicioso e recheado.</p>
          <p class="price">R$ 2,00</p>
        </div>
      </div>

      <div class="card">
        <img src="https://upload.wikimedia.org/wikipedia/commons/2/25/Bauru.JPG" alt="Bauru" />
        <div class="card-content">
          <h3>Bauru</h3>
          <p>Lanche tradicional com queijo e presunto.</p>
          <p class="price">R$ 6,00</p>
        </div>
      </div>

      <div class="card">
        <img src="https://upload.wikimedia.org/wikipedia/commons/8/8a/Energy_drink_can.jpg" alt="Energético" />
        <div class="card-content">
          <h3>Energético</h3>
          <p>Para dar aquele gás!</p>
          <p class="price">R$ 7,00</p>
        </div>
      </div>

      <div class="card">
        <img src="https://upload.wikimedia.org/wikipedia/commons/f/f6/Assorted_candies.jpg" alt="Balas, doces e chocolates" />
        <div class="card-content">
          <h3>Balas, doces e chocolates</h3>
          <p>Para adoçar seu dia.</p>
          <p class="price">A partir de R$ 1,00</p>
        </div>
      </div>

      <div class="card">
        <img src="https://upload.wikimedia.org/wikipedia/commons/c/c6/Pastel_de_queijo.JPG" alt="Pastel" />
        <div class="card-content">
          <h3>Pastel</h3>
          <p>Crocante e recheado.</p>
          <p class="price">R$ 3,00</p>
        </div>
      </div>

      <div class="card">
        <img src="https://upload.wikimedia.org/wikipedia/commons/e/e8/X-Salada.jpg" alt="X-Salada" />
        <div class="card-content">
          <h3>X-Salada</h3>
          <p>Sanduíche completo e delicioso.</p>
          <p class="price">R$ 8,00</p>
        </div>
      </div>

    </div>
  </section>
</main>

<footer>
  <p>📍 Rua Exemplo, 123 - Sua Cidade</p>
  <p>📞 (00) 12345-6789</p>
  <p>&copy; 2025 Coffee Família</p>
</footer>

<script>
  function showSection(id) {
    document.getElementById('inicio').classList.remove('active');
    document.getElementById('cardapio').classList.remove('active');
    document.getElementById(id).classList.add('active');
  }
</script>

</body>
</html>
