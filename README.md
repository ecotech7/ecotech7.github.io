
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Энергетика и экологические технологии — Ветряная энергия</title>
  <!-- Подключение шрифтов Google Fonts с поддержкой кириллицы -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Space+Grotesk:wght@600;700&display=swap" rel="stylesheet">
  <style>
    /* ==========================================================================
       БАЗОВЫЕ ПЕРЕМЕННЫЕ И СБРОС СТИЛЕЙ
       ========================================================================== */
    :root {
      --bg-main: #FFFFFF;
      --bg-subtle: #F8FAFC;
      --bg-mint: #F0FDF4;
      --bg-teal-light: #CCFBF1;
      --text-primary: #0F172A;
      --text-secondary: #475569;
      --text-muted: #64748B;
      --accent-teal: #0D9488;
      --accent-teal-dark: #0F766E;
      --accent-emerald: #10B981;
      --accent-dark: #0F172A;
      --danger: #DC2626;
      --danger-light: #FEF2F2;
      --warning: #D97706;
      --warning-light: #FFFBEB;
      --border-color: #E2E8F0;
      --shadow-sm: 0 1px 3px rgba(15, 23, 42, 0.05);
      --shadow-md: 0 10px 25px -5px rgba(15, 23, 42, 0.06), 0 4px 10px -2px rgba(15, 23, 42, 0.03);
      --shadow-lg: 0 20px 35px -10px rgba(13, 148, 136, 0.12);
      --radius-sm: 8px;
      --radius-md: 14px;
      --radius-lg: 20px;
      --transition: all 0.25s cubic-bezier(0.4, 0, 0.2, 1);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
      font-size: 16px;
    }

    body {
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
      background-color: var(--bg-main);
      color: var(--text-primary);
      line-height: 1.6;
      overflow-x: hidden;
    }

    h1, h2, h3, h4, .font-display {
      font-family: 'Space Grotesk', 'Inter', sans-serif;
      letter-spacing: -0.02em;
      line-height: 1.2;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    ul {
      list-style: none;
    }

    .container {
      width: 100%;
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 24px;
    }

    /* ==========================================================================
       НАВИГАЦИЯ (ШАПКА САЙТА)
       ========================================================================== */
    .navbar {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      z-index: 1000;
      background: rgba(255, 255, 255, 0.9);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      border-bottom: 1px solid var(--border-color);
      transition: var(--transition);
    }

    .navbar-inner {
      display: flex;
      align-items: center;
      justify-content: space-between;
      height: 72px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 10px;
      font-weight: 700;
      font-size: 1.05rem;
      color: var(--text-primary);
    }

    .brand-icon {
      width: 34px;
      height: 34px;
      border-radius: 10px;
      background: linear-gradient(135deg, var(--accent-teal), var(--accent-emerald));
      display: flex;
      align-items: center;
      justify-content: center;
      color: #FFFFFF;
      flex-shrink: 0;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 28px;
    }

    .nav-links a {
      font-size: 0.92rem;
      font-weight: 500;
      color: var(--text-secondary);
      transition: var(--transition);
      position: relative;
    }

    .nav-links a:hover {
      color: var(--accent-teal);
    }

    .nav-links a::after {
      content: '';
      position: absolute;
      bottom: -6px;
      left: 0;
      width: 0;
      height: 2px;
      background: var(--accent-teal);
      transition: width 0.25s ease;
    }

    .nav-links a:hover::after {
      width: 100%;
    }

    .nav-badge {
      background: var(--accent-dark);
      color: #FFFFFF;
      font-size: 0.78rem;
      font-weight: 600;
      padding: 6px 12px;
      border-radius: 999px;
      letter-spacing: 0.03em;
    }

    /* Кнопка бургер-меню для мобильных */
    .burger-btn {
      display: none;
      background: none;
      border: 1px solid var(--border-color);
      border-radius: var(--radius-sm);
      padding: 8px;
      cursor: pointer;
      color: var(--text-primary);
    }

    /* ==========================================================================
       ГЛАВНЫЙ ЭКРАН (HERO)
       ========================================================================== */
    .hero {
      padding: 132px 0 84px;
      background: radial-gradient(circle at 85% 20%, rgba(16, 185, 129, 0.08) 0%, rgba(255, 255, 255, 0) 55%),
                  radial-gradient(circle at 10% 80%, rgba(13, 148, 136, 0.06) 0%, rgba(255, 255, 255, 0) 50%);
      border-bottom: 1px solid var(--border-color);
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.25fr 0.85fr;
      gap: 48px;
      align-items: center;
    }

    .pill-tag {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: var(--bg-mint);
      border: 1px solid rgba(16, 185, 129, 0.3);
      color: var(--accent-teal-dark);
      font-size: 0.82rem;
      font-weight: 600;
      padding: 6px 14px;
      border-radius: 999px;
      margin-bottom: 20px;
      text-transform: uppercase;
      letter-spacing: 0.05em;
    }

    .pill-dot {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: var(--accent-emerald);
    }

    .hero-title {
      font-size: clamp(2.1rem, 4vw, 3.35rem);
      font-weight: 700;
      color: var(--text-primary);
      margin-bottom: 20px;
    }

    .hero-title span {
      color: var(--accent-teal);
    }

    .hero-desc {
      font-size: 1.08rem;
      color: var(--text-secondary);
      margin-bottom: 32px;
      max-width: 620px;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      padding: 14px 24px;
      border-radius: var(--radius-md);
      font-weight: 600;
      font-size: 0.96rem;
      cursor: pointer;
      transition: var(--transition);
      border: none;
    }

    .btn-primary {
      background: var(--accent-teal);
      color: #FFFFFF;
      box-shadow: 0 8px 20px -4px rgba(13, 148, 136, 0.35);
    }

    .btn-primary:hover {
      background: var(--accent-teal-dark);
      transform: translateY(-2px);
    }

    .btn-outline {
      background: #FFFFFF;
      color: var(--text-primary);
      border: 1px solid var(--border-color);
    }

    .btn-outline:hover {
      border-color: var(--accent-teal);
      background: var(--bg-subtle);
    }

    /* Паспорт проекта (карточка справа в Hero) */
    .passport-card {
      background: var(--bg-subtle);
      border: 1px solid var(--border-color);
      border-radius: var(--radius-lg);
      padding: 28px;
      box-shadow: var(--shadow-md);
      position: relative;
      overflow: hidden;
    }

    .passport-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 5px;
      background: linear-gradient(90deg, var(--accent-teal), var(--accent-emerald));
    }

    .passport-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 20px;
      padding-bottom: 14px;
      border-bottom: 1px solid var(--border-color);
    }

    .passport-label {
      font-size: 0.78rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      color: var(--accent-teal-dark);
    }

    .passport-year {
      background: var(--accent-dark);
      color: #FFFFFF;
      font-size: 0.8rem;
      font-weight: 700;
      padding: 4px 10px;
      border-radius: 6px;
    }

    .passport-list {
      display: flex;
      flex-direction: column;
      gap: 14px;
    }

    .passport-item {
      display: flex;
      flex-direction: column;
      gap: 2px;
    }

    .passport-key {
      font-size: 0.78rem;
      color: var(--text-muted);
      font-weight: 500;
    }

    .passport-val {
      font-size: 0.96rem;
      font-weight: 600;
      color: var(--text-primary);
    }

    .passport-tags {
      margin-top: 18px;
      padding-top: 14px;
      border-top: 1px solid var(--border-color);
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 10px;
    }

    .mini-box {
      background: #FFFFFF;
      border: 1px solid var(--border-color);
      border-radius: var(--radius-sm);
      padding: 10px 12px;
    }

    .mini-box span {
      display: block;
      font-size: 0.72rem;
      color: var(--text-muted);
      text-transform: uppercase;
    }

    .mini-box strong {
      font-size: 0.86rem;
      color: var(--accent-teal-dark);
    }

    /* ==========================================================================
       ОБЩИЕ СТИЛИ СЕКЦИЙ
       ========================================================================== */
    section {
      padding: 84px 0;
    }

    .section-alt {
      background-color: var(--bg-subtle);
      border-top: 1px solid var(--border-color);
      border-bottom: 1px solid var(--border-color);
    }

    .section-header {
      max-width: 720px;
      margin-bottom: 48px;
    }

    .section-kicker {
      display: inline-block;
      font-size: 0.8rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      color: var(--accent-teal);
      margin-bottom: 10px;
    }

    .section-title {
      font-size: clamp(1.75rem, 3vw, 2.4rem);
      font-weight: 700;
      color: var(--text-primary);
      margin-bottom: 14px;
    }

    .section-subtitle {
      font-size: 1.02rem;
      color: var(--text-secondary);
    }

    /* ==========================================================================
       СЕКЦИЯ 2: ПРОБЛЕМА, ЦЕЛЬ И ГИПОТЕЗА
       ========================================================================== */
    .triad-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 24px;
    }

    .card {
      background: #FFFFFF;
      border: 1px solid var(--border-color);
      border-radius: var(--radius-lg);
      padding: 28px;
      box-shadow: var(--shadow-sm);
      transition: var(--transition);
    }

    .card:hover {
      transform: translateY(-4px);
      box-shadow: var(--shadow-md);
      border-color: rgba(13, 148, 136, 0.35);
    }

    .card-mint {
      background: var(--bg-mint);
      border-color: rgba(16, 185, 129, 0.25);
    }

    .card-icon {
      width: 44px;
      height: 44px;
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 18px;
      font-weight: 700;
    }

    .icon-danger {
      background: var(--danger-light);
      color: var(--danger);
    }

    .icon-teal {
      background: var(--bg-teal-light);
      color: var(--accent-teal-dark);
    }

    .icon-emerald {
      background: #D1FAE5;
      color: #047857;
    }

    .card h3 {
      font-size: 1.25rem;
      margin-bottom: 12px;
      color: var(--text-primary);
    }

    .card p {
      font-size: 0.95rem;
      color: var(--text-secondary);
    }

    /* ==========================================================================
       СЕКЦИЯ 3: ТРАДИЦИОННАЯ VS ВЕТРЯНАЯ ЭНЕРГЕТИКА
       ========================================================================== */
    .compare-layout {
      display: grid;
      grid-template-columns: 1fr 1.15fr;
      gap: 32px;
      align-items: start;
    }

    .trad-box {
      background: #FFFFFF;
      border: 1px solid var(--border-color);
      border-radius: var(--radius-lg);
      padding: 32px;
    }

    .trad-header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 20px;
    }

    .badge-gray {
      background: #F1F5F9;
      color: #334155;
      font-size: 0.78rem;
      font-weight: 700;
      padding: 5px 12px;
      border-radius: 999px;
      text-transform: uppercase;
    }

    .station-types {
      display: flex;
      flex-direction: column;
      gap: 14px;
      margin-bottom: 24px;
    }

    .station-item {
      padding: 14px 16px;
      background: var(--bg-subtle);
      border-radius: var(--radius-md);
      border-left: 3px solid #64748B;
    }

    .station-item strong {
      display: block;
      font-size: 0.96rem;
      color: var(--text-primary);
      margin-bottom: 4px;
    }

    .station-item span {
      font-size: 0.88rem;
      color: var(--text-secondary);
    }

    .metrics-row {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 12px;
      padding-top: 18px;
      border-top: 1px solid var(--border-color);
    }

    .metric-pill {
      background: var(--danger-light);
      padding: 12px 14px;
      border-radius: var(--radius-sm);
    }

    .metric-pill strong {
      display: block;
      font-family: 'Space Grotesk', sans-serif;
      font-size: 1.15rem;
      color: var(--danger);
    }

    .metric-pill span {
      font-size: 0.8rem;
      color: #7F1D1D;
    }

    /* 5 этапов работы ветрогенератора */
    .wind-steps-box {
      background: #FFFFFF;
      border: 1px solid var(--border-color);
      border-radius: var(--radius-lg);
      padding: 32px;
    }

    .steps-list {
      display: flex;
      flex-direction: column;
      gap: 16px;
      margin-top: 20px;
    }

    .step-row {
      display: flex;
      gap: 16px;
      align-items: flex-start;
    }

    .step-num {
      width: 30px;
      height: 30px;
      border-radius: 8px;
      background: var(--accent-teal);
      color: #FFFFFF;
      font-family: 'Space Grotesk', sans-serif;
      font-weight: 700;
      font-size: 0.9rem;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
      margin-top: 2px;
    }

    .step-content h4 {
      font-size: 1rem;
      color: var(--text-primary);
      margin-bottom: 3px;
    }

    .step-content p {
      font-size: 0.9rem;
      color: var(--text-secondary);
    }

    .betz-banner {
      margin-top: 24px;
      background: var(--bg-mint);
      border: 1px solid rgba(16, 185, 129, 0.35);
      border-radius: var(--radius-md);
      padding: 18px 20px;
      display: flex;
      align-items: center;
      gap: 18px;
    }

    .betz-value {
      font-family: 'Space Grotesk', sans-serif;
      font-size: 2rem;
      font-weight: 700;
      color: var(--accent-teal-dark);
      line-height: 1;
      flex-shrink: 0;
    }

    .betz-text strong {
      display: block;
      font-size: 0.95rem;
      color: var(--text-primary);
    }

    .betz-text span {
      font-size: 0.86rem;
      color: var(--text-secondary);
    }

    /* ==========================================================================
       СЕКЦИЯ 4: ИНТЕРАКТИВНЫЙ СИМУЛЯТОР И ПРАКТИЧЕСКАЯ МОДЕЛЬ
       ========================================================================== */
    .simulator-grid {
      display: grid;
      grid-template-columns: 1.15fr 0.85fr;
      gap: 32px;
      align-items: stretch;
    }

    .sim-card {
      background: #FFFFFF;
      border: 1px solid var(--border-color);
      border-radius: var(--radius-lg);
      padding: 32px;
      box-shadow: var(--shadow-md);
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    .sim-stage {
      background: linear-gradient(180deg, #F0FDF4 0%, #F8FAFC 100%);
      border: 1px solid var(--border-color);
      border-radius: var(--radius-md);
      height: 290px;
      position: relative;
      overflow: hidden;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 24px;
    }

    /* Анимированные линии воздушного потока */
    .wind-lines {
      position: absolute;
      inset: 0;
      pointer-events: none;
    }

    .wind-streak {
      position: absolute;
      height: 2px;
      background: linear-gradient(90deg, transparent, rgba(13, 148, 136, 0.45), transparent);
      border-radius: 2px;
      left: -120px;
      animation: blowWind linear infinite;
    }

    @keyframes blowWind {
      0% { transform: translateX(0); opacity: 0; }
      20% { opacity: 1; }
      80% { opacity: 1; }
      100% { transform: translateX(760px); opacity: 0; }
    }

    /* Ползунок и пресеты */
    .controls-header {
      display: flex;
      justify-content: space-between;
      align-items: baseline;
      margin-bottom: 12px;
    }

    .speed-display {
      font-family: 'Space Grotesk', sans-serif;
      font-size: 1.75rem;
      font-weight: 700;
      color: var(--accent-teal);
    }

    input[type="range"] {
      -webkit-appearance: none;
      width: 100%;
      height: 8px;
      background: #E2E8F0;
      border-radius: 999px;
      outline: none;
      margin-bottom: 16px;
      cursor: pointer;
    }

    input[type="range"]::-webkit-slider-thumb {
      -webkit-appearance: none;
      width: 22px;
      height: 22px;
      border-radius: 50%;
      background: var(--accent-teal);
      border: 3px solid #FFFFFF;
      box-shadow: 0 2px 6px rgba(15, 23, 42, 0.25);
      cursor: pointer;
      transition: transform 0.15s ease;
    }

    input[type="range"]::-webkit-slider-thumb:hover {
      transform: scale(1.12);
    }

    .presets-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 24px;
    }

    .preset-btn {
      background: var(--bg-subtle);
      border: 1px solid var(--border-color);
      color: var(--text-secondary);
      font-size: 0.8rem;
      font-weight: 600;
      padding: 6px 12px;
      border-radius: 8px;
      cursor: pointer;
      transition: var(--transition);
    }

    .preset-btn:hover, .preset-btn.active {
      background: var(--accent-dark);
      color: #FFFFFF;
      border-color: var(--accent-dark);
    }

    .telemetry-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 12px;
    }

    .tele-box {
      background: var(--bg-subtle);
      border: 1px solid var(--border-color);
      border-radius: var(--radius-md);
      padding: 14px;
    }

    .tele-label {
      font-size: 0.75rem;
      color: var(--text-muted);
      margin-bottom: 4px;
    }

    .tele-val {
      font-family: 'Space Grotesk', sans-serif;
      font-size: 1.25rem;
      font-weight: 700;
      color: var(--text-primary);
    }

    .tele-sub {
      font-size: 0.76rem;
      color: var(--accent-teal-dark);
      font-weight: 500;
      margin-top: 2px;
    }

    /* Карточка реального макета из Главы 2 */
    .prototype-card {
      background: var(--bg-dark, #0F172A);
      color: #FFFFFF;
      border-radius: var(--radius-lg);
      padding: 32px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    .prototype-card .section-kicker {
      color: var(--accent-emerald);
    }

    .prototype-card h3 {
      font-size: 1.45rem;
      margin-bottom: 14px;
      color: #FFFFFF;
    }

    .prototype-card p {
      font-size: 0.93rem;
      color: #CBD5E1;
      margin-bottom: 20px;
    }

    .comp-list {
      display: flex;
      flex-direction: column;
      gap: 12px;
      margin-bottom: 24px;
    }

    .comp-item {
      background: rgba(255, 255, 255, 0.06);
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: var(--radius-md);
      padding: 12px 16px;
    }

    .comp-item strong {
      display: block;
      font-size: 0.9rem;
      color: #6EE7B7;
