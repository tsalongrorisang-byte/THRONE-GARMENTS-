<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Throne Garments | Premium Streetwear</title>
  <meta name="description" content="Throne Garments — premium streetwear. Wear your crown.">
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body { font-family: Arial, Helvetica, sans-serif; background: #050505; color: #f5f5f5; line-height: 1.5; }
    a { text-decoration: none; color: inherit; }
    :root { --black: #050505; --red: #d71920; --white: #f5f5f5; --gray: #a7a7a7; --card: #101010; --line: #292929; }
    header { position: sticky; top: 0; z-index: 50; background: rgba(5,5,5,.95); border-bottom: 1px solid #222; backdrop-filter: blur(8px); }
    .nav { max-width: 1180px; margin: auto; padding: 16px 20px; display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 12px; }
    .logo-wrap { display: flex; align-items: center; gap: 10px; }
    .logo-icon { height: 38px; width: auto; filter: brightness(0) invert(1); } /* black&white logo -> white on dark bg */
    .logo-text { font: 700 1.35rem Georgia, serif; letter-spacing: 3px; }
    .logo-text span { color: var(--red); }
    .navlinks { display: flex; gap: 24px; list-style: none; }
    .navlinks a:hover { color: var(--red); }
    .cart { background: var(--red); border: 0; color: #fff; padding: 10px 15px; font-weight: bold; cursor: pointer; border-radius: 4px; }
    .hero { min-height: 78vh; display: flex; align-items: end; padding: 80px 20px 65px; background: linear-gradient(90deg, rgba(0,0,0,.82), rgba(0,0,0,.18)), url('data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI4MCIgaGVpZ2h0PSI4MCIgdmlld0JveD0iMCAwIDQwIDQwIj48cmVjdCB3aWR0aD0iNDAiIGhlaWdodD0iNDAiIGZpbGw9IiMxYTFhMWEiLz48cGF0aCBkPSJNMjAgMTBsMTAgMTAtMTAgMTAtMTAtMTB6IiBmaWxsPSIjMjkyOTI5Ii8+PC9zdmc+') center/cover no-repeat; background-color: #0a0a0a; }
    .hero-inner { max-width: 1180px; width: 100%; margin: auto; }
    .kicker { color: var(--red); font-weight: bold; letter-spacing: 5px; text-transform: uppercase; font-size: 0.9rem; }
    .hero h1 { font: 700 clamp(3.5rem, 9vw, 7rem)/.85 Impact, Arial Black, sans-serif; text-transform: uppercase; margin: 16px 0; }
    .hero p { max-width: 550px; color: #ddd; font-size: 1.1rem; }
    .btn { display: inline-block; margin-top: 25px; background: var(--red); color: #fff; padding: 14px 23px; font-weight: bold; border: 0; cursor: pointer; border-radius: 4px; transition: .2s; }
    .btn:hover { background: #b01218; }
    section { padding: 85px 20px; }
    .wrap { max-width: 1180px; margin: auto; }
    .title { margin-bottom: 40px; }
    .title small { color: var(--red); font-weight: bold; letter-spacing: 3px; }
    .title h2 { font: 700 3rem Impact, Arial Black, sans-serif; text-transform: uppercase; }
    .products { display: grid; grid-template-columns: repeat(4, 1fr); gap: 16px; }
    .product { background: var(--card); border: 1px solid var(--line); overflow: hidden; border-radius: 6px; transition: .2s; }
    .product:hover { border-color: #555; }
    .product img { width: 100%; height: 280px; object-fit: cover; object-position: center; background: #1a1a1a; }
    .product-body { padding: 18px; }
    .product h3 { font-size: 1.05rem; }
    .desc { color: var(--gray); font-size: .9rem; min-height: 40px; margin: 6px 0; }
    .price { font-size: 1.2rem; font-weight: bold; color: #fff; }
    .from { font-size: .8rem; color: var(--red); text-transform: uppercase; }
    .sizes { display: flex; gap: 6px; flex-wrap: wrap; margin: 13px 0; }
    .size { background: #080808; border: 1px solid #444; color: #fff; padding: 6px 9px; cursor: pointer; border-radius: 4px; }
    .size.selected { background: var(--red); border-color: var(--red); }
    .add { width: 100%; margin-top: 2px; background: #fff; color: #000; border-radius: 4px; }
    .add:hover { background: var(--red); color: #fff; }
    .feature { background: #0c0c0c; border-top: 1px solid var(--line); border-bottom: 1px solid var(--line); }
    .feature-grid { display: grid; grid-template-columns: repeat(4,1fr); gap: 1px; background: var(--line); }
    .feature-box { background: #0c0c0c; padding: 28px 20px; text-align: center; }
    .feature-box b { display: block; color: var(--red); font-size: 1.1rem; margin-bottom: 5px; }
    .feature-box span { color: #bbb; font-size: .9rem; }
    .story { display: grid; grid-template-columns: 1fr 1fr; gap: 50px; align-items: center; }
    .story img { width: 100%; max-height: 620px; object-fit: cover; object-position: top; border-radius: 8px; background: #1a1a1a; }
    .story h2 { font: 700 3rem Impact, Arial Black, sans-serif; text-transform: uppercase; }
    .story p { color: #bbb; margin-top: 15px; }
    .contact { background: #080808; }
    .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 45px; }
    .contact h2 { font: 700 3rem Impact, Arial Black, sans-serif; text-transform: uppercase; }
    .contact p { color: #aaa; margin: 12px 0; }
    .contact a { color: var(--red); font-weight: bold; }
    form { display: grid; gap: 12px; }
    input, textarea { background: #111; border: 1px solid #333; color: #fff; padding: 14px; font: inherit; border-radius: 4px; }
    textarea { min-height: 130px; }
    footer { border-top: 1px solid var(--line); padding: 30px 20px; text-align: center; color: #777; }
    .drawer { position: fixed; right: -430px; top: 0; bottom: 0; width: min(430px,100%); z-index: 100; background: #0c0c0c; border-left: 1px solid #333; padding: 22px; transition: .25s; overflow: auto; box-shadow: -12px 0 30px #000; }
    .drawer.open { right: 0; }
    .drawer-head { display: flex; justify-content: space-between; align-items: center; margin-bottom: 18px; }
    .close { background: none; border: 0; color: #fff; font-size: 30px; cursor: pointer; }
    .cart-item { padding: 14px 0; border-bottom: 1px solid #292929; }
    .cart-row { display: flex; justify-content: space-between; gap: 10px; }
    .qty button { background: #222; border: 1px solid #444; color: #fff; padding: 3px 9px; cursor: pointer; border-radius: 4px; }
    .cart-total { font-weight: bold; font-size: 1.2rem; margin: 20px 0; }
    .empty { color: #777; padding: 30px 0; }
    .checkout { background: #f0f0f0; color: #111; }
    .checkout-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 45px; }
    .checkout .title p { color: #555; }
    .summary { background: #fff; border: 1px solid #ddd; padding: 20px; border-radius: 6px; }
    .summary-row { display: flex; justify-content: space-between; padding: 10px 0; border-bottom: 1px solid #ddd; }
    .summary-total { font-weight: bold; font-size: 1.2rem; padding-top: 18px; }
    @media(max-width:900px){ .products { grid-template-columns: repeat(2,1fr); } .story, .contact-grid, .checkout-grid { grid-template-columns: 1fr; } .navlinks { display: none; } }
    @media(max-width:550px){ .products { grid-template-columns: 1fr; } .feature-grid { grid-template-columns: 1fr 1fr; } .hero { min-height: 70vh; } .hero h1 { font-size: 4rem; } }
  </style>
</head>
<body>

<header>
  <div class="nav">
    <div class="logo-wrap">
      <!-- black & white throne logo as SVG text (matches brand) -->
      <svg class="logo-icon" viewBox="0 0 120 40" fill="none" xmlns="http://www.w3.org/2000/svg">
        <text x="0" y="28" font-family="Georgia, serif" font-weight="700" font-size="28" fill="#f5f5f5" letter-spacing="3">THRONE</text>
        <text x="82" y="28" font-family="Georgia, serif" font-weight="700" font-size="28" fill="#d71920">GARMENTS</text>
      </svg>
    </div>
    <ul class="navlinks"><li><a href="#shop">Shop</a></li><li><a href="#story">Our Story</a></li><li><a href="#contact">Contact</a></li></ul>
    <button class="cart" onclick="openCart()">CART (<span id="count">0</span>)</button>
  </div>
</header>

<section class="hero" id="home">
  <div class="hero-inner">
    <div class="kicker">Established 2024 · Premium Streetwear</div>
    <h1>Wear<br>Your Crown.</h1>
    <p>Your crown is waiting for you. As soon as you find the courage to wear it.</p>
    <a class="btn" href="#shop">SHOP THE COLLECTION</a>
  </div>
</section>

<section class="feature">
  <div class="wrap feature-grid">
    <div class="feature-box"><b>♛ BOLD DESIGNS</b><span>That speak</span></div>
    <div class="feature-box"><b>◈ PREMIUM QUALITY</b><span>Built to last</span></div>
    <div class="feature-box"><b>✦ EMBROIDERY</b><span>That stands out</span></div>
    <div class="feature-box"><b>🔥 MADE FOR COMFORT</b><span>Made to last</span></div>
  </div>
</section>

<section id="shop">
  <div class="wrap">
    <div class="title"><small>SHOP</small><h2>Featured Garments</h2></div>
    <div class="products">

      <!-- 1. Regular Hoodie - R449.99 (from image: R449.99) -->
      <article class="product">
        <img src="1000399691_3623029286173081780.webp" alt="Throne Regular Hoodie" style="object-position: 50% 30%;">
        <div class="product-body"><h3>Regular Hoodie</h3><p class="desc">Classic Throne embroidered hoodie.</p><strong class="price">R449.99</strong>
          <div class="sizes"><button class="size" onclick="pick(this)">S</button><button class="size" onclick="pick(this)">M</button><button class="size" onclick="pick(this)">L</button><button class="size" onclick="pick(this)">XL</button></div>
          <button class="btn add" onclick="add('Regular Hoodie',449.99,this)">ADD TO CART</button>
        </div>
      </article>

      <!-- 2. Custom Made Hoodie - R799.99 (from image: FROM R799.99) -->
      <article class="product">
        <img src="1000473890_5453315045728938415.webp" alt="Custom Made Hoodie" style="object-position: 50% 40%;">
        <div class="product-body"><h3>Custom Made Hoodie</h3><p class="desc">Custom design with signature back print.</p><span class="from">From</span> <strong class="price">R799.99</strong>
          <div class="sizes"><button class="size" onclick="pick(this)">S</button><button class="size" onclick="pick(this)">M</button><button class="size" onclick="pick(this)">L</button><button class="size" onclick="pick(this)">XL</button></div>
          <button class="btn add" onclick="add('Custom Made Hoodie',799.99,this)">ADD TO CART</button>
        </div>
      </article>

      <!-- 3. Regular Two Piece Outfit - R1499.99 (image: R1499,99) -->
      <article class="product">
        <img src="1000420435_1925724463650737048.webp" alt="Regular Two Piece" style="object-position: 50% 50%;">
        <div class="product-body"><h3>Regular Two Piece</h3><p class="desc">Matching hoodie and trouser set.</p><strong class="price">R1499.99</strong>
          <div class="sizes"><button class="size" onclick="pick(this)">S</button><button class="size" onclick="pick(this)">M</button><button class="size" onclick="pick(this)">L</button><button class="size" onclick="pick(this)">XL</button></div>
          <button class="btn add" onclick="add('Regular Two Piece',1499.99,this)">ADD TO CART</button>
        </div>
      </article>

      <!-- 4. Custom Made Two Piece - R2199.99 (image: R2199.99) -->
      <article class="product">
        <img src="1000473890_5453315045728938415.webp" alt="Custom Made Two Piece" style="object-position: 50% 60%;">
        <div class="product-body"><h3>Custom Made Two Piece</h3><p class="desc">Premium custom matching set.</p><strong class="price">R2199.99</strong>
          <div class="sizes"><button class="size" onclick="pick(this)">S</button><button class="size" onclick="pick(this)">M</button><button class="size" onclick="pick(this)">L</button><button class="size" onclick="pick(this)">XL</button></div>
          <button class="btn add" onclick="add('Custom Made Two Piece',2199.99,this)">ADD TO CART</button>
        </div>
      </article>

      <!-- 5. Embroidered Skull Cap - R149.99 (image: R149.99) -->
      <article class="product">
        <img src="1000399691_3623029286173081780.webp" alt="Embroidered Skull Cap" style="object-position: 50% 70%;">
        <div class="product-body"><h3>Embroidered Skull Cap</h3><p class="desc">Premium embroidered cap.</p><strong class="price">R149.99</strong>
          <div class="sizes"><button class="size" onclick="pick(this)">ONE SIZE</button></div>
          <button class="btn add" onclick="add('Embroidered Skull Cap',149.99,this)">ADD TO CART</button>
        </div>
      </article>

      <!-- 6. Skull Cap 2 Pack - R219.99 (image: R219.99 for 2) -->
      <article class="product">
        <img src="1000420435_1925724463650737048.webp" alt="Skull Cap 2 Pack" style="object-position: 50% 80%;">
        <div class="product-body"><h3>Skull Cap — 2 Pack</h3><p class="desc">Two embroidered caps.</p><strong class="price">R219.99</strong>
          <div class="sizes"><button class="size" onclick="pick(this)">ONE SIZE</button></div>
          <button class="btn add" onclick="add('Skull Cap 2 Pack',219.99,this)">ADD TO CART</button>
        </div>
      </article>

    </div>
  </div>
</section>

<section id="story">
  <div class="wrap story">
    <img src="1000473890_5453315045728938415.webp" alt="Throne Garments campaign">
    <div><div class="title"><small>THE BRAND</small><h2>Built for comfort.<br>Made to last.</h2></div>
      <p>Throne Garments is premium streetwear built around bold designs, quality construction and standout embroidery. Every piece is made to help you wear your crown with confidence.</p>
      <a class="btn" href="#contact">WORK WITH US</a>
    </div>
  </div>
</section>

<section class="checkout" id="checkout">
  <div class="wrap checkout-grid">
    <div><div class="title"><small>ORDER</small><h2>Checkout</h2><p>Review your order and send it directly to WhatsApp.</p></div>
      <form onsubmit="checkout(event)">
        <input id="name" required placeholder="Full name">
        <input id="phone" required placeholder="WhatsApp number">
        <input id="address" required placeholder="Delivery address">
        <button class="btn" type="submit">SEND ORDER ON WHATSAPP</button>
      </form>
    </div>
    <div class="summary"><h2>Order Summary</h2><div id="summary"><p class="empty">Your cart is empty.</p></div></div>
  </div>
</section>

<section class="contact" id="contact">
  <div class="wrap contact-grid">
    <div><div class="title"><small>CONNECT</small><h2>Let's Talk</h2></div>
      <p>For orders, custom garments and business enquiries:</p>
      <p>WhatsApp: <a href="https://wa.me/27677719518">+27 67 771 9518</a></p>
      <p>Socials: Instagram · TikTok</p>
    </div>
    <form onsubmit="contactForm(event)">
      <input required placeholder="Your name"><input type="email" required placeholder="Email address"><textarea required placeholder="Your message"></textarea><button class="btn" type="submit">SEND MESSAGE</button>
    </form>
  </div>
</section>

<footer>© 2026 Throne Garments · Wear Your Crown.</footer>

<div class="drawer" id="drawer"><div class="drawer-head"><h2>Your Cart</h2><button class="close" onclick="closeCart()">×</button></div>
  <div id="cartItems"></div><div class="cart-total">Total: R<span id="total">0.00</span></div>
  <a class="btn" href="#checkout" onclick="closeCart()">CHECKOUT</a>
</div>

<script>
  let cart=[];
  const WHATSAPP="27677719518";
  function pick(b){ b.parentElement.querySelectorAll('.size').forEach(x=>x.classList.remove('selected')); b.classList.add('selected'); }
  function add(name,price,b){
    const selected=b.previousElementSibling.querySelector('.selected');
    if(!selected){ alert('Please select a size first.'); return; }
    const size=selected.textContent;
    const item=cart.find(x=>x.name===name&&x.size===size);
    if(item) item.qty++; else cart.push({name,price,size,qty:1});
    render(); openCart();
  }
  function change(i,n){ cart[i].qty+=n; if(cart[i].qty<1) cart.splice(i,1); render(); }
  function render(){
    let count=0,total=0;
    const box=document.getElementById('cartItems'), sum=document.getElementById('summary');
    if(!cart.length){ box.innerHTML='<p class="empty">Your cart is empty.</p>'; sum.innerHTML='<p class="empty">Your cart is empty.</p>'; }
    else {
      box.innerHTML=cart.map((x,i)=>{ count+=x.qty; total+=x.price*x.qty; return `<div class="cart-item"><div class="cart-row"><b>${x.name}</b><b>R${(x.price*x.qty).toFixed(2)}</b></div><small>Size: ${x.size}</small><div class="qty"><button onclick="change(${i},-1)">−</button> ${x.qty} <button onclick="change(${i},1)">+</button></div></div>`; }).join('');
      sum.innerHTML=cart.map(x=>`<div class="summary-row"><span>${x.name} (${x.size}) × ${x.qty}</span><b>R${(x.price*x.qty).toFixed(2)}</b></div>`).join('')+`<div class="summary-total">Total: R${total.toFixed(2)}</div>`;
    }
    document.getElementById('count').textContent=count; document.getElementById('total').textContent=total.toFixed(2);
  }
  function openCart(){ document.getElementById('drawer').classList.add('open'); }
  function closeCart(){ document.getElementById('drawer').classList.remove('open'); }
  function checkout(e){
    e.preventDefault(); if(!cart.length){ alert('Your cart is empty.'); return; }
    const name=document.getElementById('name').value, phone=document.getElementById('phone').value, address=document.getElementById('address').value;
    const total=cart.reduce((s,x)=>s+x.price*x.qty,0);
    const items=cart.map(x=>`• ${x.name} | ${x.size} | Qty ${x.qty} | R${(x.price*x.qty).toFixed(2)}`).join('\\n');
    const msg=`Hello Throne Garments!\\n\\nI would like to order:\\n${items}\\n\\nTOTAL: R${total.toFixed(2)}\\n\\nName: ${name}\\nPhone: ${phone}\\nDelivery address: ${address}`;
    window.open(`https://wa.me/${WHATSAPP}?text=${encodeURIComponent(msg)}`,'_blank');
  }
  function contactForm(e){ e.preventDefault(); alert('Thanks! Your message has been sent (demo).'); }
  render();
</script>
</body>
</html>