<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
  <title>Tarik Merras · Portfolio IT | Systèmes & Réseaux</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700;14..32,800&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(135deg, #05070f 0%, #0a0f1c 100%);
      color: #eef2ff;
      font-family: 'Inter', sans-serif;
      line-height: 1.5;
      scroll-behavior: smooth;
      min-height: 100vh;
    }

    /* animation background particles */
    .particles {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 0;
      overflow: hidden;
    }
    .particle {
      position: absolute;
      background: rgba(0, 212, 255, 0.3);
      border-radius: 50%;
      animation: floatParticle 12s infinite ease-in-out;
    }
    @keyframes floatParticle {
      0%, 100% { transform: translateY(0) translateX(0) scale(1); opacity: 0.3; }
      50% { transform: translateY(-40px) translateX(20px) scale(1.2); opacity: 0.6; }
    }

    .container {
      max-width: 1150px;
      margin: 0 auto;
      padding: 40px 24px 70px;
      position: relative;
      z-index: 2;
    }

    /* animations fade-up */
    @keyframes fadeUp {
      0% { opacity: 0; transform: translateY(30px); }
      100% { opacity: 1; transform: translateY(0); }
    }
    .animate {
      animation: fadeUp 0.6s cubic-bezier(0.2, 0.9, 0.4, 1.1) forwards;
      opacity: 0;
    }

    /* cartes modernes */
    .card {
      background: rgba(15, 23, 42, 0.65);
      backdrop-filter: blur(8px);
      border: 1px solid rgba(0, 255, 255, 0.12);
      border-radius: 28px;
      padding: 1.8rem;
      transition: all 0.3s ease;
      box-shadow: 0 12px 30px -12px rgba(0, 0, 0, 0.5);
    }
    .card:hover {
      border-color: rgba(0, 212, 255, 0.5);
      box-shadow: 0 20px 40px -15px rgba(0, 212, 255, 0.25);
      transform: translateY(-2px);
    }

    /* hero avec glow animation */
    .hero {
      background: linear-gradient(135deg, rgba(11,17,32,0.9) 0%, rgba(15,23,42,0.9) 100%);
      border-radius: 32px;
      padding: 2.5rem;
      margin-bottom: 32px;
      border: 1px solid rgba(0, 212, 255, 0.25);
      position: relative;
      overflow: hidden;
    }
    .hero::before {
      content: '';
      position: absolute;
      top: -50%;
      left: -20%;
      width: 200%;
      height: 200%;
      background: radial-gradient(circle, rgba(0,212,255,0.08), transparent 70%);
      animation: rotateGlow 12s linear infinite;
    }
    @keyframes rotateGlow {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }
    .hero h1 {
      font-size: 3.4rem;
      font-weight: 800;
      font-family: 'Space Grotesk', monospace;
      letter-spacing: -0.02em;
      background: linear-gradient(135deg, #ffffff, #5ee0fa, #00d4ff);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      animation: shimmer 3s infinite;
    }
    @keyframes shimmer {
      0%, 100% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
    }

    .badge-glow {
      background: rgba(0, 229, 160, 0.12);
      border: 1px solid rgba(0, 229, 160, 0.4);
      border-radius: 40px;
      padding: 5px 16px;
      font-size: 0.75rem;
      font-weight: 600;
      color: #2ef0b0;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      backdrop-filter: blur(4px);
      transition: 0.2s;
    }
    .badge-glow:hover {
      transform: scale(1.02);
      box-shadow: 0 0 15px rgba(0,229,160,0.3);
    }

    .contact-chip {
      background: rgba(255,255,255,0.03);
      border: 1px solid rgba(255,255,255,0.08);
      border-radius: 50px;
      padding: 8px 18px;
      font-size: 0.8rem;
      transition: all 0.25s;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      text-decoration: none;
      color: #cbd5e6;
    }
    .contact-chip:hover {
      background: rgba(0,212,255,0.15);
      border-color: #00d4ff;
      color: white;
      transform: translateY(-2px);
    }

    /* layout 2 colonnes */
    .two-col {
      display: grid;
      grid-template-columns: 300px 1fr;
      gap: 28px;
    }

    /* tags compétences animés */
    .skill-tag {
      background: linear-gradient(135deg, #0f172a, #111827);
      border: 1px solid #1e2a3e;
      border-radius: 20px;
      padding: 6px 14px;
      font-size: 0.75rem;
      font-weight: 500;
      color: #a0c2e6;
      transition: all 0.2s;
      cursor: default;
    }
    .skill-tag:hover {
      border-color: #00d4ff;
      color: #00d4ff;
      transform: translateX(3px);
    }

    /* timeline */
    .timeline-item {
      border-left: 2px solid rgba(0, 212, 255, 0.4);
      padding-left: 20px;
      margin-bottom: 28px;
      position: relative;
      transition: 0.2s;
    }
    .timeline-item:hover {
      border-left-color: #00d4ff;
    }
    .timeline-item::before {
      content: '';
      position: absolute;
      left: -8px;
      top: 4px;
      width: 14px;
      height: 14px;
      background: #00d4ff;
      border-radius: 50%;
      box-shadow: 0 0 0 3px rgba(0,212,255,0.3);
      animation: pulseDot 2s infinite;
    }
    @keyframes pulseDot {
      0%, 100% { box-shadow: 0 0 0 0 rgba(0,212,255,0.7); }
      50% { box-shadow: 0 0 0 6px rgba(0,212,255,0); }
    }

    /* CERTIFICATIONS STYLE CARTES 3D + ANIMATION */
    .cert-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(210px, 1fr));
      gap: 16px;
    }
    .cert-card {
      background: linear-gradient(145deg, #0f172a, #0a0f1c);
      border-radius: 20px;
      padding: 16px 14px;
      text-decoration: none;
      display: flex;
      align-items: center;
      gap: 12px;
      transition: all 0.3s cubic-bezier(0.2, 0.9, 0.4, 1.1);
      border: 1px solid #1e2a3e;
      position: relative;
      overflow: hidden;
    }
    .cert-card i {
      font-size: 1.8rem;
      transition: transform 0.3s ease;
    }
    .cert-card .cert-info {
      flex: 1;
    }
    .cert-card .cert-name {
      font-size: 0.82rem;
      font-weight: 600;
      color: #e2e8f0;
    }
    .cert-card .cert-issuer {
      font-size: 0.65rem;
      color: #6b7280;
      letter-spacing: 0.5px;
    }
    .cert-card::after {
      content: '↗';
      position: absolute;
      right: 12px;
      top: 12px;
      opacity: 0;
      transition: 0.2s;
      color: #00d4ff;
      font-size: 0.9rem;
    }
    .cert-card:hover {
      transform: translateY(-6px) scale(1.02);
      border-color: #00d4ff;
      box-shadow: 0 15px 30px -12px rgba(0,212,255,0.3);
      background: linear-gradient(145deg, #111a2e, #0d1322);
    }
    .cert-card:hover i {
      transform: rotate(5deg) scale(1.1);
      filter: drop-shadow(0 0 6px #00d4ff);
    }
    .cert-card:hover::after {
      opacity: 1;
      transform: translateX(4px);
    }

    /* badges animés */
    .animated-badge {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      background: rgba(0,212,255,0.1);
      border-radius: 40px;
      padding: 3px 12px;
      font-size: 0.7rem;
      font-weight: 500;
      animation: badgePulse 1.5s infinite;
    }
    @keyframes badgePulse {
      0%, 100% { box-shadow: 0 0 0 0 rgba(0,212,255,0.4); }
      50% { box-shadow: 0 0 0 4px rgba(0,212,255,0); }
    }

    @media (max-width: 780px) {
      .two-col { grid-template-columns: 1fr; }
      .hero h1 { font-size: 2.4rem; }
      .container { padding: 20px 16px; }
    }
  </style>
</head>
<body>

<!-- PARTICULES ANIMÉES EN ARRIÈRE-PLAN -->
<div class="particles" id="particles"></div>

<div class="container">
  <!-- HERO ANIMÉ -->
  <div class="hero animate" style="animation-delay: 0.05s;">
    <div style="display: flex; justify-content: space-between; flex-wrap: wrap; gap: 20px; align-items: flex-start;">
      <div>
        <div class="badge-glow"><i class="fas fa-bolt"></i> Disponible · Mission IT</div>
        <h1 style="margin: 14px 0 6px 0;">Tarik Merras</h1>
        <div style="font-size: 1.15rem; color: #b9c7e0; margin-bottom: 20px;">Technicien Supérieur Systèmes & Réseaux</div>
        <div style="display: flex; flex-wrap: wrap; gap: 12px;">
          <a href="mailto:tarikmerras20@gmail.com" class="contact-chip"><i class="fas fa-envelope"></i> tarikmerras20@gmail.com</a>
          <a href="tel:+212693044430" class="contact-chip"><i class="fas fa-phone-alt"></i> +212 693 044 430</a>
          <span class="contact-chip"><i class="fas fa-map-marker-alt"></i> Meknès / Tanger</span>
        </div>
      </div>
      <div>
        <div class="badge-glow"><i class="fas fa-code-branch"></i> 30+ sites supportés</div>
      </div>
    </div>
  </div>

  <!-- 2 COLONNES -->
  <div class="two-col">
    <!-- SIDEBAR GAUCHE -->
    <div class="animate" style="animation-delay: 0.1s;">
      <div class="card" style="margin-bottom: 24px;">
        <h3 style="font-family: 'Space Grotesk'; margin-bottom: 14px;"><i class="fas fa-user-astronaut" style="color:#00d4ff;"></i> Profil IT</h3>
        <p style="font-size: 0.88rem; color: #cbd5e6; line-height: 1.55;">Spécialiste infrastructures réseau & systèmes, support multi-sites (30+ entreprises). Expert Proxmox, pfSense, Active Directory, supervision GLPI/Zabbix. Passionné par la sécurisation et l'optimisation des environnements industriels.</p>
      </div>

      <div class="card" style="margin-bottom: 24px;">
        <h3 style="font-family: 'Space Grotesk'; margin-bottom: 16px;"><i class="fas fa-microchip"></i> Compétences clés</h3>
        <div style="display: flex; flex-wrap: wrap; gap: 8px;">
          <span class="skill-tag">VLAN / LAN / Wi-Fi</span>
          <span class="skill-tag">pfSense / FortiGate</span>
          <span class="skill-tag">Aruba (Switch/AP)</span>
          <span class="skill-tag">Proxmox VE / VMware</span>
          <span class="skill-tag">Windows Server / AD</span>
          <span class="skill-tag">Linux / Bash</span>
          <span class="skill-tag">Zabbix / Nagios</span>
          <span class="skill-tag">GLPI / Jira</span>
          <span class="skill-tag">Cisco / HP / Ruijie</span>
        </div>
      </div>

      <div class="card">
        <h3 style="font-family: 'Space Grotesk'; margin-bottom: 14px;"><i class="fas fa-language"></i> Langues</h3>
        <div><span>Arabe (maternel)</span><div style="display:flex; gap:4px; margin-top:4px;"><span class="animated-badge"><i class="fas fa-star"></i> C2</span></div></div>
        <div style="margin-top: 12px;"><span>Français (courant technique)</span><div style="display:flex; gap:4px; margin-top:4px;"><span class="animated-badge"><i class="fas fa-check-circle"></i> Professionnel</span></div></div>
        <div style="margin-top: 12px;"><span>Anglais (technique / docs)</span><div style="display:flex; gap:4px; margin-top:4px;"><span class="animated-badge"><i class="fas fa-book"></i> B2 technique</span></div></div>
      </div>
    </div>

    <!-- MAIN DROITE -->
    <div>
      <!-- EXPÉRIENCE -->
      <div class="card animate" style="animation-delay: 0.15s; margin-bottom: 28px;">
        <h3 style="font-family: 'Space Grotesk'; margin-bottom: 22px;"><i class="fas fa-briefcase"></i> Parcours pro</h3>
        <div class="timeline-item">
          <div class="job-title" style="font-weight: 700; font-size: 1rem;">Technicien IT infrastructure</div>
          <div class="company" style="color:#5ee0fa;">Eurostyle Systems – Tanger (STM Prestataire)</div>
          <div class="date"><i class="far fa-calendar-alt"></i> Mars 2026 – Présent</div>
          <ul style="margin-left: 18px; font-size: 0.82rem;"><li>Administration Active Directory, GLPI, serveur d'impression, inventaire & déploiement</li></ul>
        </div>
        <div class="timeline-item">
          <div class="job-title" style="font-weight: 700;">Technicien support multi-sites</div>
          <div class="company">STM – Tanger (30+ entreprises clientes)</div>
          <div class="date"><i class="far fa-calendar-alt"></i> Novembre 2025 – Présent</div>
          <ul style="margin-left: 18px; font-size: 0.82rem;"><li>Support N1/N2, Office 365, déploiements, interventions industrielles (BAMESA, Intl Paper)</li></ul>
          <div class="animated-badge" style="margin-top: 6px;"><i class="fas fa-network-wired"></i> Mission Calsina Carré : Aruba switches + Aruba Central</div>
        </div>
        <div class="timeline-item">
          <div class="job-title">Stage systèmes & réseaux</div>
          <div class="company">Commune de Boufkrane</div>
          <div class="date">Avril 2025 – Mai 2025</div>
          <ul><li>Proxmox VE, pfSense, réseau sécurisé Wi-Fi/câblé</li></ul>
        </div>
        <div class="timeline-item">
          <div class="job-title">Stage IT production</div>
          <div class="company">Intelcia – Meknès</div>
          <div class="date">Juillet 2025 – Août 2025</div>
          <ul><li>Windows Server / AD, support Jira, gestion parc informatique</li></ul>
        </div>
      </div>

      <!-- CERTIFICATIONS + BADGES 100% FONCTIONNELS ET ANIMÉS -->
      <div class="card animate" style="animation-delay: 0.25s; margin-bottom: 28px;">
        <h3 style="font-family: 'Space Grotesk'; margin-bottom: 20px; display: flex; gap: 10px; align-items: center;">
          <i class="fas fa-certificate" style="color:#00d4ff;"></i> Certifications & Badges
          <span class="animated-badge"><i class="fas fa-mouse-pointer"></i> Cliquez sur les cartes</span>
        </h3>
        <div class="cert-grid" id="certGrid">
          <!-- CISCO -->
          <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/NetworkingBasics20250517-27-zfswbm.pdf" target="_blank" class="cert-card">
            <i class="fab fa-cisco" style="color:#00a0dc;"></i>
            <div class="cert-info"><div class="cert-name">Networking Basics</div><div class="cert-issuer">Cisco Networking Academy</div></div>
          </a>
          <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/NetworkDefense20250517-27-qe0r9e.pdf" target="_blank" class="cert-card">
            <i class="fab fa-cisco" style="color:#00a0dc;"></i>
            <div class="cert-info"><div class="cert-name">Network Defense</div><div class="cert-issuer">Cisco</div></div>
          </a>
          <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/IntroductionToCybersecurity20250519-27-djgap4.pdf" target="_blank" class="cert-card">
            <i class="fas fa-shield-alt" style="color:#2dd4bf;"></i>
            <div class="cert-info"><div class="cert-name">Intro to Cybersecurity</div><div class="cert-issuer">Cisco</div></div>
          </a>
          <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/EthicalHacker20250520-27-sxjvbg.pdf" target="_blank" class="cert-card">
            <i class="fas fa-user-secret" style="color:#a855f7;"></i>
            <div class="cert-info"><div class="cert-name">Ethical Hacker</div><div class="cert-issuer">Cisco</div></div>
          </a>
          <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/IntrotoIoTUpdate20250620-27-2xhtad.pdf" target="_blank" class="cert-card">
            <i class="fas fa-wifi" style="color:#10b981;"></i>
            <div class="cert-info"><div class="cert-name">Introduction to IoT</div><div class="cert-issuer">Cisco</div></div>
          </a>
          <!-- MICROSOFT -->
          <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/Achievements%20-%20tarikmerras-6925%20_%20Microsoft%20Learn.pdf" target="_blank" class="cert-card">
            <i class="fab fa-microsoft" style="color:#0078d4;"></i>
            <div class="cert-info"><div class="cert-name">Describe Cloud Computing</div><div class="cert-issuer">Microsoft Learn</div></div>
          </a>
          <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/Succ%C3%A8s%20-%20tarikmerras-6925%20_%20Microsoft%20Learn.pdf" target="_blank" class="cert-card">
            <i class="fab fa-microsoft" style="color:#00a4ef;"></i>
            <div class="cert-info"><div class="cert-name">Composants Azure</div><div class="cert-issuer">Microsoft Learn</div></div>
          </a>
          <!-- HP LIFE -->
          <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/certificate-1.pdf" target="_blank" class="cert-card">
            <i class="fas fa-brain" style="color:#ff8c00;"></i>
            <div class="cert-info"><div class="cert-name">AI for Beginners</div><div class="cert-issuer">HP LIFE</div></div>
          </a>
          <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/certificate.pdf" target="_blank" class="cert-card">
            <i class="fas fa-envelope-open-text" style="color:#ffb347;"></i>
            <div class="cert-info"><div class="cert-name">Business Email</div><div class="cert-issuer">HP LIFE</div></div>
          </a>
        </div>
      </div>

      <!-- PROJETS -->
      <div class="card animate" style="animation-delay: 0.3s;">
        <h3 style="font-family: 'Space Grotesk'; margin-bottom: 16px;"><i class="fas fa-rocket"></i> Projets phares</h3>
        <div style="padding: 6px 0;"><i class="fas fa-shield-virus" style="color:#00d4ff;"></i> <strong>Commune Boufkrane</strong> – Proxmox + pfSense + VLANs</div>
        <div style="padding: 6px 0;"><i class="fas fa-chart-line"></i> <strong>Supervision OFPPT</strong> – Zabbix/Nagios, optimisation réseau</div>
        <div style="padding: 6px 0;"><i class="fas fa-cloud-upload-alt"></i> <strong>Aruba Central</strong> – Gestion cloud switches/APs Calsina Carré</div>
      </div>
    </div>
  </div>
</div>

<script>
  // Génération de particules flottantes
  function createParticles() {
    const container = document.getElementById('particles');
    for (let i = 0; i < 40; i++) {
      const particle = document.createElement('div');
      particle.classList.add('particle');
      const size = Math.random() * 4 + 1;
      particle.style.width = size + 'px';
      particle.style.height = size + 'px';
      particle.style.left = Math.random() * 100 + '%';
      particle.style.animationDelay = Math.random() * 10 + 's';
      particle.style.animationDuration = Math.random() * 8 + 6 + 's';
      particle.style.opacity = Math.random() * 0.4;
      container.appendChild(particle);
    }
  }
  createParticles();

  // Animation d'apparition + hover sur certs
  const animatedElements = document.querySelectorAll('.animate');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.style.opacity = '1';
        entry.target.style.transform = 'translateY(0)';
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.1 });
  animatedElements.forEach(el => observer.observe(el));

  // Forcer l'opacité initiale
  animatedElements.forEach(el => {
    el.style.opacity = '0';
    el.style.transform = 'translateY(30px)';
    el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
  });

  // Ajouter un console log pour vérifier que les certs sont cliquables
  console.log('✅ Certifications actives — chaque carte ouvre le PDF correspondant');
</script>
</body>
</html>
