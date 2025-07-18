

<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Delicias al Horno</title>
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Quicksand:wght@400;600&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      font-family: 'Quicksand', sans-serif;
      margin: 0;
      background: url('https://www.transparenttextures.com/patterns/cream-dust.png');
      color: #4b2e2e;
    }

    header {
      background: linear-gradient(135deg, #fcd5ae, #f8b878);
      text-align: center;
      padding: 50px 20px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    header::after {
      content: '🥐 🧁 🍞 🎂 🥖';
      display: block;
      font-size: 2rem;
      margin-top: 15px;
      animation: float 3s infinite alternate ease-in-out;
    }

    @keyframes float {
      0% { transform: translateY(0); }
      100% { transform: translateY(-8px); }
    }

    header h1 {
      font-family: 'Pacifico', cursive;
      font-size: 3.5em;
      color: #5e3c2d;
      margin: 0;
      text-shadow: 1px 1px #fff;
    }

    .slogan {
      font-style: italic;
      color: #7b4b3a;
      font-size: 1.2em;
      margin-top: 10px;
    }

    .productos {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 30px;
      padding: 50px 40px;
      background: rgba(255, 243, 230, 0.9);
    }

    .producto {
      background-color: #fff;
      border-radius: 15px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.08);
      overflow: hidden;
      transform: translateY(50px);
      opacity: 0;
      animation: fadeInUp 0.7s ease-out forwards;
    }

    .producto:nth-child(odd) {
      animation-delay: 0.2s;
    }

    .producto:nth-child(even) {
      animation-delay: 0.4s;
    }

    @keyframes fadeInUp {
      to {
        transform: translateY(0);
        opacity: 1;
      }
    }

    .producto img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-bottom: 2px solid #f8b878;
    }

    .producto h3 {
      font-size: 1.4em;
      margin: 15px 0;
      color: #3b221a;
      text-align: center;
    }

    footer {
      background: #fbe2c6;
      text-align: center;
      padding: 40px 20px;
      margin-top: 50px;
      border-top: 5px dotted #f7b97b;
    }

    footer h2 {
      margin-bottom: 15px;
      color: #6a3e2b;
    }

    .pago {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
      margin-bottom: 10px;
    }

    .pago img {
      width: 70px;
      height: auto;
      border-radius: 10px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
    }

    .cuenta {
      font-weight: bold;
      color: #4b2e2e;
      font-size: 1.2em;
    }

    .whatsapp {
      display: inline-block;
      margin-top: 20px;
      padding: 12px 20px;
      background-color: #25D366;
      color: white;
      border-radius: 30px;
      text-decoration: none;
      font-weight: bold;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      transition: background-color 0.3s ease;
    }

    .whatsapp:hover {
      background-color: #1ebe5d;
    }

    /* Botón flotante de WhatsApp */
    .whatsapp-float {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background-color: #25D366;
      color: white;
      border-radius: 50%;
      width: 60px;
      height: 60px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 30px;
      text-decoration: none;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
      z-index: 999;
      animation: pulse 2s infinite;
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.1); }
      100% { transform: scale(1); }
    }
  </style>
</head>
<body>

  <header>
    <h1>Delicias al Horno</h1>
    <div class="slogan">Sabores que abrazan el alma 🍞🍪</div>
  </header>

  <section class="productos">
    <div class="producto">
      <img src="https://i.ytimg.com/vi/YemrtxNl0TY/maxresdefault.jpg" alt="Hojaldra">
      <h3>Hojaldra</h3>
    </div>
    <div class="producto">
      <img src="https://static.wixstatic.com/media/0f7489_0b1e3a150e8448a195acfb554891b038~mv2.png" alt="Brazo de Reina">
      <h3>Brazo de Reina</h3>
    </div>
    <div class="producto">
      <img src="https://elsuper.com.co/rails/active_storage/blobs/proxy/eyJfcmFpbHMiOnsiZGF0YSI6MTgxNjc5MiwicHVyIjoiYmxvYl9pZCJ9fQ==--d443c83fe61b87216ec7390dec299733f2107567/29630?locale=es" alt="Pan Cascarita">
      <h3>Pan Cascarita</h3>
    </div>
    <div class="producto">
      <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQf8yU-VgDj-_ZQ8-x68Owj4hoGZyh5huk9KA&s" alt="Pan de Queso">
      <h3>Pan de Queso</h3>
    </div>
    <div class="producto">
      <img src="https://i.ytimg.com/vi/nPWVdJtrWVY/sddefault.jpg" alt="Mantecadas">
      <h3>Mantecadas</h3>
    </div>
    <div class="producto">
      <img src="https://i.ytimg.com/vi/rJHfRo-c6Qc/mqdefault.jpg" alt="Galletas Punta de Chocolate">
      <h3>Galletas de Punta de Chocolate</h3>
    </div>
    <div class="producto">
      <img src="https://lasdeliciasdevivir.net/wp-content/uploads/2011/05/Galletas-Ajedrez-Chocolate-Receta-Las-Delicias-Del-Buen-Vivir.jpg" alt="Galleta de Ajedrez">
      <h3>Galleta de Ajedrez</h3>
    </div>
  </section>

  <footer>
    <h2>💳 Métodos de Pago</h2>
    <div class="pago">
      <img src="https://files.lafm.com.co/assets/public/styles/twitter/public/2021-12/fallas_en_nequi_1_0.jpg.webp?itok=XmL8l2bk" alt="Nequi Logo">
      <span class="cuenta">Cuenta Nequi: 313 453 4612</span>
    </div>
    <a href="https://wa.me/573134534612" class="whatsapp" target="_blank">📲 Hacer pedido por WhatsApp</a>
    <p style="margin-top: 20px;">¡Gracias por preferir nuestras delicias! 🧁</p>
  </footer>

  <a href="https://wa.me/573134534612" class="whatsapp-float" target="_blank" title="Haz tu pedido por WhatsApp">💬</a>

</body>
</html>
