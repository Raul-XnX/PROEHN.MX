<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Raúl Vargas Zalazar — Pro Enhanced Nutrition</title>
  <meta name="description" content="Entrenamiento de fuerza, aumento de masa muscular, pérdida de grasa, nutrición y salud hormonal. Pro Enhanced Nutrition." />

  <style>
    :root{
      --bg:#ffffff;
      --text:#0b0f16;
      --muted:#5b6573;
      --panel:#f6f7fb;
      --line: rgba(11,15,22,.10);

      --orange:#ff6a00;
      --orange2:#ff9a3d;

      --radius:18px;
      --shadow: 0 14px 30px rgba(11,15,22,.10);
      --max:1100px;
      --mono: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
      --sans: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji","Segoe UI Emoji";
    }
    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{
      margin:0;
      font-family:var(--sans);
      color:var(--text);
      background:
        radial-gradient(900px 500px at 20% -10%, rgba(255,106,0,.10), transparent 55%),
        radial-gradient(900px 500px at 90% 10%, rgba(11,15,22,.06), transparent 55%),
        var(--bg);
    }
    a{color:inherit; text-decoration:none}
    .wrap{max-width:var(--max); margin:0 auto; padding:26px 18px 74px}

    /* NAV */
    .nav{
      position:sticky; top:0; z-index:50;
      backdrop-filter: blur(10px);
      background: rgba(255,255,255,.78);
      border-bottom:1px solid rgba(11,15,22,.08);
    }
    .nav-inner{
      max-width:var(--max); margin:0 auto; padding:14px 18px;
      display:flex; align-items:center; justify-content:space-between; gap:14px;
    }
    .brand{display:flex; align-items:center; gap:10px}
    .badge{
      width:38px; height:38px; border-radius:14px;
      background: linear-gradient(135deg, var(--orange), var(--orange2));
      color:white;
      display:grid; place-items:center;
      font-family:var(--mono);
      font-weight:900;
      box-shadow: 0 10px 22px rgba(255,106,0,.20);
    }
    .brand h1{font-size:14px; margin:0; letter-spacing:.2px}
    .brand p{margin:0; font-size:12px; color:var(--muted)}

    .links{display:flex; flex-wrap:wrap; gap:10px; align-items:center; justify-content:flex-end}
    .pill{
      padding:10px 12px; border-radius:999px;
      border:1px solid rgba(11,15,22,.12);
      background: rgba(255,255,255,.9);
      color:var(--text);
      font-size:13px;
    }
    .pill:hover{border-color:rgba(255,106,0,.35)}
    .cta{
      padding:10px 14px; border-radius:999px;
      border:1px solid rgba(255,106,0,.35);
      background: linear-gradient(135deg, rgba(255,106,0,.14), rgba(255,154,61,.10));
      box-shadow: 0 12px 28px rgba(255,106,0,.12);
      font-weight:800;
    }
    .cta:hover{border-color:rgba(255,106,0,.55)}

    /* HERO */
    .hero{
      padding:30px 0 16px;
      display:grid; grid-template-columns: 1.2fr .8fr; gap:16px;
      align-items:stretch;
    }
    @media (max-width: 900px){ .hero{grid-template-columns:1fr} }

    .card{
      background: rgba(255,255,255,.92);
      border: 1px solid rgba(11,15,22,.10);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      overflow:hidden;
    }
    .hero-main{padding:26px}
    .kicker{
      display:inline-flex; gap:10px; align-items:center;
      font-family:var(--mono);
      font-size:12px;
      letter-spacing:.4px;
      border-radius:999px;
      padding:8px 10px;
      border:1px solid rgba(255,106,0,.25);
      background: rgba(255,106,0,.08);
      color:#8a3a00;
    }
    .kicker .dot{
      width:8px; height:8px; border-radius:99px;
      background: var(--orange);
      box-shadow: 0 0 0 4px rgba(255,106,0,.14);
    }
    .hero h2{
      margin:16px 0 10px;
      font-size:42px;
      line-height:1.06;
      letter-spacing:-.6px;
    }
    @media (max-width: 520px){ .hero h2{font-size:32px} }
    .hero p{
      margin:0;
      color: var(--muted);
      font-size:16px;
      line-height:1.6;
      max-width: 72ch;
    }
    .hero-actions{display:flex; gap:12px; flex-wrap:wrap; margin-top:18px}
    .btn{
      padding:12px 16px; border-radius:14px;
      border:1px solid rgba(11,15,22,.12);
      background: rgba(255,255,255,.95);
      color:var(--text);
      font-weight:800;
      display:inline-flex; gap:10px; align-items:center;
      cursor:pointer;
    }
    .btn:hover{border-color:rgba(255,106,0,.40)}
    .btn.primary{
      border-color: rgba(255,106,0,.40);
      background: linear-gradient(135deg, rgba(255,106,0,.14), rgba(255,154,61,.10));
      box-shadow: 0 14px 28px rgba(255,106,0,.12);
    }

    .hero-side{padding:18px; display:flex; flex-direction:column; gap:12px}
    .photo{
      position:relative;
      border-radius: 18px;
      overflow:hidden;
      border:1px solid rgba(11,15,22,.10);
      background: #fff;
    }
    .photo img{
      width:100%;
      height: 320px;
      object-fit: cover;
      display:block;
    }
    .photo .cap{
      position:absolute; left:12px; bottom:12px;
      padding:10px 12px;
      border-radius: 14px;
      border:1px solid rgba(255,106,0,.30);
      background: rgba(255,255,255,.92);
      font-weight:900;
    }
    .mini{
      padding:14px 14px;
      border:1px solid rgba(11,15,22,.10);
      border-radius:16px;
      background: var(--panel);
    }
    .mini .t{font-size:12px; color:var(--muted); margin:0}
    .mini .v{margin:8px 0 0; font-weight:900}

    /* SECCIONES */
    section{padding-top:24px}
    .section-title{
      display:flex; justify-content:space-between; align-items:flex-end; gap:14px;
      margin: 18px 0 10px;
    }
    .section-title h3{
      margin:0; font-size:20px;
      display:inline-flex; align-items:center; gap:10px;
    }
    .section-title h3 .mark{
      width:10px; height:10px; border-radius:99px;
      background: var(--orange);
      box-shadow: 0 0 0 5px rgba(255,106,0,.12);
    }
    .section-title p{margin:0; color:var(--muted); font-size:13px}

    .grid{display:grid; grid-template-columns: repeat(12, 1fr); gap:16px; margin-top:18px}
    .panel{padding:18px}
    .span-12{grid-column: span 12}
    .span-8{grid-column: span 8}
    .span-6{grid-column: span 6}
    .span-4{grid-column: span 4}
    @media (max-width: 900px){
      .span-6,.span-4,.span-8{grid-column: span 12}
    }

    .item{
      padding:14px; border-radius:16px;
      border:1px solid rgba(11,15,22,.10);
      background: var(--panel);
    }
    .item h4{margin:0 0 6px; font-size:15px}
    .item p{margin:0; color:var(--muted); font-size:13px; line-height:1.55}

    .tagrow{display:flex; flex-wrap:wrap; gap:8px; margin-top:10px}
    .tag{
      font-size:12px;
      border:1px solid rgba(255,106,0,.22);
      padding:6px 10px; border-radius:999px;
      background: rgba(255,106,0,.08);
      color:#8a3a00;
      font-family:var(--mono);
    }

    /* FORM */
    .form{display:grid; gap:10px}
    input, textarea{
      width:100%;
      padding:12px 12px;
      border-radius:14px;
      border:1px solid rgba(11,15,22,.12);
      background: rgba(255,255,255,.95);
      color: var(--text);
      outline:none;
      font: inherit;
    }
    textarea{min-height:120px; resize:vertical}
    input:focus, textarea:focus{
      border-color: rgba(255,106,0,.55);
      box-shadow: 0 0 0 4px rgba(255,106,0,.12);
    }

    .footer{
      margin-top:30px;
      padding-top:18px;
      border-top:1px solid rgba(11,15,22,.10);
      color:var(--muted);
      font-size:13px;
      display:flex; justify-content:space-between; gap:12px; flex-wrap:wrap;
    }
    .mono{font-family:var(--mono)}
    .small{font-size:12px; color:var(--muted)}
  </style>
</head>

<body>
  <div class="nav">
    <div class="nav-inner">
      <div class="brand">
        <div class="badge">PRO EHN</div>
        <div>
          <h1>Raúl Vargas Zalazar</h1>
          <p>Pro Enhanced Nutrition · Fuerza · Hipertrofia · Pérdida de grasa</p>
        </div>
      </div>

      <div class="links">
        <a class="pill" href="#sobre">Sobre mí</a>
        <a class="pill" href="#servicios">Servicios</a>
        <a class="pill" href="#contacto">Contacto</a>

        <!-- Instagram en menú -->
        <a class="pill" href="https://www.instagram.com/raulvargas_proehn" target="_blank" rel="noopener">Instagram</a>

        <!-- WhatsApp en menú -->
        <a class="cta" href="https://wa.me/5218132216529" target="_blank" rel="noopener">WhatsApp</a>
      </div>
    </div>
  </div>

  <main class="wrap">
    <div class="hero">
      <div class="card hero-main">
        <div class="kicker"><span class="dot"></span> Pro Enhanced Nutrition · Planes personalizados</div>

        <h2>Entrenamiento + nutrición para ganar músculo y perder grasa sin humo.</h2>

        <p>
          Enfoque directo: evaluación → plan individualizado → seguimiento → ajustes.
          Entrenamiento de fuerza, aumento de masa muscular, pérdida de grasa y optimización hormonal con nutrición.
        </p>

        <div class="hero-actions">
          <a class="btn primary" href="#servicios">Ver servicios</a>
          <a class="btn"
             href="https://wa.me/5218132216529?text=Hola%20Ra%C3%BAl%2C%20quiero%20una%20evaluaci%C3%B3n%20para%20masa%20muscular%20/%20p%C3%A9rdida%20de%20grasa%20/%20salud%20hormonal.%20Mis%20datos%3A%20edad%2C%20estatura%2C%20peso%2C%20d%C3%ADas%20que%20entreno%20y%20objetivo."
             target="_blank" rel="noopener">
            Agendar evaluación (WhatsApp)
          </a>
        </div>

        <p class="small" style="margin-top:14px">
          <span class="mono">Correo:</span>
          <a href="mailto:Pro.Enhanced.Nutrition@gmail.com">Pro.Enhanced.Nutrition@gmail.com</a>
        </p>
      </div>

      <div class="card hero-side">
        <div class="photo">
          <div class="cap">Raúl Vargas · PRO EHN</div>
        </div>

        <div class="mini">
          <p class="t">Servicios principales</p>
          <p class="v">Masa muscular · Pérdida de grasa · Salud hormonal</p>
        </div>
      </div>
    </div>

    <section id="sobre">
      <div class="section-title">
        <h3><span class="mark"></span> Sobre mí</h3>
        <p>Cómo trabajo contigo</p>
      </div>

      <div class="grid">
        <div class="card panel span-8">
          <p style="margin:0; color:var(--muted); line-height:1.7">
            Soy <strong>Raúl Vargas Zalazar</strong>, fundador de <strong>Pro Enhanced Nutrition</strong>.
            Te acompaño con estructura, métricas y seguimiento para lograr recomposición corporal y rendimiento.
            <br><br>
            Sistema simple: evaluación → plan → seguimiento → ajustes.
          </p>
          <div class="tagrow">
            <span class="tag">Fuerza</span>
            <span class="tag">Hipertrofia</span>
            <span class="tag">Pérdida de grasa</span>
            <span class="tag">Nutrición</span>
          </div>
        </div>

        <div class="card panel span-4">
          <div class="item">
            <h4>Qué vas a notar</h4>
            <p>Claridad, estructura y progreso real (sin improvisar).</p>
          </div>
          <div class="item" style="margin-top:10px">
            <h4>Cómo medimos</h4>
            <p>Fuerza, RPE/RIR, peso, perímetros y adherencia.</p>
          </div>
          <div class="item" style="margin-top:10px">
            <h4>Objetivo</h4>
            <p>Resultados sostenibles con rendimiento y salud.</p>
          </div>
        </div>
      </div>
    </section>

    <section id="servicios">
      <div class="section-title">
        <h3><span class="mark"></span> Servicios</h3>
        <p>Elige tu objetivo y arrancamos</p>
      </div>

      <div class="grid">
        <div class="card panel span-4">
          <div class="item">
            <h4>Aumento de masa muscular</h4>
            <p>Hipertrofia con progresión, técnica, recuperación y nutrición enfocada a crecer.</p>
          </div>
        </div>

        <div class="card panel span-4">
          <div class="item">
            <h4>Pérdida de grasa corporal</h4>
            <p>Déficit inteligente sin destruir rendimiento: adherencia, NEAT y ajustes semanales.</p>
          </div>
        </div>

        <div class="card panel span-4">
          <div class="item">
            <h4>Optimizar salud hormonal</h4>
            <p>Nutrición + suplementación puntual para apoyar energía, sueño y recuperación.</p>
          </div>
        </div>
      </div>
    </section>

    <section id="contacto">
      <div class="section-title">
        <h3><span class="mark"></span> Contacto</h3>
        <p>WhatsApp · Instagram · Correo</p>
      </div>

      <div class="grid">
        <div class="card panel span-6">
          <form class="form" onsubmit="sendMail(event)">
            <input id="name" placeholder="Tu nombre" required />
            <input id="email" type="email" placeholder="Tu correo" required />
            <textarea id="msg" placeholder="Objetivo + experiencia + días de entrenamiento + tiempo disponible" required></textarea>
            <button class="btn primary" type="submit">Enviar correo</button>
            <div class="small">Para respuesta inmediata: WhatsApp.</div>
          </form>
        </div>

        <div class="card panel span-6">
          <div class="item">
            <h4>1) WhatsApp</h4>
            <p><a class="mono" href="https://wa.me/5218132216529" target="_blank" rel="noopener">wa.me/5218132216529</a></p>
          </div>

          <div class="item" style="margin-top:10px">
            <h4>2) Instagram</h4>
            <p><a class="mono" href="https://www.instagram.com/raulvargas_proehn" target="_blank" rel="noopener">@raulvargas_proehn</a></p>
          </div>

          <div class="item" style="margin-top:10px">
            <h4>3) Correo</h4>
            <p><a class="mono" href="mailto:Pro.Enhanced.Nutrition@gmail.com">Pro.Enhanced.Nutrition@gmail.com</a></p>
          </div>
        </div>
      </div>

      <!-- Footer con los 3 datos nuevamente -->
      <div class="footer">
        <div>© <span id="year"></span> Pro Enhanced Nutrition — Raúl Vargas Zalazar</div>
        <div class="mono">
          <a href="https://wa.me/5218132216529" target="_blank" rel="noopener">WhatsApp</a>
          ·
          <a href="https://www.instagram.com/raulvargas_proehn" target="_blank" rel="noopener">Instagram</a>
          ·
          <a href="mailto:Pro.Enhanced.Nutrition@gmail.com">Correo</a>
        </div>
      </div>
    </section>
  </main>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();

    function sendMail(e){
      e.preventDefault();
      const name = document.getElementById("name").value.trim();
      const email = document.getElementById("email").value.trim();
      const msg = document.getElementById("msg").value.trim();
      const subject = encodeURIComponent("Contacto — Pro Enhanced Nutrition (" + name + ")");
      const body = encodeURIComponent(`Nombre: ${name}\nCorreo: ${email}\n\nMensaje:\n${msg}`);
      window.location.href = `mailto:Pro.Enhanced.Nutrition@gmail.com?subject=${subject}&body=${body}`;
    }
  </script>
</body>
</html>
