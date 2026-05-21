# AURA
O Aura protege 
CTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aura — Segurança Inteligente e Integração no Varejo</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

    <style>
        /* ==========================================================================
           VARIÁVEIS DE AMBIENTE E CORES GLOBAIS (DESIGN SYSTEM)
           ========================================================================== */
        :root {
            --bg-dark: #0F172A;        
            --bg-card: #1E293B;        
            --purple-tech: #7C3AED;    
            --cyan-route: #06B6D4;     
            --green-safe: #22C55E;     
            --danger: #EF4444;         
            --white: #FFFFFF;
            --gray-50: #F8FAFC;
            --gray-100: #F1F5F9;
            --gray-300: #CBD5E1;
            --gray-400: #94A3B8;
            --gray-700: #334155;
            
            --font-main: 'Inter', sans-serif;
            --transition-smooth: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            --shadow-soft: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
            --shadow-lg: 0 20px 25px -5px rgba(0, 0, 0, 0.15), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }

        /* ==========================================================================
           RESETS E CONFIGURAÇÕES BASE
           ========================================================================== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            font-size: 16px;
        }

        body {
            font-family: var(--font-main);
            background-color: var(--white);
            color: var(--gray-700);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1.5rem;
        }

        .container-narrow {
            max-width: 650px;
            margin: 0 auto;
            padding: 0 1.5rem;
        }

        .section-padding {
            padding: 6rem 0;
        }

        .bg-light { background-color: var(--gray-50); }
        .bg-dark { background-color: var(--bg-dark); }
        .text-white { color: var(--white); }

        .section-header {
            margin-bottom: 4rem;
            max-width: 700px;
        }

        .section-header h2 {
            font-size: 2.25rem;
            font-weight: 800;
            color: var(--bg-dark);
            margin-top: 0.5rem;
            letter-spacing: -0.025em;
        }

        .section-tag {
            font-size: 0.875rem;
            font-weight: 700;
            text-transform: uppercase;
            color: var(--purple-tech);
            letter-spacing: 0.05em;
        }

        .tag-light { color: var(--cyan-route); }

        /* ==========================================================================
           COMPONENTES: BOTÕES E CARDS
           ========================================================================== */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            font-weight: 600;
            font-size: 0.95rem;
            padding: 0.85rem 1.75rem;
            border-radius: 0.5rem;
            border: none;
            cursor: pointer;
            text-decoration: none;
            transition: var(--transition-smooth);
        }

        .btn-sm {
            padding: 0.5rem 1.25rem;
            font-size: 0.875rem;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--purple-tech), #6366F1);
            color: var(--white);
            box-shadow: 0 4px 14px rgba(124, 58, 237, 0.4);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(124, 58, 237, 0.6);
        }

        .btn-secondary {
            background-color: rgba(255, 255, 255, 0.1);
            color: var(--white);
            border: 1px solid rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(8px);
        }

        .btn-secondary:hover {
            background-color: rgba(255, 255, 255, 0.2);
            transform: translateY(-2px);
        }

        .btn-cyan {
            background-color: var(--cyan-route);
            color: var(--bg-dark);
            font-weight: 700;
        }

        .btn-cyan:hover {
            background-color: #22d3ee;
            transform: translateY(-2px);
            box-shadow: 0 4px 14px rgba(6, 182, 212, 0.4);
        }

        .btn-block { width: 100%; }

        .grid {
            display: grid;
            gap: 2rem;
        }
        .grid-3 { grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); }
        .grid-4 { grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); }
        .grid-5 { grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); }

        .card {
            background-color: var(--white);
            padding: 2.5rem 2rem;
            border-radius: 1rem;
            box-shadow: var(--shadow-soft);
            border: 1px solid var(--gray-100);
            transition: var(--transition-smooth);
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-lg);
        }

        .card-danger { border-top: 4px solid var(--danger); }
        .card-feature { border-top: 4px solid var(--purple-tech); }

        .card-icon {
            font-size: 2rem;
            margin-bottom: 1.25rem;
        }

        .card-icon-tech {
            font-size: 2rem;
            background: linear-gradient(135deg, rgba(124, 58, 237, 0.1), rgba(6, 182, 212, 0.1));
            width: 60px;
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 0.75rem;
            margin-bottom: 1.5rem;
        }

        .card h3 {
            font-size: 1.25rem;
            color: var(--bg-dark);
            margin-bottom: 0.75rem;
            font-weight: 700;
        }

        /* ==========================================================================
           1. CABEÇALHO FIXO
           ========================================================================== */
        .main-header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background-color: rgba(15, 23, 42, 0.9);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.08);
            transition: var(--transition-smooth);
        }

        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 1.25rem 1.5rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo-area {
            display: flex;
            flex-direction: column;
        }

        .logo-text {
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--white);
            letter-spacing: -0.5px;
            line-height: 1;
        }

        .logo-subtitle {
            font-size: 0.6875rem;
            color: var(--cyan-route);
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin-top: 0.25rem;
        }

        .nav-menu {
            display: flex;
            gap: 1.5rem;
        }

        .nav-link {
            color: var(--gray-300);
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 500;
            transition: var(--transition-smooth);
            padding: 0.25rem 0;
            position: relative;
        }

        .nav-link:hover, .nav-link.active {
            color: var(--white);
        }

        .nav-link.active::after {
            content: '';
            position: absolute;
            bottom: -4px;
            left: 0;
            width: 100%;
            height: 2px;
            background-color: var(--cyan-route);
        }

        .header-actions {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .menu-toggle {
            display: none;
            background: none;
            border: none;
            cursor: pointer;
            flex-direction: column;
            gap: 5px;
        }

        .menu-toggle .bar {
            width: 25px;
            height: 2px;
            background-color: var(--white);
            transition: var(--transition-smooth);
        }

        /* ==========================================================================
           2. SEÇÃO HERO (INTERFACE DE MAPA ABSTRATA)
           ========================================================================== */
        .hero-section {
            background-color: var(--bg-dark);
            padding: 10rem 0 7rem 0;
            color: var(--white);
            position: relative;
            overflow: hidden;
        }

        .hero-section::before {
            content: '';
            position: absolute;
            top: -20%;
            right: -10%;
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(124, 58, 237, 0.15) 0%, transparent 70%);
            z-index: 1;
        }

        .hero-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1.5rem;
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            gap: 4rem;
            align-items: center;
            position: relative;
            z-index: 2;
        }

        .badge {
            display: inline-block;
            background-color: rgba(124, 58, 237, 0.2);
            border: 1px solid rgba(124, 58, 237, 0.4);
            color: #a78bfa;
            padding: 0.35rem 1rem;
            border-radius: 2rem;
            font-size: 0.8rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.05em;
            margin-bottom: 1.5rem;
        }

        .hero-title {
            font-size: 3rem;
            font-weight: 800;
            line-height: 1.15;
            letter-spacing: -0.03em;
            margin-bottom: 1.5rem;
            background: linear-gradient(to right, #ffffff, var(--gray-300));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-subtitle {
            font-size: 1.15rem;
            color: var(--gray-400);
            margin-bottom: 2rem;
            max-width: 600px;
        }

        .hero-quote {
            border-left: 3px solid var(--cyan-route);
            padding-left: 1rem;
            font-style: italic;
            color: var(--cyan-route);
            margin-bottom: 2.5rem;
            font-weight: 500;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
        }

        /* Simulador do App de Mapa */
        .hero-visual {
            display: flex;
            justify-content: center;
        }

        .map-mockup {
            background-color: #1e293b;
            width: 100%;
            max-width: 360px;
            height: 460px;
            border-radius: 1.5rem;
            border: 4px solid #334155;
            box-shadow: var(--shadow-lg);
            display: flex;
            flex-direction: column;
            overflow: hidden;
            position: relative;
        }

        .map-header {
            background-color: rgba(15, 23, 42, 0.8);
            padding: 1rem;
            z-index: 5;
        }

        .search-bar-mock {
            background-color: #334155;
            padding: 0.5rem 1rem;
            border-radius: 0.5rem;
            font-size: 0.8rem;
            color: var(--gray-300);
        }

        .map-body {
            flex: 1;
            background-color: #0f172a;
            background-image: 
                linear-gradient(rgba(255,255,255,0.03) 1px, transparent 1px),
                linear-gradient(90deg, rgba(255,255,255,0.03) 1px, transparent 1px);
            background-size: 20px 20px;
            position: relative;
            overflow: hidden;
        }

        .map-route-line {
            position: absolute;
            width: 4px;
            height: 250px;
            background-color: var(--cyan-route);
            top: 80px;
            left: 120px;
            transform: rotate(25deg);
            box-shadow: 0 0 12px var(--cyan-route);
        }

        .map-user-dot {
            position: absolute;
            width: 12px;
            height: 12px;
            background-color: #3b82f6;
            border: 2px solid var(--white);
            border-radius: 50%;
            top: 75px;
            left: 115px;
            box-shadow: 0 0 8px #3b82f6;
        }

        .safe-zone-marker {
            position: absolute;
            background-color: var(--bg-dark);
            border: 1px solid var(--green-safe);
            padding: 0.35rem 0.6rem;
            border-radius: 0.5rem;
            font-size: 0.7rem;
            font-weight: 700;
            color: var(--white);
            display: flex;
            align-items: center;
            gap: 4px;
        }

        .marker-1 { top: 180px; left: 140px; }
        .marker-2 { top: 280px; left: 190px; }

        .marker-pulse {
            width: 6px;
            height: 6px;
            background-color: var(--green-safe);
            border-radius: 50%;
            display: inline-block;
            animation: pulse 1.8s infinite;
        }

        .risk-area-indicator {
            position: absolute;
            bottom: 40px;
            left: 20px;
            background-color: rgba(239, 68, 110, 0.2);
            border: 1px dashed var(--danger);
            color: #fca5a5;
            padding: 0.25rem 0.5rem;
            border-radius: 0.25rem;
            font-size: 0.65rem;
        }

        .map-card-info {
            background-color: rgba(15, 23, 42, 0.95);
            padding: 1rem;
            border-top: 1px solid #334155;
            z-index: 5;
        }

        .info-status {
            font-size: 0.8rem;
            font-weight: 700;
            color: var(--green-safe);
            margin-bottom: 0.25rem;
        }

        .info-details {
            font-size: 0.75rem;
            color: var(--gray-400);
        }

        /* ==========================================================================
           3. CONCEITO CENTRAL: SAFE ZONES COM SELO VETORIAL
           ========================================================================== */
        .safe-zones-section {
            background: linear-gradient(135deg, #1E1B4B 0%, var(--bg-dark) 100%);
            color: var(--white);
        }

        .safe-zones-wrapper {
            display: grid;
            grid-template-columns: 1.1fr 0.9fr;
            gap: 4rem;
            align-items: center;
        }

        .benefits-split {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            margin-top: 2.5rem;
        }

        .benefit-block h4 {
            font-size: 1.15rem;
            color: var(--cyan-route);
            margin-bottom: 1rem;
            font-weight: 700;
        }

        .benefit-block ul { list-style: none; }

        .benefit-block ul li {
            font-size: 0.9rem;
            color: var(--gray-300);
            margin-bottom: 0.75rem;
            position: relative;
            padding-left: 1.25rem;
        }

        .benefit-block ul li::before {
            content: "✓";
            position: absolute;
            left: 0;
            color: var(--green-safe);
            font-weight: 700;
        }

        /* Selo de Certificação Digital */
        .safe-zones-badge-display {
            display: flex;
            justify-content: center;
            position: relative;
        }

        .seal-container {
            position: relative;
            padding: 2rem;
        }

        .seal-glow {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 280px;
            height: 280px;
            background: radial-gradient(circle, rgba(6, 182, 212, 0.2) 0%, transparent 70%);
            z-index: 1;
        }

        .seal-badge {
            background: radial-gradient(135deg, #1e293b, #0f172a);
            border: 4px double var(--cyan-route);
            width: 280px;
            height: 280px;
            border-radius: 50%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 1.5rem;
            box-shadow: var(--shadow-lg), inset 0 0 20px rgba(6, 182, 212, 0.2);
            position: relative;
            z-index: 2;
            animation: rotateSlow 20s linear infinite;
        }

        .seal-badge * {
            animation: stopRotation 20s linear infinite;
        }

        .seal-icon {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }

        .seal-badge h3 {
            font-size: 0.65rem;
            color: var(--gray-400);
            letter-spacing: 2px;
            text-transform: uppercase;
            margin-bottom: 0.25rem;
        }

        .seal-badge h2 {
            font-size: 1.25rem;
            color: var(--white);
            font-weight: 800;
            letter-spacing: 0.5px;
            margin-bottom: 0.5rem;
            text-shadow: 0 2px 4px rgba(0,0,0,0.5);
        }

        .seal-badge p {
            font-size: 0.65rem;
            color: var(--cyan-route);
            font-weight: 600;
            max-width: 180px;
            line-height: 1.3;
        }

        .seal-year {
            font-size: 0.75rem;
            font-weight: 700;
            margin-top: 0.5rem;
            color: var(--gray-400);
        }

        /* ==========================================================================
           4. BUSINESS MODEL CANVAS (MATRIZ)
           ========================================================================== */
        .canvas-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 1rem;
            margin-top: 2rem;
        }

        .canvas-cell {
            background-color: var(--white);
            border: 1px solid var(--gray-300);
            padding: 1.5rem;
            border-radius: 0.5rem;
            transition: var(--transition-smooth);
        }

        .canvas-cell:hover {
            border-color: var(--purple-tech);
            background-color: rgba(124, 58, 237, 0.01);
        }

        .canvas-cell h4 {
            font-size: 0.95rem;
            color: var(--bg-dark);
            margin-bottom: 0.7rem;
            font-weight: 700;
        }

        .canvas-cell p {
            font-size: 0.85rem;
            color: var(--gray-700);
            line-height: 1.5;
        }

        .canvas-wide {
            grid-column: span 2;
            background-color: rgba(241, 245, 249, 0.5);
        }

        /* ==========================================================================
           5. METRICAS E EQUIPE ACADÊMICA
           ========================================================================== */
        .impact-section {
            background: linear-gradient(135deg, var(--bg-dark), #111827);
            text-align: center;
        }

        .impact-card { padding: 1.5rem; }

        .impact-num {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }

        .impact-card p {
            font-size: 0.9rem;
            color: var(--gray-300);
            font-weight: 500;
        }

        .card-team {
            text-align: center;
            padding: 2rem 1.5rem;
        }

        .avatar-placeholder {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, #EEF2F6, var(--gray-300));
            border-radius: 50%;
            margin: 0 auto 1.25rem auto;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            color: var(--gray-700);
            font-size: 1.25rem;
        }

        .card-team h3 {
            font-size: 1.15rem;
            margin-bottom: 0.25rem;
        }

        .card-team .role {
            font-size: 0.85rem;
            color: var(--purple-tech);
            font-weight: 600;
        }

        .academic-footer-box {
            margin-top: 4rem;
            padding: 2rem;
            background-color: var(--gray-50);
            border-radius: 0.75rem;
            border-left: 4px solid var(--purple-tech);
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 1.5rem;
        }

        .academic-footer-box p { font-size: 0.9rem; }

        /* ==========================================================================
           6. FORMULÁRIO DE LEADS E INTERESSE
           ========================================================================== */
        .form-lead {
            background-color: var(--bg-card);
            padding: 3rem;
            border-radius: 1rem;
            border: 1px solid rgba(255, 255, 255, 0.05);
            box-shadow: var(--shadow-lg);
        }

        .form-group {
            margin-bottom: 1.5rem;
            display: flex;
            flex-direction: column;
        }

        .form-group label {
            font-size: 0.875rem;
            font-weight: 600;
            color: var(--gray-300);
            margin-bottom: 0.5rem;
        }

        .form-group input, .form-group select, .form-group textarea {
            font-family: var(--font-main);
            background-color: var(--bg-dark);
            border: 1px solid var(--gray-700);
            padding: 0.85rem 1rem;
            border-radius: 0.5rem;
            color: var(--white);
            font-size: 0.95rem;
            transition: var(--transition-smooth);
        }

        .form-group input:focus, .form-group select:focus, .form-group textarea:focus {
            outline: none;
            border-color: var(--cyan-route);
            box-shadow: 0 0 0 3px rgba(6, 182, 212, 0.15);
        }

        .error-msg {
            color: var(--danger);
            font-size: 0.75rem;
            margin-top: 0.35rem;
            font-weight: 500;
            display: none;
        }

        .form-group.invalid input, .form-group.invalid select { border-color: var(--danger); }
        .form-group.invalid .error-msg { display: block; }

        .success-box-toast {
            display: none;
            align-items: center;
            gap: 1rem;
            background-color: rgba(34, 197, 94, 0.15);
            border: 1px solid var(--green-safe);
            padding: 1.5rem;
            border-radius: 0.75rem;
            margin-top: 2rem;
            color: var(--white);
        }

        .success-icon {
            background-color: var(--green-safe);
            width: 32px;
            height: 32px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            font-weight: bold;
            font-size: 1rem;
            flex-shrink: 0;
        }

        .success-box-toast h4 { color: var(--green-safe); margin-bottom: 0.15rem; }
        .success-box-toast p { font-size: 0.85rem; color: var(--gray-300); }

        /* ==========================================================================
           7. RODAPÉ DA PÁGINA
           ========================================================================== */
        .main-footer {
            background-color: #0B0F19;
            color: var(--gray-400);
            padding: 4rem 0 2rem 0;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr;
            gap: 4rem;
            margin-bottom: 3rem;
        }

        .footer-tagline {
            font-size: 0.9rem;
            margin-top: 0.75rem;
            max-width: 300px;
        }

        .main-footer h4 {
            color: var(--white);
            font-size: 1rem;
            margin-bottom: 1.25rem;
            font-weight: 600;
        }

        .footer-links { list-style: none; }
        .footer-links li { margin-bottom: 0.65rem; }
        .footer-links a {
            color: var(--gray-400);
            text-decoration: none;
            font-size: 0.9rem;
            transition: var(--transition-smooth);
        }
        .footer-links a:hover { color: var(--cyan-route); }

        .footer-bottom {
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            padding-top: 2rem;
            text-align: center;
            font-size: 0.8rem;
            display: flex;
            flex-direction: column;
            gap: 0.5rem;
        }

        /* ==========================================================================
           KEYFRAMES DE ANIMAÇÃO
           ========================================================================== */
        @keyframes pulse {
            0% { transform: scale(0.9); box-shadow: 0 0 0 0 rgba(34, 197, 94, 0.7); }
            70% { transform: scale(1); box-shadow: 0 0 0 8px rgba(34, 197, 94, 0); }
            100% { transform: scale(0.9); box-shadow: 0 0 0 0 rgba(34, 197, 94, 0); }
        }

        @keyframes rotateSlow {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        @keyframes stopRotation {
            from { transform: rotate(0deg); }
            to { transform: rotate(-360deg); }
        }

        /* ==========================================================================
           RESPONSIVIDADE (MEDIA QUERIES)
           ========================================================================== */
        @media (max-width: 992px) {
            .hero-container, .safe-zones-wrapper { grid-template-columns: 1fr; gap: 3rem; }
            .hero-content { text-align: center; }
            .hero-subtitle, .hero-quote { margin-left: auto; margin-right: auto; }
            .hero-buttons { justify-content: center; }
            .canvas-grid { grid-template-columns: repeat(2, 1fr); }
            .canvas-wide { grid-column: span 2; }
            .footer-grid { grid-template-columns: 1fr 1fr; gap: 2rem; }
        }

        @media (max-width: 768px) {
            .section-padding { padding: 4rem 0; }
            .hero-title { font-size: 2.25rem; }
            .menu-toggle { display: flex; }
            
            .nav-menu {
                position: fixed;
                top: 74px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 74px);
                background-color: var(--bg-dark);
                flex-direction: column;
                padding: 2rem;
                gap: 2rem;
                transition: var(--transition-smooth);
                z-index: 999;
            }
            
            .nav-menu.active { left: 0; }
            .header-actions .btn { display: none; }
            .benefits-split { grid-template-columns: 1fr; }
            .canvas-grid { grid-template-columns: 1fr; }
            .canvas-wide { grid-column: span 1; }
            .footer-grid { grid-template-columns: 1fr; }
            .academic-footer-box { flex-direction: column; gap: 0.75rem; }
        }
    </style>
</head>
<body>

    <header class="main-header">
        <div class="header-container">
            <div class="logo-area">
                <span class="logo-text">Aura</span>
                <span class="logo-subtitle">Segurança Inteligente no Varejo</span> [cite: 33]
            </div>
            
            <nav class="nav-menu" id="navMenu">
                <a href="#inicio" class="nav-link active">Início</a>
                <a href="#problema" class="nav-link">Problema</a>
                <a href="#solucao" class="nav-link">Solução</a>
                <a href="#safe-zones" class="nav-link">Safe Zones</a>
                <a href="#modelo-negocio" class="nav-link">Modelo de Negócio</a>
                <a href="#equipe" class="nav-link">Equipe</a>
                <a href="#contato" class="nav-link">Contato</a>
            </nav>

            <div class="header-actions">
                <a href="#contato" class="btn btn-primary btn-sm">Conheça o Projeto</a>
                <button class="menu-toggle" id="menuToggle" aria-label="Abrir Menu">
                    <span class="bar"></span>
                    <span class="bar"></span>
                    <span class="bar"></span>
                </button>
            </div>
        </div>
    </header>

    <main>
        <section id="inicio" class="hero-section">
            <div class="hero-container">
                <div class="hero-content">
                    <span class="badge">5° SENAC INNOVADAY — 2026</span> [cite: 31]
                    <h1 class="hero-title">Aura: Segurança Inteligente e Integração no Varejo</h1> [cite: 32, 33]
                    <p class="hero-subtitle">Uma plataforma preditiva que conecta mulheres, rotas seguras e estabelecimentos certificados para transformar o comércio em redes ativas de proteção.</p> [cite: 46, 47, 48]
                    <blockquote class="hero-quote">“Transformando o comércio em redes ativas de proteção.”</blockquote> [cite: 49]
                    <div class="hero-buttons">
                        <a href="#solucao" class="btn btn-primary">Ver Solução</a>
                        <a href="#safe-zones" class="btn btn-secondary">Conhecer Safe Zones</a>
                    </div>
                </div>
                
                <div class="hero-visual">
                    <div class="map-mockup">
                        <div class="map-header">
                            <div class="search-bar-mock">🔍 Rota Segura para: Trabalho</div>
                        </div>
                        <div class="map-body">
                            <div class="map-route-line"></div>
                            <div class="map-user-dot"></div>
                            <div class="safe-zone-marker marker-1">
                                <span class="marker-pulse"></span>
                                🛡️ Safe Zone (Farmácia)
                            </div>
                            <div class="safe-zone-marker marker-2">
                                <span class="marker-pulse"></span>
                                🛡️ Safe Zone (Restaurante)
                            </div>
                            <div class="risk-area-indicator">Área de Risco Mapeada por IA</div>
                        </div>
                        <div class="map-card-info">
                            <div class="info-status">🟢 Rota Otimizada Ativa</div>
                            <div class="info-details">Rede de apoio a menos de 2 min de distância.</div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="problema" class="section-padding bg-light">
            <div class="container">
                <div class="section-header">
                    <span class="section-tag">Desafio Identificado</span> [cite: 38]
                    <h2>A Dor do Mercado e a Lacuna Tecnológica</h2> [cite: 39, 42]
                    <p>A insegurança urbana gera impactos sociais graves e retrai o desenvolvimento econômico do comércio de rua.</p>
                </div>
                
                <div class="grid grid-4">
                    <div class="card card-danger">
                        <div class="card-icon">🌙</div>
                        <h3>Afastamento Noturno</h3>
                        <p>A insegurança urbana afasta as mulheres do comércio local, especialmente no período noturno.[cite: 40]</p>
                    </div>
                    <div class="card card-danger">
                        <div class="card-icon">📉</div>
                        <h3>Esvaziamento Comercial</h3>
                        <p>Ruas vazias reduzem drasticamente o fluxo de clientes em bares, restaurantes e farmácias, gerando queda no faturamento.[cite: 41]</p>
                    </div>
                    <div class="card card-danger">
                        <div class="card-icon">⚠️</div>
                        <h3>Soluções Reativas</h3>
                        <p>As ferramentas atuais do mercado atuam apenas após o crime consumado. Falta prevenção ativa.[cite: 43]</p>
                    </div>
                    <div class="card card-danger">
                        <div class="card-icon">🔌</div>
                        <h3>Desconexão Física</h3>
                        <p>Falta total de integração sistêmica entre a tecnologia móvel e os pontos físicos de apoio imediato no comércio.[cite: 43]</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="solucao" class="section-padding">
            <div class="container">
                <div class="section-header">
                    <span class="section-tag">Resultado Pretendido</span> [cite: 44]
                    <h2>A Solução: Produto Inteligente & Serviço Coeso</h2>
                    <p>O Aura redefine a proteção integrando um <strong>Software Baseado em IA</strong> com um modelo de <strong>Serviço de Certificação</strong> para lojistas.[cite: 45]</p>
                </div>

                <div class="grid grid-3">
                    <div class="card card-feature">
                        <div class="card-icon-tech">🤖</div>
                        <h3>IA Preditiva</h3>
                        <p>Plataforma inteligente para o mapeamento e modelagem preditiva de riscos urbanos na malha comercial.[cite: 46]</p>
                    </div>
                    <div class="card card-feature">
                        <div class="card-icon-tech">🗺️</div>
                        <h3>Rotas Seguras</h3>
                        <p>Sugestão automatizada de trajetos protegidos em tempo real, recalculados conforme novos dados de segurança.[cite: 47]</p>
                    </div>
                    <div class="card card-feature">
                        <div class="card-icon-tech">🛡️</div>
                        <h3>Rede de Safe Zones</h3>
                        <p>Pontos de comércio físicos convertidos em elos ativos de segurança mútua e acolhimento imediato.[cite: 48]</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="safe-zones" class="section-padding safe-zones-section">
            <div class="container">
                <div class="safe-zones-wrapper">
                    <div class="safe-zones-info">
                        <span class="section-tag tag-light">Iniciativa de Impacto</span>
                        <h2>O Conceito Safe Zone</h2>
                        <p>As <strong>Safe Zones</strong> são estabelecimentos parceiros (como bares, restaurantes e farmácias) [cite: 41] certificados para oferecer amparo imediato sob risco.[cite: 48]</p>
                        
                        <div class="benefits-split">
                            <div class="benefit-block">
                                <h4>Para Mulheres</h4>
                                <ul>
                                    <li>Mais segurança no deslocamento diário e noturno.</li>
                                    <li>Pontos confiáveis de suporte físico emergencial.</li>
                                    <li>Rotas com previsibilidade baseada em inteligência.</li>
                                    <li>Forte senso de acolhimento social.</li>
                                </ul>
                            </div>
                            <div class="benefit-block">
                                <h4>Para Lojistas</h4>
                                <ul>
                                    <li>Aumento orgânico do fluxo de pessoas em horários críticos.</li>
                                    <li>Diferenciação competitiva e atração de novos públicos.</li>
                                    <li>Fortalecimento contínuo da reputação de marca.</li>
                                    <li>Adesão prática e mensurável à agenda ESG.[cite: 51]</li>
                                </ul>
                            </div>
                        </div>
                    </div>

                    <div class="safe-zones-badge-display">
                        <div class="seal-container">
                            <div class="seal-glow"></div>
                            <div class="seal-badge">
                                <div class="seal-icon">🛡️</div>
                                <h3>ESTABELECIMENTO CERTIFICADO</h3>
                                <h2>AURA SAFE ZONE</h2>
                                <p>Ambiente Conectado à Rede Ativa de Proteção</p>
                                <span class="seal-year">2026</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="modelo-negocio" class="section-padding bg-light">
            <div class="container">
                <div class="section-header">
                    <span class="section-tag">Business Model Canvas</span> [cite: 50]
                    <h2>Viabilidade Comercial e Sustentabilidade</h2>
                    <p>Modelo estruturado para alinhar geração de valor de mercado com transformações sociais reais.</p>
                </div>

                <div class="canvas-grid">
                    <div class="canvas-cell">
                        <h4>🤝 Parceiros-Chave</h4>
                        <p>Senac-DF, Lojistas locais, Órgãos de Segurança.[cite: 51]</p>
                    </div>
                    <div class="canvas-cell">
                        <h4>⚡ Atividades-Chave</h4>
                        <p>Desenvolvimento de IA, Certificação de lojas.[cite: 51]</p>
                    </div>
                    <div class="canvas-cell">
                        <h4>💎 Proposta de Valor</h4>
                        <p>Segurança para mulheres + Fluxo e ESG para o Varejo.[cite: 51]</p>
                    </div>
                    <div class="canvas-cell">
                        <h4>❤️ Relacionamento</h4>
                        <p>Comunidade ativa, Suporte B2B.[cite: 51]</p>
                    </div>
                    <div class="canvas-cell">
                        <h4>🎯 Segmentos de Mercado</h4>
                        <p><strong>B2B:</strong> Comércio noturno.<br><strong>B2C:</strong> Mulheres.[cite: 51]</p>
                    </div>
                    <div class="canvas-cell">
                        <h4>🛠️ Recursos-Chave</h4>
                        <p>Algoritmo preditivo, Base de dados Senac.[cite: 51]</p>
                    </div>
                    <div class="canvas-cell">
                        <h4>📣 Canais</h4>
                        <p>App Mobile, Selo Físico nas lojas.[cite: 51]</p>
                    </div>
                    <div class="canvas-cell canvas-wide">
                        <h4>💰 Estrutura de Custos</h4>
                        <p>Manutenção de servidor, Marketing B2B.[cite: 51]</p>
                    </div>
                    <div class="canvas-cell canvas-wide">
                        <h4>💳 Fontes de Receita</h4>
                        <p>Assinatura Premium de lojistas (Mapa), Parcerias Institucionais.[cite: 51]</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="section-padding impact-section">
            <div class="container">
                <div class="section-header text-center">
                    <span class="section-tag tag-light">Métricas Conceituais de Valor</span>
                    <h2 style="color: var(--white)">Projeção de Impacto Urbano</h2>
                </div>
                <div class="grid grid-5">
                    <div class="impact-card">
                        <div class="impact-num">+🧭</div>
                        <p>Sensação Real de Segurança Percebida</p>
                    </div>
                    <div class="impact-card">
                        <div class="impact-num">+📈</div>
                        <p>Aumento de Fluxo Noturno no Varejo</p>
                    </div>
                    <div class="impact-card">
                        <div class="impact-num">🚀</div>
                        <p>Rotas Otimizadas Dinamicamente por IA</p>
                    </div>
                    <div class="impact-card">
                        <div class="impact-num">🤝</div>
                        <p>Rede Social Colaborativa Consolidada</p>
                    </div>
                    <div class="impact-card">
                        <div class="impact-num">🌱</div>
                        <p>Valorização da Agenda ESG Prática</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="equipe" class="section-padding">
            <div class="container">
                <div class="section-header">
                    <span class="section-tag">Capital Humano</span> [cite: 52]
                    <h2>Equipe e Corpo Científico</h2>
                    <p>Desenvolvido no escopo da disciplina Laboratório de Inovação III na Faculdade Senac-DF.[cite: 35, 37]</p>
                </div>

                <div class="grid grid-4">
                    <div class="card card-team">
                        <div class="avatar-placeholder">AB</div>
                        <h3>Anna Beatriz Pereira da Silva</h3> [cite: 36]
                        <p class="role">UX/UI e Jornada do Lojista[cite: 56]</p>
                    </div>
                    <div class="card card-team">
                        <div class="avatar-placeholder">ES</div>
                        <h3>Elaine Silva</h3> [cite: 36]
                        <p class="role">Pesquisa de Mercado e B2B[cite: 57]</p>
                    </div>
                    <div class="card card-team">
                        <div class="avatar-placeholder">RP</div>
                        <h3>Raphaela</h3> [cite: 36]
                        <p class="role">Desenvolvimento de IA[cite: 58]</p>
                    </div>
                    <div class="card card-team">
                        <div class="avatar-placeholder">VS</div>
                        <h3>Vitória de Souza</h3> [cite: 36]
                        <p class="role">Estratégia de Negócios e ESG[cite: 59]</p>
                    </div>
                </div>

                <div class="academic-footer-box">
                    <p><strong>Professor Orientador:</strong> Prof. Márcio Araya[cite: 34]</p>
                    <p><strong>Instituição:</strong> Faculdade Senac-DF (Campus 913 Sul)[cite: 37, 53]</p>
                    <p><strong>Ambiente:</strong> Laboratório de Inovação III / Prototipagem e Mentoria[cite: 35, 54, 55]</p>
                </div>
            </div>
        </section>

        <section id="contato" class="section-padding bg-dark text-white">
            <div class="container container-narrow">
                <div class="section-header text-center">
                    <span class="section-tag"> Cadastro </span>
                    <h2 style="color: var(--white)">Junte-se ao Aura</h2>
                    <p style="color: var(--gray-400)">Preencha o formulario e esteja a um passo de embarcar nessa jornada segura e acolhedora.</p>
                </div>

                <form id="formContato" class="form-lead" novalidate>
                    <div class="form-group">
                        <label for="nome">Nome Completo</label>
                        <input type="text" id="nome" name="nome" placeholder="Seu nome" required>
                        <span class="error-msg" id="erroNome">Por favor, insira o seu nome.</span>
                    </div>

                    <div class="form-group">
                        <label for="email">E-mail</label>
                        <input type="email" id="email" name="email" placeholder="seuemail@gmail.com" required>
                        <span class="error-msg" id="erroEmail">Insira um endereço de e-mail válido.</span>
                    </div>

                    <div class="form-group">
                        <label for="interesse">Informe o seu sexo</label>
                        <select id="interesse" name="interesse" required>
                            <option value="" disabled selected>Selecione uma opção</option>
                            <option value="lojista">Sou mulher</option>
                            <option value="parceiro">Sou Homem</option>
                            <option value="saber-mais">Prefiro não informar</option>
                        </select>
                        <span class="error-msg" id="erroInteresse">Selecione o seu perfil de interesse.</span>
                    </div>

                    <button type="submit" class="btn btn-cyan btn-block">CADASTRAR</button>
                </form>

                <div id="msgSucesso" class="success-box-toast" role="alert">
                    <span class="success-icon">✓</span>
                    <div>
                        <h4>Cadastro Realizado!</h4>
                        <p>Aproveite, nos indique e avalie nosso site.</p>
                    </div>
                </div>
            </div>
        </section>
    </main>

 <section id="contato" class="section-padding">
            <div class="container container-narrow">
                <div class="section-header text-center">
                    <span class="section-tag">Networking e Parcerias</span>
                    <h2 style="color: var(--dark)">Faça parte da rede Aura</h2>
                    <p style="color: var(--gray-400)">Se você é lojista, parceiro institucional ou deseja conhecer melhor a nossa tecnologia, preencha o formulário e mude o rumo da segurança no varejo.</p>
                </div>

                <form id="formContato" class="form-lead" novalidate>
                    <div class="form-group">
                        <label for="nome">Nome Completo</label>
                        <input type="text" id="nome" name="nome" placeholder="Seu nome ou nome da empresa" required>
                        <span class="error-msg" id="erroNome">Por favor, insira o seu nome.</span>
                    </div>

                    <div class="form-group">
                        <label for="email">E-mail Profissional</label>
                        <input type="email" id="email" name="email" placeholder="seuemail@empresa.com" required>
                        <span class="error-msg" id="erroEmail">Insira um endereço de e-mail corporativo válido.</span>
                    </div>

                    <div class="form-group">
                        <label for="interesse">Tipo de Interesse</label>
                        <select id="interesse" name="interesse" required>
                            <option value="" disabled selected>Selecione uma opção</option>
                            <option value="lojista">Sou Lojista / Quero ser Safe Zone</option>
                            <option value="parceiro">Sou Parceiro Institucional / Governamental</option>
                            <option value="saber-mais">Quero saber mais detalhes da tecnologia</option>
                        </select>
                        <span class="error-msg" id="erroInteresse">Selecione o seu perfil de interesse.</span>
                    </div>

                    <div class="form-group">
                        <label for="mensagem">Mensagem / Observação</label>
                        <textarea id="mensagem" name="mensagem" rows="4" placeholder="Conte-nos brevemente o seu objetivo..."></textarea>
                    </div>

                    <button type="submit" class="btn btn-cyan btn-block">Enviar Interesse</button>
                </form>

                <div id="msgSucesso" class="success-box-toast" role="alert">
                    <span class="success-icon">✓</span>
                    <div>
                        <h4>Interesse Registrado!</h4>
                        <p>Nossa equipe entrará em contato em até 24 horas úteis.</p>
                    </div>
                </div>
            </div>
        </section>
    </main>



    <footer class="main-footer">
        <div class="container footer-grid">
            <div>
                <span class="logo-text">Aura</span>
                <p class="footer-tagline">Segurança inteligente para cidades mais conectadas.</p>
            </div>
            <div>
                <h4>Navegação</h4>
                <ul class="footer-links">
                    <li><a href="#inicio">Início</a></li>
                    <li><a href="#problema">O Problema</a></li>
                    <li><a href="#solucao">A Solução</a></li>
                    <li><a href="#safe-zones">Safe Zones</a></li>
                </ul>
            </div>
            <div>
                <h4>Acadêmico</h4>
                <ul class="footer-links">
                    <li><a href="#equipe">A Equipe</a></li>
                    <li><a href="#modelo-negocio">Canvas do Projeto</a></li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <p>Projeto acadêmico desenvolvido para o <strong>5° SENAC INNOVADAY - 2026</strong> | Faculdade Senac-DF</p> 
            <p>&copy; 2026 Projeto Aura. Todos os direitos reservados de prototipagem conceitual.</p>
        </div>
    </footer>

    <script>
        document.addEventListener("DOMContentLoaded", () => {
            // Controle do Menu Mobile (Hambúrguer)
            const menuToggle = document.getElementById("menuToggle");
            const navMenu = document.getElementById("navMenu");
            const navLinks = document.querySelectorAll(".nav-link");

            if (menuToggle && navMenu) {
                menuToggle.addEventListener("click", () => {
                    navMenu.classList.toggle("active");
                    menuToggle.classList.toggle("open");
                    
                    const bars = menuToggle.querySelectorAll(".bar");
                    if (menuToggle.classList.contains("open")) {
                        bars[0].style.transform = "rotate(45deg) translate(5px, 5px)";
                        bars[1].style.opacity = "0";
                        bars[2].style.transform = "rotate(-45deg) translate(5px, -5px)";
                    } else {
                        bars[0].style.transform = "none";
                        bars[1].style.opacity = "1";
                        bars[2].style.transform = "none";
                    }
                });
            }

            // Fecha o menu ao clicar em um link
            navLinks.forEach(link => {
                link.addEventListener("click", () => {
                    if (navMenu.classList.contains("active")) {
                        navMenu.classList.remove("active");
                        menuToggle.classList.remove("open");
                        const bars = menuToggle.querySelectorAll(".bar");
                        bars[0].style.transform = "none";
                        bars[1].style.opacity = "1";
                        bars[2].style.transform = "none";
                    }
                });
            });

            // Validação de Formulário de Interesse
            const formContato = document.getElementById("formContato");
            const msgSucesso = document.getElementById("msgSucesso");

            if (formContato) {
                formContato.addEventListener("submit", (e) => {
                    e.preventDefault();
                    
                    const nomeInput = document.getElementById("nome");
                    const emailInput = document.getElementById("email");
                    const interesseSelect = document.getElementById("interesse");
                    let isFormValid = true;

                    if (nomeInput.value.trim() === "") {
                        nomeInput.parentElement.classList.add("invalid");
                        isFormValid = false;
                    } else {
                        nomeInput.parentElement.classList.remove("invalid");
                    }

                    const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
                    if (!emailRegex.test(emailInput.value.trim())) {
                        emailInput.parentElement.classList.add("invalid");
                        isFormValid = false;
                    } else {
                        emailInput.parentElement.classList.remove("invalid");
                    }

                    if (interesseSelect.value === "") {
                        interesseSelect.parentElement.classList.add("invalid");
                        isFormValid = false;
                    } else {
                        interesseSelect.parentElement.classList.remove("invalid");
                    }

                    if (isFormValid) {
                        formContato.style.display = "none";
                        msgSucesso.style.display = "flex";
                        
                        console.log("=== Aura Lead Capturado ===");
                        console.log("Nome:", nomeInput.value);
                        console.log("E-mail:", emailInput.value);
                    }
                });
                
                const inputs = formContato.querySelectorAll("input, select");
                inputs.forEach(input => {
                    input.addEventListener("input", () => {
                        if (input.parentElement.classList.contains("invalid")) {
                            input.parentElement.classList.remove("invalid");
                        }
                    });
                });
            }
        });
    </script>
</body>
</html>
