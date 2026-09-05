<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Throne Garments | Premium Streetwear</title>
  <meta name="description" content="Throne Garments — premium streetwear. Wear your crown.">
  <style>
    /* ============================================
       THRONE GARMENTS - COMPLETE CSS STYLESHEET
       ============================================ */

    /* ---------- RESET & BASE ---------- */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Arial', 'Helvetica', sans-serif;
      background: #050505;
      color: #f5f5f5;
      line-height: 1.5;
      -webkit-font-smoothing: antialiased;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    img {
      display: block;
      max-width: 100%;
    }

    button {
      cursor: pointer;
      border: none;
      font-family: inherit;
    }

    /* ---------- VARIABLES ---------- */
    :root {
      --black: #050505;
      --red: #d71920;
      --white: #f5f5f5;
      --gray: #a7a7a7;
      --card: #101010;
      --line: #292929;
      --shadow: rgba(0, 0, 0, 0.8);
      --radius: 6px;
      --transition: 0.25s ease;
    }

    /* ---------- HEADER ---------- */
    header {
      position: sticky;
      top: 0;
      z-index: 50;
      background: rgba(5, 5, 5, 0.95);
      border-bottom: 1px solid #222;
      backdrop-filter: blur(8px);
      -webkit-backdrop-filter: blur(8px);
    }

    .nav {
      max-width: 1180px;
      margin: 0 auto;
      padding: 16px 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 12px;
    }

    .logo-wrap {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .logo-icon {
      height: 38px;
      width: auto;
      filter: brightness(0) invert(1);
    }

    .logo-text {
      font: 700 1.35rem Georgia, serif;
      letter-spacing: 3px;
    }

    .logo-text span {
      color: var(--red);
    }

    .navlinks {
      display: flex;
      gap: 24px;
      list-style: none;
      align-items: center;
    }

    .navlinks a {
      font-weight: 500;
      font-size: 0.95rem;
      transition: color var(--transition);
      position: relative;
    }

    .navlinks a::after {
      content: '';
      position: absolute;
      bottom: -4px;
      left: 0;
      width: 0;
      height: 2px;
      background: var(--red);
      transition: width var(--transition);
    }

    .navlinks a:hover::after {
      width: 100%;
    }

    .navlinks a:hover {
      color: var(--red);
    }

    .cart-btn {
      background: var(--red);
      color: #fff;
      padding: 10px 18px;
      font-weight: 700;
      font-size: 0.9rem;
      border-radius: var(--radius);
      transition: background var(--transition);
      letter-spacing: 0.5px;
    }

    .cart-btn:hover {
      background: #b01218;
    }

    /* ---------- BUTTONS ---------- */
    .btn {
      display: inline-block;
      background: var(--red);
      color: #fff;
      padding: 14px 28px;
      font-weight: 700;
      border: 0;
      border-radius: var(--radius);
      cursor: pointer;
      transition: background var(--transition), transform 0.15s;
      text-align: center;
      letter-spacing: 0.5px;
    }

    .btn:hover {
      background: #b01218;
      transform: translateY(-2px);
    }

    .btn:active {
      transform: translateY(0);
    }

    .btn-outline {
      background: transparent;
      border: 2px solid var(--red);
      color: var(--white);
    }

    .btn-outline:hover {
      background: var(--red);
      color: #fff;
    }

    /* ---------- HERO ---------- */
    .hero {
      min-height: 78vh;
      display: flex;
      align-items: flex-end;
      padding: 80px 20px 65px;
      background: linear-gradient(90deg, rgba(0, 0, 0, 0.85), rgba(0, 0, 0, 0.2)),
        url('data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI4MCIgaGVpZ2h0PSI4MCIgdmlld0JveD0iMCAwIDQwIDQwIj48cmVjdCB3aWR0aD0iNDAiIGhlaWdodD0iNDAiIGZpbGw9IiMxYTFhMWEiLz48cGF0aCBkPSJNMjAgMTBsMTAgMTAtMTAgMTAtMTAtMTB6IiBmaWxsPSIjMjkyOTI5Ii8+PC9zdmc+') center/cover no-repeat;
      background-color: #0a0a0a;
      position: relative;
    }

    .hero::before {
      content: '';
      position: absolute;
      inset: 0;
      background: radial-gradient(ellipse at 30% 50%, rgba(215, 25, 32, 0.08), transparent 70%);
      pointer-events: none;
    }

    .hero-inner {
      max-width: 1180px;
      width: 100%;
      margin: 0 auto;
      position: relative;
      z-index: 1;
    }

    .kicker {
      color: var(--red);
      font-weight: 700;
      letter-spacing: 5px;
      text-transform: uppercase;
      font-size: 0.85rem;
    }

    .hero h1 {
      font: 700 clamp(3.5rem, 9vw, 7rem) / 0.85 Impact, 'Arial Black', sans-serif;
      text-transform: uppercase;
      margin: 16px 0 8px;
      letter-spacing: -2px;
    }

    .hero p {
      max-width: 550px;
      color: #ddd;
      font-size: 1.1rem;
      line-height: 1.6;
    }

    .hero .btn {
      margin-top: 28px;
    }

    /* ---------- SECTIONS ---------- */
    section {
      padding: 85px 20px;
    }

    .wrap {
      max-width: 1180px;
      margin: 0 auto;
    }

    .title {
      margin-bottom: 40px;
    }

    .title small {
      color: var(--red);
      font-weight: 700;
      letter-spacing: 3px;
      text-transform: uppercase;
      font-size: 0.8rem;
      display: block;
      margin-bottom: 4px;
    }

    .title h2 {
      font: 700 3rem Impact, 'Arial Black', sans-serif;
      text-transform: uppercase;
      letter-spacing: -1px;
      line-height: 1.1;
    }

    /* ---------- FEATURES ---------- */
    .feature {
      background: #0c0c0c;
      border-top: 1px solid var(--line);
      border-bottom: 1px solid var(--line);
      padding: 0;
    }

    .feature-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 1px;
      background: var(--line);
    }

    .feature-box {
      background: #0c0c0c;
      padding: 32px 20px;
      text-align: center;
      transition: background var(--transition);
    }

    .feature-box:hover {
      background: #141414;
    }

    .feature-box b {
      display: block;
      color: var(--red);
      font-size: 1.1rem;
      margin-bottom: 5px;
      font-weight: 700;
    }

    .feature-box span {
      color: #bbb;
      font-size: 0.9rem;
    }

    /* ---------- PRODUCTS ---------- */
    .products {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 18px;
    }

    .product {
      background: var(--card);
      border: 1px solid var(--line);
      overflow: hidden;
      border-radius: var(--radius);
      transition: border-color var(--transition), transform var(--transition);
    }

    .product:hover {
      border-color: #555;
      transform: translateY(-4px);
    }

    .product img {
      width: 100%;
      height: 280px;
      object-fit: cover;
      object-position: center;
      background: #1a1a1a;
      transition: transform 0.4s;
    }

    .product:hover img {
      transform: scale(1.02);
    }

    .product-body {
      padding: 18px 18px 20px;
    }

    .product h3 {
      font-size: 1.05rem;
      font-weight: 700;
      letter-spacing: 0.3px;
    }

    .desc {
      color: var(--gray);
      font-size: 0.9rem;
      min-height: 40px;
      margin: 6px 0 10px;
      line-height: 1.4;
    }

    .price-row {
      display: flex;
      align-items: baseline;
      gap: 6px;
      flex-wrap: wrap;
    }

    .price {
      font-size: 1.25rem;
      font-weight: 700;
      color: #fff;
    }

    .from {
      font-size: 0.75rem;
      color: var(--red);
      text-transform: uppercase;
      font-weight: 600;
    }

    .sizes {
      display: flex;
      gap: 6px;
      flex-wrap: wrap;
      margin: 14px 0 16px;
    }

    .size {
      background: #080808;
      border: 1px solid #444;
      color: #fff;
      padding: 6px 12px;
      cursor: pointer;
      border-radius: 4px;
      font-size: 0.8rem;
      font-weight: 600;
      transition: all var(--transition);
    }

    .size:hover {
      border-color: #777;
    }

    .size.selected {
      background: var(--red);
      border-color: var(--red);
      color: #fff;
    }

    .add-to-cart {
      width: 100%;
      margin-top: 2px;
      background: #fff;
      color: #000;
      border-radius: var(--radius);
      font-weight: 700;
      transition: all var(--transition);
      padding: 12px;
    }

    .add-to-cart:hover {
      background: var(--red);
      color: #fff;
      transform: translateY(0);
    }

    /* ---------- STORY ---------- */
    .story {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 50px;
      align-items: center;
    }

    .story-image {
      width: 100%;
      max-height: 620px;
      object-fit: cover;
      object-position: top;
      border-radius: var(--radius);
      background: #1a1a1a;
    }

    .story h2 {
      font: 700 3rem Impact, 'Arial Black', sans-serif;
      text-transform: uppercase;
      line-height: 1.1;
    }

    .story p {
      color: #bbb;
      margin-top: 15px;
      font-size: 1.05rem;
      line-height: 1.7;
      max-width: 520px;
    }

    .story .btn {
      margin-top: 25px;
    }

    /* ---------- CHECKOUT ---------- */
    .checkout {
      background: #f0f0f0;
      color: #111;
    }

    .checkout .title h2 {
      color: #111;
    }

    .checkout .title p {
      color: #555;
      margin-top: 4px;
    }

    .checkout-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 45px;
      align-items: start;
    }

    .checkout form {
      display: grid;
      gap: 14px;
    }

    .checkout form input {
      background: #fff;
      border: 1px solid #ccc;
      color: #111;
      padding: 14px 16px;
      border-radius: var(--radius);
      font: inherit;
      transition: border-color var(--transition);
    }

    .checkout form input:focus {
      outline: none;
      border-color: var(--red);
    }

    .checkout form .btn {
      background: var(--red);
      color: #fff;
      padding: 16px;
    }

    .checkout form .btn:hover {
      background: #b01218;
    }

    .summary {
      background: #fff;
      border: 1px solid #ddd;
      padding: 24px;
      border-radius: var(--radius);
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.06);
    }

    .summary h2 {
      font-size: 1.3rem;
      margin-bottom: 16px;
      color: #111;
    }

    .summary-row {
      display: flex;
      justify-content: space-between;
      padding: 10px 0;
      border-bottom: 1px solid #eee;
      font-size: 0.95rem;
    }

    .summary-row:last-child {
      border-bottom: none;
    }

    .summary-total {
      font-weight: 700;
      font-size: 1.2rem;
      padding-top: 16px;
      border-top: 2px solid #ddd;
      margin-top: 4px;
      display: flex;
      justify-content: space-between;
    }

    .empty-cart {
      color: #999;
      padding: 20px 0;
      text-align: center;
    }

    /* ---------- CONTACT ---------- */
    .contact {
      background: #080808;
    }

    .contact-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 45px;
    }

    .contact h2 {
      font: 700 3rem Impact, 'Arial Black', sans-serif;
      text-transform: uppercase;
      line-height: 1.1;
    }

    .contact p {
      color: #aaa;
      margin: 12px 0;
      font-size: 1rem;
    }

    .contact a {
      color: var(--red);
      font-weight: 600;
      transition: color var(--transition);
    }

    .contact a:hover {
      color: #ff4444;
    }

    .contact form {
      display: grid;
      gap: 14px;
    }

    .contact form input,
    .contact form textarea {
      background: #111;
      border: 1px solid #333;
      color: #fff;
      padding: 14px 16px;
      border-radius: var(--radius);
      font: inherit;
      transition: border-color var(--transition);
    }

    .contact form input:focus,
    .contact form textarea:focus {
      outline: none;
      border-color: var(--red);
    }

    .contact form textarea {
      min-height: 130px;
      resize: vertical;
    }

    .contact form .btn {
      padding: 16px;
    }

    /* ---------- FOOTER ---------- */
    footer {
      border-top: 1px solid var(--line);
      padding: 30px 20px;
      text-align: center;
      color: #777;
      font-size: 0.9rem;
      letter-spacing: 0.5px;
    }

    /* ---------- CART DRAWER ---------- */
    .drawer {
      position: fixed;
      right: -430px;
      top: 0;
      bottom: 0;
      width: min(430px, 100%);
      z-index: 100;
      background: #0c0c0c;
      border-left: 1px solid #333;
      padding: 24px;
      transition: right var(--transition);
      overflow-y: auto;
      box-shadow: -12px 0 40px rgba(0, 0, 0, 0.8);
    }

    .drawer.open {
      right: 0;
    }

    .drawer-head {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 20px;
      padding-bottom: 12px;
      border-bottom: 1px solid var(--line);
    }

    .drawer-head h2 {
      font-size: 1.4rem;
    }

    .close-drawer {
      background: none;
      border: 0;
      color: #fff;
      font-size: 32px;
      cursor: pointer;
      line-height: 1;
      transition: color var(--transition);
      padding: 0 4px;
    }

    .close-drawer:hover {
      color: var(--red);
    }

    .cart-item {
      padding: 14px 0;
      border-bottom: 1px solid #292929;
    }

    .cart-item:last-child {
      border-bottom: none;
    }

    .cart-row {
      display: flex;
      justify-content: space-between;
      gap: 10px;
      align-items: baseline;
    }

    .cart-row b {
      font-size: 1rem;
    }

    .cart-item small {
      color: var(--gray);
      font-size: 0.8rem;
    }

    .qty-control {
      display: flex;
      align-items: center;
      gap: 10px;
      margin-top: 8px;
    }

    .qty-control button {
      background: #222;
      border: 1px solid #444;
      color: #fff;
      padding: 4px 12px;
      cursor: pointer;
      border-radius: 4px;
      font-size: 1rem;
      transition: all var(--transition);
    }

    .qty-control button:hover {
      background: var(--red);
      border-color: var(--red);
    }

    .qty-control span {
      font-weight: 600;
      min-width: 24px;
      text-align: center;
    }

    .cart-total {
      font-weight: 700;
      font-size: 1.3rem;
      margin: 20px 0;
      padding-top: 16px;
      border-top: 2px solid var(--line);
      display: flex;
      justify-content: space-between;
    }

    .drawer .btn {
      width: 100%;
      text-align: center;
      padding: 16px;
    }

    /* ---------- TOAST NOTIFICATION ---------- */
    .toast {
      position: fixed;
      bottom: 30px;
      left: 50%;
      transform: translateX(-50%) translateY(20px);
      background: #1a1a1a;
      color: #fff;
      padding: 14px 32px;
      border-radius: var(--radius);
      border: 1px solid #333;
      box-shadow: 0 8px 40px rgba(0, 0, 0, 0.9);
      z-index: 200;
      opacity: 0;
      transition: opacity 0.3s, transform 0.3s;
      pointer-events: none;
      font-weight: 600;
      font-size: 0.95rem;
      white-space: nowrap;
    }

    .toast.show {
      opacity: 1;
      transform: translateX(-50%) translateY(0);
    }

    /* ---------- RESPONSIVE ---------- */
    @media (max-width: 1024px) {
      .products {
        grid-template-columns: repeat(3, 1fr);
      }
    }

    @media (max-width: 900px) {
      .products {
        grid-template-columns: repeat(2, 1fr);
      }

      .story,
      .contact-grid,
      .checkout-grid {
        grid-template-columns: 1fr;
      }

      .navlinks {
        display: none;
      }

      .hero h1 {
        font-size: clamp(3rem, 8vw, 5rem);
      }

      .title h2 {
        font-size: 2.4rem;
      }

      .story h2 {
        font-size: 2.4rem;
      }
    }

    @media (max-width: 600px) {
      .products {
        grid-template-columns: 1fr;
        gap: 16px;
      }

      .feature-grid {
        grid-template-columns: 1fr 1fr;
      }

      .hero {
        min-height: 65vh;
        padding: 60px 16px 50px;
      }

      .hero h1 {
        font-size: 3.4rem;
      }

      section {
        padding: 60px 16px;
      }

      .title h2 {
        font-size: 2rem;
      }

      .story h2 {
        font-size: 2rem;
      }

      .contact h2 {
        font-size: 2rem;
      }

      .checkout-grid {
        gap: 30px;
      }

      .toast {
        white-space: normal;
        max-width: 90%;
        text-align: center;
        padding: 12px 20px;
        font-size: 0.85rem;
      }

      .drawer {
        width: 100%;
        right: -100%;
        padding: 18px;
      }
    }

    @media (max-width: 400px) {
      .hero h1 {
        font-size: 2.8rem;
      }

      .feature-grid {
        grid-template-columns: 1fr;
      }

      .nav {
        padding: 12px 14px;
      }

      .cart-btn {
        padding: 8px 14px;
        font-size: 0.8rem;
      }
    }
  </style>
</head>
<body>

  <!-- ===== HEADER ===== -->
  <header>
    <div class="nav">
      <div class="logo-wrap">
        <svg class="logo-icon" viewBox="0 0 140 40" fill="none" xmlns="http://www.w3.org/2000/svg">
          <text x="0" y="28" font-family="Georgia, serif" font-weight="700" font-size="28" fill="#f5f5f5" letter-spacing="3">THRONE</text>
          <text x="95" y="28" font-family="Georgia, serif" font-weight="700" font-size="28" fill="#d71920">GARMENTS</text>
        </svg>
      </div>
      <ul class="navlinks">
        <li><a href="#shop">Shop</a></li>
        <li><a href="#story">Our Story</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
      <button class="cart-btn" onclick="openCart()">🛒 CART (<span id="count">0</span>)</button>
    </div>
  </header>

  <!-- ===== HERO ===== -->
  <section class="hero" id="home">
    <div class="hero-inner">
      <div class="kicker">Established 2024 · Premium Streetwear</div>
      <h1>Wear<br>Your Crown.</h1>
      <p>Your crown is waiting for you. As soon as you find the courage to wear it.</p>
      <a class="btn" href="#shop">SHOP THE COLLECTION</a>
    </div>
  </section>

  <!-- ===== FEATURES ===== -->
  <section class="feature">
    <div class="wrap feature-grid">
      <div class="feature-box"><b>♛ BOLD DESIGNS</b><span>That speak</span></div>
      <div class="feature-box"><b>◈ PREMIUM QUALITY</b><span>Built to last</span></div>
      <div class="feature-box"><b>✦ EMBROIDERY</b><span>That stands out</span></div>
      <div class="feature-box"><b>🔥 MADE FOR COMFORT</b><span>Made to last</span></div>
    </div>
  </section>

  <!-- ===== SHOP ===== -->
  <section id="shop">
    <div class="wrap">
      <div class="title">
        <small>SHOP</small>
        <h2>Featured Garments</h2>
      </div>
      <div class="products">

        <!-- Product 1 -->
        <article class="product">
          <img src="1000399691_3623029286173081780.webp" alt="Regular Hoodie" style="object-position: 50% 30%;">
          <div class="product-body">
            <h3>Regular Hoodie</h3>
            <p class="desc">Classic Throne embroidered hoodie.</p>
            <div class="price-row">
              <strong class="price">R449.99</strong>
            </div>
            <div class="sizes">
              <button class="size" onclick="pick(this)">S</button>
              <button class="size" onclick="pick(this)">M</button>
              <button class="size" onclick="pick(this)">L</button>
              <button class="size" onclick="pick(this)">XL</button>
            </div>
            <button class="btn add-to-cart" onclick="add('Regular Hoodie',449.99,this)">ADD TO CART</button>
          </div>
        </article>

        <!-- Product 2 -->
        <article class="product">
          <img src="1000473890_5453315045728938415.webp" alt="Custom Made Hoodie" style="object-position: 50% 40%;">
          <div class="product-body">
            <h3>Custom Made Hoodie</h3>
            <p class="desc">Custom design with signature back print.</p>
            <div class="price-row">
              <span class="from">From</span>
              <strong class="price">R799.99</strong>
            </div>
            <div class="sizes">
              <button class="size" onclick="pick(this)">S</button>
              <button class="size" onclick="pick(this)">M</button>
              <button class="size" onclick="pick(this)">L</button>
              <button class="size" onclick="pick(this)">XL</button>
            </div>
            <button class="btn add-to-cart" onclick="add('Custom Made Hoodie',799.99,this)">ADD TO CART</button>
          </div>
        </article>

        <!-- Product 3 -->
        <article class="product">
          <img src="1000420435_1925724463650737048.webp" alt="Regular Two Piece" style="object-position: 50% 50%;">
          <div class="product-body">
            <h3>Regular Two Piece</h3>
            <p class="desc">Matching hoodie and trouser set.</p>
            <div class="price-row">
              <strong class="price">R1499.99</strong>
            </div>
            <div class="sizes">
              <button class="size" onclick="pick(this)">S</button>
              <button class="size" onclick="pick(this)">M</button>
              <button class="size" onclick="pick(this)">L</button>
              <button class="size" onclick="pick(this)">XL</button>
            </div>
            <button class="btn add-to-cart" onclick="add('Regular Two Piece',1499.99,this)">ADD TO CART</button>
          </div>
        </article>

        <!-- Product 4 -->
        <article class="product">
          <img src="1000473890_5453315045728938415.webp" alt="Custom Two Piece" style="object-position: 50% 60%;">
          <div class="product-body">
            <h3>Custom Two Piece</h3>
            <p class="desc">Premium custom matching set.</p>
            <div class="price-row">
              <strong class="price">R2199.99</strong>
            </div>
            <div class="sizes">
              <button class="size" onclick="pick(this)">S</button>
              <button class="size" onclick="pick(this)">M</button>
              <button class="size" onclick="pick(this)">L</button>
              <button class="size" onclick="pick(this)">XL</button>
            </div>
            <button class="btn add-to-cart" onclick="add('Custom Two Piece',2199.99,this)">ADD TO CART</button>
          </div>
        </article>

        <!-- Product 5 -->
        <article class="product">
          <img src="1000399691_3623029286173081780.webp" alt="Skull Cap" style="object-position: 50% 70%;">
          <div class="product-body">
            <h3>Embroidered Skull Cap</h3>
            <p class="desc">Premium embroidered cap.</p>
            <div class="price-row">
              <strong class="price">R149.99</strong>
            </div>
            <div class="sizes">
              <button class="size" onclick="pick(this)">ONE SIZE</button>
            </div>
            <button class="btn add-to-cart" onclick="add('Embroidered Skull Cap',149.99,this)">ADD TO CART</button>
          </div>
        </article>

        <!-- Product 6 -->
        <article class="product">
          <img src="1000420435_1925724463650737048.webp" alt="Skull Cap 2 Pack" style="object-position: 50% 80%;">
          <div class="product-body">
            <h3>Skull Cap — 2 Pack</h3>
            <p class="desc">Two embroidered caps.</p>
            <div class="price-row">
              <strong class="price">R219.99</strong>
            </div>
            <div class="sizes">
              <button class="size" onclick="pick(this)">ONE SIZE</button>
            </div>
            <button class="btn add-to-cart" onclick="add('Skull Cap 2 Pack',219.99,this)">ADD TO CART</button>
          </div>
        </article>

      </div>
    </div>
  </section>

  <!-- ===== STORY ===== -->
  <section id="story">
    <div class="wrap story">
      <img class="story-image" src="1000473890_5453315045728938415.webp" alt="Throne Garments campaign">
      <div>
        <div class="title">
          <small>THE BRAND</small>
          <h2>Built for comfort.<br>Made to last.</h2>
        </div>
        <p>Throne Garments is premium streetwear built around bold designs, quality construction and standout embroidery. Every piece is made to help you wear your crown with confidence.</p>
        <a class="btn" href="#contact">WORK WITH US</a>
      </div>
    </div>
  </section>

  <!-- ===== CHECKOUT ===== -->
  <section class="checkout" id="checkout">
    <div class="wrap checkout-grid">
      <div>
        <div class="title">
          <small>ORDER</small>
          <h2>Checkout</h2>
          <p>Review your order and send it directly to WhatsApp.</p>
        </div>
        <form onsubmit="checkout(event)">
          <input id="name" required placeholder="Full name">
          <input id="phone" required placeholder="WhatsApp number">
          <input id="address" required placeholder="Delivery address">
          <button class="btn" type="submit">📤 SEND ORDER ON WHATSAPP</button>
        </form>
      </div>
      <div class="summary">
        <h2>Order Summary</h2>
        <div id="summary">
          <p class="empty-cart">Your cart is empty.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- ===== CONTACT ===== -->
  <section class="contact" id="contact">
    <div class="wrap contact-grid">
      <div>
        <div class="title">
          <small>CONNECT</small>
          <h2>Let's Talk</h2>
        </div>
        <p>For orders, custom garments and business enquiries:</p>
        <p>📱 WhatsApp: <a href="https://wa.me/27677719518">+27 67 771 9518</a></p>
        <p>📸 Socials: Instagram · TikTok</p>
      </div>
      <form onsubmit="contactForm(event)">
        <input required placeholder="Your name">
        <input type="email" required placeholder="Email address">
        <textarea required placeholder="Your message"></textarea>
        <button class="btn" type="submit">✉️ SEND MESSAGE</button>
      </form>
    </div>
  </section>

  <!-- ===== FOOTER ===== -->
  <footer>© 2026 Throne Garments · Wear Your Crown.</footer>

  <!-- ===== CART DRAWER ===== -->
  <div class="drawer" id="drawer">
    <div class="drawer-head">
      <h2>Your Cart</h2>
      <button class="close-drawer" onclick="closeCart()">×</button>
    </div>
    <div id="cartItems"></div>
    <div class="cart-total">
      <span>Total:</span>
      <span>R<span id="total">0.00</span></span>
    </div>
    <a class="btn" href="#checkout" onclick="closeCart()">CHECKOUT</a>
  </div>

  <!-- ===== TOAST ===== -->
  <div class="toast" id="toast"></div>

  <!-- ===== JAVASCRIPT ===== -->
  <script>
    // ============================================
    // THRONE GARMENTS - JAVASCRIPT
    // ============================================

    // ---------- STATE ----------
    let cart = [];
    const WHATSAPP = "27677719518";
    let toastTimer = null;

    // ---------- HELPERS ----------
    function pick(el) {
      const parent = el.parentElement;
      parent.querySelectorAll('.size').forEach(x => x.classList.remove('selected'));
      el.classList.add('selected');
    }

    function showToast(msg) {
      const el = document.getElementById('toast');
      el.textContent = msg;
      el.classList.add('show');
      clearTimeout(toastTimer);
      toastTimer = setTimeout(() => el.classList.remove('show'), 2500);
    }

    // ---------- CART ----------
    function add(name, price, btn) {
      const selected = btn.previousElementSibling.querySelector('.selected');
      if (!