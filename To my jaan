<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Love Message</title>
  <style>
    /* page */
    :root{
      --bg1: #0f172a;
      --bg2: #1f2937;
      --accent: #ff5c8a;
      --glass: rgba(255,255,255,0.06);
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      min-height:100vh;
      font-family: "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      background: radial-gradient(1200px 600px at 10% 20%, #0b1220 0%, transparent 10%),
                  linear-gradient(180deg,var(--bg1),var(--bg2));
      color: #f8fafc;
      display:flex;
      align-items:center;
      justify-content:center;
      padding:24px;
    }

    /* main button */
    .open-btn{
      background: linear-gradient(135deg,#ff7aa2,#ffb199);
      border: none;
      color:white;
      font-weight:700;
      padding:18px 28px;
      border-radius:14px;
      box-shadow: 0 8px 30px rgba(255,92,138,0.2);
      cursor:pointer;
      font-size:18px;
      letter-spacing:0.2px;
      transition: transform .12s ease, box-shadow .12s ease;
    }
    .open-btn:active{ transform: translateY(2px) scale(.998); }
    .subtitle{
      margin-top:12px;
      text-align:center;
      font-size:14px;
      color: #cbd5e1;
    }

    /* modal */
    .modal-backdrop{
      position:fixed;
      inset:0;
      display:none;
      align-items:center;
      justify-content:center;
      background: linear-gradient(0deg, rgba(2,6,23,0.6), rgba(2,6,23,0.6));
      z-index:40;
      padding:20px;
      backdrop-filter: blur(6px) saturate(120%);
    }
    .modal{
      max-width:720px;
      width:100%;
      background: linear-gradient(180deg, rgba(255,255,255,0.03), rgba(255,255,255,0.02));
      border-radius:18px;
      padding:20px;
      border: 1px solid rgba(255,255,255,0.06);
      box-shadow: 0 20px 60px rgba(2,6,23,0.6);
      position:relative;
      overflow:hidden;
    }

    /* decorative floating emojis */
    .float-emoji{
      position:absolute;
      font-size:26px;
      opacity:.95;
      animation: float 6s ease-in-out infinite;
      pointer-events:none;
      filter: drop-shadow(0 6px 12px rgba(0,0,0,0.5));
    }
    .e1{ left: 8%; top:-10px; animation-duration:7s; transform-origin:center; }
    .e2{ right: 6%; top:8px; animation-duration:6.5s; }
    .e3{ left: 30%; bottom:-8px; animation-duration:8s; }
    .e4{ right: 26%; bottom:6px; animation-duration:6.2s; }
    @keyframes float {
      0% { transform: translateY(0) rotate(0deg) }
      50% { transform: translateY(-18px) rotate(8deg) }
      100% { transform: translateY(0) rotate(0deg) }
    }

    /* message content */
    .message{
      color:#f1f5f9;
      line-height:1.6;
      font-size:16px;
      padding:10px 6px 0 6px;
      max-height:62vh;
      overflow:auto;
    }
    .message p{ margin:0 0 12px 0; white-space:pre-wrap; } /* preserve new lines */

    /* header and controls */
    .modal-header{
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:12px;
      margin-bottom:6px;
    }
    .title{
      display:flex;
      gap:10px;
      align-items:center;
      font-weight:700;
      font-size:18px;
    }
    .title .heart{
      background: linear-gradient(90deg,#ff6b8a,#ffb5a2);
      padding:8px;
      border-radius:8px;
      box-shadow: 0 6px 18px rgba(255,92,138,0.12);
      font-size:16px;
    }
    .controls{ display:flex; gap:8px; align-items:center; }
    .btn{
      background:var(--glass);
      border: 1px solid rgba(255,255,255,0.04);
      color:#e6eef8;
      padding:8px 12px;
      border-radius:10px;
      cursor:pointer;
      font-weight:600;
      font-size:14px;
    }
    .close{ background:transparent; border:0; font-size:22px; color:#cbd5e1; cursor:pointer; }

    /* small responsive tweaks */
    @media (max-width:520px){
      .modal{ padding:14px; border-radius:12px; }
      .message{ font-size:15px; }
      .open-btn{ padding:14px 20px; font-size:16px; }
      .float-emoji{ font-size:20px; opacity:.9; }
    }

    /* tiny fade in */
    .show{ display:flex; animation: fadeIn .18s ease both; }
    @keyframes fadeIn { from {opacity:0; transform:scale(.995)} to {opacity:1; transform:none} }
  </style>
</head>
<body>

  <div style="text-align:center;">
    <button class="open-btn" id="openBtn">Open message for Maryam 🌸</button>
    <div class="subtitle">Tap the button to reveal the message with flowers & hearts</div>
  </div>

  <!-- modal -->
  <div class="modal-backdrop" id="backdrop" role="dialog" aria-modal="true" aria-hidden="true">
    <div class="modal" role="document" aria-labelledby="modalTitle">
      <!-- floating emoji decorations -->
      <div class="float-emoji e1">🌸</div>
      <div class="float-emoji e2">🌹</div>
      <div class="float-emoji e3">💖</div>
      <div class="float-emoji e4">✨</div>

      <div class="modal-header">
        <div class="title" id="modalTitle">
          <div class="heart">💘</div>
          <div>For Maryam</div>
        </div>
        <div class="controls">
          <button class="btn" id="copyBtn" title="Copy message">Copy</button>
          <button class="close" id="closeBtn" aria-label="Close">✕</button>
        </div>
      </div>

      <div class="message" id="message">
ap meri deewangi ho jana 🔥 apko chahna sirf meri aadat nahi, balki meri zarurat ban chuke hai ☁️... ap meri rooh ka sukoon ho jana 💘 meri khwahish ka jawab aur meri har raat ka sapna ho 🌙😘 ap meri ankhon ka noor ho jana 👀✨ apki muskan meri duniya roshan karti ha 🌸🌹 apki baatein dil ko sukoon deti ha 🥺💘 ap meri muhabbat hi nahi meri tamanna bhi ho..😭 wo tamanna jo din ba din gehri hoti ja rahi ha 🤔☁️ mai chahti hu kai ap meri zindagi ka har lamhe ka hissa bane 💗 har subha meri neend apki muskaan se khule 🌅 har raat meri neend apki baahon mein ho 🙈❤️ ap meri muhabbat ka wo jadoo ho jo mujhe hamesha apne andr kheench leta 😢❤️ meri jaan ap merai ho aur mai chahti hu kai ap sirf merai rahe zindagi bar 💍☁️ ap meri rooh ka wo sukoon ho jise mai har lamha apne pass mehsoos karna chahti hu 😤💘 chahe duniya kehti rahe kuch bhi, chahe waqt kaise bhi badle mera dil apko chahne se kabhi nahi rukega ❤️💘😭☁️ ap meri zindagi meri jaan aur mera sukoon ho jana 🌍💘🔐 jana mujhe kabhi chor kar mat jana 😢🪽🎀💞🔥
      </div>
    </div>
  </div>

  <script>
    // elements
    const openBtn = document.getElementById('openBtn');
    const backdrop = document.getElementById('backdrop');
    const closeBtn = document.getElementById('closeBtn');
    const copyBtn = document.getElementById('copyBtn');
    const messageDiv = document.getElementById('message');

    // open modal
    openBtn.addEventListener('click', () => {
      backdrop.classList.add('show');
      backdrop.setAttribute('aria-hidden', 'false');
      // trap focus to close button (simple)
      closeBtn.focus();
    });

    // close modal (buttons and click outside)
    function closeModal(){
      backdrop.classList.remove('show');
      backdrop.setAttribute('aria-hidden', 'true');
      openBtn.focus();
    }
    closeBtn.addEventListener('click', closeModal);
    backdrop.addEventListener('click', (e) => {
      if (e.target === backdrop) closeModal();
    });

    // copy to clipboard
    copyBtn.addEventListener('click', async () => {
      try {
        const text = messageDiv.innerText.trim();
        await navigator.clipboard.writeText(text);
        copyBtn.textContent = 'Copied ✓';
        setTimeout(()=> copyBtn.textContent = 'Copy', 1800);
      } catch (err) {
        copyBtn.textContent = 'Copy failed';
        setTimeout(()=> copyBtn.textContent = 'Copy', 1800);
      }
    });

    // keyboard accessible close (Esc)
    document.addEventListener('keydown', (e) => {
      if (e.key === 'Escape' && backdrop.classList.contains('show')) closeModal();
    });
  </script>
</body>
</html>
