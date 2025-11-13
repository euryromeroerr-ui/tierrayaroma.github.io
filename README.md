<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Tierra y Aroma | Jabones Artesanales</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
  <style>
    /* --- Estilos generales --- */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }
    :root {
      --tierra: #8d7b68;
      --verde: #5e7d55;
      --crema: #f8f4ed;
      --fondo: #fdfcf8;
    }
    body {
      background-color: var(--fondo);
      color: #333;
      line-height: 1.6;
    }
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }

    /* --- Header --- */
    header {
      background-color: white;
      box-shadow: 0 2px 10px rgba(0,0,0,0.08);
      position: fixed;
      width: 100%;
      top: 0;
      z-index: 1000;
    }
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 0;
    }
    .logo {
      font-size: 1.8rem;
      font-weight: 800;
      color: var(--verde);
      letter-spacing: 1px;
    }
    .logo span {
      color: var(--tierra);
    }
    .nav-links {
      display: flex;
      gap: 25px;
    }
    .nav-links a {
      text-decoration: none;
      color: #555;
      font-weight: 500;
      transition: color 0.3s;
    }
    .nav-links a:hover {
      color: var(--verde);
    }

    /* --- Hero --- */
    .hero {
      background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), url('https://images.unsplash.com/photo-1613991583446-26e107e8e288?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=80') center/cover no-repeat;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: white;
      margin-top: 70px;
    }
    .hero h1 {
      font-size: 3rem;
      margin-bottom: 20px;
      font-weight: 800;
    }
    .hero p {
      font-size: 1.3rem;
      max-width: 700px;
      margin-bottom: 30px;
      font-weight: 300;
    }
    .btn {
      background-color: var(--tierra);
      color: white;
      padding: 14px 36px;
      border-radius: 50px;
      text-decoration: none;
      font-weight: bold;
      font-size: 1.1rem;
      transition: all 0.3s ease;
      box-shadow: 0 4px 15px rgba(141, 123, 104, 0.3);
    }
    .btn:hover {
      background-color: var(--verde);
      transform: translateY(-3px);
    }

    /* --- Secciones --- */
    section {
      padding: 80px 0;
    }
    .section-title {
      text-align: center;
      font-size: 2.4rem;
      margin-bottom: 50px;
      color: var(--tierra);
      font-weight: 700;
    }

    /* --- Sobre mí --- */
    .sobre {
      background-color: white;
    }
    .sobre-content {
      display: flex;
      gap: 40px;
      align-items: center;
    }
    .sobre-text h3 {
      color: var(--verde);
      margin-bottom: 15px;
      font-size: 1.6rem;
    }
    .sobre-text p {
      margin-bottom: 15px;
    }
    .sobre-img {
      flex: 1;
      height: 400px;
      background: linear-gradient(135deg, var(--crema), #e9e2d5);
      border-radius: 15px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.2rem;
      color: var(--tierra);
    }

    /* --- Productos --- */
    .productos {
      background-color: var(--crema);
    }
    .productos-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 30px;
    }
    .producto {
      background: white;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 6px 15px rgba(0,0,0,0.08);
      transition: all 0.4s ease;
    }
    .producto:hover {
      transform: translateY(-10px);
      box-shadow: 0 12px 25px rgba(0,0,0,0.12);
    }
    .producto-img {
      height: 220px;
      background: #e6dfd0;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--tierra);
      font-weight: bold;
    }
    .producto-info {
      padding: 25px;
    }
    .producto h3 {
      color: var(--tierra);
      margin-bottom: 10px;
      font-size: 1.4rem;
    }
    .producto p {
      color: #555;
      margin-bottom: 12px;
    }
    .precio {
      font-weight: bold;
      color: var(--verde);
      font-size: 1.2rem;
    }

    /* --- Contacto --- */
    .contacto {
      text-align: center;
    }
    .contacto p {
      max-width: 700px;
      margin: 0 auto 30px;
      font-size: 1.1rem;
    }
    .redes {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-top: 20px;
    }
    .redes a {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 56px;
      height: 56px;
      background: var(--tierra);
      border-radius: 50%;
      color: white;
      font-size: 1.4rem;
      text-decoration: none;
      transition: all 0.3s;
    }
    .redes a:hover {
      background: var(--verde);
      transform: scale(1.1);
    }

    /* --- Botón flotante de WhatsApp --- */
    .whatsapp-float {
      position: fixed;
      width: 60px;
      height: 60px;
      bottom: 30px;
      right: 30px;
      background-color: #25D366;
      color: white;
      border-radius: 50px;
      text-align: center;
      box-shadow: 0 4px 15px rgba(37, 211, 102, 0.4);
      z-index: 999;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.8rem;
      text-decoration: none;
      transition: all 0.3s;
    }
    .whatsapp-float:hover {
      transform: scale(1.1);
      background-color: #128C7E;
    }

    /* --- Footer --- */
    footer {
      background: var(--tierra);
      color: white;
      text-align: center;
      padding: 25px 0;
      font-size: 0.95rem;
    }
    footer a {
      color: #e0d6c5;
      text-decoration: underline;
    }

    /* --- Responsive --- */
    @media (max-width: 768px) {
      .sobre-content {
        flex-direction: column;
      }
      .hero h1 {
        font-size: 2.3rem;
      }
      .section-title {
        font-size: 2rem;
      }
      nav {
        flex-direction: column;
        gap: 15px;
      }
    }
  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <div class="container">
      <nav>
        <div class="logo">Tierra <span>&</span> Aroma</div>
        <div class="nav-links">
          <a href="#inicio">Inicio</a>
          <a href="#productos">Jabones</a>
          <a href="#sobre">Sobre mí</a>
          <a href="#contacto">Contacto</a>
        </div>
      </nav>
    </div>
  </header>

  <!-- Hero -->
  <section id="inicio" class="hero">
    <h1>Tierra y Aroma</h1>
    <p>Jabones artesanales hechos a mano con ingredientes naturales, respetando tu piel y el planeta.</p>
    <a href="#productos" class="btn">Conoce nuestros jabones</a>
  </section>

  <!-- Sobre mí -->
  <section id="sobre" class="sobre">
    <div class="container">
      <h2 class="section-title">De la tierra, para ti</h2>
      <div class="sobre-content">
        <div class="sobre-text">
          <h3>Con raíces en lo natural 🌱</h3>
          <p>Hola, soy [Tu Nombre], artesana detrás de <strong>Tierra y Aroma</strong>.</p>
          <p>Cada jabón nace de una receta pensada con cuidado: aceite de oliva virgen, manteca de karité, arcillas naturales, hierbas secas y aceites esenciales puros.</p>
          <p>Lo hacemos en frío, para preservar las propiedades benéficas de cada ingrediente. Sin sulfatos, parabenos ni colorantes artificiales.</p>
          <p>📦 Embalaje sostenible | 🐇 No testeado en animales | 🌿 Vegano</p>
        </div>
        <div class="sobre-img">
          ✨ Hecho con amor en [Tu Ciudad]
        </div>
      </div>
    </div>
  </section>

  <!-- Productos -->
  <section id="productos" class="productos">
    <div class="container">
      <h2 class="section-title">Nuestros Jabones</h2>
      <div class="productos-grid">
        <div class="producto">
          <div class="producto-img">🌿 Lavanda + Avena</div>
          <div class="producto-info">
            <h3>Calma Profunda</h3>
            <p>Para pieles sensibles. Avena fina exfolia suavemente; lavanda relaja cuerpo y mente.</p>
            <p class="precio">$1.800</p>
          </div>
        </div>
        <div class="producto">
          <div class="producto-img">🍋 Limón + Romero</div>
          <div class="producto-info">
            <h3>Brillo Natural</h3>
            <p>Refrescante y energizante. Ideal para pieles grasas o mixtas. Astringente suave y purificante.</p>
            <p class="precio">$1.800</p>
          </div>
        </div>
        <div class="producto">
          <div class="producto-img">⚫ Carbón + Arcilla Verde</div>
          <div class="producto-info">
            <h3>Purifica</h3>
            <p>Desintoxica y matifica. Perfecto para pieles con tendencia acneica o expuestas a la contaminación.</p>
            <p class="precio">$2.000</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Contacto -->
  <section id="contacto" class="contacto">
    <div class="container">
      <h2 class="section-title">Conectemos</h2>
      <p>¿Quieres un pedido especial? ¿Buscas jabones para regalo, eventos o tu negocio? Escríbeme y armamos juntos lo que necesitas.</p>
      <div class="redes">
        <a href="https://wa.me/tunumero" target="_blank" title="WhatsApp"><i class="fab fa-whatsapp"></i></a>
        <a href="https://instagram.com/tierrayaroma" target="_blank" title="Instagram"><i class="fab fa-instagram"></i></a>
        <!-- Agrega más: <a href="mailto:tucorreo@gmail.com"><i class="fas fa-envelope"></i></a> -->
      </div>
      <p style="margin-top: 25px; color: var(--tierra); font-weight: 500;">
        📍 Basado en [Tu Ciudad] | Envíos a todo Chile 🇨🇱
      </p>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <div class="container">
      <p>&copy; 2025 Tierra y Aroma — Jabones artesanales con propósito.</p>
      <p>Hechos con tierra, aroma y conciencia.</p>
    </div>
  </footer>

  <!-- Botón flotante de WhatsApp -->
  <a href="https://wa.me/tunumero" class="whatsapp-float" target="_blank" title="Escríbeme por WhatsApp">
    <i class="fab fa-whatsapp"></i>
  </a>

</body>
</html>
