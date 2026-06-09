* ============================================================
   I.I.S. Capellini–Sauro — Stylesheet
   Font: Syne (display) + Inter (body)
   Palette: #003d7a (primary) · #0077b6 (accent) · #0d1b3e (dark)
   ============================================================ */

/* ---------- Reset & Base ---------- */
*, *::before, *::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

:root {
  --color-primary:   #003d7a;
  --color-accent:    #0077b6;
  --color-dark:      #0d1b3e;
  --color-light-bg:  #f8fafd;
  --color-border:    #e8ecf4;
  --color-text:      #1a1a2e;
  --color-muted:     #5a6a85;
  --color-subtle:    #6b7a99;
  --font-display:    'Syne', sans-serif;
  --font-body:       'Inter', sans-serif;
  --radius-sm:       6px;
  --radius-md:       10px;
  --radius-lg:       14px;
  --transition:      0.2s ease;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-body);
  background: #fff;
  color: var(--color-text);
  line-height: 1.6;
  -webkit-font-smoothing: antialiased;
}

a {
  color: inherit;
  text-decoration: none;
}

img {
  max-width: 100%;
  display: block;
}

/* ---------- NAVBAR ---------- */
.nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 2rem;
  height: 60px;
  background: var(--color-primary);
  color: #fff;
  position: sticky;
  top: 0;
  z-index: 100;
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.15);
}

.nav-logo {
  display: flex;
  align-items: center;
  gap: 10px;
}

.nav-logo-icon {
  width: 36px;
  height: 36px;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.15);
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: var(--font-display);
  font-weight: 800;
  font-size: 13px;
  color: #fff;
  flex-shrink: 0;
}

.nav-logo-text {
  font-family: var(--font-display);
  font-size: 13px;
  font-weight: 600;
  line-height: 1.3;
  color: #fff;
}

.nav-logo-text span {
  font-weight: 400;
  opacity: 0.7;
  font-size: 11px;
  display: block;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 1.5rem;
}

.nav-links a {
  color: rgba(255, 255, 255, 0.8);
  font-size: 13px;
  font-weight: 500;
  letter-spacing: 0.02em;
  transition: color var(--transition);
}

.nav-links a:hover {
  color: #fff;
}

.nav-cta {
  background: var(--color-accent) !important;
  color: #fff !important;
  padding: 6px 14px;
  border-radius: var(--radius-sm);
  font-size: 12px !important;
  font-weight: 600 !important;
}

.nav-toggle {
  display: none;
  flex-direction: column;
  gap: 5px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 4px;
}

.nav-toggle span {
  display: block;
  width: 22px;
  height: 2px;
  background: #fff;
  border-radius: 2px;
  transition: var(--transition);
}

/* ---------- HERO ---------- */
.hero {
  position: relative;
  overflow: hidden;
  background: linear-gradient(160deg, var(--color-primary) 0%, #005fad 55%, var(--color-accent) 100%);
  padding: 5rem 2.5rem 0;
  min-height: 400px;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
}

.hero-content {
  position: relative;
  z-index: 1;
  max-width: 600px;
}

.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  background: rgba(255, 255, 255, 0.12);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 20px;
  padding: 4px 12px;
  margin-bottom: 1.2rem;
  font-size: 11px;
  font-weight: 600;
  color: #a8d8f0;
  letter-spacing: 0.06em;
  text-transform: uppercase;
}

.hero-badge::before {
  content: '';
  width: 6px;
  height: 6px;
  background: #4fc3f7;
  border-radius: 50%;
  flex-shrink: 0;
}

.hero h1 {
  font-family: var(--font-display);
  font-size: clamp(2rem, 5vw, 3rem);
  font-weight: 800;
  color: #fff;
  line-height: 1.1;
  letter-spacing: -0.02em;
  margin-bottom: 1rem;
}

.hero h1 em {
  font-style: normal;
  color: #7dd3fc;
}

.hero-sub {
  color: rgba(255, 255, 255, 0.72);
  font-size: 15px;
  font-weight: 400;
  line-height: 1.7;
  margin-bottom: 2rem;
}

.hero-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-bottom: 4rem;
}

.btn-primary {
  background: #fff;
  color: var(--color-primary);
  padding: 11px 22px;
  border-radius: var(--radius-md);
  font-size: 13px;
  font-weight: 700;
  letter-spacing: 0.01em;
  transition: opacity var(--transition), transform var(--transition);
}

.btn-primary:hover {
  opacity: 0.92;
  transform: translateY(-1px);
}

.btn-secondary {
  background: transparent;
  color: rgba(255, 255, 255, 0.85);
  border: 1px solid rgba(255, 255, 255, 0.3);
  padding: 11px 22px;
  border-radius: var(--radius-md);
  font-size: 13px;
  font-weight: 500;
  transition: border-color var(--transition), color var(--transition);
}

.btn-secondary:hover {
  border-color: rgba(255, 255, 255, 0.6);
  color: #fff;
}

.hero-wave {
  display: block;
  width: 100%;
  flex-shrink: 0;
}

/* ---------- STATS BAR ---------- */
.stats-bar {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  background: var(--color-primary);
  border-top: 1px solid rgba(255, 255, 255, 0.1);
}

.stat-item {
  padding: 1.2rem 1.5rem;
  border-right: 1px solid rgba(255, 255, 255, 0.1);
}

.stat-item:last-child {
  border-right: none;
}

.stat-num {
  font-family: var(--font-display);
  font-size: 1.6rem;
  font-weight: 800;
  color: #fff;
  line-height: 1;
}

.stat-label {
  font-size: 11px;
  color: rgba(255, 255, 255, 0.5);
  margin-top: 4px;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  font-weight: 500;
}

/* ---------- SECTIONS ---------- */
.section {
  padding: 3.5rem 2.5rem;
}

.section + .section {
  border-top: 1px solid var(--color-border);
}

.section--alt {
  background: var(--color-light-bg);
}

.section-eyebrow {
  font-size: 11px;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--color-accent);
  margin-bottom: 0.4rem;
}

.section-title {
  font-family: var(--font-display);
  font-size: clamp(1.4rem, 3vw, 1.8rem);
  font-weight: 700;
  color: var(--color-dark);
  line-height: 1.2;
  margin-bottom: 0.5rem;
}

.section-sub {
  font-size: 14px;
  color: var(--color-muted);
  line-height: 1.7;
  max-width: 500px;
}

/* ---------- NEWS ---------- */
.news-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
  margin-top: 2rem;
}

.news-card {
  border: 1px solid var(--color-border);
  border-radius: var(--radius-lg);
  overflow: hidden;
  background: #fff;
  transition: box-shadow var(--transition), transform var(--transition);
  display: flex;
  flex-direction: column;
}

.news-card:hover {
  box-shadow: 0 8px 24px rgba(0, 61, 122, 0.1);
  transform: translateY(-2px);
}

.news-card-featured {
  grid-column: 1 / -1;
  flex-direction: row;
}

.news-card-img {
  overflow: hidden;
  height: 140px;
  flex-shrink: 0;
}

.news-card-featured .news-card-img {
  width: 45%;
  height: auto;
  min-height: 200px;
}

.news-card-img-bg {
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: center;
  /* Fallback color if image not found */
  background-color: #c3daf5;
  transition: transform 0.4s ease;
}

.news-card:hover .news-card-img-bg {
  transform: scale(1.04);
}

.news-card-img--wave,
.news-card-img--radio {
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2.5rem;
  height: 140px;
}

.news-card-img--wave {
  background: linear-gradient(135deg, #0077b6, #00b4d8);
}

.news-card-img--radio {
  background: linear-gradient(135deg, var(--color-primary), #0077b6);
}

.news-card-body {
  padding: 1.1rem 1.2rem;
  display: flex;
  flex-direction: column;
  flex: 1;
}

.news-card-featured .news-card-body {
  padding: 1.8rem 1.8rem;
  justify-content: center;
}

.news-tag {
  font-size: 10px;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.07em;
  color: var(--color-accent);
  margin-bottom: 6px;
}

.news-card-title {
  font-family: var(--font-display);
  font-size: 14px;
  font-weight: 700;
  color: var(--color-dark);
  line-height: 1.35;
  margin-bottom: 6px;
}

.news-card-featured .news-card-title {
  font-size: 18px;
}

.news-card-desc {
  font-size: 12px;
  color: var(--color-subtle);
  line-height: 1.6;
  flex: 1;
}

.news-card-featured .news-card-desc {
  font-size: 13px;
}

.news-date {
  display: block;
  font-size: 11px;
  color: #aab3c5;
  margin-top: 10px;
}

/* ---------- INDIRIZZI ---------- */
.indirizzi-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 14px;
  margin-top: 2rem;
}

.indirizzo-card {
  border: 1px solid var(--color-border);
  border-radius: var(--radius-lg);
  padding: 1.4rem 1.2rem;
  display: flex;
  flex-direction: column;
  gap: 8px;
  background: #fff;
  transition: border-color var(--transition), box-shadow var(--transition), transform var(--transition);
}

.indirizzo-card:hover {
  border-color: var(--color-accent);
  box-shadow: 0 4px 16px rgba(0, 119, 182, 0.12);
  transform: translateY(-2px);
}

.indirizzo-icon {
  width: 44px;
  height: 44px;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 22px;
  margin-bottom: 4px;
}

.indirizzo-icon--blue   { background: #e0f2fe; }
.indirizzo-icon--green  { background: #f0fdf4; }
.indirizzo-icon--orange { background: #fff7ed; }
.indirizzo-icon--purple { background: #fdf4ff; }
.indirizzo-icon--yellow { background: #fefce8; }

.indirizzo-name {
  font-family: var(--font-display);
  font-size: 13.5px;
  font-weight: 700;
  color: var(--color-dark);
  line-height: 1.3;
}

.indirizzo-desc {
  font-size: 12px;
  color: var(--color-subtle);
  line-height: 1.6;
  flex: 1;
}

.indirizzo-arrow {
  font-size: 12px;
  color: var(--color-accent);
  font-weight: 600;
  margin-top: 4px;
}

/* ---------- SERVIZI ---------- */
.servizi-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 12px;
  margin-top: 2rem;
}

.servizio-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  padding: 1.4rem 0.8rem;
  border: 1px solid var(--color-border);
  border-radius: var(--radius-lg);
  background: #fff;
  gap: 10px;
  transition: border-color var(--transition), background var(--transition);
}

.servizio-item:hover {
  border-color: var(--color-accent);
  background: #f0f7ff;
}

.servizio-icon {
  width: 50px;
  height: 50px;
  border-radius: 12px;
  background: #e8f4fd;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 22px;
}

.servizio-name {
  font-size: 12px;
  font-weight: 600;
  color: var(--color-dark);
  line-height: 1.3;
}

/* ---------- ERASMUS BANNER ---------- */
.erasmus-banner {
  background: linear-gradient(135deg, var(--color-primary), var(--color-accent));
  border-radius: 16px;
  padding: 2.2rem 2.5rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1.5rem;
  flex-wrap: wrap;
}

.erasmus-tag {
  font-size: 10px;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: #7dd3fc;
  margin-bottom: 6px;
}

.erasmus-title {
  font-family: var(--font-display);
  font-size: 1.4rem;
  font-weight: 700;
  color: #fff;
  line-height: 1.2;
  margin-bottom: 8px;
}

.erasmus-sub {
  font-size: 13px;
  color: rgba(255, 255, 255, 0.65);
  line-height: 1.6;
  max-width: 380px;
}

.btn-white {
  background: #fff;
  color: var(--color-primary);
  padding: 11px 22px;
  border-radius: var(--radius-md);
  font-size: 13px;
  font-weight: 700;
  white-space: nowrap;
  flex-shrink: 0;
  transition: opacity var(--transition), transform var(--transition);
}

.btn-white:hover {
  opacity: 0.92;
  transform: translateY(-1px);
}

/* ---------- FOOTER ---------- */
.footer {
  background: var(--color-dark);
  padding: 3rem 2.5rem 1.5rem;
}

.footer-top {
  display: grid;
  grid-template-columns: 1.5fr 1fr 1fr;
  gap: 2rem;
  padding-bottom: 2rem;
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}

.footer-brand-name {
  font-family: var(--font-display);
  font-size: 15px;
  font-weight: 800;
  color: #fff;
  margin-bottom: 6px;
}

.footer-brand-sub {
  font-size: 12px;
  color: rgba(255, 255, 255, 0.4);
  line-height: 1.6;
  margin-bottom: 1rem;
  font-style: normal;
}

.footer-contact {
  font-size: 12px;
  color: rgba(255, 255, 255, 0.5);
  line-height: 2;
  font-style: normal;
}

.footer-contact strong {
  color: rgba(255, 255, 255, 0.7);
  font-weight: 500;
}

.footer-contact a {
  color: rgba(255, 255, 255, 0.5);
  transition: color var(--transition);
}

.footer-contact a:hover {
  color: #7dd3fc;
}

.footer-col-title {
  font-size: 10px;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: rgba(255, 255, 255, 0.35);
  margin-bottom: 14px;
}

.footer-links {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.footer-links a {
  font-size: 12px;
  color: rgba(255, 255, 255, 0.55);
  transition: color var(--transition);
}

.footer-links a:hover {
  color: #7dd3fc;
}

.footer-bottom {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 1.2rem;
  flex-wrap: wrap;
  gap: 1rem;
}

.footer-bottom-text {
  font-size: 11px;
  color: rgba(255, 255, 255, 0.25);
}

.footer-social {
  display: flex;
  gap: 8px;
}

.social-icon {
  width: 30px;
  height: 30px;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.08);
  border: 1px solid rgba(255, 255, 255, 0.12);
  display: flex;
  align-items: center;
  justify-content: center;
  color: rgba(255, 255, 255, 0.5);
  font-size: 12px;
  font-weight: 600;
  transition: background var(--transition), color var(--transition);
}

.social-icon:hover {
  background: rgba(255, 255, 255, 0.18);
  color: #fff;
}

/* ---------- RESPONSIVE ---------- */
@media (max-width: 900px) {
  .indirizzi-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .servizi-grid {
    grid-template-columns: repeat(4, 1fr);
  }

  .footer-top {
    grid-template-columns: 1fr 1fr;
  }

  .footer-brand {
    grid-column: 1 / -1;
  }
}

@media (max-width: 680px) {
  .nav-links {
    display: none;
    flex-direction: column;
    gap: 0;
    position: absolute;
    top: 60px;
    left: 0;
    right: 0;
    background: var(--color-primary);
    padding: 1rem 0;
    box-shadow: 0 8px 20px rgba(0,0,0,0.2);
  }

  .nav-links.is-open {
    display: flex;
  }

  .nav-links a {
    padding: 0.75rem 2rem;
    font-size: 14px;
    border-bottom: 1px solid rgba(255,255,255,0.08);
  }

  .nav-links .nav-cta {
    margin: 0.5rem 2rem 0;
    text-align: center;
    border-radius: var(--radius-sm);
  }

  .nav-toggle {
    display: flex;
  }

  .stats-bar {
    grid-template-columns: repeat(2, 1fr);
  }

  .stat-item:nth-child(2) {
    border-right: none;
  }

  .news-grid {
    grid-template-columns: 1fr;
  }

  .news-card-featured {
    flex-direction: column;
  }

  .news-card-featured .news-card-img {
    width: 100%;
    height: 180px;
  }

  .indirizzi-grid {
    grid-template-columns: 1fr;
  }

  .servizi-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .erasmus-banner {
    flex-direction: column;
    text-align: center;
  }

  .erasmus-sub {
    max-width: 100%;
  }

  .footer-top {
    grid-template-columns: 1fr;
  }

  .section {
    padding: 2.5rem 1.5rem;
  }

  .hero {
    padding: 3rem 1.5rem 0;
  }
}

/* ---------- REDUCED MOTION ---------- */
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    transition: none !important;
    animation: none !important;
  }

  html {
    scroll-behavior: auto;
  }
}
