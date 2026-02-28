[index.html](https://github.com/user-attachments/files/25619312/index.html)
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tu producto – Comprar ahora</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;500;600;700;800&family=DM+Sans:ital,opsz,wght@0,9..40,400;0,9..40,500;0,9..40,600;0,9..40,700;1,9..40,400&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0d0f0e;
      --surface: #161a18;
      --text: #f0f2f1;
      --text-muted: #8a928e;
      --accent: #22c55e;
      --accent-hover: #16a34a;
      --border: #2a302d;
      --badge: #14532d;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'DM Sans', sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
      min-height: 100vh;
    }

    .container { max-width: 1120px; margin: 0 auto; padding: 0 20px; }

    /* Header */
    header {
      padding: 16px 0;
      border-bottom: 1px solid var(--border);
    }
    header .container {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .logo { font-family: 'Outfit', sans-serif; font-weight: 800; font-size: 1.35rem; letter-spacing: -0.02em; }
    .logo span { color: var(--accent); }
    nav a {
      color: var(--text-muted);
      text-decoration: none;
      font-size: 0.95rem;
      margin-left: 24px;
    }
    nav a:hover { color: var(--text); }

    /* Hero / Product */
    .hero {
      padding: 48px 0 64px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 48px;
      align-items: center;
    }
    @media (max-width: 768px) {
      .hero { grid-template-columns: 1fr; gap: 32px; padding: 32px 0 48px; }
    }

    .hero-image {
      aspect-ratio: 1;
      background: var(--surface);
      border-radius: 20px;
      overflow: hidden;
      border: 1px solid var(--border);
    }
    .hero-image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .hero-content h1 {
      font-family: 'Outfit', sans-serif;
      font-weight: 800;
      font-size: clamp(2rem, 4vw, 2.75rem);
      line-height: 1.15;
      letter-spacing: -0.03em;
      margin-bottom: 12px;
    }
    .reviews-badge {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      color: var(--text-muted);
      font-size: 0.9rem;
      margin-bottom: 20px;
    }
    .reviews-badge strong { color: var(--accent); }
    .price-row {
      display: flex;
      align-items: baseline;
      gap: 12px;
      margin-bottom: 8px;
    }
    .price { font-family: 'Outfit', sans-serif; font-weight: 700; font-size: 2rem; color: var(--accent); }
    .price-old { font-size: 1.15rem; color: var(--text-muted); text-decoration: line-through; }
    .save-badge {
      background: var(--badge);
      color: var(--accent);
      font-size: 0.8rem;
      font-weight: 600;
      padding: 4px 10px;
      border-radius: 6px;
    }
    .stock-note { font-size: 0.9rem; color: var(--text-muted); margin-bottom: 24px; }
    .cta-block { margin-bottom: 20px; }
    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      padding: 16px 28px;
      font-family: 'Outfit', sans-serif;
      font-weight: 600;
      font-size: 1rem;
      border: none;
      border-radius: 12px;
      cursor: pointer;
      text-decoration: none;
      transition: transform 0.15s, box-shadow 0.15s;
    }
    .btn-primary {
      background: var(--accent);
      color: var(--bg);
      width: 100%;
      max-width: 320px;
    }
    .btn-primary:hover {
      background: var(--accent-hover);
      transform: translateY(-1px);
      box-shadow: 0 8px 24px rgba(34, 197, 94, 0.35);
    }
    .trust-row {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      margin-top: 24px;
      font-size: 0.85rem;
      color: var(--text-muted);
    }
    .trust-row span { display: flex; align-items: center; gap: 6px; }

    /* Benefits */
    .benefits {
      padding: 56px 0;
      border-top: 1px solid var(--border);
    }
    .benefits h2 {
      font-family: 'Outfit', sans-serif;
      font-weight: 700;
      font-size: 1.75rem;
      margin-bottom: 32px;
      text-align: center;
    }
    .benefits-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 24px;
    }
    .benefit-card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 24px;
    }
    .benefit-card h3 {
      font-family: 'Outfit', sans-serif;
      font-weight: 600;
      font-size: 1.1rem;
      margin-bottom: 8px;
    }
    .benefit-card p { color: var(--text-muted); font-size: 0.95rem; }

    /* Reviews */
    .reviews {
      padding: 56px 0;
      border-top: 1px solid var(--border);
    }
    .reviews h2 {
      font-family: 'Outfit', sans-serif;
      font-weight: 700;
      font-size: 1.75rem;
      margin-bottom: 8px;
      text-align: center;
    }
    .reviews-sub { text-align: center; color: var(--text-muted); font-size: 0.95rem; margin-bottom: 32px; }
    .reviews-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 20px;
    }
    .review-card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 20px;
    }
    .review-card .name { font-weight: 600; margin-bottom: 4px; }
    .review-card .verified { font-size: 0.8rem; color: var(--accent); margin-bottom: 8px; }
    .review-card .text { color: var(--text-muted); font-size: 0.9rem; }

    /* Payment section – tu procesador */
    .payment-section {
      padding: 56px 0;
      border-top: 1px solid var(--border);
      background: var(--surface);
    }
    .payment-section h2 {
      font-family: 'Outfit', sans-serif;
      font-weight: 700;
      font-size: 1.75rem;
      margin-bottom: 12px;
      text-align: center;
    }
    .payment-section p {
      text-align: center;
      color: var(--text-muted);
      max-width: 480px;
      margin: 0 auto 28px;
    }
    .payment-box {
      max-width: 400px;
      margin: 0 auto;
      background: var(--bg);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 28px;
    }
    .payment-box .price { margin-bottom: 16px; }
    #payment-button {
      width: 100%;
      padding: 18px;
      font-size: 1.05rem;
    }

    /* FAQ */
    .faq {
      padding: 56px 0;
      border-top: 1px solid var(--border);
    }
    .faq h2 {
      font-family: 'Outfit', sans-serif;
      font-weight: 700;
      font-size: 1.75rem;
      margin-bottom: 28px;
      text-align: center;
    }
    .faq-list { max-width: 640px; margin: 0 auto; }
    .faq-item {
      border-bottom: 1px solid var(--border);
      padding: 18px 0;
    }
    .faq-item h4 { font-size: 1rem; margin-bottom: 6px; }
    .faq-item p { color: var(--text-muted); font-size: 0.9rem; }

    /* Footer */
    footer {
      padding: 32px 0;
      border-top: 1px solid var(--border);
      text-align: center;
      color: var(--text-muted);
      font-size: 0.9rem;
    }
    footer a { color: var(--text-muted); text-decoration: none; }
    footer a:hover { color: var(--accent); }
  </style>
</head>
<body>
  <header>
    <div class="container">
      <div class="logo">Tu<span>Tienda</span></div>
      <nav>
        <a href="#producto">Producto</a>
        <a href="#reviews">Opiniones</a>
        <a href="#pago">Pagar</a>
        <a href="#faq">FAQ</a>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero" id="producto">
      <div class="container" style="display: contents;">
        <div class="hero-image">
          <!-- Cambia la URL por la imagen de tu producto -->
          <img src="https://images.unsplash.com/photo-1584308666744-24d5c474f2ae?w=600&h=600&fit=crop" alt="Producto">
        </div>
        <div class="hero-content">
          <h1>X3 VITASUPLEMENTO</h1>
          <p class="reviews-badge">★ <strong>2,500+</strong> reseñas verificadas</p>
          <div class="price-row">
            <span class="price">$115.00</span>
            <span class="price-old">$130.00</span>
            <span class="save-badge">Ahorra $15</span>
          </div>
          <p class="stock-note">Disponibilidad limitada. ¡Reserva ya!</p>
          <div class="cta-block">
            <a href="#pago" class="btn btn-primary" id="hero-cta">COMPRAR AHORA</a>
          </div>
          <div class="trust-row">
            <span>✓ Envío gratis</span>
            <span>✓ Devoluciones fáciles</span>
            <span>✓ Soporte 24/7</span>
          </div>
        </div>
      </div>
    </section>

    <section class="benefits">
      <div class="container">
        <h2>Beneficios</h2>
        <div class="benefits-grid">
          <div class="benefit-card">
            <h3>Calidad premium</h3>
            <p>Ingredientes seleccionados y fórmula probada para resultados que notas.</p>
          </div>
          <div class="benefit-card">
            <h3>Envío seguro</h3>
            <p>Embalaje discreto y envío 100% seguro a tu domicilio.</p>
          </div>
          <div class="benefit-card">
            <h3>Garantía</h3>
            <p>Tu satisfacción es nuestra prioridad. Garantía de devolución si no te convence.</p>
          </div>
        </div>
      </div>
    </section>

    <section class="reviews" id="reviews">
      <div class="container">
        <h2>Lo que dicen nuestros clientes</h2>
        <p class="reviews-sub">+2000 clientes satisfechos</p>
        <div class="reviews-grid">
          <div class="review-card">
            <div class="name">María G.</div>
            <div class="verified">Comprador verificado</div>
            <p class="text">"Llegó rápido y el producto cumple. Muy recomendado."</p>
          </div>
          <div class="review-card">
            <div class="name">Carlos R.</div>
            <div class="verified">Comprador verificado</div>
            <p class="text">"Segunda compra. Excelente calidad y atención."</p>
          </div>
          <div class="review-card">
            <div class="name">Ana L.</div>
            <div class="verified">Comprador verificado</div>
            <p class="text">"Todo perfecto. Pagué con confianza y sin problemas."</p>
          </div>
        </div>
      </div>
    </section>

    <section class="payment-section" id="pago">
      <div class="container">
        <h2>Pago seguro</h2>
        <p>Completa tu compra con tu método preferido. Redirigirás a un checkout seguro.</p>
        <div class="payment-box">
          <div class="price">$115.00</div>
          <!-- OPCIÓN A: Enlace directo a tu checkout (Stripe, Mercado Pago, PayPal, etc.) -->
          <a href="https://tu-enlace-de-pago.com/checkout" class="btn btn-primary" id="payment-button" target="_blank" rel="noopener">
            Ir a pagar
          </a>
          <!-- OPCIÓN B: Si usas Stripe/Mercado Pago embebido, sustituye el <a> anterior por el botón que te den ellos -->
        </div>
      </div>
    </section>

    <section class="faq" id="faq">
      <div class="container">
        <h2>Preguntas frecuentes</h2>
        <div class="faq-list">
          <div class="faq-item">
            <h4>¿Cómo es el envío?</h4>
            <p>Enviamos a todo el país. El tiempo depende de tu zona; suele ser 3–7 días hábiles.</p>
          </div>
          <div class="faq-item">
            <h4>¿Puedo devolver el producto?</h4>
            <p>Sí. Si no estás satisfecho, puedes solicitar devolución en un plazo definido.</p>
          </div>
          <div class="faq-item">
            <h4>¿El pago es seguro?</h4>
            <p>Sí. El pago se procesa en una pasarela segura; no guardamos datos de tu tarjeta.</p>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">
      <p><a href="#">Política de privacidad</a> · <a href="#">Política de reembolso</a></p>
      <p style="margin-top: 8px;">© 2026 Tu Tienda. Página independiente.</p>
    </div>
  </footer>

  <script>
    // ——— CONFIGURA TU PROCESADOR DE PAGOS ———
    // Pega aquí la URL de tu checkout (Stripe Payment Link, Mercado Pago, PayPal, etc.)
    const PAYMENT_URL = 'https://tu-enlace-de-pago.com/checkout';

    document.getElementById('payment-button').href = PAYMENT_URL;
    document.getElementById('hero-cta').href = '#pago';
  </script>
</body>
</html>
