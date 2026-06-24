# GCF---Global-Consulting-Formations
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="GCF - Global Consulting & Formations. Cabinet de Comptabilité, Fiscalité et Formation Professionnelle à Rabat. Plus de 25 ans d'expérience.">
<title>GCF - Global Consulting & Formations | Rabat</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root {
    --navy: #163A5F;
    --navy-dark: #0d2640;
    --gold: #D9A441;
    --gold-light: #f0c46a;
    --mint: #68C8B6;
    --mint-light: #9dddd0;
    --white: #FFFFFF;
    --gray-50: #f8f9fb;
    --gray-100: #eef0f4;
    --gray-300: #c4cad6;
    --gray-600: #4a5568;
    --gray-800: #1a202c;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Inter', sans-serif;
    color: var(--gray-800);
    background: var(--white);
    overflow-x: hidden;
  }

  /* NAV */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 1000;
    background: rgba(22, 58, 95, 0.97);
    backdrop-filter: blur(10px);
    padding: 0 5%;
    display: flex; align-items: center; justify-content: space-between;
    height: 72px;
    border-bottom: 2px solid var(--gold);
  }

  .nav-logo {
    display: flex; align-items: center; gap: 12px; text-decoration: none;
  }
  .nav-logo-diamond {
    width: 38px; height: 38px;
    background: var(--gold);
    transform: rotate(45deg);
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0;
  }
  .nav-logo-diamond span {
    transform: rotate(-45deg);
    font-family: 'Playfair Display', serif;
    font-weight: 900;
    font-size: 16px;
    color: var(--navy);
  }
  .nav-logo-text { color: var(--white); }
  .nav-logo-text strong { display: block; font-size: 18px; font-weight: 700; letter-spacing: 1px; }
  .nav-logo-text span { font-size: 11px; color: var(--gold); letter-spacing: 0.5px; }

  .nav-links { display: flex; gap: 32px; list-style: none; }
  .nav-links a {
    color: rgba(255,255,255,0.85);
    text-decoration: none;
    font-size: 14px;
    font-weight: 500;
    transition: color 0.2s;
    letter-spacing: 0.5px;
  }
  .nav-links a:hover { color: var(--gold); }

  .nav-cta {
    background: var(--gold);
    color: var(--navy) !important;
    padding: 8px 20px;
    border-radius: 3px;
    font-weight: 600 !important;
    transition: background 0.2s !important;
  }
  .nav-cta:hover { background: var(--gold-light) !important; color: var(--navy) !important; }

  .hamburger { display: none; flex-direction: column; gap: 5px; cursor: pointer; }
  .hamburger span { width: 24px; height: 2px; background: white; display: block; }

  /* HERO */
  .hero {
    min-height: 100vh;
    background: var(--navy);
    display: flex; align-items: center;
    position: relative;
    overflow: hidden;
    padding-top: 72px;
  }

  .hero-bg-shape {
    position: absolute; inset: 0;
    overflow: hidden;
  }
  .hero-bg-shape::before {
    content: '';
    position: absolute;
    right: -10%;
    top: -20%;
    width: 65%;
    height: 140%;
    background: linear-gradient(135deg, var(--navy-dark) 0%, #1e4d7a 100%);
    transform: skewX(-8deg);
    z-index: 0;
  }
  .hero-bg-shape::after {
    content: '';
    position: absolute;
    right: 25%;
    bottom: 0;
    top: 0;
    width: 4px;
    background: var(--gold);
    opacity: 0.3;
  }

  /* Geometric diamonds */
  .hero-diamond {
    position: absolute;
    background: var(--gold);
    transform: rotate(45deg);
    opacity: 0.08;
  }
  .hero-diamond.d1 { width: 200px; height: 200px; top: 10%; right: 8%; }
  .hero-diamond.d2 { width: 120px; height: 120px; bottom: 15%; right: 18%; opacity: 0.05; }
  .hero-diamond.d3 { width: 60px; height: 60px; top: 40%; left: 42%; background: var(--mint); opacity: 0.15; }

  .hero-stripe {
    position: absolute;
    left: 0; right: 0;
    height: 4px;
    background: linear-gradient(90deg, var(--gold) 0%, var(--mint) 50%, transparent 100%);
    bottom: 80px;
    opacity: 0.4;
  }

  .hero-content {
    position: relative; z-index: 1;
    display: flex; align-items: center;
    width: 90%; max-width: 1200px;
    margin: 0 auto;
    gap: 60px;
    padding: 80px 0;
  }

  .hero-text { flex: 1; }

  .hero-eyebrow {
    display: inline-flex; align-items: center; gap: 10px;
    background: rgba(217, 164, 65, 0.15);
    border: 1px solid rgba(217, 164, 65, 0.4);
    padding: 6px 16px;
    border-radius: 2px;
    margin-bottom: 24px;
  }
  .hero-eyebrow span { color: var(--gold); font-size: 12px; font-weight: 600; letter-spacing: 2px; text-transform: uppercase; }
  .hero-eyebrow::before {
    content: '';
    width: 18px; height: 18px;
    background: var(--gold);
    transform: rotate(45deg);
    flex-shrink: 0;
  }

  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.4rem, 4.5vw, 3.8rem);
    font-weight: 900;
    color: var(--white);
    line-height: 1.15;
    margin-bottom: 12px;
  }
  .hero h1 em {
    font-style: normal;
    color: var(--gold);
  }

  .hero-subtitle {
    font-size: 1.1rem;
    color: var(--mint);
    font-weight: 500;
    margin-bottom: 20px;
    letter-spacing: 0.3px;
  }

  .hero-desc {
    color: rgba(255,255,255,0.75);
    font-size: 1rem;
    line-height: 1.75;
    max-width: 500px;
    margin-bottom: 36px;
  }

  .hero-stats {
    display: flex; gap: 32px;
    margin-bottom: 40px;
  }
  .hero-stat { text-align: center; }
  .hero-stat strong {
    display: block;
    font-size: 2rem;
    font-weight: 700;
    color: var(--gold);
    font-family: 'Playfair Display', serif;
  }
  .hero-stat span {
    font-size: 0.75rem;
    color: rgba(255,255,255,0.6);
    text-transform: uppercase;
    letter-spacing: 1px;
  }

  .hero-buttons { display: flex; gap: 16px; flex-wrap: wrap; }

  .btn-primary {
    background: var(--gold);
    color: var(--navy);
    padding: 14px 32px;
    font-size: 0.9rem;
    font-weight: 700;
    text-decoration: none;
    border-radius: 3px;
    transition: background 0.2s, transform 0.2s;
    letter-spacing: 0.5px;
    border: none; cursor: pointer;
  }
  .btn-primary:hover { background: var(--gold-light); transform: translateY(-2px); }

  .btn-secondary {
    background: transparent;
    color: var(--white);
    padding: 13px 32px;
    font-size: 0.9rem;
    font-weight: 600;
    text-decoration: none;
    border-radius: 3px;
    border: 2px solid rgba(255,255,255,0.3);
    transition: border-color 0.2s, transform 0.2s;
    cursor: pointer;
  }
  .btn-secondary:hover { border-color: var(--mint); color: var(--mint); transform: translateY(-2px); }

  .hero-image {
    flex: 0 0 340px;
    position: relative;
  }
  .hero-image-frame {
    width: 300px; height: 380px;
    background: linear-gradient(135deg, rgba(217,164,65,0.15), rgba(104,200,182,0.1));
    border: 2px solid rgba(217,164,65,0.3);
    border-radius: 4px;
    display: flex; align-items: center; justify-content: center;
    position: relative;
    overflow: hidden;
    margin: 0 auto;
  }
  .hero-image-frame::before {
    content: '';
    position: absolute;
    top: -30px; right: -30px;
    width: 100px; height: 100px;
    background: var(--gold);
    transform: rotate(45deg);
    opacity: 0.15;
  }
  .hero-image-placeholder {
    display: flex; flex-direction: column; align-items: center; gap: 16px;
  }
  .hero-avatar {
    width: 120px; height: 120px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--gold) 0%, var(--gold-light) 100%);
    display: flex; align-items: center; justify-content: center;
    font-size: 3rem;
    color: var(--navy);
    font-weight: 900;
    font-family: 'Playfair Display', serif;
  }
  .hero-image-name { color: var(--white); text-align: center; }
  .hero-image-name strong { display: block; font-size: 1rem; font-weight: 600; }
  .hero-image-name span { font-size: 0.8rem; color: var(--gold); }

  .hero-badge {
    position: absolute;
    bottom: -15px; right: -15px;
    width: 90px; height: 90px;
    background: var(--mint);
    border-radius: 50%;
    display: flex; flex-direction: column; align-items: center; justify-content: center;
    border: 4px solid var(--navy);
  }
  .hero-badge strong { font-size: 1.5rem; font-weight: 900; color: var(--navy); font-family: 'Playfair Display', serif; line-height: 1; }
  .hero-badge span { font-size: 0.5rem; color: var(--navy); font-weight: 700; text-transform: uppercase; text-align: center; letter-spacing: 0.5px; line-height: 1.2; }

  /* ABOUT */
  .section { padding: 90px 5%; }
  .container { max-width: 1200px; margin: 0 auto; }

  .section-header { text-align: center; margin-bottom: 60px; }
  .section-eyebrow {
    display: inline-block;
    color: var(--gold);
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    margin-bottom: 12px;
  }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 3vw, 2.6rem);
    font-weight: 700;
    color: var(--navy);
    line-height: 1.3;
  }
  .section-title em { font-style: normal; color: var(--gold); }
  .section-divider {
    width: 60px; height: 3px;
    background: linear-gradient(90deg, var(--gold), var(--mint));
    margin: 16px auto 0;
    border-radius: 2px;
  }

  /* ABOUT SECTION */
  .about-section { background: var(--gray-50); }
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
    align-items: center;
  }
  .about-text p {
    color: var(--gray-600);
    font-size: 1rem;
    line-height: 1.8;
    margin-bottom: 20px;
  }
  .about-highlight {
    background: var(--navy);
    color: var(--white);
    padding: 24px 28px;
    border-radius: 4px;
    border-left: 4px solid var(--gold);
    margin-top: 28px;
  }
  .about-highlight p {
    color: rgba(255,255,255,0.85) !important;
    font-style: italic;
    margin: 0 !important;
    font-size: 1.05rem !important;
  }
  .about-highlight strong { color: var(--gold); }

  .about-values {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
  }
  .value-card {
    background: var(--white);
    border: 1px solid var(--gray-100);
    border-radius: 6px;
    padding: 24px 20px;
    position: relative;
    overflow: hidden;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .value-card:hover { transform: translateY(-4px); box-shadow: 0 12px 40px rgba(22,58,95,0.1); }
  .value-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 3px;
    background: linear-gradient(90deg, var(--gold), var(--mint));
  }
  .value-icon {
    width: 44px; height: 44px;
    background: rgba(217,164,65,0.1);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    margin-bottom: 14px;
    font-size: 1.3rem;
  }
  .value-card h4 { font-size: 0.95rem; font-weight: 600; color: var(--navy); margin-bottom: 6px; }
  .value-card p { font-size: 0.82rem; color: var(--gray-600); line-height: 1.5; }

  /* FORMATEUR */
  .formateur-section { background: var(--navy); }
  .formateur-section .section-title { color: var(--white); }
  .formateur-card {
    max-width: 900px;
    margin: 0 auto;
    display: flex;
    gap: 48px;
    align-items: flex-start;
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(217,164,65,0.2);
    border-radius: 8px;
    padding: 48px;
    position: relative;
    overflow: hidden;
  }
  .formateur-card::after {
    content: '';
    position: absolute;
    bottom: -40px; right: -40px;
    width: 180px; height: 180px;
    background: var(--gold);
    transform: rotate(45deg);
    opacity: 0.05;
  }
  .formateur-photo {
    flex: 0 0 180px;
  }
  .formateur-avatar {
    width: 160px; height: 160px;
    border-radius: 4px;
    background: linear-gradient(135deg, var(--gold) 0%, var(--gold-light) 100%);
    display: flex; align-items: center; justify-content: center;
    font-size: 3.5rem;
    color: var(--navy);
    font-weight: 900;
    font-family: 'Playfair Display', serif;
    position: relative;
  }
  .formateur-avatar::after {
    content: '';
    position: absolute;
    bottom: -8px; right: -8px;
    width: 40px; height: 40px;
    background: var(--mint);
    transform: rotate(45deg);
  }
  .formateur-info h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.8rem;
    color: var(--white);
    margin-bottom: 4px;
  }
  .formateur-title { color: var(--gold); font-weight: 500; margin-bottom: 16px; font-size: 0.95rem; }
  .formateur-exp {
    display: inline-flex; align-items: center; gap: 8px;
    background: rgba(104,200,182,0.15);
    border: 1px solid rgba(104,200,182,0.3);
    padding: 6px 14px;
    border-radius: 20px;
    color: var(--mint);
    font-size: 0.85rem;
    font-weight: 600;
    margin-bottom: 20px;
  }
  .formateur-desc { color: rgba(255,255,255,0.7); font-size: 0.95rem; line-height: 1.7; margin-bottom: 24px; }
  .formateur-skills { display: flex; gap: 10px; flex-wrap: wrap; }
  .skill-tag {
    background: rgba(217,164,65,0.15);
    border: 1px solid rgba(217,164,65,0.3);
    color: var(--gold);
    padding: 5px 14px;
    border-radius: 20px;
    font-size: 0.8rem;
    font-weight: 500;
  }

  /* FORMATIONS */
  .formations-section { background: var(--white); }
  .formations-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 28px;
  }
  .formation-card {
    background: var(--white);
    border: 1px solid var(--gray-100);
    border-radius: 6px;
    overflow: hidden;
    transition: transform 0.25s, box-shadow 0.25s;
    position: relative;
  }
  .formation-card:hover { transform: translateY(-6px); box-shadow: 0 20px 60px rgba(22,58,95,0.12); }
  .formation-card-header {
    background: var(--navy);
    padding: 32px 28px 24px;
    position: relative;
    overflow: hidden;
  }
  .formation-card-header::before {
    content: '';
    position: absolute;
    top: -20px; right: -20px;
    width: 80px; height: 80px;
    background: var(--gold);
    transform: rotate(45deg);
    opacity: 0.12;
  }
  .formation-num {
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 10px;
  }
  .formation-card-header h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem;
    color: var(--white);
    line-height: 1.4;
  }
  .formation-badge {
    position: absolute;
    top: 16px; right: 20px;
    background: var(--gold);
    color: var(--navy);
    font-size: 0.7rem;
    font-weight: 700;
    padding: 4px 10px;
    border-radius: 2px;
    letter-spacing: 0.5px;
  }
  .formation-card-body { padding: 24px 28px; }
  .formation-features { list-style: none; margin-bottom: 24px; }
  .formation-features li {
    display: flex; align-items: center; gap: 10px;
    font-size: 0.88rem;
    color: var(--gray-600);
    padding: 8px 0;
    border-bottom: 1px solid var(--gray-100);
  }
  .formation-features li::before {
    content: '✓';
    width: 22px; height: 22px;
    background: rgba(104,200,182,0.15);
    color: var(--mint);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 0.75rem;
    font-weight: 700;
    flex-shrink: 0;
  }
  .formation-footer {
    display: flex; align-items: center; justify-content: space-between;
    padding-top: 16px;
  }
  .formation-duration {
    display: flex; align-items: center; gap: 6px;
    font-size: 0.85rem;
    color: var(--navy);
    font-weight: 600;
  }
  .formation-duration span { font-size: 1.2rem; }
  .btn-formation {
    background: var(--navy);
    color: var(--white);
    padding: 8px 20px;
    border-radius: 3px;
    font-size: 0.8rem;
    font-weight: 600;
    text-decoration: none;
    transition: background 0.2s;
    border: none; cursor: pointer;
  }
  .btn-formation:hover { background: var(--gold); color: var(--navy); }

  /* STAGE */
  .stage-section { background: var(--gray-50); }
  .stage-header-content {
    display: grid; grid-template-columns: 1fr 1fr; gap: 60px; align-items: start;
    margin-bottom: 48px;
  }
  .stage-intro p { color: var(--gray-600); font-size: 1rem; line-height: 1.8; margin-bottom: 20px; }
  .stage-badge-large {
    background: var(--navy);
    color: var(--white);
    padding: 28px 32px;
    border-radius: 6px;
    text-align: center;
    border-bottom: 4px solid var(--gold);
  }
  .stage-badge-large .big-text {
    font-family: 'Playfair Display', serif;
    font-size: 3rem;
    font-weight: 900;
    color: var(--gold);
    display: block;
    line-height: 1;
  }
  .stage-badge-large p { color: rgba(255,255,255,0.8); font-size: 0.9rem; margin-top: 8px; }

  .niveaux-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 24px; }
  .niveau-card {
    background: var(--white);
    border-radius: 6px;
    border: 1px solid var(--gray-100);
    overflow: hidden;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .niveau-card:hover { transform: translateY(-4px); box-shadow: 0 16px 48px rgba(22,58,95,0.1); }
  .niveau-header {
    padding: 20px 24px;
    display: flex; align-items: center; gap: 14px;
  }
  .niveau-card:nth-child(1) .niveau-header { background: var(--navy); }
  .niveau-card:nth-child(2) .niveau-header { background: #1a4a74; }
  .niveau-card:nth-child(3) .niveau-header { background: var(--navy-dark); }
  .niveau-num {
    width: 40px; height: 40px;
    background: var(--gold);
    transform: rotate(45deg);
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0;
  }
  .niveau-num span { transform: rotate(-45deg); font-family: 'Playfair Display', serif; font-weight: 900; color: var(--navy); font-size: 1.1rem; }
  .niveau-header h3 { color: var(--white); font-size: 1rem; font-weight: 600; }
  .niveau-body { padding: 20px 24px; }
  .niveau-body ul { list-style: none; }
  .niveau-body ul li {
    display: flex; align-items: flex-start; gap: 8px;
    font-size: 0.85rem;
    color: var(--gray-600);
    padding: 7px 0;
    border-bottom: 1px solid rgba(0,0,0,0.04);
    line-height: 1.4;
  }
  .niveau-body ul li::before {
    content: '→';
    color: var(--mint);
    font-weight: 700;
    flex-shrink: 0;
    margin-top: 1px;
  }

  /* AVANTAGES */
  .avantages-section { background: var(--navy); }
  .avantages-section .section-title { color: var(--white); }
  .avantages-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 24px; }
  .avantage-card {
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(255,255,255,0.08);
    border-radius: 6px;
    padding: 32px 28px;
    transition: background 0.25s, border-color 0.25s, transform 0.2s;
    position: relative;
    overflow: hidden;
  }
  .avantage-card:hover {
    background: rgba(255,255,255,0.08);
    border-color: rgba(217,164,65,0.3);
    transform: translateY(-4px);
  }
  .avantage-icon {
    font-size: 2rem;
    margin-bottom: 16px;
    display: block;
  }
  .avantage-card h4 { color: var(--gold); font-size: 1rem; font-weight: 600; margin-bottom: 10px; }
  .avantage-card p { color: rgba(255,255,255,0.6); font-size: 0.87rem; line-height: 1.6; }

  /* TÉMOIGNAGES */
  .temoignages-section { background: var(--white); }
  .temoignages-slider {
    position: relative;
    overflow: hidden;
  }
  .temoignages-track {
    display: flex;
    gap: 28px;
    transition: transform 0.45s cubic-bezier(0.4, 0, 0.2, 1);
  }
  .temoignage-card {
    flex: 0 0 calc(33.33% - 19px);
    background: var(--gray-50);
    border: 1px solid var(--gray-100);
    border-radius: 6px;
    padding: 32px 28px;
    border-top: 3px solid var(--gold);
  }
  .temoignage-stars { color: var(--gold); font-size: 1rem; margin-bottom: 16px; letter-spacing: 2px; }
  .temoignage-text { color: var(--gray-600); font-size: 0.9rem; line-height: 1.75; margin-bottom: 20px; font-style: italic; }
  .temoignage-author { display: flex; align-items: center; gap: 12px; }
  .temoignage-avatar {
    width: 44px; height: 44px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--navy), var(--mint));
    display: flex; align-items: center; justify-content: center;
    color: white;
    font-weight: 700;
    font-size: 1rem;
  }
  .temoignage-author-info strong { display: block; font-size: 0.9rem; color: var(--navy); }
  .temoignage-author-info span { font-size: 0.78rem; color: var(--gold); font-weight: 500; }
  .slider-controls {
    display: flex; justify-content: center; gap: 12px; margin-top: 36px;
  }
  .slider-btn {
    width: 44px; height: 44px;
    border-radius: 50%;
    border: 2px solid var(--gray-300);
    background: transparent;
    cursor: pointer;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.1rem;
    transition: border-color 0.2s, background 0.2s;
    color: var(--navy);
  }
  .slider-btn:hover { border-color: var(--gold); background: var(--gold); color: var(--navy); }

  /* CONTACT */
  .contact-section { background: var(--gray-50); }
  .contact-grid { display: grid; grid-template-columns: 1fr 1.3fr; gap: 60px; align-items: start; }
  .contact-info h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.5rem;
    color: var(--navy);
    margin-bottom: 8px;
  }
  .contact-info > p { color: var(--gray-600); font-size: 0.9rem; line-height: 1.7; margin-bottom: 32px; }
  .contact-items { display: flex; flex-direction: column; gap: 20px; margin-bottom: 32px; }
  .contact-item { display: flex; gap: 16px; align-items: flex-start; }
  .contact-item-icon {
    width: 46px; height: 46px;
    background: var(--navy);
    border-radius: 4px;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.1rem;
    flex-shrink: 0;
  }
  .contact-item-text strong { display: block; font-size: 0.8rem; font-weight: 700; text-transform: uppercase; letter-spacing: 1px; color: var(--navy); margin-bottom: 3px; }
  .contact-item-text a, .contact-item-text span { color: var(--gray-600); font-size: 0.9rem; text-decoration: none; }
  .contact-item-text a:hover { color: var(--gold); }

  .map-placeholder {
    background: var(--gray-100);
    border-radius: 6px;
    height: 180px;
    display: flex; align-items: center; justify-content: center;
    color: var(--gray-600);
    font-size: 0.85rem;
    gap: 8px;
    border: 1px solid var(--gray-300);
  }

  .contact-form {
    background: var(--white);
    border-radius: 8px;
    padding: 40px;
    border: 1px solid var(--gray-100);
    box-shadow: 0 4px 24px rgba(22,58,95,0.06);
  }
  .contact-form h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.3rem;
    color: var(--navy);
    margin-bottom: 24px;
  }
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
  .form-group { margin-bottom: 18px; }
  .form-group label {
    display: block;
    font-size: 0.78rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 1px;
    color: var(--navy);
    margin-bottom: 6px;
  }
  .form-group input,
  .form-group select,
  .form-group textarea {
    width: 100%;
    padding: 12px 16px;
    border: 1.5px solid var(--gray-300);
    border-radius: 4px;
    font-family: 'Inter', sans-serif;
    font-size: 0.9rem;
    color: var(--gray-800);
    transition: border-color 0.2s;
    background: var(--white);
  }
  .form-group input:focus,
  .form-group select:focus,
  .form-group textarea:focus {
    outline: none;
    border-color: var(--navy);
  }
  .form-group textarea { resize: vertical; min-height: 100px; }
  .btn-submit {
    width: 100%;
    background: var(--navy);
    color: var(--white);
    padding: 15px 32px;
    font-size: 0.95rem;
    font-weight: 600;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background 0.2s, transform 0.2s;
    letter-spacing: 0.5px;
    position: relative;
    overflow: hidden;
  }
  .btn-submit::after {
    content: '';
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 4px;
    background: var(--gold);
  }
  .btn-submit:hover { background: var(--gold); color: var(--navy); transform: translateY(-2px); }
  .btn-submit:hover::after { background: var(--navy); }

  /* FOOTER */
  footer {
    background: var(--navy-dark);
    padding: 60px 5% 30px;
    position: relative;
    overflow: hidden;
  }
  footer::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 3px;
    background: linear-gradient(90deg, var(--gold), var(--mint));
  }
  .footer-grid {
    display: grid; grid-template-columns: 2fr 1fr 1fr; gap: 48px;
    max-width: 1200px; margin: 0 auto;
    padding-bottom: 40px;
    border-bottom: 1px solid rgba(255,255,255,0.08);
    margin-bottom: 28px;
  }
  .footer-brand p { color: rgba(255,255,255,0.55); font-size: 0.88rem; line-height: 1.7; margin-top: 16px; max-width: 280px; }
  .footer-col h4 { color: var(--gold); font-size: 0.75rem; font-weight: 700; letter-spacing: 2px; text-transform: uppercase; margin-bottom: 16px; }
  .footer-col ul { list-style: none; }
  .footer-col ul li { margin-bottom: 10px; }
  .footer-col ul li a {
    color: rgba(255,255,255,0.55);
    text-decoration: none;
    font-size: 0.88rem;
    transition: color 0.2s;
  }
  .footer-col ul li a:hover { color: var(--gold); }
  .footer-bottom {
    max-width: 1200px; margin: 0 auto;
    display: flex; align-items: center; justify-content: space-between;
  }
  .footer-bottom p { color: rgba(255,255,255,0.35); font-size: 0.8rem; }

  /* FLOATING BUTTONS */
  .floating-buttons {
    position: fixed;
    bottom: 28px; right: 28px;
    z-index: 999;
    display: flex; flex-direction: column; gap: 12px;
  }
  .float-btn {
    width: 52px; height: 52px;
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.4rem;
    text-decoration: none;
    box-shadow: 0 4px 20px rgba(0,0,0,0.25);
    transition: transform 0.2s;
  }
  .float-btn:hover { transform: scale(1.1); }
  .float-whatsapp { background: #25D366; }
  .float-phone { background: var(--gold); }

  /* SCROLL ANIMATION */
  .reveal {
    opacity: 0;
    transform: translateY(28px);
    transition: opacity 0.6s ease, transform 0.6s ease;
  }
  .reveal.visible { opacity: 1; transform: none; }

  /* RESPONSIVE */
  @media (max-width: 900px) {
    .nav-links { display: none; }
    .hamburger { display: flex; }
    .nav-links.open {
      display: flex; flex-direction: column;
      position: absolute; top: 72px; left: 0; right: 0;
      background: var(--navy);
      padding: 20px 5%;
      border-top: 1px solid rgba(255,255,255,0.1);
    }

    .hero-content { flex-direction: column; padding: 60px 0; }
    .hero-image { display: none; }
    .hero-stats { gap: 20px; }

    .about-grid,
    .stage-header-content,
    .contact-grid { grid-template-columns: 1fr; gap: 40px; }

    .formations-grid,
    .niveaux-grid,
    .avantages-grid { grid-template-columns: 1fr 1fr; }

    .about-values { grid-template-columns: 1fr; }
    .form-row { grid-template-columns: 1fr; }

    .footer-grid { grid-template-columns: 1fr 1fr; }
    .temoignage-card { flex: 0 0 calc(50% - 14px); }
  }
  @media (max-width: 600px) {
    .formations-grid,
    .niveaux-grid,
    .avantages-grid { grid-template-columns: 1fr; }
    .footer-grid { grid-template-columns: 1fr; }
    .temoignage-card { flex: 0 0 100%; }
    .hero-stats { flex-wrap: wrap; }
    .contact-form { padding: 28px 20px; }
  }
</style>
</head>
<body>

<!-- NAVIGATION -->
<nav id="navbar">
  <a href="#accueil" class="nav-logo">
    <div class="nav-logo-diamond"><span>G</span></div>
    <div class="nav-logo-text">
      <strong>GCF</strong>
      <span>Global Consulting & Formations</span>
    </div>
  </a>
  <ul class="nav-links" id="navLinks">
    <li><a href="#accueil">Accueil</a></li>
    <li><a href="#apropos">À propos</a></li>
    <li><a href="#formations">Formations</a></li>
    <li><a href="#stage">Stage</a></li>
    <li><a href="#contact" class="nav-cta">Nous contacter</a></li>
  </ul>
  <div class="hamburger" id="hamburger">
    <span></span><span></span><span></span>
  </div>
</nav>

<!-- HERO -->
<section class="hero" id="accueil">
  <div class="hero-bg-shape"></div>
  <div class="hero-diamond d1"></div>
  <div class="hero-diamond d2"></div>
  <div class="hero-diamond d3"></div>
  <div class="hero-stripe"></div>
  <div class="hero-content">
    <div class="hero-text">
      <div class="hero-eyebrow"><span>Cabinet Expert · Rabat · Maroc</span></div>
      <h1>
        <em>GCF</em> — Global<br>
        Consulting &<br>
        Formations
      </h1>
      <p class="hero-subtitle">Cabinet de Comptabilité, Fiscalité & Formation Professionnelle</p>
      <p class="hero-desc">Une expertise reconnue au service de votre montée en compétences. Formations 200% pratiques sur dossiers réels et logiciels professionnels.</p>
      <div class="hero-stats">
        <div class="hero-stat"><strong>25+</strong><span>Ans d'expérience</span></div>
        <div class="hero-stat"><strong>3</strong><span>Niveaux de stage</span></div>
        <div class="hero-stat"><strong>100%</strong><span>Pratique</span></div>
      </div>
      <div class="hero-buttons">
        <a href="#formations" class="btn-primary">Découvrir nos formations</a>
        <a href="#contact" class="btn-secondary">Nous contacter</a>
      </div>
    </div>
    <div class="hero-image">
      <div class="hero-image-frame">
        <div class="hero-image-placeholder">
          <div class="hero-avatar">KB</div>
          <div class="hero-image-name">
            <strong>M. Khalid Benmessaoud</strong>
            <span>Consultant · Formateur</span>
          </div>
        </div>
        <div class="hero-badge">
          <strong>25</strong>
          <span>ANS EXP.</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- À PROPOS -->
<section class="section about-section" id="apropos">
  <div class="container">
    <div class="section-header reveal">
      <span class="section-eyebrow">Notre mission</span>
      <h2 class="section-title">Qui sommes-<em>nous</em> ?</h2>
      <div class="section-divider"></div>
    </div>
    <div class="about-grid">
      <div class="about-text reveal">
        <p>GCF accompagne les étudiants, diplômés et professionnels souhaitant maîtriser la comptabilité pratique, la fiscalité, la paie et les travaux de fin d'exercice dans un cadre pédagogique rigoureux et concret.</p>
        <p>Notre cabinet allie expertise professionnelle et pédagogie active. Chaque session de formation est conçue autour de cas réels, de logiciels métier et d'un suivi individualisé pour garantir une maîtrise opérationnelle immédiate.</p>
        <div class="about-highlight">
          <p>"Notre approche est <strong>200% pratique</strong> — avec des dossiers réels issus de notre activité de cabinet et des exercices appliqués sur logiciel professionnel."</p>
        </div>
      </div>
      <div class="about-values reveal">
        <div class="value-card">
          <div class="value-icon">🎯</div>
          <h4>100% Pratique</h4>
          <p>Chaque formation s'appuie sur des dossiers comptables réels traités en cabinet.</p>
        </div>
        <div class="value-card">
          <div class="value-icon">🏆</div>
          <h4>Expertise reconnue</h4>
          <p>Plus de 25 ans d'expérience en comptabilité et fiscalité au Maroc.</p>
        </div>
        <div class="value-card">
          <div class="value-icon">📜</div>
          <h4>Certification</h4>
          <p>Un certificat officiel délivré à chaque stagiaire ayant validé sa formation.</p>
        </div>
        <div class="value-card">
          <div class="value-icon">🤝</div>
          <h4>Satisfaction garantie</h4>
          <p>Satisfaction ou remboursé — notre engagement envers votre réussite.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- FORMATEUR -->
<section class="section formateur-section" id="formateur">
  <div class="container">
    <div class="section-header reveal">
      <span class="section-eyebrow" style="color: var(--mint)">Votre expert</span>
      <h2 class="section-title">Votre <em>formateur</em></h2>
      <div class="section-divider"></div>
    </div>
    <div class="formateur-card reveal">
      <div class="formateur-photo">
        <div class="formateur-avatar">KB</div>
      </div>
      <div class="formateur-info">
        <h3>M. Khalid Benmessaoud</h3>
        <p class="formateur-title">Consultant — Formateur Expert en Comptabilité & Fiscalité</p>
        <div class="formateur-exp">⭐ Plus de 25 ans d'expérience professionnelle</div>
        <p class="formateur-desc">Après 25 ans d'exercice en cabinet comptable à Rabat, M. Benmessaoud a développé une pédagogie unique fondée sur la transmission de cas réels. Sa double casquette de praticien et de formateur lui permet d'ancrer chaque enseignement dans les réalités du terrain marocain.</p>
        <div class="formateur-skills">
          <span class="skill-tag">Comptabilité générale</span>
          <span class="skill-tag">Fiscalité (IS, IR, TVA)</span>
          <span class="skill-tag">Gestion de la paie</span>
          <span class="skill-tag">Déclarations CNSS</span>
          <span class="skill-tag">États de synthèse</span>
          <span class="skill-tag">Logiciels comptables</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- FORMATIONS -->
<section class="section formations-section" id="formations">
  <div class="container">
    <div class="section-header reveal">
      <span class="section-eyebrow">Catalogue</span>
      <h2 class="section-title">Nos <em>formations</em></h2>
      <div class="section-divider"></div>
    </div>
    <div class="formations-grid">
      <div class="formation-card reveal">
        <div class="formation-card-header">
          <div class="formation-num">Formation 01</div>
          <h3>Maîtriser les bonnes bases de la Comptabilité Générale</h3>
          <span class="formation-badge">Débutant</span>
        </div>
        <div class="formation-card-body">
          <ul class="formation-features">
            <li>Plan comptable marocain (CGNC)</li>
            <li>Enregistrement des opérations courantes</li>
            <li>Rapprochement bancaire</li>
            <li>Application sur logiciel comptable</li>
            <li>Dossier réel de cabinet</li>
          </ul>
          <div class="formation-footer">
            <div class="formation-duration"><span>⏱</span> 32 heures</div>
            <a href="#contact" class="btn-formation">S'inscrire</a>
          </div>
        </div>
      </div>
      <div class="formation-card reveal">
        <div class="formation-card-header">
          <div class="formation-num">Formation 02</div>
          <h3>Gestion de la Paie</h3>
          <span class="formation-badge">Pratique</span>
        </div>
        <div class="formation-card-body">
          <ul class="formation-features">
            <li>Calcul des salaires et retenues</li>
            <li>Déclarations CNSS mensuelles</li>
            <li>Déclarations IR sur salaires</li>
            <li>Bulletins de paie réels</li>
            <li>Logiciel de paie professionnel</li>
          </ul>
          <div class="formation-footer">
            <div class="formation-duration"><span>⏱</span> 32 heures</div>
            <a href="#contact" class="btn-formation">S'inscrire</a>
          </div>
        </div>
      </div>
      <div class="formation-card reveal">
        <div class="formation-card-header">
          <div class="formation-num">Formation 03</div>
          <h3>Travaux de Fin d'Exercice & États de Synthèse</h3>
          <span class="formation-badge">Avancé</span>
        </div>
        <div class="formation-card-body">
          <ul class="formation-features">
            <li>Inventaire et amortissements</li>
            <li>Provisions et régularisations</li>
            <li>Calcul et déclaration IS</li>
            <li>Bilan de fin d'exercice</li>
            <li>CPC, ESG, TF et TT</li>
          </ul>
          <div class="formation-footer">
            <div class="formation-duration"><span>⏱</span> 32 heures</div>
            <a href="#contact" class="btn-formation">S'inscrire</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- STAGE -->
<section class="section stage-section" id="stage">
  <div class="container">
    <div class="section-header reveal">
      <span class="section-eyebrow">Programme</span>
      <h2 class="section-title">Stage <em>professionnel</em> en comptabilité</h2>
      <div class="section-divider"></div>
    </div>
    <div class="stage-header-content reveal">
      <div class="stage-intro">
        <p>Notre stage pédagogique professionnel est conçu pour vous immerger dans la réalité du métier. Vous travaillez sur un dossier comptable complet d'une entreprise réelle, avec les mêmes logiciels utilisés par les cabinets professionnels.</p>
        <p>Le programme est structuré en trois niveaux progressifs, chacun correspondant à une étape du cycle comptable annuel d'une entreprise marocaine.</p>
      </div>
      <div class="stage-badge-large">
        <span class="big-text">200%</span>
        <p>Pratique sur dossier réel et logiciel professionnel</p>
      </div>
    </div>
    <div class="niveaux-grid">
      <div class="niveau-card reveal">
        <div class="niveau-header">
          <div class="niveau-num"><span>1</span></div>
          <h3>Niveau 1 — Fondamentaux</h3>
        </div>
        <div class="niveau-body">
          <ul>
            <li>Organisation du dossier comptable</li>
            <li>Manipulation du logiciel comptable</li>
            <li>Traitement du dossier comptable</li>
            <li>Rapprochement bancaire</li>
            <li>Analyse des comptes</li>
            <li>Achats fournisseurs</li>
            <li>Ventes clients</li>
            <li>Opérations de banque</li>
            <li>Établissement du bilan</li>
          </ul>
        </div>
      </div>
      <div class="niveau-card reveal">
        <div class="niveau-header">
          <div class="niveau-num"><span>2</span></div>
          <h3>Niveau 2 — Déclarations</h3>
        </div>
        <div class="niveau-body">
          <ul>
            <li>Déclarations TVA</li>
            <li>Déclarations CNSS</li>
            <li>Déclarations IR sur salaires</li>
            <li>Analyse approfondie des comptes</li>
            <li>Bilan avant inventaire</li>
          </ul>
        </div>
      </div>
      <div class="niveau-card reveal">
        <div class="niveau-header">
          <div class="niveau-num"><span>3</span></div>
          <h3>Niveau 3 — Clôture</h3>
        </div>
        <div class="niveau-body">
          <ul>
            <li>Travaux d'inventaire</li>
            <li>Gestion des stocks</li>
            <li>Amortissements et provisions</li>
            <li>Régularisation des charges et produits</li>
            <li>Bilan après inventaire</li>
            <li>Calcul et déclaration IS</li>
            <li>États de synthèse complets</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- AVANTAGES -->
<section class="section avantages-section" id="avantages">
  <div class="container">
    <div class="section-header reveal">
      <span class="section-eyebrow" style="color: var(--mint)">Pourquoi nous choisir</span>
      <h2 class="section-title">Nos <em>engagements</em></h2>
      <div class="section-divider"></div>
    </div>
    <div class="avantages-grid">
      <div class="avantage-card reveal">
        <span class="avantage-icon">🎯</span>
        <h4>Formation 200% pratique</h4>
        <p>Aucune théorie creuse — chaque exercice est tiré d'un dossier client réel traité en cabinet.</p>
      </div>
      <div class="avantage-card reveal">
        <span class="avantage-icon">📂</span>
        <h4>Dossiers réels</h4>
        <p>Vous apprenez sur les mêmes pièces comptables et fichiers qu'un professionnel en exercice.</p>
      </div>
      <div class="avantage-card reveal">
        <span class="avantage-icon">👤</span>
        <h4>Accompagnement personnalisé</h4>
        <p>Suivi individuel tout au long de la formation — questions, corrections et conseils à la demande.</p>
      </div>
      <div class="avantage-card reveal">
        <span class="avantage-icon">📜</span>
        <h4>Certificat délivré</h4>
        <p>Un certificat de formation professionnel remis à la fin du parcours, valorisable sur votre CV.</p>
      </div>
      <div class="avantage-card reveal">
        <span class="avantage-icon">⭐</span>
        <h4>25 ans d'expérience</h4>
        <p>Un formateur issu du terrain, avec une maîtrise des spécificités du droit fiscal marocain.</p>
      </div>
      <div class="avantage-card reveal">
        <span class="avantage-icon">💯</span>
        <h4>Satisfaction ou remboursé</h4>
        <p>Si la formation ne répond pas à vos attentes, nous vous remboursons — sans condition.</p>
      </div>
    </div>
  </div>
</section>

<!-- TÉMOIGNAGES -->
<section class="section temoignages-section" id="temoignages">
  <div class="container">
    <div class="section-header reveal">
      <span class="section-eyebrow">Retours stagiaires</span>
      <h2 class="section-title">Ils nous font <em>confiance</em></h2>
      <div class="section-divider"></div>
    </div>
    <div class="temoignages-slider reveal">
      <div class="temoignages-track" id="temoTrack">
        <div class="temoignage-card">
          <div class="temoignage-stars">★★★★★</div>
          <p class="temoignage-text">"La formation sur les travaux de fin d'exercice m'a permis de décrocher mon premier poste en cabinet comptable dès la fin du stage. La méthode de M. Benmessaoud est vraiment efficace."</p>
          <div class="temoignage-author">
            <div class="temoignage-avatar">SA</div>
            <div class="temoignage-author-info"><strong>Salma A.</strong><span>Comptable — Casablanca</span></div>
          </div>
        </div>
        <div class="temoignage-card">
          <div class="temoignage-stars">★★★★★</div>
          <p class="temoignage-text">"Avant la formation GCF, je ne maîtrisais pas du tout la paie. Après 32 heures de pratique intensive, je gère maintenant les déclarations CNSS de mon employeur sans aucune difficulté."</p>
          <div class="temoignage-author">
            <div class="temoignage-avatar">YB</div>
            <div class="temoignage-author-info"><strong>Youssef B.</strong><span>Gestionnaire RH — Rabat</span></div>
          </div>
        </div>
        <div class="temoignage-card">
          <div class="temoignage-stars">★★★★★</div>
          <p class="temoignage-text">"Le stage niveau 3 couvre tout ce qu'un comptable doit maîtriser pour clôturer un exercice. Les explications sont claires, les exercices concrets. Je recommande vivement GCF."</p>
          <div class="temoignage-author">
            <div class="temoignage-avatar">NK</div>
            <div class="temoignage-author-info"><strong>Nadia K.</strong><span>Étudiante en BTS Comptabilité</span></div>
          </div>
        </div>
        <div class="temoignage-card">
          <div class="temoignage-stars">★★★★★</div>
          <p class="temoignage-text">"J'ai suivi la formation comptabilité générale après mon diplôme ENCG. Le fait de travailler sur de vrais dossiers m'a donné une vraie confiance face aux employeurs lors des entretiens."</p>
          <div class="temoignage-author">
            <div class="temoignage-avatar">AO</div>
            <div class="temoignage-author-info"><strong>Amine O.</strong><span>Lauréat ENCG — Rabat</span></div>
          </div>
        </div>
        <div class="temoignage-card">
          <div class="temoignage-stars">★★★★★</div>
          <p class="temoignage-text">"L'accompagnement personnalisé fait toute la différence. M. Benmessaoud prend le temps d'expliquer chaque détail jusqu'à ce que vous compreniez vraiment. Excellent cabinet de formation."</p>
          <div class="temoignage-author">
            <div class="temoignage-avatar">LM</div>
            <div class="temoignage-author-info"><strong>Laila M.</strong><span>Comptable indépendante</span></div>
          </div>
        </div>
        <div class="temoignage-card">
          <div class="temoignage-stars">★★★★★</div>
          <p class="temoignage-text">"J'ai recommandé GCF à trois collègues de mon entreprise. Tous ont obtenu leur certificat et tous travaillent maintenant de façon autonome sur les déclarations fiscales. Résultats concrets garantis."</p>
          <div class="temoignage-author">
            <div class="temoignage-avatar">HT</div>
            <div class="temoignage-author-info"><strong>Hamid T.</strong><span>Directeur financier — PME</span></div>
          </div>
        </div>
      </div>
    </div>
    <div class="slider-controls">
      <button class="slider-btn" id="prevBtn">←</button>
      <button class="slider-btn" id="nextBtn">→</button>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section class="section contact-section" id="contact">
  <div class="container">
    <div class="section-header reveal">
      <span class="section-eyebrow">Prenez contact</span>
      <h2 class="section-title">Demandez un <em>rendez-vous</em></h2>
      <div class="section-divider"></div>
    </div>
    <div class="contact-grid">
      <div class="contact-info reveal">
        <h3>Nous sommes à Agdal, Rabat</h3>
        <p>Prenez contact pour une formation sur mesure ou pour en savoir plus sur nos stages professionnels. Notre équipe vous répond dans les 24 heures.</p>
        <div class="contact-items">
          <div class="contact-item">
            <div class="contact-item-icon">📞</div>
            <div class="contact-item-text">
              <strong>Téléphone</strong>
              <a href="tel:+212600255555">06 00 25 55 55</a>
            </div>
          </div>
          <div class="contact-item">
            <div class="contact-item-icon">📍</div>
            <div class="contact-item-text">
              <strong>Adresse</strong>
              <span>25 Bis Rue Jabal Bouiblane, Appartement N°15<br>Agdal, Rabat</span>
            </div>
          </div>
          <div class="contact-item">
            <div class="contact-item-icon">💬</div>
            <div class="contact-item-text">
              <strong>WhatsApp</strong>
              <a href="https://wa.me/212600255555">Écrire sur WhatsApp</a>
            </div>
          </div>
        </div>
        <div class="map-placeholder">
          📍 Agdal, Rabat — 25 Bis Rue Jabal Bouiblane, Appt. 15
        </div>
      </div>
      <div class="contact-form reveal">
        <h3>Formulaire de contact</h3>
        <div class="form-row">
          <div class="form-group">
            <label>Nom complet</label>
            <input type="text" placeholder="Votre nom">
          </div>
          <div class="form-group">
            <label>Téléphone</label>
            <input type="tel" placeholder="06 XX XX XX XX">
          </div>
        </div>
        <div class="form-group">
          <label>Email</label>
          <input type="email" placeholder="votre@email.com">
        </div>
        <div class="form-group">
          <label>Formation souhaitée</label>
          <select>
            <option value="">— Sélectionner une formation —</option>
            <option>Comptabilité générale (32h)</option>
            <option>Gestion de la paie (32h)</option>
            <option>Travaux de fin d'exercice (32h)</option>
            <option>Stage professionnel — Niveau 1</option>
            <option>Stage professionnel — Niveau 2</option>
            <option>Stage professionnel — Niveau 3</option>
            <option>Autre</option>
          </select>
        </div>
        <div class="form-group">
          <label>Message</label>
          <textarea placeholder="Décrivez votre situation ou posez vos questions…"></textarea>
        </div>
        <button class="btn-submit" onclick="handleSubmit()">Demander un rendez-vous →</button>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-grid">
    <div class="footer-brand">
      <a href="#accueil" class="nav-logo" style="display:inline-flex">
        <div class="nav-logo-diamond"><span>G</span></div>
        <div class="nav-logo-text">
          <strong>GCF</strong>
          <span>Global Consulting & Formations</span>
        </div>
      </a>
      <p>Cabinet de Comptabilité, Fiscalité et Formation Professionnelle à Rabat. Plus de 25 ans d'expérience au service de votre développement professionnel.</p>
    </div>
    <div class="footer-col">
      <h4>Navigation</h4>
      <ul>
        <li><a href="#accueil">Accueil</a></li>
        <li><a href="#apropos">À propos</a></li>
        <li><a href="#formations">Formations</a></li>
        <li><a href="#stage">Stages</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Contact</h4>
      <ul>
        <li><a href="tel:+212600255555">06 00 25 55 55</a></li>
        <li><a href="https://wa.me/212600255555">WhatsApp</a></li>
        <li><a href="#">Agdal, Rabat</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <p>© 2025 GCF — Global Consulting & Formations. Tous droits réservés.</p>
    <p>Agdal, Rabat · Maroc</p>
  </div>
</footer>

<!-- FLOATING BUTTONS -->
<div class="floating-buttons">
  <a href="https://wa.me/212600255555" class="float-btn float-whatsapp" title="WhatsApp">💬</a>
  <a href="tel:+212600255555" class="float-btn float-phone" title="Appeler">📞</a>
</div>

<script>
  // HAMBURGER
  const hamburger = document.getElementById('hamburger');
  const navLinks = document.getElementById('navLinks');
  hamburger.addEventListener('click', () => navLinks.classList.toggle('open'));

  // SCROLL REVEAL
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
  }, { threshold: 0.1 });
  document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

  // SLIDER
  const track = document.getElementById('temoTrack');
  let current = 0;
  const visibleCount = () => window.innerWidth <= 600 ? 1 : window.innerWidth <= 900 ? 2 : 3;
  const cards = track.querySelectorAll('.temoignage-card');

  function updateSlider() {
    const vc = visibleCount();
    const maxIndex = cards.length - vc;
    current = Math.min(current, maxIndex);
    const w = cards[0].offsetWidth + 28;
    track.style.transform = `translateX(-${current * w}px)`;
  }

  document.getElementById('nextBtn').addEventListener('click', () => {
    const vc = visibleCount();
    if (current < cards.length - vc) { current++; updateSlider(); }
    else { current = 0; updateSlider(); }
  });
  document.getElementById('prevBtn').addEventListener('click', () => {
    if (current > 0) { current--; updateSlider(); }
    else { current = cards.length - visibleCount(); updateSlider(); }
  });
  window.addEventListener('resize', () => updateSlider());

  // FORM
  function handleSubmit() {
    const btn = document.querySelector('.btn-submit');
    btn.textContent = '✓ Message envoyé — nous vous rappelons sous 24h';
    btn.style.background = 'var(--mint)';
    btn.style.color = 'var(--navy)';
    setTimeout(() => {
      btn.textContent = 'Demander un rendez-vous →';
      btn.style.background = '';
      btn.style.color = '';
    }, 4000);
  }

  // NAV scroll effect
  window.addEventListener('scroll', () => {
    const nav = document.getElementById('navbar');
    nav.style.boxShadow = window.scrollY > 20 ? '0 4px 24px rgba(0,0,0,0.2)' : '';
  });
</script>
</body>
</html>
