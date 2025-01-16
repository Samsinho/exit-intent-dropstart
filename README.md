<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Drop Start - Oferta Exclusiva</title>
  <style>
    /* Fontes */
    @font-face {
      font-family: 'CenturyGothic';
      src: url('https://fonts.cdnfonts.com/s/6033/CenturyGothic.woff') format('woff');
    }
    @font-face {
      font-family: 'Geometos';
      src: url('https://fonts.cdnfonts.com/s/19873/Geometos.woff') format('woff');
    }

    body {
      font-family: 'CenturyGothic', Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: #000; /* Fundo preto */
      color: #fff;
    }

    .container {
      text-align: center;
      padding: 20px;
    }

    h1 {
      font-family: 'CenturyGothic', sans-serif;
      font-size: 2.5rem;
      color: #fff;
      margin: 20px 0;
    }

    .highlight {
      color: #e74c3c; /* Vermelho vibrante */
      font-weight: bold;
    }

    .sub-highlight {
      color: #fff; /* Branco */
      font-weight: bold;
    }

    .product-name {
      color: #f0c808; /* Amarelo mostarda */
    }

    .discount-banner {
      background-color: #2ecc71; /* Verde para destacar */
      color: #000;
      padding: 10px;
      font-family: 'Geometos', sans-serif;
      font-size: 1.2rem;
      border-radius: 5px;
    }

    .pricing {
      margin: 30px 0;
      font-size: 1.5rem;
    }

    .pricing .original-price {
      text-decoration: line-through;
      color: #e74c3c; /* Vermelho para o preço original */
    }

    .pricing .discounted-price {
      color: #fff; /* Branco para o preço com desconto */
      font-size: 2rem;
      font-weight: bold;
    }

    .cta {
      margin: 20px 0;
    }

    .cta button {
      background-color: #00ff00; /* Verde florescente */
      color: #000; /* Letra preta */
      border: none;
      padding: 15px 30px;
      font-size: 1.2rem;
      font-family: 'CenturyGothic', sans-serif;
      cursor: pointer;
      border-radius: 5px;
      transition: background-color 0.3s;
    }

    .cta button:hover {
      background-color: #32cd32;
    }

    .countdown {
      margin: 20px 0;
      font-size: 1.2rem;
      font-weight: bold;
      color: #2ecc71;
    }

    footer {
      margin-top: 30px;
      font-size: 0.8rem;
      color: #888;
    }

    /* Botão Flutuante do WhatsApp */
    .whatsapp-float {
      position: fixed;
      bottom: 20px;
      right: 20px;
      width: 60px;
      height: 60px;
      background-color: #25d366;
      color: #fff;
      border-radius: 50%;
      display: flex;
      justify-content: center;
      align-items: center;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      cursor: pointer;
      transition: transform 0.3s ease;
    }

    .whatsapp-float:hover {
      transform: scale(1.1);
    }

    .whatsapp-float img {
      width: 35px;
      height: 35px;
    }
  </style>
</head>
<body>

  <div class="container">
    <div class="discount-banner">
      Você acabou de desbloquear um <span class="highlight">DESCONTÃO</span>! <br> 
      <span class="sub-highlight">Mas cuidado, é por tempo limitado. Até já!</span>
    </div>
    <h1><span class="product-name">Drop Start</span> - O Curso Que Vai Transformar Seu Futuro no Dropshipping!</h1>
    <p>Aprenda a gerar ganhos extraordinários começando do zero!</p>

    <div class="pricing">
      <p class="original-price">De: R$ 97,00</p>
      <p class="discounted-price">Por: R$ 67,00</p>
    </div>

    <div class="cta">
      <button onclick="buyNow()">Garantir Desconto</button>
    </div>

    <div class="countdown">
      Oferta termina em: <span id="countdown-timer">00:10:00</span>
    </div>
  </div>

  <footer>
    © 2025 - Todos os direitos reservados. Drop Start.
  </footer>

  <!-- Botão Flutuante do WhatsApp -->
  <div class="whatsapp-float" onclick="openWhatsApp()">
    <img src="https://cdn-icons-png.flaticon.com/512/733/733585.png" alt="WhatsApp">
  </div>

  <script>
    // Contador Regressivo
    const countdownTimer = document.getElementById('countdown-timer');

    // Data de término (10 minutos a partir de agora)
    const endTime = new Date().getTime() + 10 * 60 * 1000;

    function updateCountdown() {
      const now = new Date().getTime();
      const timeLeft = endTime - now;

      if (timeLeft > 0) {
        const minutes = Math.floor((timeLeft / (1000 * 60)) % 60);
        const seconds = Math.floor((timeLeft / 1000) % 60);

        countdownTimer.textContent = `${String(minutes).padStart(2, '0')}:${String(seconds).padStart(2, '0')}`;
      } else {
        countdownTimer.textContent = "Oferta Expirada!";
      }
    }

    setInterval(updateCountdown, 1000);

    // Redirecionar para o link de afiliado
    function buyNow() {
      alert('Você será redirecionado para garantir o desconto!');
      window.location.href = "https://pay.kiwify.com.br/SJ7OIfj?afid=I9ocoaJq";
    }

    // Abrir WhatsApp
    function openWhatsApp() {
      const phoneNumber = "5521965118341"; // Número com código do país (55)
      const message = "Olá, estou interessado no curso Drop Start!";
      window.open(`https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`, "_blank");
    }
  </script>

</body>
</html>
