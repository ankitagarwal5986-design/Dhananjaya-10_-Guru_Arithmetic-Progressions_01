<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Brain & Mind | DHANANJAYA 10 - Arithmetic Progressions (Expanded NCERT Question Bank)</title>
  
  <!-- MathJax Configuration -->
  <script>
    window.MathJax = {
      tex: {
        inlineMath: [['\\(', '\\)'], ['$', '$']],
        displayMath: [['\\[', '\\]'], ['$$', '$$']],
        processEscapes: true
      },
      options: {
        skipHtmlTags: ['script', 'noscript', 'style', 'textarea', 'pre', 'code']
      },
      startup: {
        pageReady: () => MathJax.startup.defaultPageReady()
      }
    };
  </script>
  <script type="text/javascript" id="MathJax-script" async
    src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>

  <style>
    :root {
      --primary-blue: #0284c7;
      --primary-dark: #0c4a6e;
      --accent-blue: #0ea5e9;
      --light-blue-bg: #f0f9ff;
      --light-blue-card: #f8fafc;
      --blue-border: #7dd3fc;
      --blue-border-soft: #bae6fd;
      --card-white: #ffffff;
      --correct-green: #059669;
      --correct-green-light: #d1fae5;
      --incorrect-red: #dc2626;
      --incorrect-red-light: #fee2e2;
      --brand-gold: #f59e0b;
      --brand-gold-dark: #d97706;
      --text-main: #0f172a;
      --text-muted: #475569;
      --radius-sm: 8px;
      --radius-md: 14px;
      --radius-lg: 20px;
      --shadow-sm: 0 1px 3px rgba(2, 132, 199, 0.08);
      --shadow-md: 0 4px 8px -1px rgba(2, 132, 199, 0.12);
      --shadow-lg: 0 12px 24px -4px rgba(12, 74, 110, 0.15);
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      font-family: 'Segoe UI', -apple-system, BlinkMacSystemFont, Roboto, sans-serif;
      background: linear-gradient(180deg, #f0f9ff 0%, #ffffff 320px, #f0f9ff 100%);
      color: var(--text-main);
      line-height: 1.6;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    /* Header */
    header {
      background: linear-gradient(135deg, var(--primary-dark) 0%, #0369a1 60%, var(--primary-blue) 100%);
      color: #ffffff; padding: 0.85rem 1.75rem; box-shadow: var(--shadow-md); position: sticky; top: 0; z-index: 100;
    }
    .header-container {
      max-width: 1440px; margin: 0 auto; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 1rem;
    }
    .brand-group { display: flex; align-items: center; gap: 14px; }
    .brand-logo-wrap {
      background: #ffffff; padding: 6px 12px; border-radius: 12px; display: flex; align-items: center; justify-content: center; box-shadow: 0 2px 8px rgba(0,0,0,0.15);
    }
    .brand-logo-svg { width: 48px; height: 48px; display: block; }
    .brand-title h1 { font-size: 1.25rem; font-weight: 800; letter-spacing: -0.02em; }
    .brand-title p { font-size: 0.8rem; color: #bae6fd; font-weight: 600; }

    /* Live Timer */
    .timer-widget {
      display: none; align-items: center; gap: 8px; background: rgba(255, 255, 255, 0.18);
      border: 1px solid rgba(255, 255, 255, 0.3); padding: 5px 14px; border-radius: 20px;
    }
    .timer-display {
      font-family: 'Segoe UI', monospace; font-size: 1.05rem; font-weight: 800; color: #ffffff; letter-spacing: 1px; min-width: 54px; text-align: center;
    }
    .timer-btn {
      background: #ffffff; border: none; color: var(--primary-dark); font-size: 0.75rem; font-weight: 700;
      padding: 4px 9px; border-radius: 12px; cursor: pointer; transition: all 0.2s;
    }
    .timer-btn:hover { background: #e0f2fe; color: var(--primary-blue); }

    /* Toast Notification */
    .toast-reminder {
      display: none; position: fixed; bottom: 25px; right: 25px; background: #0c4a6e; color: #ffffff;
      padding: 14px 22px; border-radius: 14px; box-shadow: 0 10px 25px rgba(0,0,0,0.25); border: 2px solid var(--blue-border);
      z-index: 1000; font-weight: 700; font-size: 0.95rem; animation: slideUp 0.3s ease-out;
    }
    @keyframes slideUp { from { transform: translateY(20px); opacity: 0; } to { transform: translateY(0); opacity: 1; } }

    .nav-tabs { display: none; align-items: center; gap: 8px; flex-wrap: wrap; }
    .tab-btn {
      background: rgba(255, 255, 255, 0.18); border: 1px solid rgba(255, 255, 255, 0.3);
      color: #ffffff; padding: 7px 15px; border-radius: 20px; cursor: pointer; font-size: 0.86rem; font-weight: 600; transition: all 0.2s;
    }
    .tab-btn:hover, .tab-btn.active {
      background: #ffffff; color: var(--primary-blue); box-shadow: 0 2px 8px rgba(0,0,0,0.12);
    }
    .user-actions { display: flex; align-items: center; gap: 10px; flex-wrap: wrap; }
    .user-badge {
      background: rgba(255, 255, 255, 0.18); border: 1px solid rgba(255, 255, 255, 0.3);
      padding: 6px 14px; border-radius: 20px; font-size: 0.85rem; color: #f1f5f9; display: flex; align-items: center; gap: 6px;
    }
    .btn-icon {
      background: rgba(255, 255, 255, 0.22); border: none; color: #ffffff; padding: 8px 14px; border-radius: var(--radius-sm); cursor: pointer; font-size: 0.85rem; font-weight: 600; transition: all 0.2s;
    }
    .btn-icon:hover { background: rgba(255, 255, 255, 0.35); }

    main { max-width: 1440px; width: 100%; margin: 1.5rem auto; padding: 0 1rem; flex: 1; }
    .view-section { display: none; }
    .view-section.active { display: block; animation: fadeIn 0.25s ease-in-out; }
    @keyframes fadeIn { from { opacity: 0; transform: translateY(6px); } to { opacity: 1; transform: translateY(0); } }

    /* Login Gate */
    .login-gate-card {
      max-width: 500px; margin: 3rem auto; background: var(--card-white); border-radius: var(--radius-lg);
      padding: 2.75rem 2.25rem; border: 2.5px solid var(--blue-border); box-shadow: var(--shadow-lg); text-align: center;
    }
    .login-lock-icon {
      width: 64px; height: 64px; margin: 0 auto 1.25rem auto; background: #e0f2fe; color: var(--primary-blue);
      border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 1.8rem;
    }
    .login-gate-card h2 { color: var(--primary-dark); font-size: 1.5rem; margin-bottom: 0.5rem; font-weight: 800; }
    .login-gate-card p { color: var(--text-muted); font-size: 0.92rem; margin-bottom: 1.75rem; }
    .input-field-group { text-align: left; margin-bottom: 1.25rem; }
    .input-field-group label { display: block; font-size: 0.85rem; font-weight: 700; color: var(--primary-dark); margin-bottom: 6px; }
    .login-input {
      width: 100%; padding: 11px 14px; font-size: 1rem; border: 2px solid var(--blue-border-soft); border-radius: var(--radius-sm);
      outline: none; transition: border-color 0.2s; font-family: inherit;
    }
    .login-input:focus { border-color: var(--primary-blue); box-shadow: 0 0 0 3px rgba(2, 132, 199, 0.15); }
    .login-btn-submit {
      width: 100%; padding: 12px; background: linear-gradient(135deg, var(--primary-blue), var(--accent-blue));
      color: #ffffff; border: none; border-radius: var(--radius-sm); font-size: 1.05rem; font-weight: 700; cursor: pointer; transition: all 0.2s; margin-top: 0.5rem;
    }
    .login-btn-submit:hover { opacity: 0.95; transform: translateY(-1px); }
    .login-error-text {
      color: var(--incorrect-red); background: var(--incorrect-red-light); padding: 10px 14px; border-radius: var(--radius-sm);
      border: 1px solid #fecaca; font-size: 0.88rem; font-weight: 600; margin-top: 14px; display: none; line-height: 1.5; text-align: left;
    }

    /* Theory Notes Layout */
    .notes-card { max-width: 1100px; margin: 1rem auto 2rem auto; background: var(--card-white); border-radius: var(--radius-lg); padding: 2.5rem; border: 2px solid var(--blue-border-soft); box-shadow: var(--shadow-lg); }
    .notes-header { border-bottom: 2px solid var(--blue-border-soft); padding-bottom: 1.25rem; margin-bottom: 1.5rem; }
    .notes-header h2 { color: var(--primary-dark); font-size: 1.7rem; }
    .notes-body h3 { color: var(--primary-blue); margin: 1.8rem 0 0.6rem 0; font-size: 1.22rem; border-bottom: 1.5px solid var(--blue-border-soft); padding-bottom: 5px; display: flex; align-items: center; gap: 8px; }
    .notes-body p, .notes-body ul, .notes-body ol { color: var(--text-main); font-size: 1.02rem; line-height: 1.8; margin-bottom: 1rem; }
    .notes-body ul, .notes-body ol { padding-left: 1.6rem; }
    .formula-callout { background: #f0f9ff; border: 1px solid var(--blue-border-soft); border-left: 4px solid var(--primary-blue); padding: 14px 18px; border-radius: var(--radius-sm); margin: 14px 0; font-size: 1.05rem; }
    .video-callout { background: #eff6ff; border: 1.5px solid #bfdbfe; border-radius: var(--radius-md); padding: 16px; margin: 14px 0; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 12px; }
    .step-badge { display: inline-block; background: #e0f2fe; color: #0369a1; font-weight: 800; font-size: 0.8rem; padding: 2px 10px; border-radius: 12px; margin-right: 6px; }

    /* Learning Grid */
    .learning-grid-layout { display: grid; grid-template-columns: 1fr 390px; gap: 1.5rem; align-items: start; }
    @media (max-width: 1080px) { .learning-grid-layout { grid-template-columns: 1fr; } }
    
    .problem-card { background: var(--card-white); border-radius: var(--radius-lg); padding: 2rem; box-shadow: var(--shadow-md); border: 2px solid var(--blue-border-soft); }
    .problem-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 1.25rem; padding-bottom: 0.75rem; border-bottom: 1.5px solid var(--blue-border-soft); }
    .p-tag { font-size: 1.15rem; font-weight: 800; color: var(--primary-blue); }
    .category-badge { background: #e0f2fe; color: var(--primary-dark); font-weight: 700; font-size: 0.8rem; padding: 3px 10px; border-radius: 6px; border: 1px solid var(--blue-border); margin-left: 8px; }
    .parts-badge { background: #fef3c7; color: #b45309; font-weight: 700; font-size: 0.8rem; padding: 3px 9px; border-radius: 6px; border: 1px solid #fde68a; margin-left: 6px; }
    .status-badge { font-size: 0.8rem; font-weight: 700; padding: 4px 10px; border-radius: 12px; text-transform: uppercase; }
    .badge-unvisited { background: #f8fafc; color: var(--text-muted); border: 1px solid #cbd5e1; }
    .badge-progress { background: #dbeafe; color: #1e40af; }
    .badge-complete { background: var(--correct-green-light); color: var(--correct-green); }
    .badge-skipped { background: #fef3c7; color: #b45309; }

    .problem-context { font-size: 1.15rem; font-weight: 500; margin-bottom: 1.25rem; background: #f0f9ff; border-left: 4px solid var(--accent-blue); padding: 16px 20px; border-radius: var(--radius-sm); line-height: 2.2; border: 1px solid var(--blue-border-soft); border-left-width: 4px; }

    .diagram-container {
      display: flex; flex-direction: column; justify-content: center; align-items: center; background: #ffffff;
      border: 1.5px solid var(--blue-border-soft); border-radius: var(--radius-md); padding: 1.25rem; margin: 1rem 0 1.5rem 0;
      box-shadow: inset 0 0 10px rgba(2, 132, 199, 0.04);
    }
    .diagram-svg { max-width: 460px; width: 100%; height: auto; }
    .diagram-caption { font-size: 0.88rem; color: var(--text-muted); font-weight: 600; margin-top: 8px; }

    .steps-container { display: flex; flex-direction: column; gap: 1.25rem; }
    .step-card { border: 2px solid var(--blue-border-soft); border-radius: var(--radius-md); padding: 1.25rem 1.5rem; background: #ffffff; transition: all 0.25s ease-in-out; }
    .step-card.active { border-color: var(--accent-blue); box-shadow: 0 4px 12px rgba(2, 132, 199, 0.15); }
    .step-card.completed { border-color: var(--correct-green); background: #fcfdfc; }
    
    .step-header-bar { display: flex; justify-content: space-between; align-items: center; margin-bottom: 0.75rem; }
    .step-title-text { font-weight: 700; font-size: 1rem; color: var(--primary-dark); }
    .step-status-indicator { font-size: 0.8rem; font-weight: 700; padding: 2px 8px; border-radius: 6px; }
    .step-card.completed .step-status-indicator { background: var(--correct-green-light); color: var(--correct-green); }
    .step-card.active .step-status-indicator { background: #e0f2fe; color: var(--primary-dark); }

    .step-prompt { font-size: 1.05rem; font-weight: 500; margin-bottom: 1rem; color: var(--text-main); line-height: 2.4; }

    .step-input {
      display: inline-block; width: 220px; padding: 7px 11px; font-size: 1.05rem; font-weight: 700; font-family: 'Segoe UI', monospace;
      text-align: center; color: var(--primary-blue); background: #ffffff; border: 2px solid #7dd3fc; border-radius: var(--radius-sm); outline: none; margin: 0 4px; vertical-align: middle;
    }
    .step-input:focus { border-color: var(--primary-blue); box-shadow: 0 0 0 3px rgba(2, 132, 199, 0.2); }
    .step-input.input-correct { border-color: var(--correct-green) !important; background: var(--correct-green-light) !important; color: #065f46 !important; }
    .step-input.input-incorrect { border-color: var(--incorrect-red) !important; background: var(--incorrect-red-light) !important; color: #991b1b !important; }

    .step-controls { display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px; margin-top: 0.75rem; padding-top: 0.75rem; border-top: 1px dashed var(--blue-border-soft); }
    .step-feedback-msg { font-size: 0.88rem; font-weight: 600; }
    .step-feedback-msg.correct { color: #166534; }
    .step-feedback-msg.incorrect { color: #b91c1c; }

    /* Tools */
    .tools-panel {
      background: #f0f9ff; border: 1.5px solid var(--blue-border); border-radius: var(--radius-md); padding: 1rem; margin-bottom: 1.25rem;
    }
    .tool-tab-header {
      display: flex; gap: 8px; border-bottom: 1.5px solid var(--blue-border-soft); padding-bottom: 8px; margin-bottom: 12px;
    }
    .tool-tab-btn {
      background: none; border: none; font-size: 0.85rem; font-weight: 700; color: var(--text-muted); cursor: pointer; padding: 4px 8px; border-radius: 4px;
    }
    .tool-tab-btn.active { color: var(--primary-blue); background: #e0f2fe; }
    .math-pad-grid { display: grid; grid-template-columns: repeat(7, 1fr); gap: 6px; }
    .math-pad-btn {
      background: #ffffff; border: 1px solid var(--blue-border); padding: 8px 4px; border-radius: var(--radius-sm); font-weight: 700; font-size: 0.95rem; cursor: pointer; text-align: center; color: var(--primary-dark);
    }
    .math-pad-btn:hover { background: var(--primary-blue); color: #ffffff; }

    .calc-box { background: #ffffff; border: 1.5px solid var(--blue-border); border-radius: var(--radius-sm); padding: 10px; }
    .calc-screen { width: 100%; background: #0c4a6e; color: #7dd3fc; font-family: monospace; font-size: 1.1rem; padding: 10px; border-radius: 4px; text-align: right; margin-bottom: 8px; overflow-x: auto; }
    .calc-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 6px; }
    .calc-btn { background: #f0f9ff; border: 1px solid var(--blue-border-soft); padding: 8px; border-radius: 4px; font-weight: 700; font-size: 0.9rem; cursor: pointer; text-align: center; color: var(--primary-dark); }
    .calc-btn:hover { background: #e0f2fe; }
    .calc-btn.op { background: #bae6fd; color: #0c4a6e; }
    .calc-btn.eq { background: var(--primary-blue); color: #fff; }

    .palette-card { background: var(--card-white); border-radius: var(--radius-lg); padding: 1.25rem; border: 2px solid var(--blue-border-soft); position: sticky; top: 90px; box-shadow: var(--shadow-md); }
    .palette-grid { display: grid; grid-template-columns: repeat(5, 1fr); gap: 6px; margin: 1rem 0; max-height: 380px; overflow-y: auto; padding-right: 4px; }
    .palette-btn { aspect-ratio: 1; border-radius: var(--radius-sm); border: 1.5px solid var(--blue-border-soft); background: #f8fafc; color: var(--text-muted); font-weight: 700; cursor: pointer; display: flex; align-items: center; justify-content: center; font-size: 0.85rem; }
    .palette-btn.active { border: 2.5px solid var(--primary-blue) !important; background: #e0f2fe !important; color: var(--primary-blue) !important; }
    .palette-btn.completed { background: var(--correct-green) !important; color: #ffffff !important; border-color: var(--correct-green) !important; }
    .palette-btn.progress { background: #93c5fd !important; border-color: #3b82f6 !important; color: #0f172a !important; }
    .palette-btn.skipped { background: #fef3c7 !important; color: #b45309 !important; border-color: #fde68a !important; }

    .problem-action-bar { display: flex; justify-content: space-between; align-items: center; padding-top: 1.25rem; border-top: 1.5px solid var(--blue-border-soft); margin-top: 1.5rem; flex-wrap: wrap; gap: 10px; }
    .btn { padding: 9px 16px; border-radius: var(--radius-sm); font-weight: 700; font-size: 0.92rem; cursor: pointer; border: none; display: inline-flex; align-items: center; gap: 6px; transition: all 0.2s ease; }
    .btn-step-check { background: var(--primary-blue); color: #ffffff; }
    .btn-step-back { background: #f0f9ff; color: var(--primary-dark); border: 1px solid var(--blue-border); }
    .btn-secondary { background: #e2e8f0; color: var(--text-main); }
    .btn-skip { background: #ffffff; color: var(--brand-gold-dark); border: 1.5px solid var(--brand-gold-dark); }

    .score-hero-card { background: linear-gradient(135deg, var(--primary-dark) 0%, var(--primary-blue) 60%, var(--accent-blue) 100%); color: #ffffff; border-radius: var(--radius-lg); padding: 2.5rem 2rem; text-align: center; margin-bottom: 2rem; box-shadow: var(--shadow-lg); }
    .score-circle { width: 115px; height: 115px; border-radius: 50%; background: rgba(255,255,255,0.15); border: 4px solid #7dd3fc; display: flex; flex-direction: column; align-items: center; justify-content: center; margin: 0 auto 1rem auto; }
    .stats-row { display: grid; grid-template-columns: repeat(auto-fit, minmax(120px, 1fr)); gap: 1rem; max-width: 600px; margin: 1.5rem auto 0 auto; }
    .stat-pill { background: rgba(255,255,255,0.12); padding: 10px; border-radius: var(--radius-md); }
    .review-card { background: #ffffff; border: 2px solid var(--blue-border-soft); border-radius: var(--radius-md); padding: 1.5rem; margin-bottom: 1rem; box-shadow: var(--shadow-sm); line-height: 2.2; }
  </style>
</head>
<body>

  <header>
    <div class="header-container">
      <div class="brand-group">
        <div class="brand-logo-wrap">
          <svg class="brand-logo-svg" viewBox="0 0 160 160" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M45 42 C66 22, 94 22, 115 42" stroke="#f59e0b" stroke-width="8" stroke-linecap="round" fill="none"/>
            <path d="M56 56 C70 42, 90 42, 104 56" stroke="#f59e0b" stroke-width="8" stroke-linecap="round" fill="none"/>
            <path d="M68 70 C75 62, 85 62, 92 70" stroke="#f59e0b" stroke-width="7" stroke-linecap="round" fill="none"/>
            <path d="M25 80 L76 96 L76 136 L25 120 Z" stroke="#334155" stroke-width="7" fill="#ffffff" stroke-linejoin="round"/>
            <path d="M135 80 L84 96 L84 136 L135 120 Z" stroke="#334155" stroke-width="7" fill="#ffffff" stroke-linejoin="round"/>
            <line x1="40" y1="94" x2="68" y2="103" stroke="#334155" stroke-width="5" stroke-linecap="round"/>
            <line x1="40" y1="108" x2="68" y2="117" stroke="#334155" stroke-width="5" stroke-linecap="round"/>
            <line x1="120" y1="94" x2="92" y2="103" stroke="#334155" stroke-width="5" stroke-linecap="round"/>
            <line x1="120" y1="108" x2="92" y2="117" stroke="#334155" stroke-width="5" stroke-linecap="round"/>
          </svg>
        </div>
        <div class="brand-title">
          <h1>Brain &amp; Mind Academy</h1>
          <p>B&amp;M - The Experts • DHANANJAYA 10 (Arithmetic Progressions Master Bank)</p>
        </div>
      </div>

      <div class="timer-widget" id="mainTimerWidget">
        <span style="font-size:0.9rem;">⏱️</span>
        <span class="timer-display" id="timerDisplay">00:00</span>
        <button class="timer-btn" id="timerToggleBtn" onclick="toggleTimer()">Pause</button>
        <button class="timer-btn" onclick="resetTimer()">Reset</button>
        <button class="timer-btn" style="background:#e0f2fe; color:var(--primary-dark);" onclick="playReminderChime()">🔔 Test Sound</button>
      </div>

      <div class="nav-tabs" id="mainHeaderNav">
        <button class="tab-btn active" onclick="switchMainTab('theory')">📖 Theory &amp; 5 Topic Videos</button>
        <button class="tab-btn" onclick="switchMainTab('sheet')">✍️ Board Practice Sheet (40 Items)</button>
        <button class="tab-btn" onclick="switchMainTab('solutions')">📋 Complete Solutions</button>
      </div>
      <div class="user-actions">
        <div class="user-badge"><span id="userEmailSpan">🔒 Locked Portal</span></div>
        <button class="btn-icon" id="soundToggleBtn"><span id="soundIcon">🔊</span></button>
      </div>
    </div>
  </header>

  <div id="reminderToast" class="toast-reminder"></div>

  <main>
    
    <!-- 0. COMPULSORY LOGIN GATE -->
    <section id="loginGateView" class="view-section active">
      <div class="login-gate-card">
        <div class="login-lock-icon">🔒</div>
        <h2>DHANANJAYA 10 Portal</h2>
        <p>CBSE Class 10 Board Series: Chapter 5 Arithmetic Progressions (Expanded Master Bank). Strictly <strong>one attempt per student</strong> unless authorized by the administrator.</p>
        
        <form id="studentLoginForm" onsubmit="handlePortalLogin(event)">
          <div class="input-field-group">
            <label for="studentIdInput">Student ID / Roll No</label>
            <input type="text" id="studentIdInput" class="login-input" placeholder="e.g. DHANANJAY-101" required autocomplete="username" />
          </div>
          <div class="input-field-group">
            <label for="studentPasscodeInput">Security Passcode</label>
            <input type="password" id="studentPasscodeInput" class="login-input" placeholder="••••••••" required autocomplete="current-password" />
          </div>
          <button type="submit" class="login-btn-submit" id="loginSubmitBtn">Authenticate &amp; Open Arithmetic Progressions</button>
          <div class="login-error-text" id="loginErrorMsg"></div>
        </form>
      </div>
    </section>

    <!-- 1. Theory Notes & 5 Topic Videos -->
    <section id="theoryView" class="view-section">
      <div class="notes-card">
        <div class="notes-header">
          <h2>Chapter 5: Arithmetic Progressions — Complete CBSE Board Theory</h2>
          <p style="color: var(--text-muted); font-size: 0.95rem;">General Form of an AP, nth Term Formula, Sum of First n Terms, and Real-World Modeling.</p>
        </div>

        <div class="notes-body">
          <h3><span class="step-badge">TOPIC 1</span> What is an Arithmetic Progression?</h3>
          <p>An arithmetic progression is a list of numbers in which each term is obtained by adding a fixed number \( d \) to the preceding term, except the first term \( a \):</p>
          <div class="formula-callout">
            • <strong>General Form of an AP:</strong> \( a, a + d, a + 2d, a + 3d, \dots \)<br>
            • <strong>Common Difference:</strong> \( d = a_{k+1} - a_k \). Remember \( d \) can be <strong>positive, negative, or zero</strong>.<br>
            • <strong>Finite vs Infinite AP:</strong> An AP with a finite number of terms has a last term \( l \). An infinite AP continues indefinitely without a last term.
          </div>

          <div class="video-callout">
            <div>
              <strong>🎥 Khan Academy Video 1:</strong>
              <div style="font-size:0.9rem; color:#1e40af;">Intro to arithmetic progressions</div>
            </div>
            <a href="https://www.khanacademy.org/math/ncert-class-10/xd6a17b08edbd2443:arithmetic-progression-ncert-new/xd6a17b08edbd2443:arithmetic-progression/v/intro-to-arithmetic-progressions-arithmetic-progressions" target="_blank" class="btn btn-step-check" style="text-decoration:none;">Watch Lesson 1 ↗</a>
          </div>

          <div class="video-callout">
            <div>
              <strong>🎥 Khan Academy Video 2:</strong>
              <div style="font-size:0.9rem; color:#1e40af;">Extending arithmetic sequences</div>
            </div>
            <a href="https://www.khanacademy.org/math/ncert-class-10/xd6a17b08edbd2443:arithmetic-progression-ncert-new/xd6a17b08edbd2443:arithmetic-progression/v/extending-arithmetic-sequences-indian-accent" target="_blank" class="btn btn-step-check" style="text-decoration:none;">Watch Lesson 2 ↗</a>
          </div>

          <h3><span class="step-badge">TOPIC 2</span> The nth Term of an AP</h3>
          <p>The \( n \)-th term (or general term) of an AP with first term \( a \) and common difference \( d \) is:</p>
          <div class="formula-callout">
            \[ a_n = a + (n - 1)d \]
            • If an AP has \( m \) terms, then \( a_m \) denotes the last term, often written as \( l \).<br>
            • The \( n \)-th term from the end of an AP with last term \( l \) and common difference \( d \) is:
            \[ a_n' = l - (n - 1)d \]
            • <strong>Arithmetic Mean:</strong> If \( a, b, c \) are in AP, then \( b = \frac{a + c}{2} \).
          </div>

          <div class="video-callout">
            <div>
              <strong>🎥 Khan Academy Video 3:</strong>
              <div style="font-size:0.9rem; color:#1e40af;">nth term of an arithmetic progression</div>
            </div>
            <a href="https://www.khanacademy.org/math/ncert-class-10/xd6a17b08edbd2443:arithmetic-progression-ncert-new/xd6a17b08edbd2443:nth-term-of-an-ap/v/nth-term-of-an-arithmetic-progression-arithmetic-progressions" target="_blank" class="btn btn-step-check" style="text-decoration:none;">Watch Lesson 3 ↗</a>
          </div>

          <h3><span class="step-badge">TOPIC 3</span> Sum of First n Terms of an AP</h3>
          <p>The sum \( S_n \) of the first \( n \) terms of an AP is given by Gauss's summation formulation:</p>
          <div class="formula-callout">
            \[ S_n = \frac{n}{2}[2a + (n - 1)d] \]
            • When first term \( a \) and last term \( l \) are known:
            \[ S_n = \frac{n}{2}(a + l) \]
            • Sum of first \( n \) positive integers:
            \[ S_n = \frac{n(n + 1)}{2} \]
            • <strong>Relationship between \( a_n \) and \( S_n \):</strong>
            \[ a_n = S_n - S_{n-1} \]
          </div>

          <div class="video-callout">
            <div>
              <strong>🎥 Khan Academy Video 4:</strong>
              <div style="font-size:0.9rem; color:#1e40af;">Arithmetic series intro</div>
            </div>
            <a href="https://www.khanacademy.org/math/ncert-class-10/xd6a17b08edbd2443:arithmetic-progression-ncert-new/xd6a17b08edbd2443:sum-of-first-n-terms-of-an-ap/v/arithmetic-series-intro-indian-accent" target="_blank" class="btn btn-step-check" style="text-decoration:none;">Watch Lesson 4 ↗</a>
          </div>

          <div class="video-callout">
            <div>
              <strong>🎥 Khan Academy Video 5:</strong>
              <div style="font-size:0.9rem; color:#1e40af;">Arithmetic series formula</div>
            </div>
            <a href="https://www.khanacademy.org/math/ncert-class-10/xd6a17b08edbd2443:arithmetic-progression-ncert-new/xd6a17b08edbd2443:sum-of-first-n-terms-of-an-ap/v/arithmetic-series-formula-indian-accent" target="_blank" class="btn btn-step-check" style="text-decoration:none;">Watch Lesson 5 ↗</a>
          </div>
        </div>

        <div style="margin-top:2rem; background:#f0f9ff; border:2px solid var(--blue-border); border-radius:var(--radius-md); padding:1.5rem; display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:1rem;">
          <div>
            <strong>Ready to practice the complete chapter question bank?</strong>
            <p style="font-size: 0.9rem; color: var(--primary-dark); margin-top:2px;">Work through all 40 NCERT examples, exercise problems, and optional challenge tasks with clear figures.</p>
          </div>
          <button class="btn btn-primary" onclick="switchMainTab('sheet')" style="background:var(--primary-blue); color:#fff;">
            Start 40-Question Practice Sheet →
          </button>
        </div>
      </div>
    </section>

    <!-- 2. Guided Practice Sheet (Workspace) -->
    <section id="sheetView" class="view-section">
      <div class="learning-grid-layout">
        
        <div class="problem-card">
          <div class="problem-header">
            <div>
              <span class="p-tag" id="pNumberDisplay">Question 1</span>
              <span class="category-badge" id="pCategoryBadge">NCERT Example</span>
              <span class="parts-badge" id="pPartsBadge">2 Steps</span>
            </div>
            <div class="status-badge badge-unvisited" id="pStatusBadge">Unvisited</div>
          </div>
          
          <div class="problem-context" id="pContextDisplay"></div>

          <!-- Dynamic SVG Vector Diagram Display -->
          <div id="diagramDisplayContainer" class="diagram-container" style="display:none;"></div>

          <!-- On-Screen Virtual Tools -->
          <div class="tools-panel">
            <div class="tool-tab-header">
              <button class="tool-tab-btn active" id="tabPadBtn" onclick="switchToolTab('pad')">⌨️ Math Keypad</button>
              <button class="tool-tab-btn" id="tabCalcBtn" onclick="switchToolTab('calc')">🧮 Calculator</button>
            </div>
            
            <div id="mathPadView">
              <div class="math-pad-grid">
                <button class="math-pad-btn" onclick="insertSymbol('a')">a</button>
                <button class="math-pad-btn" onclick="insertSymbol('d')">d</button>
                <button class="math-pad-btn" onclick="insertSymbol('n')">n</button>
                <button class="math-pad-btn" onclick="insertSymbol('l')">l</button>
                <button class="math-pad-btn" onclick="insertSymbol('x')">x</button>
                <button class="math-pad-btn" onclick="insertSymbol('√')">√</button>
                <button class="math-pad-btn" onclick="insertSymbol('^')">^</button>
                <button class="math-pad-btn" onclick="insertSymbol('0')">0</button>
                <button class="math-pad-btn" onclick="insertSymbol('1')">1</button>
                <button class="math-pad-btn" onclick="insertSymbol('2')">2</button>
                <button class="math-pad-btn" onclick="insertSymbol('3')">3</button>
                <button class="math-pad-btn" onclick="insertSymbol('4')">4</button>
                <button class="math-pad-btn" onclick="insertSymbol('5')">5</button>
                <button class="math-pad-btn" onclick="insertSymbol('6')">6</button>
                <button class="math-pad-btn" onclick="insertSymbol('-')">-</button>
                <button class="math-pad-btn" onclick="insertSymbol('+')">+</button>
                <button class="math-pad-btn" onclick="insertSymbol('/')">/</button>
                <button class="math-pad-btn" onclick="insertSymbol('.')">.</button>
                <button class="math-pad-btn" onclick="insertSymbol('(')">(</button>
                <button class="math-pad-btn" onclick="insertSymbol(')')">)</button>
                <button class="math-pad-btn" onclick="insertSymbol('Yes')">Yes</button>
                <button class="math-pad-btn" style="background:#fee2e2; color:#dc2626;" onclick="clearActiveField()">Clear</button>
              </div>
            </div>

            <div id="calcView" style="display:none;">
              <div class="calc-box">
                <div class="calc-screen" id="calcScreen">0</div>
                <div class="calc-grid">
                  <button class="calc-btn" onclick="calcAppend('(')">(</button>
                  <button class="calc-btn" onclick="calcAppend(')')">)</button>
                  <button class="calc-btn" onclick="calcClear()">C</button>
                  <button class="calc-btn op" onclick="calcAppend('/')">/</button>
                  <button class="calc-btn" onclick="calcAppend('7')">7</button>
                  <button class="calc-btn" onclick="calcAppend('8')">8</button>
                  <button class="calc-btn" onclick="calcAppend('9')">9</button>
                  <button class="calc-btn op" onclick="calcAppend('*')">*</button>
                  <button class="calc-btn" onclick="calcAppend('4')">4</button>
                  <button class="calc-btn" onclick="calcAppend('5')">5</button>
                  <button class="calc-btn" onclick="calcAppend('6')">6</button>
                  <button class="calc-btn op" onclick="calcAppend('-')">-</button>
                  <button class="calc-btn" onclick="calcAppend('1')">1</button>
                  <button class="calc-btn" onclick="calcAppend('2')">2</button>
                  <button class="calc-btn" onclick="calcAppend('3')">3</button>
                  <button class="calc-btn op" onclick="calcAppend('+')">+</button>
                  <button class="calc-btn" onclick="calcAppend('0')">0</button>
                  <button class="calc-btn" onclick="calcAppend('.')">.</button>
                  <button class="calc-btn op" onclick="calcSqrt()">√</button>
                  <button class="calc-btn eq" onclick="calcEval()">=</button>
                </div>
              </div>
            </div>
          </div>

          <div class="steps-container" id="stepsListContainer"></div>

          <div class="problem-action-bar">
            <div style="display: flex; gap: 8px;">
              <button class="btn btn-secondary" id="prevProblemBtn">← Prev Question</button>
              <button class="btn btn-secondary" id="nextProblemBtn">Next Question →</button>
            </div>
            <button class="btn btn-skip" id="skipProblemBtn">Skip Question</button>
          </div>
        </div>

        <aside class="palette-card">
          <div style="display:flex; justify-content:space-between; align-items:center;">
            <strong style="color:var(--primary-dark); font-size:1.02rem;">40-Item Index</strong>
            <span style="font-size:0.85rem; color:var(--primary-blue); font-weight:700;" id="completionRateText">0/40 Solved</span>
          </div>
          <div class="palette-grid" id="paletteGridContainer"></div>
          <button class="btn btn-primary" id="finishAssessmentBtn" style="margin-top: 1.25rem; width: 100%; background:var(--primary-blue); color:#fff;">Finish &amp; View All Solutions</button>
        </aside>

      </div>
    </section>

    <!-- 3. Final Review & Complete Solutions -->
    <section id="solutionsView" class="view-section">
      <div class="score-hero-card">
        <span style="background:rgba(255,255,255,0.2); color:#bae6fd; padding:4px 10px; border-radius:12px; font-weight:700;">Board Diagnostic Report</span>
        <h2 style="margin: 0.5rem 0; font-size: 1.7rem;">Arithmetic Progressions Complete Mastery Report</h2>
        <div class="score-circle">
          <div id="finalScoreVal" style="font-size:2rem; font-weight:800;">0</div>
          <div style="font-size:0.8rem; color:#bae6fd;">out of 40</div>
        </div>
        <p id="performanceFeedbackDesc" style="color: #bae6fd; font-size:0.95rem; max-width:540px; margin:0 auto;"></p>
        <div class="stats-row">
          <div class="stat-pill"><div style="font-size:0.75rem; color:#bae6fd;">Accuracy</div><div id="accuracyStat" style="font-size:1.2rem; font-weight:700;">0%</div></div>
          <div class="stat-pill"><div style="font-size:0.75rem; color:#bae6fd;">Solved</div><div id="correctCountStat" style="font-size:1.2rem; font-weight:700; color:#86efac;">0</div></div>
          <div class="stat-pill"><div style="font-size:0.75rem; color:#bae6fd;">Skipped</div><div id="skippedCountStat" style="font-size:1.2rem; font-weight:700; color:#fde047;">0</div></div>
        </div>
        <div style="margin-top: 1.5rem; display:flex; justify-content:center; gap:10px;">
          <button class="btn" style="background: rgba(255,255,255,0.25); color:#fff;" id="retakeQuizBtn">🔒 Exit &amp; Lock Session</button>
          <button class="btn" style="background:#fff; color:var(--primary-dark);" onclick="window.print()">🖨️ Print Solutions</button>
        </div>
      </div>
      <h3 style="color: var(--primary-dark); margin-bottom:1rem;">Complete Step-by-Step Solutions (Questions 1 to 40)</h3>
      <div id="reviewListContainer"></div>
    </section>

  </main>

  <script>
    const BACKEND_URL = "https://script.google.com/macros/s/AKfycbwmH_oK_IGRkYPm9DRcdKIdp7nSP2zyftCrnY-wwX45fd9KHfAt26VzOQy1QC7PMsOr/exec";

    let currentAuthUser = {
      studentId: "",
      studentName: ""
    };

    async function handlePortalLogin(e) {
      e.preventDefault();
      const sId = document.getElementById("studentIdInput").value.trim();
      const pass = document.getElementById("studentPasscodeInput").value.trim();
      const errEl = document.getElementById("loginErrorMsg");
      const btn = document.getElementById("loginSubmitBtn");

      errEl.style.display = "none";
      btn.disabled = true;
      btn.textContent = "Verifying with Database...";

      try {
        const response = await fetch(BACKEND_URL, {
          method: "POST",
          body: JSON.stringify({
            action: "verifyStudent",
            studentId: sId,
            accessKey: pass
          })
        });

        const result = await response.json();

        if (result.success) {
          currentAuthUser.studentId = sId;
          currentAuthUser.studentName = result.name || sId;
          sessionStorage.setItem("dhananjaya_auth_id", sId);
          sessionStorage.setItem("dhananjaya_auth_name", currentAuthUser.studentName);

          document.getElementById("userEmailSpan").textContent = `👤 ${currentAuthUser.studentName} (${sId})`;
          document.getElementById("mainTimerWidget").style.display = "flex";
          document.getElementById("mainHeaderNav").style.display = "flex";
          switchMainTab("sheet");
          startTimer();
        } else {
          errEl.textContent = result.error || "Access Denied: Invalid Student ID, Passcode, or Attempt Limit Reached.";
          errEl.style.display = "block";
        }
      } catch (err) {
        errEl.textContent = "Connection error while reaching the server. Please check your network.";
        errEl.style.display = "block";
      } finally {
        btn.disabled = false;
        btn.textContent = "Authenticate & Open Arithmetic Progressions";
      }
    }

    function sendReportToSheet(solvedCount, totalCount, totalSecs) {
      if (!currentAuthUser.studentId) return;

      const payload = {
        action: "submitReport",
        studentId: currentAuthUser.studentId,
        studentName: currentAuthUser.studentName,
        score: solvedCount,
        totalQuestions: totalCount,
        accuracy: Math.round((solvedCount / totalCount) * 100),
        timeSpent: formatTime(totalSecs),
        details: {
          assessment: "DHANANJAYA 10 - Arithmetic Progressions (NCERT Complete Chapter 5)",
          submittedAt: new Date().toISOString(),
          questionsSolved: solvedCount,
          questionsSkipped: totalCount - solvedCount
        }
      };

      fetch(BACKEND_URL, {
        method: "POST",
        mode: "no-cors",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify(payload)
      }).catch(() => {});
    }

    /* ==========================================================================
       SVG VECTOR DIAGRAMS (NCERT CHAPTER 5 ARITHMETIC PROGRESSIONS)
       ========================================================================== */
    const SVG_SPIRAL = `
      <svg class="diagram-svg" viewBox="0 0 380 230" xmlns="http://www.w3.org/2000/svg">
        <rect width="380" height="230" fill="#f8fafc" rx="8"/>
        <line x1="20" y1="115" x2="360" y2="115" stroke="#0f172a" stroke-width="1.8"/>
        <circle cx="175" cy="115" r="3.5" fill="#0284c7"/>
        <circle cx="190" cy="115" r="3.5" fill="#dc2626"/>
        <text x="171" y="132" font-size="11" font-weight="800">A</text>
        <text x="189" y="132" font-size="11" font-weight="800">B</text>
        <path d="M 175 115 A 15 15 0 0 1 190 115" fill="none" stroke="#0284c7" stroke-width="2.5"/>
        <text x="180" y="94" font-size="10" font-weight="700">l₁</text>
        <path d="M 190 115 A 30 30 0 0 1 160 115" fill="none" stroke="#0284c7" stroke-width="2.5"/>
        <text x="172" y="156" font-size="11" font-weight="700">l₂</text>
        <path d="M 160 115 A 45 45 0 0 1 220 115" fill="none" stroke="#0284c7" stroke-width="2.5"/>
        <text x="188" y="62" font-size="11" font-weight="700">l₃</text>
        <path d="M 220 115 A 60 60 0 0 1 130 115" fill="none" stroke="#0284c7" stroke-width="2.5"/>
        <text x="172" y="190" font-size="11" font-weight="700">l₄</text>
      </svg>
      <div class="diagram-caption">Fig 5.4: Successive Semicircles with Radii 0.5 cm, 1.0 cm, 1.5 cm, ...</div>
    `;

    const SVG_LOGS = `
      <svg class="diagram-svg" viewBox="0 0 380 170" xmlns="http://www.w3.org/2000/svg">
        <rect width="380" height="170" fill="#f8fafc" rx="8"/>
        <g fill="#bae6fd" stroke="#0284c7" stroke-width="1.5">
          <rect x="30" y="125" width="320" height="22" rx="4"/>
          <text x="190" y="140" font-size="11" font-weight="800" fill="#0369a1" text-anchor="middle">Bottom Row (Row 1): 20 logs</text>
          <rect x="42" y="101" width="296" height="22" rx="4"/>
          <text x="190" y="116" font-size="11" font-weight="800" fill="#0369a1" text-anchor="middle">Row 2: 19 logs</text>
          <rect x="54" y="77" width="272" height="22" rx="4"/>
          <text x="190" y="92" font-size="11" font-weight="800" fill="#0369a1" text-anchor="middle">Row 3: 18 logs</text>
          <circle cx="190" cy="62" r="3" fill="#0284c7"/>
          <circle cx="190" cy="52" r="3" fill="#0284c7"/>
          <rect x="130" y="22" width="120" height="22" rx="4" fill="#fef3c7" stroke="#b45309"/>
          <text x="190" y="37" font-size="11" font-weight="800" fill="#b45309" text-anchor="middle">Top Row: ? logs</text>
        </g>
      </svg>
      <div class="diagram-caption">Fig 5.5: 200 Logs Stacked in Rows with Decreasing Counts</div>
    `;

    const SVG_POTATO = `
      <svg class="diagram-svg" viewBox="0 0 460 160" xmlns="http://www.w3.org/2000/svg">
        <rect width="460" height="160" fill="#f8fafc" rx="8"/>
        <line x1="20" y1="110" x2="440" y2="110" stroke="#0f172a" stroke-width="2"/>
        <rect x="35" y="75" width="26" height="35" rx="2" fill="#94a3b8" stroke="#0f172a" stroke-width="1.8"/>
        <text x="48" y="68" font-size="10" font-weight="800" text-anchor="middle">Bucket</text>
        <circle cx="120" cy="110" r="4.5" fill="#f59e0b" stroke="#0f172a" stroke-width="1.5"/>
        <line x1="48" y1="125" x2="120" y2="125" stroke="#0284c7" stroke-width="1.5"/>
        <text x="84" y="138" font-size="10" font-weight="800" fill="#0284c7" text-anchor="middle">5 m</text>
        <circle cx="170" cy="110" r="4.5" fill="#f59e0b" stroke="#0f172a" stroke-width="1.5"/>
        <line x1="120" y1="125" x2="170" y2="125" stroke="#0284c7" stroke-width="1.5"/>
        <text x="145" y="138" font-size="10" font-weight="800" fill="#0284c7" text-anchor="middle">3 m</text>
        <circle cx="220" cy="110" r="4.5" fill="#f59e0b" stroke="#0f172a" stroke-width="1.5"/>
        <text x="195" y="138" font-size="10" font-weight="800" fill="#0284c7" text-anchor="middle">3 m</text>
        <circle cx="270" cy="110" r="4.5" fill="#f59e0b" stroke="#0f172a" stroke-width="1.5"/>
        <circle cx="320" cy="110" r="4.5" fill="#f59e0b" stroke="#0f172a" stroke-width="1.5"/>
        <circle cx="370" cy="110" r="4.5" fill="#f59e0b" stroke="#0f172a" stroke-width="1.5"/>
        <text x="410" y="113" font-size="12" font-weight="800">... (10 potatoes)</text>
      </svg>
      <div class="diagram-caption">Fig 5.6: The Potato Race Track Setup</div>
    `;

    const SVG_LADDER = `
      <svg class="diagram-svg" viewBox="0 0 280 260" xmlns="http://www.w3.org/2000/svg">
        <rect width="280" height="260" fill="#f8fafc" rx="8"/>
        <line x1="70" y1="230" x2="105" y2="30" stroke="#0369a1" stroke-width="4"/>
        <line x1="210" y1="230" x2="175" y2="30" stroke="#0369a1" stroke-width="4"/>
        <line x1="105" y1="40" x2="175" y2="40" stroke="#0284c7" stroke-width="3"/>
        <text x="140" y="34" font-size="10" font-weight="800" text-anchor="middle">25 cm</text>
        <line x1="101" y1="65" x2="179" y2="65" stroke="#0284c7" stroke-width="2.5"/>
        <line x1="97" y1="90" x2="183" y2="90" stroke="#0284c7" stroke-width="2.5"/>
        <line x1="93" y1="115" x2="187" y2="115" stroke="#0284c7" stroke-width="2.5"/>
        <line x1="89" y1="140" x2="191" y2="140" stroke="#0284c7" stroke-width="2.5"/>
        <line x1="85" y1="165" x2="195" y2="165" stroke="#0284c7" stroke-width="2.5"/>
        <line x1="81" y1="190" x2="199" y2="190" stroke="#0284c7" stroke-width="2.5"/>
        <line x1="74" y1="215" x2="206" y2="215" stroke="#0284c7" stroke-width="3"/>
        <text x="140" y="235" font-size="10" font-weight="800" text-anchor="middle">45 cm</text>
        <line x1="235" y1="40" x2="235" y2="215" stroke="#dc2626" stroke-width="1.8"/>
        <text x="248" y="132" font-size="10" font-weight="800" fill="#dc2626">2 ½ m</text>
      </svg>
      <div class="diagram-caption">Fig 5.7: Ladder with Tapering Rungs Spaced 25 cm Apart</div>
    `;

    const SVG_TERRACE = `
      <svg class="diagram-svg" viewBox="0 0 380 200" xmlns="http://www.w3.org/2000/svg">
        <rect width="380" height="200" fill="#f8fafc" rx="8"/>
        <path d="M 60 160 L 110 160 L 110 140 L 160 140 L 160 120 L 210 120 L 210 100 L 260 100 L 260 80 L 310 80 L 310 170 L 60 170 Z" fill="#bae6fd" stroke="#0284c7" stroke-width="2"/>
        <text x="85" y="154" font-size="10" font-weight="700">Tread ½ m</text>
        <text x="115" y="132" font-size="10" font-weight="700">Rise ¼ m</text>
        <line x1="60" y1="185" x2="310" y2="185" stroke="#0369a1" stroke-width="2"/>
        <text x="185" y="197" font-size="11" font-weight="800" fill="#0369a1" text-anchor="middle">Length of terrace = 50 m (15 steps total)</text>
      </svg>
      <div class="diagram-caption">Fig 5.8: Solid Concrete Terrace Steps (15 Steps Total)</div>
    `;

    /* ==========================================================================
       COMPLETE 40 EXPANDED NCERT QUESTIONS & EXAMPLES
       ========================================================================== */
    const PROBLEMS_DATA = [
      // 1. Example 1
      {
        id: 1,
        title: "Question 1",
        category: "NCERT Example 1",
        partsInfo: "2 Steps Required",
        context: "For the AP: \\( \\frac{3}{2}, \\frac{1}{2}, -\\frac{1}{2}, -\\frac{3}{2}, \\dots \\), write the first term \\( a \\) and the common difference \\( d \\).",
        steps: [
          {
            title: "Step 1: First Term a",
            prompt: "State the first term \\( a \\): <input class='step-input' style='width:70px;' data-ans='3/2' data-alt='1.5'>",
            explanation: "The first term is the initial number a = 3/2."
          },
          {
            title: "Step 2: Common Difference d",
            prompt: "\\( d = a_2 - a_1 = \\frac{1}{2} - \\frac{3}{2} = \\) <input class='step-input' style='width:50px;' data-ans='-1'>",
            explanation: "d = (1 - 3)/2 = -2/2 = -1."
          }
        ]
      },
      // 2. Example 2(i)
      {
        id: 2,
        title: "Question 2",
        category: "NCERT Example 2(i)",
        partsInfo: "2 Steps Required",
        context: "Does the list \\( 4, 10, 16, 22, \\dots \\) form an AP? If so, write the next two terms.",
        steps: [
          {
            title: "Step 1: Difference Check",
            prompt: "\\( 10 - 4 = 6 \\), \\( 16 - 10 = 6 \\), \\( 22 - 16 = 6 \\). Does it form an AP? (Yes/No): <input class='step-input' style='width:60px;' data-ans='Yes' data-alt='yes'>",
            explanation: "Consecutive differences are equal to 6, so it is an AP."
          },
          {
            title: "Step 2: Next Two Terms",
            prompt: "Next two terms are \\( 22 + 6 = \\) <input class='step-input' style='width:50px;' data-ans='28'> and \\( 28 + 6 = \\) <input class='step-input' style='width:50px;' data-ans='34'>",
            explanation: "Next terms are 28 and 34."
          }
        ]
      },
      // 3. Ex 5.1 Q1(i)
      {
        id: 3,
        title: "Question 3",
        category: "Exercise 5.1, Q1(i)",
        partsInfo: "2 Steps Required",
        context: "The taxi fare is ₹15 for the first km and ₹8 for each additional km. Does this situation make an AP?",
        steps: [
          {
            title: "Step 1: Form Sequence of Fares",
            prompt: "Fares are ₹15, ₹23, ₹<input class='step-input' style='width:50px;' data-ans='31'>, ...",
            explanation: "Sequence: 15, 15+8=23, 23+8=31, ..."
          },
          {
            title: "Step 2: Verify AP",
            prompt: "Does this form an arithmetic progression? (Yes/No): <input class='step-input' style='width:60px;' data-ans='Yes' data-alt='yes'>",
            explanation: "Yes, common difference d = 8."
          }
        ]
      },
      // 4. Ex 5.1 Q1(ii)
      {
        id: 4,
        title: "Question 4",
        category: "Exercise 5.1, Q1(ii)",
        partsInfo: "2 Steps Required",
        context: "A vacuum pump removes \\( \\frac{1}{4} \\) of the air remaining in a cylinder at a time. Does the remaining air form an AP?",
        steps: [
          {
            title: "Step 1: Successive Volumes",
            prompt: "Initial volume = \\( V \\). After 1st stroke = \\( \\frac{3}{4}V \\). After 2nd stroke = \\( \\left(\\frac{3}{4}\\right)^2 V = \\) <input class='step-input' style='width:70px;' data-ans='9/16V' data-alt='9/16 V|9/16'>",
            explanation: "Volumes are V, 3/4 V, 9/16 V, 27/64 V..."
          },
          {
            title: "Step 2: Check Differences",
            prompt: "\\( \\frac{3}{4}V - V = -\\frac{1}{4}V \\), while \\( \\frac{9}{16}V - \\frac{3}{4}V = -\\frac{3}{16}V \\). Is it an AP? (Yes/No): <input class='step-input' style='width:60px;' data-ans='No' data-alt='no'>",
            explanation: "The differences are not constant, so it does not form an AP."
          }
        ]
      },
      // 5. Ex 5.1 Q2(iii)
      {
        id: 5,
        title: "Question 5",
        category: "Exercise 5.1, Q2(iii)",
        partsInfo: "2 Steps Required",
        context: "Write first four terms of the AP when first term \\( a = 4 \\) and common difference \\( d = -3 \\).",
        steps: [
          {
            title: "Step 1: Compute Terms",
            prompt: "\\( a_1 = 4, a_2 = 1, a_3 = 1 - 3 = \\) <input class='step-input' style='width:50px;' data-ans='-2'>",
            explanation: "a3 = -2."
          },
          {
            title: "Step 2: Fourth Term",
            prompt: "\\( a_4 = -2 - 3 = \\) <input class='step-input' style='width:50px;' data-ans='-5'>",
            explanation: "The first four terms are 4, 1, -2, -5."
          }
        ]
      },
      // 6. Ex 5.1 Q4(v)
      {
        id: 6,
        title: "Question 6",
        category: "Exercise 5.1, Q4(v)",
        partsInfo: "2 Steps Required",
        context: "Is \\( 3, 3+\\sqrt{2}, 3+2\\sqrt{2}, 3+3\\sqrt{2}, \\dots \\) an AP? If so, find \\( d \\) and write the next term.",
        steps: [
          {
            title: "Step 1: Difference",
            prompt: "\\( (3 + \\sqrt{2}) - 3 = \\) <input class='step-input' style='width:60px;' data-ans='√2' data-alt='sqrt(2)'>",
            explanation: "Common difference d = sqrt(2)."
          },
          {
            title: "Step 2: Next Term",
            prompt: "Fifth term = \\( 3 + 3\\sqrt{2} + \\sqrt{2} = \\) <input class='step-input' style='width:120px;' data-ans='3+4√2' data-alt='3 + 4√2|3+4sqrt(2)'>",
            explanation: "a5 = 3 + 4*sqrt(2)."
          }
        ]
      },
      // 7. Ex 5.1 Q4(xii)
      {
        id: 7,
        title: "Question 7",
        category: "Exercise 5.1, Q4(xii)",
        partsInfo: "3 Steps Required",
        context: "Check if \\( \\sqrt{2}, \\sqrt{8}, \\sqrt{18}, \\sqrt{32}, \\dots \\) is an AP. If so, find \\( d \\) and the next term.",
        steps: [
          {
            title: "Step 1: Simplify Radicals",
            prompt: "\\( \\sqrt{8} = 2\\sqrt{2} \\), \\( \\sqrt{18} = 3\\sqrt{2} \\), \\( \\sqrt{32} = 4\\sqrt{2} \\). Is it an AP? (Yes/No): <input class='step-input' style='width:60px;' data-ans='Yes' data-alt='yes'>",
            explanation: "The terms are sqrt(2), 2sqrt(2), 3sqrt(2), 4sqrt(2)... which form an AP."
          },
          {
            title: "Step 2: Common Difference",
            prompt: "\\( d = 2\\sqrt{2} - \\sqrt{2} = \\) <input class='step-input' style='width:60px;' data-ans='√2' data-alt='sqrt(2)'>",
            explanation: "d = sqrt(2)."
          },
          {
            title: "Step 3: Next Term in Simplified Radical Form",
            prompt: "Fifth term is \\( 5\\sqrt{2} = \\sqrt{50} \\). Enter as \\( \\sqrt{50} \\): <input class='step-input' style='width:80px;' data-ans='√50' data-alt='sqrt(50)|5√2'>",
            explanation: "a5 = sqrt(50)."
          }
        ]
      },
      // 8. Example 3
      {
        id: 8,
        title: "Question 8",
        category: "NCERT Example 3",
        partsInfo: "2 Steps Required",
        context: "Find the 10th term of the AP: \\( 2, 7, 12, \\dots \\)",
        steps: [
          {
            title: "Step 1: Identify Parameters",
            prompt: "\\( a = 2 \\), \\( d = 7 - 2 = \\) <input class='step-input' style='width:50px;' data-ans='5'>",
            explanation: "a = 2 and d = 5."
          },
          {
            title: "Step 2: Compute a_10",
            prompt: "\\( a_{10} = 2 + (10 - 1)5 = 2 + 45 = \\) <input class='step-input' style='width:50px;' data-ans='47'>",
            explanation: "a10 = 47."
          }
        ]
      },
      // 9. Example 4
      {
        id: 9,
        title: "Question 9",
        category: "NCERT Example 4",
        partsInfo: "2 Steps Required",
        context: "Which term of the AP: \\( 21, 18, 15, \\dots \\) is \\( -81 \\)? Also, which term is 0?",
        steps: [
          {
            title: "Step 1: Solve for n when a_n = -81",
            prompt: "\\( -81 = 21 + (n - 1)(-3) \\implies -102 = -3(n - 1) \\implies n = \\) <input class='step-input' style='width:50px;' data-ans='35'>",
            explanation: "The 35th term is -81."
          },
          {
            title: "Step 2: Solve for n when a_n = 0",
            prompt: "\\( 0 = 21 + (n - 1)(-3) \\implies n = \\) <input class='step-input' style='width:50px;' data-ans='8'>",
            explanation: "The 8th term is 0."
          }
        ]
      },
      // 10. Example 5
      {
        id: 10,
        title: "Question 10",
        category: "NCERT Example 5",
        partsInfo: "2 Steps Required",
        context: "Determine the AP whose 3rd term is 5 and 7th term is 9.",
        steps: [
          {
            title: "Step 1: Find a and d",
            prompt: "\\( a + 2d = 5 \\) and \\( a + 6d = 9 \\implies 4d = 4 \\implies d = \\) <input class='step-input' style='width:50px;' data-ans='1'>, \\( a = \\) <input class='step-input' style='width:50px;' data-ans='3'>",
            explanation: "d = 1 and a = 3."
          },
          {
            title: "Step 2: State First Three Terms",
            prompt: "The AP is: <input class='step-input' style='width:100px;' data-ans='3, 4, 5' data-alt='3,4,5'>",
            explanation: "The AP is 3, 4, 5, 6, ..."
          }
        ]
      },
      // 11. Example 6
      {
        id: 11,
        title: "Question 11",
        category: "NCERT Example 6",
        partsInfo: "2 Steps Required",
        context: "Check whether 301 is a term of the list \\( 5, 11, 17, 23, \\dots \\)",
        steps: [
          {
            title: "Step 1: Solve for n",
            prompt: "\\( 301 = 5 + (n - 1)6 \\implies 296 = 6(n - 1) \\implies n = \\) <input class='step-input' style='width:70px;' data-ans='151/3'>",
            explanation: "n = 151/3 (not an integer)."
          },
          {
            title: "Step 2: Conclusion",
            prompt: "Is 301 a term of this AP? (Yes/No): <input class='step-input' style='width:60px;' data-ans='No' data-alt='no'>",
            explanation: "No, because n must be a positive natural number."
          }
        ]
      },
      // 12. Example 7
      {
        id: 12,
        title: "Question 12",
        category: "NCERT Example 7",
        partsInfo: "2 Steps Required",
        context: "How many two-digit numbers are divisible by 3?",
        steps: [
          {
            title: "Step 1: First and Last Multiples",
            prompt: "First is 12, last is 99. \\( 99 = 12 + (n - 1)3 \\implies n - 1 = \\) <input class='step-input' style='width:50px;' data-ans='29'>",
            explanation: "n - 1 = 29."
          },
          {
            title: "Step 2: Total Count n",
            prompt: "\\( n = \\) <input class='step-input' style='width:50px;' data-ans='30'>",
            explanation: "There are 30 two-digit numbers divisible by 3."
          }
        ]
      },
      // 13. Example 8
      {
        id: 13,
        title: "Question 13",
        category: "NCERT Example 8",
        partsInfo: "2 Steps Required",
        context: "Find the 11th term from the last term of the AP: \\( 10, 7, 4, \\dots, -62 \\).",
        steps: [
          {
            title: "Step 1: Reverse Parameters",
            prompt: "Reversing gives first term \\( a' = -62 \\) and \\( d' = \\) <input class='step-input' style='width:50px;' data-ans='3'>",
            explanation: "In reverse, common difference becomes +3."
          },
          {
            title: "Step 2: Calculate 11th Term",
            prompt: "\\( a_{11}' = -62 + (11 - 1)3 = -62 + 30 = \\) <input class='step-input' style='width:50px;' data-ans='-32'>",
            explanation: "The 11th term from the last is -32."
          }
        ]
      },
      // 14. Example 9
      {
        id: 14,
        title: "Question 14",
        category: "NCERT Example 9",
        partsInfo: "2 Steps Required",
        context: "A sum of ₹1000 is invested at 8% simple interest per year. Find the interest at the end of 30 years.",
        steps: [
          {
            title: "Step 1: Annual Interest",
            prompt: "Annual interest = \\( \\frac{1000 \\times 8 \\times 1}{100} = ₹\\) <input class='step-input' style='width:50px;' data-ans='80'>",
            explanation: "Annual interest is ₹80, forming an AP with a = 80 and d = 80."
          },
          {
            title: "Step 2: Interest at 30 Years",
            prompt: "\\( I_{30} = 80 + 29(80) = 30 \\times 80 = ₹\\) <input class='step-input' style='width:60px;' data-ans='2400'>",
            explanation: "Interest at 30 years is ₹2400."
          }
        ]
      },
      // 15. Example 10
      {
        id: 15,
        title: "Question 15",
        category: "NCERT Example 10",
        partsInfo: "2 Steps Required",
        context: "A flower bed has 23 rose plants in row 1, 21 in row 2, 19 in row 3, and 5 in the last row. How many rows are there?",
        steps: [
          {
            title: "Step 1: Set up nth Term Formula",
            prompt: "\\( 5 = 23 + (n - 1)(-2) \\implies -18 = -2(n - 1) \\implies n - 1 = \\) <input class='step-input' style='width:50px;' data-ans='9'>",
            explanation: "n - 1 = 9."
          },
          {
            title: "Step 2: Number of Rows",
            prompt: "Total rows \\( n = \\) <input class='step-input' style='width:50px;' data-ans='10'>",
            explanation: "There are 10 rows in the flower bed."
          }
        ]
      },
      // 16. Ex 5.2 Q2(i)
      {
        id: 16,
        title: "Question 16",
        category: "Exercise 5.2, Q2(i)",
        partsInfo: "2 Steps Required",
        context: "Find the 30th term of the AP: \\( 10, 7, 4, \\dots \\)",
        steps: [
          {
            title: "Step 1: Parameters",
            prompt: "\\( a = 10, d = 7 - 10 = \\) <input class='step-input' style='width:50px;' data-ans='-3'>",
            explanation: "d = -3."
          },
          {
            title: "Step 2: 30th Term",
            prompt: "\\( a_{30} = 10 + 29(-3) = 10 - 87 = \\) <input class='step-input' style='width:50px;' data-ans='-77'>",
            explanation: "a30 = -77 (Option C)."
          }
        ]
      },
      // 17. Ex 5.2 Q2(ii)
      {
        id: 17,
        title: "Question 17",
        category: "Exercise 5.2, Q2(ii)",
        partsInfo: "2 Steps Required",
        context: "Find the 11th term of the AP: \\( -3, -\\frac{1}{2}, 2, \\dots \\)",
        steps: [
          {
            title: "Step 1: Find Common Difference d",
            prompt: "\\( d = -\\frac{1}{2} - (-3) = -\\frac{1}{2} + 3 = \\) <input class='step-input' style='width:70px;' data-ans='5/2' data-alt='2.5'>",
            explanation: "d = 5/2 = 2.5."
          },
          {
            title: "Step 2: Compute a_11",
            prompt: "\\( a_{11} = -3 + 10\\left(\\frac{5}{2}\\right) = -3 + 25 = \\) <input class='step-input' style='width:50px;' data-ans='22'>",
            explanation: "a11 = 22 (Option B)."
          }
        ]
      },
      // 18. Ex 5.2 Q3(ii)
      {
        id: 18,
        title: "Question 18",
        category: "Exercise 5.2, Q3(ii)",
        partsInfo: "2 Steps Required",
        context: "In the AP: \\( \\square, 13, \\square, 3 \\), find the missing terms.",
        steps: [
          {
            title: "Step 1: Find Common Difference d",
            prompt: "\\( a_4 - a_2 = 2d = 3 - 13 = -10 \\implies d = \\) <input class='step-input' style='width:50px;' data-ans='-5'>",
            explanation: "d = -5."
          },
          {
            title: "Step 2: Find First and Third Terms",
            prompt: "First term = <input class='step-input' style='width:50px;' data-ans='18'>, Third term = <input class='step-input' style='width:50px;' data-ans='8'>",
            explanation: "Terms are 18, 13, 8, 3."
          }
        ]
      },
      // 19. Ex 5.2 Q4
      {
        id: 19,
        title: "Question 19",
        category: "Exercise 5.2, Q4",
        partsInfo: "2 Steps Required",
        context: "Which term of the AP: \\( 3, 8, 13, 18, \\dots \\) is 78?",
        steps: [
          {
            title: "Step 1: Set up Formula",
            prompt: "\\( a = 3, d = 5 \\). \\( 78 = 3 + (n - 1)5 \\implies 75 = 5(n - 1) \\implies n - 1 = \\) <input class='step-input' style='width:50px;' data-ans='15'>",
            explanation: "n - 1 = 15."
          },
          {
            title: "Step 2: Value of n",
            prompt: "\\( n = \\) <input class='step-input' style='width:50px;' data-ans='16'>",
            explanation: "The 16th term is 78."
          }
        ]
      },
      // 20. Ex 5.2 Q7
      {
        id: 20,
        title: "Question 20",
        category: "Exercise 5.2, Q7",
        partsInfo: "2 Steps Required",
        context: "Find the 31st term of an AP whose 11th term is 38 and 16th term is 73.",
        steps: [
          {
            title: "Step 1: Find a and d",
            prompt: "\\( 5d = 73 - 38 = 35 \\implies d = 7 \\). Then \\( a = 38 - 70 = \\) <input class='step-input' style='width:50px;' data-ans='-32'>",
            explanation: "a = -32 and d = 7."
          },
          {
            title: "Step 2: 31st Term",
            prompt: "\\( a_{31} = -32 + 30(7) = -32 + 210 = \\) <input class='step-input' style='width:60px;' data-ans='178'>",
            explanation: "a31 = 178."
          }
        ]
      },
      // 21. Ex 5.2 Q8
      {
        id: 21,
        title: "Question 21",
        category: "Exercise 5.2, Q8",
        partsInfo: "2 Steps Required",
        context: "An AP consists of 50 terms of which 3rd term is 12 and the last term is 106. Find the 29th term.",
        steps: [
          {
            title: "Step 1: Solve for d",
            prompt: "\\( a_{50} - a_3 = 47d = 106 - 12 = 94 \\implies d = \\) <input class='step-input' style='width:50px;' data-ans='2'>",
            explanation: "d = 2, and a = 12 - 4 = 8."
          },
          {
            title: "Step 2: Compute a_29",
            prompt: "\\( a_{29} = 8 + 28(2) = 8 + 56 = \\) <input class='step-input' style='width:60px;' data-ans='64'>",
            explanation: "a29 = 64."
          }
        ]
      },
      // 22. Ex 5.2 Q10
      {
        id: 22,
        title: "Question 22",
        category: "Exercise 5.2, Q10",
        partsInfo: "2 Steps Required",
        context: "The 17th term of an AP exceeds its 10th term by 7. Find the common difference.",
        steps: [
          {
            title: "Step 1: Set up Difference",
            prompt: "\\( a_{17} - a_{10} = 7d = \\) <input class='step-input' style='width:50px;' data-ans='7'>",
            explanation: "7d = 7."
          },
          {
            title: "Step 2: Solve for d",
            prompt: "\\( d = \\) <input class='step-input' style='width:50px;' data-ans='1'>",
            explanation: "d = 1."
          }
        ]
      },
      // 23. Ex 5.2 Q11
      {
        id: 23,
        title: "Question 23",
        category: "Exercise 5.2, Q11",
        partsInfo: "2 Steps Required",
        context: "Which term of the AP: \\( 3, 15, 27, 39, \\dots \\) will be 132 more than its 54th term?",
        steps: [
          {
            title: "Step 1: Express Difference in terms of d",
            prompt: "\\( d = 12 \\). \\( a_n - a_{54} = (n - 54)d = 132 \\implies n - 54 = \\frac{132}{12} = \\) <input class='step-input' style='width:50px;' data-ans='11'>",
            explanation: "n - 54 = 11."
          },
          {
            title: "Step 2: Solve for n",
            prompt: "\\( n = 54 + 11 = \\) <input class='step-input' style='width:50px;' data-ans='65'>",
            explanation: "The 65th term is 132 more than the 54th term."
          }
        ]
      },
      // 24. Ex 5.2 Q13
      {
        id: 24,
        title: "Question 24",
        category: "Exercise 5.2, Q13",
        partsInfo: "2 Steps Required",
        context: "How many three-digit numbers are divisible by 7?",
        steps: [
          {
            title: "Step 1: Extremes",
            prompt: "First is 105, last is 994. \\( 994 = 105 + (n - 1)7 \\implies n - 1 = \\) <input class='step-input' style='width:60px;' data-ans='127'>",
            explanation: "n - 1 = 127."
          },
          {
            title: "Step 2: Total Three-Digit Numbers",
            prompt: "\\( n = \\) <input class='step-input' style='width:60px;' data-ans='128'>",
            explanation: "There are 128 three-digit numbers divisible by 7."
          }
        ]
      },
      // 25. Ex 5.2 Q14
      {
        id: 25,
        title: "Question 25",
        category: "Exercise 5.2, Q14",
        partsInfo: "2 Steps Required",
        context: "How many multiples of 4 lie between 10 and 250?",
        steps: [
          {
            title: "Step 1: First and Last Multiples",
            prompt: "First multiple > 10 is 12. Last multiple < 250 is: <input class='step-input' style='width:60px;' data-ans='248'>",
            explanation: "The AP is 12, 16, ..., 248 with d = 4."
          },
          {
            title: "Step 2: Count of Multiples",
            prompt: "\\( 248 = 12 + (n - 1)4 \\implies 236 = 4(n - 1) \\implies n = \\) <input class='step-input' style='width:50px;' data-ans='60'>",
            explanation: "n = 59 + 1 = 60."
          }
        ]
      },
      // 26. Ex 5.2 Q17
      {
        id: 26,
        title: "Question 26",
        category: "Exercise 5.2, Q17",
        partsInfo: "2 Steps Required",
        context: "Find the 20th term from the last term of the AP: \\( 3, 8, 13, \\dots, 253 \\).",
        steps: [
          {
            title: "Step 1: Reverse Parameters",
            prompt: "Reversed: \\( a' = 253, d' = \\) <input class='step-input' style='width:50px;' data-ans='-5'>",
            explanation: "d' = -5."
          },
          {
            title: "Step 2: 20th Term from End",
            prompt: "\\( a_{20}' = 253 + 19(-5) = 253 - 95 = \\) <input class='step-input' style='width:60px;' data-ans='158'>",
            explanation: "20th term from the end is 158."
          }
        ]
      },
      // 27. Ex 5.2 Q19
      {
        id: 27,
        title: "Question 27",
        category: "Exercise 5.2, Q19",
        partsInfo: "2 Steps Required",
        context: "Subba Rao's starting salary in 1995 was ₹5000 with annual increment ₹200. In which year did his income reach ₹7000?",
        steps: [
          {
            title: "Step 1: Solve for Years n",
            prompt: "\\( 7000 = 5000 + (n - 1)200 \\implies 2000 = 200(n - 1) \\implies n = \\) <input class='step-input' style='width:50px;' data-ans='11'>",
            explanation: "n = 11 years."
          },
          {
            title: "Step 2: Target Year",
            prompt: "Calendar year = \\( 1995 + 10 = \\) <input class='step-input' style='width:60px;' data-ans='2005'>",
            explanation: "The year 2005."
          }
        ]
      },
      // 28. Example 11
      {
        id: 28,
        title: "Question 28",
        category: "NCERT Example 11",
        partsInfo: "2 Steps Required",
        context: "Find the sum of the first 22 terms of the AP: \\( 8, 3, -2, \\dots \\)",
        steps: [
          {
            title: "Step 1: Inner Sum Terms",
            prompt: "\\( 2a + (n - 1)d = 2(8) + 21(-5) = 16 - 105 = \\) <input class='step-input' style='width:60px;' data-ans='-89'>",
            explanation: "16 - 105 = -89."
          },
          {
            title: "Step 2: Total Sum S_22",
            prompt: "\\( S_{22} = 11(-89) = \\) <input class='step-input' style='width:60px;' data-ans='-979'>",
            explanation: "S22 = -979."
          }
        ]
      },
      // 29. Example 12
      {
        id: 29,
        title: "Question 29",
        category: "NCERT Example 12",
        partsInfo: "2 Steps Required",
        context: "If the sum of first 14 terms is 1050 and first term is 10, find the 20th term.",
        steps: [
          {
            title: "Step 1: Solve for d",
            prompt: "\\( 1050 = 7[20 + 13d] \\implies 150 = 20 + 13d \\implies d = \\) <input class='step-input' style='width:50px;' data-ans='10'>",
            explanation: "d = 10."
          },
          {
            title: "Step 2: 20th Term",
            prompt: "\\( a_{20} = 10 + 19(10) = \\) <input class='step-input' style='width:60px;' data-ans='200'>",
            explanation: "a20 = 200."
          }
        ]
      },
      // 30. Example 13
      {
        id: 30,
        title: "Question 30",
        category: "NCERT Example 13",
        partsInfo: "2 Steps Required",
        context: "How many terms of \\( 24, 21, 18, \\dots \\) must be taken so that their sum is 78?",
        steps: [
          {
            title: "Step 1: Quadratic Equation in n",
            prompt: "\\( 78 = \\frac{n}{2}[48 + (n - 1)(-3)] \\implies n^2 - 17n + 52 = 0 \\). Factorise: \\( (n - 4)(n - 13) = 0 \\).",
            explanation: "n = 4 or 13."
          },
          {
            title: "Step 2: Admissible Values",
            prompt: "The two valid values of \\( n \\) are: <input class='step-input' style='width:80px;' data-ans='4, 13' data-alt='4,13|13, 4'>",
            explanation: "Both n = 4 and n = 13 are valid."
          }
        ]
      },
      // 31. Example 16
      {
        id: 31,
        title: "Question 31",
        category: "NCERT Example 16",
        partsInfo: "3 Steps Required",
        context: "TV sets manufacturer: 600 sets in 3rd year, 700 in 7th year. Production increases uniformly each year.",
        steps: [
          {
            title: "Step 1: First Year Production",
            prompt: "\\( a + 2d = 600, a + 6d = 700 \\implies d = 25 \\). Production in 1st year \\( a = \\) <input class='step-input' style='width:60px;' data-ans='550'>",
            explanation: "a = 550 sets."
          },
          {
            title: "Step 2: 10th Year Production",
            prompt: "\\( a_{10} = 550 + 9(25) = \\) <input class='step-input' style='width:60px;' data-ans='775'>",
            explanation: "a10 = 775 sets."
          },
          {
            title: "Step 3: Total Production in First 7 Years",
            prompt: "\\( S_7 = \\frac{7}{2}[1100 + 150] = \\) <input class='step-input' style='width:60px;' data-ans='4375'>",
            explanation: "S7 = 4375 sets."
          }
        ]
      },
      // 32. Ex 5.3 Q1(i)
      {
        id: 32,
        title: "Question 32",
        category: "Exercise 5.3, Q1(i)",
        partsInfo: "2 Steps Required",
        context: "Find the sum of the AP: \\( 2, 7, 12, \\dots \\) to 10 terms.",
        steps: [
          {
            title: "Step 1: Parameters",
            prompt: "\\( a = 2, d = 5, n = 10 \\). Bracket value \\( 2a + 9d = 4 + 45 = \\) <input class='step-input' style='width:50px;' data-ans='49'>",
            explanation: "2(2) + 9(5) = 49."
          },
          {
            title: "Step 2: Sum S_10",
            prompt: "\\( S_{10} = 5 \\times 49 = \\) <input class='step-input' style='width:60px;' data-ans='245'>",
            explanation: "S10 = 245."
          }
        ]
      },
      // 33. Ex 5.3 Q4
      {
        id: 33,
        title: "Question 33",
        category: "Exercise 5.3, Q4",
        partsInfo: "2 Steps Required",
        context: "How many terms of the AP: \\( 9, 17, 25, \\dots \\) must be taken to give a sum of 636?",
        steps: [
          {
            title: "Step 1: Quadratic Equation",
            prompt: "\\( 4n^2 + 5n - 636 = 0 \\implies (4n + 53)(n - 12) = 0 \\).",
            explanation: "Roots are -53/4 and 12."
          },
          {
            title: "Step 2: Number of Terms",
            prompt: "\\( n = \\) <input class='step-input' style='width:50px;' data-ans='12'>",
            explanation: "n = 12."
          }
        ]
      },
      // 34. Ex 5.3 Q9
      {
        id: 34,
        title: "Question 34",
        category: "Exercise 5.3, Q9",
        partsInfo: "2 Steps Required",
        context: "If the sum of first 7 terms is 49 and that of 17 terms is 289, find the sum of first \\( n \\) terms.",
        steps: [
          {
            title: "Step 1: Solve for a and d",
            prompt: "\\( a + 3d = 7 \\) and \\( a + 8d = 17 \\implies d = 2, a = \\) <input class='step-input' style='width:50px;' data-ans='1'>",
            explanation: "a = 1 and d = 2."
          },
          {
            title: "Step 2: Sum of First n Terms",
            prompt: "\\( S_n = \\frac{n}{2}[2(1) + (n - 1)2] = \\) <input class='step-input' style='width:60px;' data-ans='n^2'>",
            explanation: "Sn = n^2."
          }
        ]
      },
      // 35. Ex 5.3 Q12
      {
        id: 35,
        title: "Question 35",
        category: "Exercise 5.3, Q12",
        partsInfo: "2 Steps Required",
        context: "Find the sum of the first 40 positive integers divisible by 6.",
        steps: [
          {
            title: "Step 1: Sequence Values",
            prompt: "The integers are \\( 6, 12, 18, \\dots \\) where \\( a = 6, d = 6, n = 40 \\). The 40th integer \\( l = \\) <input class='step-input' style='width:60px;' data-ans='240'>",
            explanation: "l = 40 * 6 = 240."
          },
          {
            title: "Step 2: Compute Sum S_40",
            prompt: "\\( S_{40} = \\frac{40}{2}(6 + 240) = 20 \\times 246 = \\) <input class='step-input' style='width:70px;' data-ans='4920'>",
            explanation: "S40 = 4920."
          }
        ]
      },
      // 36. Ex 5.3 Q15
      {
        id: 36,
        title: "Question 36",
        category: "Exercise 5.3, Q15",
        partsInfo: "2 Steps Required",
        context: "Construction penalty: ₹200 on day 1, ₹250 on day 2, ₹300 on day 3, increasing by ₹50 each day. Find penalty for 30 days of delay.",
        steps: [
          {
            title: "Step 1: Parameters",
            prompt: "\\( a = 200, d = 50, n = 30 \\). Sum formula brackets: \\( 2(200) + 29(50) = \\) <input class='step-input' style='width:60px;' data-ans='1850'>",
            explanation: "2a + 29d = 1850."
          },
          {
            title: "Step 2: Total Penalty Paid",
            prompt: "Penalty = \\( 15 \\times 1850 = ₹\\) <input class='step-input' style='width:70px;' data-ans='27750'>",
            explanation: "Total penalty is ₹27,750."
          }
        ]
      },
      // 37. Ex 5.3 Q18
      {
        id: 37,
        title: "Question 37",
        category: "Exercise 5.3, Q18",
        partsInfo: "2 Steps Required",
        context: "A spiral is made of 13 consecutive semicircles with radii 0.5 cm, 1.0 cm, 1.5 cm, ... Find total length. (Take \\( \\pi = \\frac{22}{7} \\))",
        diagramSVG: SVG_SPIRAL,
        steps: [
          {
            title: "Step 1: AP of Semicircle Lengths",
            prompt: "Lengths are \\( 0.5\\pi, 1.0\\pi, \\dots \\) with \\( a = 0.5\\pi, d = 0.5\\pi, n = 13 \\). Sum = \\( \\frac{13}{2}(7\\pi) \\). Compute \\( 7\\pi \\): <input class='step-input' style='width:50px;' data-ans='22'>",
            explanation: "7 * (22/7) = 22."
          },
          {
            title: "Step 2: Total Spiral Length",
            prompt: "Total length = \\( \\frac{13}{2} \\times 22 = \\) <input class='step-input' style='width:60px;' data-ans='143'> cm",
            explanation: "Total length is 143 cm."
          }
        ]
      },
      // 38. Ex 5.3 Q19
      {
        id: 38,
        title: "Question 38",
        category: "Exercise 5.3, Q19",
        partsInfo: "3 Steps Required",
        context: "200 logs are stacked: 20 in bottom row, 19 in next, 18 in next, etc. In how many rows are they placed and how many logs in top row?",
        diagramSVG: SVG_LOGS,
        steps: [
          {
            title: "Step 1: Solve for Rows n",
            prompt: "\\( 200 = \\frac{n}{2}[40 + (n - 1)(-1)] \\implies n^2 - 41n + 400 = 0 \\implies (n - 16)(n - 25) = 0 \\).",
            explanation: "n = 16 or 25."
          },
          {
            title: "Step 2: Reject Invalid Solution",
            prompt: "If \\( n = 25 \\), logs in top row would be negative (-4). Valid number of rows = <input class='step-input' style='width:50px;' data-ans='16'>",
            explanation: "Number of rows is 16."
          },
          {
            title: "Step 3: Logs in Top Row",
            prompt: "\\( a_{16} = 20 + 15(-1) = \\) <input class='step-input' style='width:50px;' data-ans='5'> logs",
            explanation: "There are 5 logs in the top row."
          }
        ]
      },
      // 39. Ex 5.3 Q20
      {
        id: 39,
        title: "Question 39",
        category: "Exercise 5.3, Q20",
        partsInfo: "2 Steps Required",
        context: "Potato race: bucket is 5 m from 1st potato, next 9 are 3 m apart in a line. Competitor runs back and forth for all 10 potatoes. Find total distance run.",
        diagramSVG: SVG_POTATO,
        steps: [
          {
            title: "Step 1: Sequence of Distances Run",
            prompt: "Distances run are 10 m, 16 m, 22 m... Common difference \\( d = \\) <input class='step-input' style='width:50px;' data-ans='6'> m",
            explanation: "a = 10 and d = 6."
          },
          {
            title: "Step 2: Total Distance for 10 Potatoes",
            prompt: "\\( S_{10} = 5[2(10) + 9(6)] = 5[74] = \\) <input class='step-input' style='width:60px;' data-ans='370'> m",
            explanation: "Total distance run is 370 m."
          }
        ]
      },
      // 40. Ex 5.4 Q3
      {
        id: 40,
        title: "Question 40",
        category: "Exercise 5.4, Q3 (Optional)",
        partsInfo: "3 Steps Required",
        context: "A ladder has rungs 25 cm apart decreasing uniformly from 45 cm at bottom to 25 cm at top. Distance between top and bottom rungs is \\( 2\\frac{1}{2} \\) m. Find total wood length.",
        diagramSVG: SVG_LADDER,
        steps: [
          {
            title: "Step 1: Number of Rungs",
            prompt: "\\( 2\\frac{1}{2} \\text{ m} = 250 \\text{ cm} \\). Number of rungs = \\( \\frac{250}{25} + 1 = \\) <input class='step-input' style='width:50px;' data-ans='11'>",
            explanation: "Total rungs n = 11."
          },
          {
            title: "Step 2: Use First and Last Terms",
            prompt: "\\( a = 45 \\text{ cm}, l = 25 \\text{ cm} \\). Average length = \\( \\frac{45 + 25}{2} = \\) <input class='step-input' style='width:50px;' data-ans='35'> cm",
            explanation: "(a + l)/2 = 35."
          },
          {
            title: "Step 3: Total Wood Required",
            prompt: "\\( S_{11} = 11 \\times 35 = \\) <input class='step-input' style='width:60px;' data-ans='385'> cm",
            explanation: "Total length of wood required is 385 cm."
          }
        ]
      }
    ];

    /* ==========================================================================
       STOPWATCH ENGINE WITH 20-MIN & 5-MIN AUDIO REMINDERS
       ========================================================================== */
    let timerSeconds = 0;
    let timerInterval = null;
    let timerRunning = false;

    function formatTime(totalSecs) {
      const mins = Math.floor(totalSecs / 60);
      const secs = totalSecs % 60;
      return `${mins.toString().padStart(2, '0')}:${secs.toString().padStart(2, '0')}`;
    }

    function checkTimerSoundMilestones(secs) {
      if (secs === 1200) {
        playReminderChime();
        showToast("⏰ Milestone Alert: 20 minutes elapsed! Maintain focus and pace.");
      } else if (secs > 1200 && (secs - 1200) % 300 === 0) {
        playReminderChime();
        const mins = Math.floor(secs / 60);
        showToast(`⏰ Pace Alert: ${mins} minutes elapsed.`);
      }
    }

    function showToast(msg) {
      const toast = document.getElementById('reminderToast');
      if (toast) {
        toast.textContent = msg;
        toast.style.display = 'block';
        setTimeout(() => { toast.style.display = 'none'; }, 6000);
      }
    }

    function startTimer() {
      if (!timerRunning) {
        timerRunning = true;
        document.getElementById('timerToggleBtn').textContent = 'Pause';
        timerInterval = setInterval(() => {
          timerSeconds++;
          document.getElementById('timerDisplay').textContent = formatTime(timerSeconds);
          checkTimerSoundMilestones(timerSeconds);
        }, 1000);
      }
    }

    function pauseTimer() {
      timerRunning = false;
      document.getElementById('timerToggleBtn').textContent = 'Resume';
      clearInterval(timerInterval);
    }

    function toggleTimer() {
      if (timerRunning) pauseTimer();
      else startTimer();
    }

    function resetTimer() {
      pauseTimer();
      timerSeconds = 0;
      document.getElementById('timerDisplay').textContent = '00:00';
      document.getElementById('timerToggleBtn').textContent = 'Start';
    }

    /* ==========================================================================
       SYNTHESIZER AUDIO ENGINE
       ========================================================================== */
    let soundEnabled = true;
    let audioCtx = null;

    function getAudioContext() {
      if (!audioCtx) {
        const AudioClass = window.AudioContext || window.webkitAudioContext;
        if (AudioClass) audioCtx = new AudioClass();
      }
      if (audioCtx && audioCtx.state === 'suspended') {
        audioCtx.resume().catch(() => {});
      }
      return audioCtx;
    }

    function playSound(type) {
      if (!soundEnabled) return;
      try {
        const ctx = getAudioContext();
        if (!ctx) return;
        const now = ctx.currentTime;
        if (type === 'correct') {
          const osc = ctx.createOscillator();
          const gain = ctx.createGain();
          osc.type = 'sine';
          osc.frequency.setValueAtTime(659.25, now);
          osc.frequency.exponentialRampToValueAtTime(880, now + 0.15);
          gain.gain.setValueAtTime(0.15, now);
          gain.gain.linearRampToValueAtTime(0.001, now + 0.25);
          osc.connect(gain);
          gain.connect(ctx.destination);
          osc.start(now);
          osc.stop(now + 0.26);
        } else if (type === 'incorrect') {
          const osc = ctx.createOscillator();
          const gain = ctx.createGain();
          osc.type = 'triangle';
          osc.frequency.setValueAtTime(196, now);
          osc.frequency.exponentialRampToValueAtTime(146, now + 0.18);
          gain.gain.setValueAtTime(0.15, now);
          gain.gain.linearRampToValueAtTime(0.001, now + 0.22);
          osc.connect(gain);
          gain.connect(ctx.destination);
          osc.start(now);
          osc.stop(now + 0.24);
        }
      } catch(e) {}
    }

    function playReminderChime() {
      if (!soundEnabled) return;
      try {
        const ctx = getAudioContext();
        if (!ctx) return;
        const now = ctx.currentTime;
        const chimeNotes = [523.25, 659.25, 783.99, 1046.50];
        chimeNotes.forEach((freq, idx) => {
          const osc = ctx.createOscillator();
          const gain = ctx.createGain();
          osc.type = 'sine';
          osc.frequency.setValueAtTime(freq, now + idx * 0.14);
          gain.gain.setValueAtTime(0.001, now + idx * 0.14);
          gain.gain.linearRampToValueAtTime(0.22, now + idx * 0.14 + 0.03);
          gain.gain.exponentialRampToValueAtTime(0.0001, now + idx * 0.14 + 0.65);
          osc.connect(gain);
          gain.connect(ctx.destination);
          osc.start(now + idx * 0.14);
          osc.stop(now + idx * 0.14 + 0.7);
        });
      } catch(e) {}
    }

    /* ==========================================================================
       IN-MEMORY STATE MANAGEMENT
       ========================================================================== */
    let state = {
      currentProblemIdx: 0,
      problems: {}
    };

    function getProblemState(idx) {
      if (!state.problems[idx]) {
        state.problems[idx] = { completedSteps: [], inputs: {}, isSolved: false, isSkipped: false };
      }
      return state.problems[idx];
    }

    function cleanString(s) {
      return (s || "").toString().trim().toLowerCase().replace(/\s+/g, '').replace(/−/g, '-');
    }

    function testInputMatching(userStr, targetStr, altStr) {
      const u = cleanString(userStr);
      const t = cleanString(targetStr);
      if (!u) return false;
      if (u === t) return true;
      if (altStr) {
        const alts = altStr.split('|').map(cleanString);
        if (alts.includes(u)) return true;
      }
      const numU = parseFloat(u);
      const numT = parseFloat(t);
      if (!isNaN(numU) && !isNaN(numT)) {
        return Math.abs(numU - numT) < 0.02;
      }
      return false;
    }

    function triggerMathTypeset() {
      if (window.MathJax && typeof window.MathJax.typesetPromise === 'function') {
        window.MathJax.typesetPromise().catch(() => {});
      }
    }

    let activeInputElement = null;
    window.trackActiveField = function(el) { activeInputElement = el; };
    window.insertSymbol = function(sym) {
      if (!activeInputElement) return;
      const start = activeInputElement.selectionStart || 0;
      const end = activeInputElement.selectionEnd || 0;
      const val = activeInputElement.value;
      activeInputElement.value = val.substring(0, start) + sym + val.substring(end);
      activeInputElement.focus();
      activeInputElement.dispatchEvent(new Event('input', { bubbles: true }));
    };
    window.clearActiveField = function() {
      if (!activeInputElement) return;
      activeInputElement.value = '';
      activeInputElement.dispatchEvent(new Event('input', { bubbles: true }));
      activeInputElement.focus();
    };

    window.switchToolTab = function(tab) {
      document.getElementById('tabPadBtn').classList.toggle('active', tab === 'pad');
      document.getElementById('tabCalcBtn').classList.toggle('active', tab === 'calc');
      document.getElementById('mathPadView').style.display = tab === 'pad' ? 'grid' : 'none';
      document.getElementById('calcView').style.display = tab === 'calc' ? 'block' : 'none';
    };

    let calcExpression = "";
    window.calcAppend = function(val) { calcExpression += val; document.getElementById('calcScreen').textContent = calcExpression || "0"; };
    window.calcClear = function() { calcExpression = ""; document.getElementById('calcScreen').textContent = "0"; };
    window.calcSqrt = function() {
      try { calcExpression = String(Math.sqrt(eval(calcExpression || "0"))); document.getElementById('calcScreen').textContent = calcExpression; } catch(e) {}
    };
    window.calcEval = function() {
      try { calcExpression = String(eval(calcExpression || "0")); document.getElementById('calcScreen').textContent = calcExpression; } catch(e) {}
    };

    function switchMainTab(tabId) {
      document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
      const targetBtn = Array.from(document.querySelectorAll('.tab-btn')).find(b => b.getAttribute('onclick') && b.getAttribute('onclick').includes(tabId));
      if (targetBtn) targetBtn.classList.add('active');

      document.querySelectorAll('.view-section').forEach(sec => sec.classList.remove('active'));
      const targetSec = document.getElementById(`${tabId}View`);
      if (targetSec) targetSec.classList.add('active');
      window.scrollTo({ top: 0, behavior: 'smooth' });

      if (tabId === 'sheet') {
        renderProblem(state.currentProblemIdx);
      }
      if (tabId === 'solutions') renderSolutions();
      triggerMathTypeset();
    }

    function renderProblem(idx) {
      if (idx < 0 || idx >= PROBLEMS_DATA.length) return;
      state.currentProblemIdx = idx;
      const prob = PROBLEMS_DATA[idx];
      const pState = getProblemState(idx);

      document.getElementById('pNumberDisplay').textContent = prob.title;
      document.getElementById('pCategoryBadge').textContent = prob.category;
      document.getElementById('pPartsBadge').textContent = prob.partsInfo;
      document.getElementById('pContextDisplay').innerHTML = prob.context;

      const diagramBox = document.getElementById('diagramDisplayContainer');
      if (prob.diagramSVG) {
        diagramBox.style.display = 'flex';
        diagramBox.innerHTML = prob.diagramSVG;
      } else {
        diagramBox.style.display = 'none';
        diagramBox.innerHTML = '';
      }

      const badge = document.getElementById('pStatusBadge');
      if (pState.isSolved) { badge.className = 'status-badge badge-complete'; badge.textContent = 'Completed'; }
      else if (pState.isSkipped) { badge.className = 'status-badge badge-skipped'; badge.textContent = 'Skipped'; }
      else if (pState.completedSteps.length > 0) { badge.className = 'status-badge badge-progress'; badge.textContent = 'In Progress'; }
      else { badge.className = 'status-badge badge-unvisited'; badge.textContent = 'Unvisited'; }

      const container = document.getElementById('stepsListContainer');
      container.innerHTML = '';

      const maxStep = pState.isSolved ? prob.steps.length - 1 : Math.min(pState.completedSteps.length, prob.steps.length - 1);

      for (let sIdx = 0; sIdx <= maxStep; sIdx++) {
        const step = prob.steps[sIdx];
        const isDone = pState.completedSteps.includes(sIdx);

        const card = document.createElement('div');
        card.className = `step-card ${isDone ? 'completed' : 'active'}`;
        card.innerHTML = `
          <div class="step-header-bar">
            <div class="step-title-text">${step.title}</div>
            <span class="step-status-indicator">${isDone ? '✓ Verified' : 'Current Step'}</span>
          </div>
          <div class="step-prompt">${step.prompt}</div>
          <div class="step-controls">
            <div></div>
            <div style="display:flex; align-items:center; gap:8px;">
              <span class="step-feedback-msg" id="step-msg-${idx}-${sIdx}"></span>
              ${!isDone ? `
                <button class="btn btn-step-check" onclick="verifyStepAnswers(${idx}, ${sIdx})">
                  ${sIdx === prob.steps.length - 1 ? 'Verify & Finish Problem ✓' : 'Verify & Continue →'}
                </button>
              ` : '<span style="color:var(--correct-green); font-weight:700;">✓ Correct</span>'}
            </div>
          </div>
        `;
        container.appendChild(card);

        card.querySelectorAll('.step-input').forEach((inp, iIdx) => {
          const inputKey = `p${idx}_s${sIdx}_i${iIdx}`;
          inp.setAttribute('data-key', inputKey);
          inp.setAttribute('onfocus', 'trackActiveField(this)');
          if (pState.inputs[inputKey] !== undefined) inp.value = pState.inputs[inputKey];

          if (isDone) {
            inp.disabled = true;
            inp.classList.add('input-correct');
          } else {
            inp.addEventListener('input', (e) => { pState.inputs[inputKey] = e.target.value; });
            inp.addEventListener('keypress', (e) => { if (e.key === 'Enter') verifyStepAnswers(idx, sIdx); });
          }
        });
      }

      document.getElementById('prevProblemBtn').disabled = idx === 0;
      document.getElementById('nextProblemBtn').disabled = idx === PROBLEMS_DATA.length - 1;
      renderPalette();
      triggerMathTypeset();
    }

    window.verifyStepAnswers = function(pIdx, sIdx) {
      const prob = PROBLEMS_DATA[pIdx];
      const pState = getProblemState(pIdx);
      const card = document.querySelectorAll('.step-card')[sIdx];
      if (!card) return;

      const inputs = card.querySelectorAll('.step-input');
      let ok = true;

      inputs.forEach(inp => {
        const ans = inp.getAttribute('data-ans') || '';
        const alt = inp.getAttribute('data-alt') || '';
        const inputKey = inp.getAttribute('data-key');
        pState.inputs[inputKey] = inp.value;

        if (testInputMatching(inp.value, ans, alt)) {
          inp.classList.remove('input-incorrect');
          inp.classList.add('input-correct');
        } else {
          inp.classList.remove('input-correct');
          inp.classList.add('input-incorrect');
          ok = false;
        }
      });

      const msg = document.getElementById(`step-msg-${pIdx}-${sIdx}`);
      if (ok) {
        playSound('correct');
        if (!pState.completedSteps.includes(sIdx)) pState.completedSteps.push(sIdx);
        pState.isSkipped = false;
        if (msg) {
          msg.className = "step-feedback-msg correct";
          msg.textContent = "✓ Correct!";
        }
        if (pState.completedSteps.length === prob.steps.length) {
          pState.isSolved = true;
          setTimeout(() => renderProblem(pIdx), 350);
        } else {
          setTimeout(() => renderProblem(pIdx), 300);
        }
      } else {
        playSound('incorrect');
        if (msg) {
          msg.className = "step-feedback-msg incorrect";
          msg.textContent = "✗ Check calculation and try again.";
        }
      }
    };

    function renderPalette() {
      const grid = document.getElementById('paletteGridContainer');
      grid.innerHTML = '';
      let solvedCount = 0;

      PROBLEMS_DATA.forEach((p, idx) => {
        const btn = document.createElement('button');
        btn.className = 'palette-btn';
        btn.textContent = p.id;
        const ps = state.problems[idx];
        if (ps) {
          if (ps.isSolved) { btn.classList.add('completed'); solvedCount++; }
          else if (ps.isSkipped) btn.classList.add('skipped');
          else if (ps.completedSteps.length > 0) btn.classList.add('progress');
        }
        if (idx === state.currentProblemIdx) btn.classList.add('active');
        btn.onclick = () => renderProblem(idx);
        grid.appendChild(btn);
      });
      document.getElementById('completionRateText').textContent = `${solvedCount}/${PROBLEMS_DATA.length} Solved`;
    }

    document.getElementById('prevProblemBtn').onclick = () => { if (state.currentProblemIdx > 0) renderProblem(state.currentProblemIdx - 1); };
    document.getElementById('nextProblemBtn').onclick = () => { if (state.currentProblemIdx < PROBLEMS_DATA.length - 1) renderProblem(state.currentProblemIdx + 1); };
    document.getElementById('skipProblemBtn').onclick = () => {
      const ps = getProblemState(state.currentProblemIdx);
      ps.isSkipped = true;
      if (state.currentProblemIdx < PROBLEMS_DATA.length - 1) renderProblem(state.currentProblemIdx + 1);
      else renderProblem(state.currentProblemIdx);
    };

    document.getElementById('finishAssessmentBtn').onclick = () => {
      pauseTimer();
      switchMainTab('solutions');
    };

    function renderSolutions() {
      let solved = 0, skipped = 0;
      PROBLEMS_DATA.forEach((p, idx) => {
        const ps = state.problems[idx];
        if (ps && ps.isSolved) solved++;
        else if (ps && ps.isSkipped) skipped++;
      });
      const total = PROBLEMS_DATA.length;
      document.getElementById('finalScoreVal').textContent = solved;
      document.getElementById('accuracyStat').textContent = `${Math.round((solved/total)*100)}%`;
      document.getElementById('correctCountStat').textContent = solved;
      document.getElementById('skippedCountStat').textContent = skipped;

      const desc = document.getElementById('performanceFeedbackDesc');
      desc.textContent = solved === total 
        ? `🌟 Flawless mastery! All ${total} NCERT Arithmetic Progressions problems completed correctly in ${formatTime(timerSeconds)}.` 
        : `Completed in ${formatTime(timerSeconds)}. Review the step rationales below to polish your AP problem solving for CBSE boards.`;

      const container = document.getElementById('reviewListContainer');
      container.innerHTML = '';

      PROBLEMS_DATA.forEach((prob, idx) => {
        const card = document.createElement('div');
        card.className = 'review-card';
        let stepsHTML = prob.steps.map(st => `
          <div style="margin-top:10px; padding:12px; background:#f0f9ff; border-left:3px solid var(--primary-blue); border-radius:4px; border:1px solid var(--blue-border-soft); border-left-width:3px;">
            <strong style="color:var(--primary-dark); font-size:0.95rem;">${st.title}</strong>
            <p style="margin-top:4px; font-size:0.95rem; color:#0c4a6e;">${st.explanation}</p>
          </div>
        `).join('');
        card.innerHTML = `
          <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:0.5rem;">
            <strong style="color:var(--primary-dark); font-size:1.1rem;">${prob.title} (${prob.category})</strong>
            <span class="status-badge ${state.problems[idx]?.isSolved ? 'badge-complete' : 'badge-skipped'}">
              ${state.problems[idx]?.isSolved ? 'Solved' : 'Review'}
            </span>
          </div>
          <div style="font-size:1.05rem; margin-bottom:0.5rem;">${prob.context}</div>
          ${stepsHTML}
        `;
        container.appendChild(card);
      });

      sendReportToSheet(solved, total, timerSeconds);
      triggerMathTypeset();
    }

    document.getElementById('retakeQuizBtn').onclick = () => {
      sessionStorage.clear();
      window.location.reload();
    };

    document.getElementById('soundToggleBtn').onclick = () => {
      soundEnabled = !soundEnabled;
      document.getElementById('soundIcon').textContent = soundEnabled ? '🔊' : '🔇';
    };

    window.addEventListener('DOMContentLoaded', () => {
      triggerMathTypeset();
    });
  </script>
</body>
</html>
