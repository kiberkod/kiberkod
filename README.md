<!DOCTYPE html>
<html lang="az">
<head>
  <meta charset="UTF-8" />
  <title>KiberKod MMC · GitHub Overview</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    :root {
      --bg: #050816;
      --bg-alt: #070b19;
      --card-bg: #0b1022;
      --border: rgba(255, 255, 255, 0.06);
      --accent: #4f46e5;
      --accent-soft: rgba(79, 70, 229, 0.15);
      --accent-2: #06b6d4;
      --text-main: #f9fafb;
      --text-muted: #9ca3af;
      --radius-xl: 18px;
      --shadow-soft: 0 18px 45px rgba(15, 23, 42, 0.7);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI",
        sans-serif;
      background: radial-gradient(circle at top, #111827 0, #020617 45%, #000 100%);
      color: var(--text-main);
      line-height: 1.6;
      padding: 32px 16px 48px;
    }

    .page {
      max-width: 1080px;
      margin: 0 auto;
    }

    .glass {
      border-radius: 24px;
      border: 1px solid rgba(148, 163, 184, 0.35);
      background: radial-gradient(circle at 0 0, rgba(148, 163, 184, 0.12), transparent 55%),
                  radial-gradient(circle at 100% 100%, rgba(56, 189, 248, 0.12), transparent 55%),
                  linear-gradient(135deg, rgba(15, 23, 42, 0.96), rgba(15, 23, 42, 0.93));
      box-shadow: var(--shadow-soft);
      padding: 32px 24px 28px;
      border-radius: 24px;
    }

    @media (min-width: 768px) {
      .glass {
        padding: 36px 32px 32px;
      }
    }

    .hero {
      display: flex;
      flex-direction: column;
      gap: 18px;
      margin-bottom: 28px;
    }

    .badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 4px 10px;
      border-radius: 999px;
      font-size: 12px;
      background: rgba(15, 23, 42, 0.85);
      border: 1px solid rgba(148, 163, 184, 0.6);
      color: var(--text-muted);
    }

    .badge-dot {
      width: 8px;
      height: 8px;
      border-radius: 999px;
      background: radial-gradient(circle at 30% 30%, #22c55e, #15803d);
      box-shadow: 0 0 0 4px rgba(34, 197, 94, 0.18);
    }

    .hero-title {
      font-size: clamp(2.1rem, 3vw, 2.6rem);
      font-weight: 700;
      letter-spacing: 0.03em;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 10px;
    }

    .hero-title span.logo {
      padding: 6px 12px;
      border-radius: 999px;
      background: radial-gradient(circle at 0 0, rgba(59, 130, 246, 0.3), transparent 60%),
                  radial-gradient(circle at 100% 100%, rgba(56, 189, 248, 0.25), transparent 60%);
      border: 1px solid rgba(129, 140, 248, 0.6);
      font-size: 0.9em;
    }

    .gradient-text {
      background: linear-gradient(120deg, #e5e7eb, #a5b4fc, #22d3ee);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    .hero-subtitle {
      max-width: 620px;
      font-size: 0.98rem;
      color: var(--text-muted);
    }

    .hero-subtitle strong {
      color: #e5e7eb;
      font-weight: 600;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 6px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      padding: 9px 16px;
      border-radius: 999px;
      font-size: 0.9rem;
      font-weight: 500;
      border: 1px solid transparent;
      cursor: pointer;
      text-decoration: none;
      transition: transform 0.1s ease, box-shadow 0.1s ease, background 0.15s ease,
        border-color 0.15s ease, color 0.15s ease;
      white-space: nowrap;
    }

    .btn-primary {
      background: radial-gradient(circle at 0 0, #4f46e5, #1d4ed8);
      color: white;
      box-shadow: 0 16px 30px rgba(37, 99, 235, 0.4);
    }

    .btn-primary:hover {
      transform: translateY(-1px);
      box-shadow: 0 18px 40px rgba(37, 99, 235, 0.55);
    }

    .btn-ghost {
      background: rgba(15, 23, 42, 0.75);
      border-color: rgba(148, 163, 184, 0.6);
      color: var(--text-muted);
    }

    .btn-ghost:hover {
      background: rgba(15, 23, 42, 0.9);
      border-color: rgba(148, 163, 184, 0.9);
      color: #e5e7eb;
    }

    .pill-icon {
      width: 18px;
      height: 18px;
      border-radius: 999px;
      border: 1px solid rgba(148, 163, 184, 0.7);
      display: inline-flex;
      align-items: center;
      justify-content: center;
      font-size: 11px;
      background: radial-gradient(circle at 30% 30%, rgba(248, 250, 252, 0.12), transparent 60%);
    }

    .layout-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.5fr) minmax(0, 1.1fr);
      gap: 20px;
    }

    @media (max-width: 900px) {
      .layout-grid {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .card {
      background: rgba(15, 23, 42, 0.9);
      border-radius: var(--radius-xl);
      border: 1px solid rgba(148, 163, 184, 0.35);
      padding: 18px 18px 16px;
      position: relative;
      overflow: hidden;
    }

    .card::before {
      content: "";
      position: absolute;
      inset: -40%;
      background: radial-gradient(circle at 0 0, rgba(59, 130, 246, 0.1), transparent 60%);
      opacity: 0.7;
      pointer-events: none;
    }

    .card-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      margin-bottom: 8px;
      position: relative;
      z-index: 1;
    }

    .card-title {
      font-size: 0.95rem;
      font-weight: 600;
      letter-spacing: 0.04em;
      text-transform: uppercase;
      color: #9ca3af;
    }

    .card-tag {
      padding: 3px 8px;
      border-radius: 999px;
      font-size: 11px;
      border: 1px solid rgba(148, 163, 184, 0.6);
      background: rgba(15, 23, 42, 0.7);
      color: #e5e7eb;
    }

    .projects-grid {
      display: grid;
      gap: 10px;
      position: relative;
      z-index: 1;
    }

    .project-item {
      padding: 10px 11px;
      border-radius: 14px;
      border: 1px solid rgba(148, 163, 184, 0.45);
      background: radial-gradient(circle at 0 0, rgba(59, 130, 246, 0.12), transparent 55%),
                  rgba(15, 23, 42, 0.95);
      display: flex;
      flex-direction: column;
      gap: 3px;
    }

    .project-name {
      font-size: 0.92rem;
      font-weight: 600;
      display: inline-flex;
      align-items: center;
      gap: 6px;
    }

    .project-badge {
      font-size: 10px;
      padding: 2px 7px;
      border-radius: 999px;
      border: 1px solid rgba(129, 140, 248, 0.7);
      background: rgba(79, 70, 229, 0.12);
      text-transform: uppercase;
      letter-spacing: 0.1em;
      color: #c7d2fe;
    }

    .project-desc {
      font-size: 0.82rem;
      color: var(--text-muted);
    }

    .stack-list,
    .principles-list {
      list-style: none;
      display: grid;
      gap: 6px;
      margin-top: 6px;
      font-size: 0.86rem;
    }

    .stack-pill {
      padding: 5px 8px;
      border-radius: 999px;
      border: 1px solid rgba(148, 163, 184, 0.5);
      display: inline-flex;
      align-items: center;
      gap: 6px;
      margin: 2px 4px 2px 0;
      font-size: 0.8rem;
      color: var(--text-muted);
      background: rgba(15, 23, 42, 0.9);
    }

    .stack-pill-dot {
      width: 6px;
      height: 6px;
      border-radius: 999px;
      background: var(--accent-2);
    }

    .stack-row {
      margin-top: 4px;
      margin-bottom: 4px;
    }

    .stack-heading {
      font-size: 0.8rem;
      text-transform: uppercase;
      letter-spacing: 0.14em;
      color: #6b7280;
      margin-bottom: 4px;
    }

    .code-block {
      margin-top: 8px;
      padding: 9px 10px;
      border-radius: 14px;
      background: #020617;
      border: 1px solid rgba(30, 64, 175, 0.9);
      font-family: SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono",
        "Courier New", monospace;
      font-size: 0.76rem;
      color: #e5e7eb;
      overflow-x: auto;
      white-space: pre;
    }

    .footer {
      margin-top: 18px;
      padding-top: 12px;
      border-top: 1px dashed rgba(148, 163, 184, 0.5);
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      justify-content: space-between;
      font-size: 0.8rem;
      color: var(--text-muted);
    }

    .footer-links {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .footer a {
      color: #93c5fd;
      text-decoration: none;
    }

    .footer a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <main class="page">
    <section class="glass">
      <!-- HERO -->
      <header class="hero">
        <div class="badge">
          <span class="badge-dot"></span>
          GitHub · KiberKod MMC · Public Overview
        </div>

        <h1 class="hero-title">
          <span class="logo">KiberKod MMC</span>
          <span class="gradient-text">Lokal, təhlükəsiz & miqyaslana bilən həllər</span>
        </h1>

        <p class="hero-subtitle">
          <strong>KiberKod</strong> – real biznes proseslərini rəqəmsallaşdıran,
          on-prem və cloud əsaslı sistemlər quran inkişaf studiyasıdır:
          POS & kassa, LMS, ERP, inteqrasiya olunmuş ödəniş, AI & OCR servisləri
          və daha çoxu.
        </p>

        <div class="hero-actions">
          <a
            class="btn btn-primary"
            href="https://github.com/kiberkod"
            target="_blank"
            rel="noreferrer"
          >
            <span class="pill-icon">GH</span>
            GitHub təşkilatına keç
          </a>
          <a class="btn btn-ghost" href="mailto:contact@kiberkod.az">
            <span class="pill-icon">✉</span>
            Bizimlə əlaqə saxla
          </a>
        </div>
      </header>

      <!-- GRID LAYOUT -->
      <section class="layout-grid">
        <!-- LEFT: PROJECTS -->
        <article class="card">
          <div class="card-header">
            <div>
              <div class="card-title">Layihələr & Ekosistem</div>
            </div>
            <span class="card-tag">Real-case əsaslı həllər</span>
          </div>

          <div class="projects-grid">
            <div class="project-item">
              <div class="project-name">
                POSNET
                <span class="project-badge">POS / Kassa</span>
              </div>
              <p class="project-desc">
                Restoran, kafe, market, aptek və digər sahələr üçün çox-sahəli POS & kassa platforması.
                Multi-tenant arxitektura, çoxdilli interfeys, region əsaslı vergi qaydaları və inteqrasiya
                olunan ödəniş sistemləri (kart, onlayn satış, e-kassa inteqrasiyası üçün hazır baza).
              </p>
            </div>

            <div class="project-item">
              <div class="project-name">
                Sina LMS
                <span class="project-badge">Təhsil / LMS</span>
              </div>
              <p class="project-desc">
                Onlayn kurslar, tapşırıqlar, imtahanlar və sertifikatlar üçün LMS platforması.
                Müəllim & tələbə panelləri, video hostinq, sertifikat generasiyası və
                modullar üzrə analitika ilə tədris prosesini tam izləməyə imkan verir.
              </p>
            </div>

            <div class="project-item">
              <div class="project-name">
                Globix
                <span class="project-badge">ERP / Biznes</span>
              </div>
              <p class="project-desc">
                Logistika, mühasibatlıq və əməliyyat proseslərini vahid məkanda birləşdirən
                biznes idarəetmə həlli. Maliyyə axınları, hesabatlar, müştəri və müqavilə
                idarəetməsi üçün modul struktur.
              </p>
            </div>

            <div class="project-item">
              <div class="project-name">
                KiberKod Core Tools
                <span class="project-badge">DevTools</span>
              </div>
              <p class="project-desc">
                Daxili kitabxanalar, UI komponentləri, mikroservis şablonları və
                infra skriptləri. Bütün ekosistem üzrə eyni standartları qorumaq üçün
                istifadə olunan paylaşılan kod bazası.
              </p>
            </div>
          </div>
        </article>

        <!-- RIGHT: STACK + PRINCIPLES + STRUCTURE -->
        <article class="card">
          <div class="card-header">
            <div>
              <div class="card-title">Texnoloji Stack & Prinsiplər</div>
            </div>
            <span class="card-tag">Modern arxitektura</span>
          </div>

          <!-- STACK -->
          <div class="stack-row">
            <div class="stack-heading">Backend</div>
            <div>
              <span class="stack-pill">
                <span class="stack-pill-dot"></span> Laravel / PHP
              </span>
              <span class="stack-pill">
                <span class="stack-pill-dot"></span> Python · FastAPI
              </span>
              <span class="stack-pill">
                <span class="stack-pill-dot"></span> Node.js · Inteqrasiyalar
              </span>
            </div>
          </div>

          <div class="stack-row">
            <div class="stack-heading">Frontend</div>
            <div>
              <span class="stack-pill">
                <span class="stack-pill-dot"></span> Vue / Nuxt
              </span>
              <span class="stack-pill">
                <span class="stack-pill-dot"></span> React / Next
              </span>
              <span class="stack-pill">
                <span class="stack-pill-dot"></span> Tailwind CSS · Modern UI
              </span>
            </div>
          </div>

          <div class="stack-row">
            <div class="stack-heading">Infra & Data</div>
            <div>
              <span class="stack-pill">
                <span class="stack-pill-dot"></span> Proxmox · Ubuntu
              </span>
              <span class="stack-pill">
                <span class="stack-pill-dot"></span> Docker & Nginx
              </span>
              <span class="stack-pill">
                <span class="stack-pill-dot"></span> PostgreSQL / MySQL
              </span>
              <span class="stack-pill">
                <span class="stack-pill-dot"></span> MinIO · Redis
              </span>
            </div>
          </div>

          <div class="stack-row">
            <div class="stack-heading">AI & OCR</div>
            <div>
              <span class="stack-pill">
                <span class="stack-pill-dot"></span> OCR (Tesseract / PaddleOCR)
              </span>
              <span class="stack-pill">
                <span class="stack-pill-dot"></span> LLM əsaslı sənəd analizi
              </span>
            </div>
          </div>

          <!-- PRINCIPLES -->
          <ul class="principles-list">
            <li>✅ <strong>Security-first</strong> – RBAC, audit izləri, şifrələnmiş data, on-prem seçimləri.</li>
            <li>✅ <strong>Miqyaslana bilən arxitektura</strong> – modul dizayn, mikroservis yanaşması.</li>
            <li>✅ <strong>Biznes dəyəri</strong> – hər modul real istifadə case-lərinə görə planlaşdırılır.</li>
            <li>✅ <strong>Sənədləşmə</strong> – README, arxitektura diaqramları, roadmap və changelog mədəniyyəti.</li>
          </ul>

          <!-- REPO STRUCTURE -->
          <div class="stack-row" style="margin-top:10px;">
            <div class="stack-heading">Repo strukturu (nümunə)</div>
            <pre class="code-block">kiberkod/
├─ posnet/        # POS & kassa ekosistemi
├─ sina-lms/      # Təhsil platforması (LMS)
├─ globix/        # ERP / logistika & mühasibat
└─ shared-libs/   # Ortak kitabxanalar & komponentlər
</pre>
          </div>
        </article>
      </section>

      <!-- FOOTER -->
      <footer class="footer">
        <div>
          © <span id="year">2025</span> KiberKod MMC · Bütün hüquqlar qorunur.
        </div>
        <div class="footer-links">
          <span>🌐 <a href="https://kiberkod.az" target="_blank" rel="noreferrer">kiberkod.az</a> (placeholder)</span>
          <span>💻 <a href="https://github.com/kiberkod" target="_blank" rel="noreferrer">GitHub / kiberkod</a></span>
        </div>
      </footer>
    </section>
  </main>

  <script>
    // README-də də problemsiz qalır, sadəcə ili avtomatik doldurur
    (function () {
      var el = document.getElementById("year");
      if (el) el.textContent = new Date().getFullYear();
    })();
  </script>
</body>
</html>
