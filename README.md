# My-first-website-
<!doctype html>
<html lang="tl">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Pangalan ng Negosyo / Website</title>
  <meta name="description" content="Simpleng modern website template — copy paste lang.">
  <!-- Basic SEO -->
  <meta name="author" content="Iyong Pangalan">
  <!-- Favicon (simple SVG data URI) -->
  <link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='0.9em' font-size='90'>🌟</text></svg>">
  <!-- Styles (all in one file for easy copy/paste) -->
  <style>
    :root{
      --bg:#0f1724;
      --card:#0b1220;
      --muted:#94a3b8;
      --accent:#7c3aed; /* purple-ish accent, change as needed */
      --glass: rgba(255,255,255,0.04);
      --radius:12px;
      --fw-regular: 400;
      --fw-bold: 700;
      --max-w:1100px;
      color-scheme: dark;
    }
    /* Reset */
    *{box-sizing:border-box;margin:0;padding:0}
    html,body{height:100%}
    body{
      font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background: linear-gradient(180deg,#071028 0%, #0b1220 100%);
      color:#e6eef8;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
      padding:32px;
      display:flex;
      justify-content:center;
    }
    .container{
      width:100%;
      max-width:var(--max-w);
      margin:0 auto;
    }

    /* NAV */
    .nav{
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:16px;
      margin-bottom:28px;
    }
    .brand{
      display:flex;
      align-items:center;
      gap:12px;
      text-decoration:none;
      color:inherit;
    }
    .logo{
      width:44px;height:44px;border-radius:10px;background:linear-gradient(135deg,var(--accent),#4f46e5);display:flex;align-items:center;justify-content:center;font-size:20px;
      box-shadow:0 6px 18px rgba(124,58,237,0.18);
    }
    .nav-links{
      display:flex;
      gap:18px;
      align-items:center;
    }
    .nav-links a{
      color:var(--muted);
      text-decoration:none;
      font-weight:600;
      font-size:15px;
    }
    .cta{
      background:linear-gradient(90deg,var(--accent),#5b21b6);
      padding:10px 14px;border-radius:10px;text-decoration:none;font-weight:700;
      box-shadow:0 6px 20px rgba(92,33,182,0.18);
      color:white;
    }

    /* Mobile menu button */
    .menu-btn{display:none;background:transparent;border:0;color:var(--muted);font-size:20px}
    /* HERO */
    .hero{
      display:grid;
      grid-template-columns:1fr 380px;
      gap:28px;
      align-items:stretch;
      margin-bottom:36px;
    }
    .card{
      background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      border-radius:var(--radius);
      padding:28px;
      box-shadow: 0 8px 30px rgba(2,6,23,0.6);
    }
    .hero-left h1{
      font-size:36px;
      margin-bottom:12px;
      letter-spacing:-0.6px;
    }
    .hero-left p{color:var(--muted);margin-bottom:18px}
    .buttons{display:flex;gap:12px;margin-top:12px}
    .btn{
      padding:10px 14px;border-radius:10px;text-decoration:none;font-weight:700;border:1px solid rgba(255,255,255,0.04);
      background:transparent;color:#fff;
    }

    /* Features */
    .features{
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:14px;
      margin-top:18px;
    }
    .feature{
      background:var(--glass);
      border-radius:12px;padding:14px;
    }
    .feature h3{margin-bottom:6px;font-size:16px}
    .feature p{color:var(--muted);font-size:14px}

    /* Right column - quick card */
    .quick{
      display:flex;flex-direction:column;gap:14px;
    }
    .price{
      font-weight:800;font-size:28px;
    }
    .meta{color:var(--muted);font-size:14px}

    /* Gallery */
    .gallery{
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:12px;
      margin-top:22px;
    }
    .thumb{
      height:120px;border-radius:10px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      display:flex;align-items:center;justify-content:center;color:var(--muted);font-weight:700;
    }

    /* Contact section */
    .contact{
      display:grid;
      grid-template-columns:1fr 360px;
      gap:20px;
      margin-top:26px;
      align-items:start;
    }
    form label{display:block;margin-bottom:6px;font-weight:600}
    input[type="text"], input[type="email"], textarea{
      width:100%;padding:10px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit;margin-bottom:12px;
    }
    textarea{min-height:120px;resize:vertical}
    .form-actions{display:flex;gap:10px;align-items:center}
    .secondary{background:transparent;border:1px solid rgba(255,255,255,0.06);padding:10px 12px;border-radius:10px;color:var(--muted)}

    /* Footer */
    footer{margin-top:28px;color:var(--muted);font-size:14px;display:flex;justify-content:space-between;align-items:center}

    /* Responsive */
    @media (max-width:980px){
      .hero{grid-template-columns:1fr}
      .contact{grid-template-columns:1fr}
      .features{grid-template-columns:repeat(2,1fr)}
      .gallery{grid-template-columns:repeat(2,1fr)}
      .nav-links{display:none}
      .menu-btn{display:inline-block}
    }
    @media (max-width:560px){
      body{padding:18px}
      .features{grid-template-columns:1fr}
      .gallery{grid-template-columns:1fr}
      .hero-left h1{font-size:28px}
    }

    /* small helpers */
    .muted{color:var(--muted)}
    .small{font-size:13px;color:var(--muted)}
  </style>
</head>
<body>
  <div class="container">
    <!-- NAV -->
    <nav class="nav">
      <a class="brand" href="#">
        <div class="logo">★</div>
        <div>
          <div style="font-weight:800">BrandMo</div>
          <div class="small">simple • elegant</div>
        </div>
      </a>

      <div style="display:flex;align-items:center;gap:12px">
        <div class="nav-links" id="navLinks">
          <a href="#home">Home</a>
          <a href="#services">Serbisyo</a>
          <a href="#gallery">Gallery</a>
          <a href="#contact">Kontak</a>
        </div>
        <button class="menu-btn" id="menuBtn" aria-label="menu">☰</button>
        <a class="cta" href="#contact">Magpa-quote</a>
      </div>
    </nav>

    <!-- HERO -->
    <section id="home" class="hero">
      <div class="card hero-left">
        <h1>Gagawa kami ng website na business-ready.</h1>
        <p>Template na pwede mong i-copy/paste agad. Mobile responsive, mabilis, at madaling i-customize. Pwede kitang tulungan i-personalize kung gusto mo.</p>

        <div class="buttons">
          <a class="btn" href="#services">Tingnan ang Serbisyo</a>
          <a class="btn" href="mailto:hello@example.com?subject=Interest%20sa%20Website" aria-label="Email">Mag-email sa Amin</a>
        </div>

        <div class="features" style="margin-top:20px">
          <div class="feature">
            <h3>Responsive</h3>
            <p>Maganda sa mobile, tablet, at desktop.</p>
          </div>
          <div class="feature">
            <h3>Madaling i-edit</h3>
            <p>Isang file lang — palitan ang text at images.</p>
          </div>
          <div class="feature">
            <h3>Light & Fast</h3>
            <p>Simpleng CSS at maliit ang footprint.</p>
          </div>
        </div>
      </div>

      <aside class="card quick">
        <div>
          <div class="price">₱0 — or start at ₱5,000</div>
          <div class="meta small">Basic template: copy-paste. Custom work: contact for quote.</div>
        </div>

        <div style="margin-top:auto">
          <div style="font-weight:700;margin-bottom:8px">Quick info</div>
          <div class="small">Built: HTML + CSS + tiny JS</div>
          <div class="small">Editable: Open with any text editor</div>
        </div>
      </aside>
    </section>

    <!-- GALLERY -->
    <section id="gallery">
      <div class="card">
        <h2 style="margin-bottom:12px">Gallery / Sample</h2>
        <div class="gallery">
          <div class="thumb">Image 1</div>
          <div class="thumb">Image 2</div>
          <div class="thumb">Image 3</div>
          <div class="thumb">Image 4</div>
          <div class="thumb">Image 5</div>
          <div class="thumb">Image 6</div>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="contact">
      <div class="card">
        <h2>Kontakin mo kami</h2>
        <p class="muted">Ilagay ang detalye — lalabas ang email `mailto:` sa browser mo. Kung gusto mo ng backend form, pwede ko ring gawin (may dagdag na setup).</p>

        <form id="contactForm" onsubmit="return handleSubmit(event)">
          <label for="name">Pangalan</label>
          <input id="name" name="name" type="text" required placeholder="Juan dela Cruz">

          <label for="email">Email</label>
          <input id="email" name="email" type="email" required placeholder="name@example.com">

          <label for="message">Mensaheng gusto mong sabihin</label>
          <textarea id="message" name="message" required placeholder="Sabihin ang kailangan mo..."></textarea>

          <div class="form-actions">
            <button class="btn" type="submit">I-send</button>
            <button type="button" class="secondary" onclick="openEmail()">Buksan Email App</button>
          </div>
          <div id="formFeedback" class="small muted" style="margin-top:8px"></div>
        </form>
      </div>

      <aside class="card" style="height:fit-content">
        <h3 style="margin-bottom:6px">Address</h3>
        <div class="small">Makati / Manila / Philippines</div>
        <div style="height:12px"></div>
        <h3 style="margin-bottom:6px">Social</h3>
        <div class="small">IG: @example • FB: example</div>
        <div style="height:18px"></div>
        <h3 style="margin-bottom:6px">Hours</h3>
        <div class="small">Mon–Fri: 9:00–18:00</div>
      </aside>
    </section>

    <footer>
      <div>© <span id="year"></span> BrandMo. All rights reserved.</div>
      <div class="small muted">Built w/ ❤️ — Edit this template to match your brand.</div>
    </footer>
  </div>

  <!-- Minimal JS for interactivity -->
  <script>
    // set year
    document.getElementById('year').textContent = new Date().getFullYear();

    // mobile menu toggle
    const menuBtn = document.getElementById('menuBtn');
    const navLinks = document.getElementById('navLinks');
    menuBtn && menuBtn.addEventListener('click', () => {
      if(navLinks.style.display === 'flex'){
        navLinks.style.display = 'none';
      } else {
        navLinks.style.display = 'flex';
        navLinks.style.flexDirection = 'column';
        navLinks.style.position = 'absolute';
        navLinks.style.right = '32px';
        navLinks.style.top = '72px';
        navLinks.style.background = 'var(--card)';
        navLinks.style.padding = '12px';
        navLinks.style.borderRadius = '10px';
        navLinks.style.boxShadow = '0 8px 30px rgba(2,6,23,0.6)';
      }
    });

    // form handling: mailto fallback + inline feedback
    function openEmail(){
      const name = document.getElementById('name').value || '—';
      const email = document.getElementById('email').value || '—';
      const message = document.getElementById('message').value || '—';
      const subject = encodeURIComponent("Contact from website: " + name);
      const body = encodeURIComponent("Name: " + name + "%0AEmail: " + email + "%0A%0A" + message);
      window.location.href = "mailto:hello@example.com?subject=" + subject + "&body=" + body;
    }

    function handleSubmit(e){
      e.preventDefault();
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const message = document.getElementById('message').value.trim();
      const fb = document.getElementById('formFeedback');

      // minimal validation
      if(!name || !email || !message){
        fb.textContent = "Paki-fill ang lahat ng fields.";
        return false;
      }
      // Try mailto
      const subject = encodeURIComponent("Contact from website: " + name);
      const body = encodeURIComponent("Name: " + name + "\nEmail: " + email + "\n\n" + message);
      const mailto = "mailto:hello@example.com?subject=" + subject + "&body=" + body;

      fb.textContent = "Nagbubukas ng email client mo... (kung walang email client, click 'Buksan Email App')";
      // Short pause then open mailto (best effort)
      setTimeout(() => { window.location.href = mailto; }, 400);

      return false;
    }
  </script>
</body>
</html>