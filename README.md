<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>تاروت | مجموعه کامل ۷۸ کارت</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;500;600;700&family=Cinzel:wght@500;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #07040f;
      --bg-elevated: #110a1c;
      --bg-card: #160e24;
      --gold: #c9a227;
      --gold-soft: #e8d48b;
      --gold-deep: #8a6d1a;
      --violet: #5c2d91;
      --violet-soft: #7b4bb8;
      --text: #f3e9d2;
      --text-muted: #a8977a;
      --border: rgba(201, 162, 39, 0.28);
      --shadow: 0 12px 40px rgba(0,0,0,0.55);
      --radius: 16px;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      font-family: 'Vazirmatn', system-ui, sans-serif;
      background: var(--bg);
      color: var(--text);
      min-height: 100vh;
      line-height: 1.6;
      background-image:
        radial-gradient(ellipse 80% 50% at 15% 0%, rgba(92,45,145,0.22) 0%, transparent 55%),
        radial-gradient(ellipse 60% 40% at 85% 100%, rgba(201,162,39,0.07) 0%, transparent 50%),
        radial-gradient(ellipse 50% 30% at 50% 50%, rgba(22,14,36,0.8) 0%, transparent 70%);
    }

    /* Subtle noise overlay for depth */
    body::before {
      content: '';
      position: fixed;
      inset: 0;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.035'/%3E%3C/svg%3E");
      pointer-events: none;
      z-index: 0;
    }

    .wrap {
      position: relative;
      z-index: 1;
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 1.25rem 3rem;
    }

    /* Header */
    header {
      text-align: center;
      padding: 2rem 0 1.25rem;
    }

    header h1 {
      font-family: 'Cinzel', 'Vazirmatn', serif;
      font-size: clamp(1.75rem, 4vw, 2.35rem);
      font-weight: 700;
      letter-spacing: 0.18em;
      background: linear-gradient(120deg, var(--gold-soft) 0%, var(--gold) 45%, var(--gold-deep) 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    /* Controls */
    .controls {
      display: flex;
      justify-content: center;
      gap: 0.85rem;
      flex-wrap: wrap;
      margin-bottom: 1.75rem;
    }

    .btn {
      font-family: inherit;
      font-size: 0.92rem;
      font-weight: 500;
      padding: 0.72rem 1.55rem;
      border: 1px solid var(--border);
      border-radius: 999px;
      background: linear-gradient(160deg, rgba(92,45,145,0.35), rgba(17,10,28,0.9));
      color: var(--gold-soft);
      cursor: pointer;
      transition: all 0.28s ease;
      box-shadow: 0 4px 18px rgba(0,0,0,0.35), inset 0 1px 0 rgba(255,255,255,0.06);
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
    }

    .btn:hover {
      border-color: var(--gold);
      color: #fff;
      background: linear-gradient(160deg, rgba(123,75,184,0.45), rgba(30,18,50,0.95));
      transform: translateY(-2px);
      box-shadow: 0 8px 24px rgba(201,162,39,0.18);
    }

    .btn:active { transform: translateY(0); }

    .btn svg { width: 17px; height: 17px; fill: currentColor; flex-shrink: 0; }

    /* Selected panel */
    .selected-panel {
      background: linear-gradient(165deg, rgba(22,14,36,0.92), rgba(12,7,22,0.96));
      border: 1px solid var(--border);
      border-radius: var(--radius);
      box-shadow: var(--shadow), inset 0 1px 0 rgba(255,255,255,0.03);
      padding: 1.35rem 1.4rem 1.5rem;
      margin-bottom: 2rem;
    }

    .panel-head {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 1.1rem;
      padding-bottom: 0.75rem;
      border-bottom: 1px solid rgba(201,162,39,0.15);
    }

    .panel-head h2 {
      font-size: 1rem;
      font-weight: 600;
      color: var(--gold-soft);
      letter-spacing: 0.04em;
    }

    .badge {
      font-size: 0.78rem;
      font-weight: 500;
      background: rgba(201,162,39,0.12);
      color: var(--gold);
      padding: 0.2rem 0.75rem;
      border-radius: 999px;
      border: 1px solid rgba(201,162,39,0.2);
    }

    .selected-row {
      display: flex;
      gap: 1.1rem;
      overflow-x: auto;
      padding: 0.35rem 0.15rem 0.9rem;
      min-height: 175px;
      align-items: flex-start;
    }

    .selected-row::-webkit-scrollbar { height: 6px; }
    .selected-row::-webkit-scrollbar-track { background: rgba(255,255,255,0.04); border-radius: 10px; }
    .selected-row::-webkit-scrollbar-thumb { background: var(--gold-deep); border-radius: 10px; }

    .empty-state {
      width: 100%;
      text-align: center;
      color: var(--text-muted);
      font-size: 0.92rem;
      padding: 2.2rem 1rem;
      opacity: 0.85;
    }

    /* Meanings under selected */
    .meanings-block {
      margin-top: 0.5rem;
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    .meaning-card {
      background: rgba(0,0,0,0.28);
      border: 1px solid rgba(201,162,39,0.12);
      border-radius: 12px;
      padding: 1.05rem 1.2rem;
      display: grid;
      grid-template-columns: auto 1fr;
      gap: 1rem;
      align-items: start;
      animation: fadeUp 0.45s ease;
    }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .meaning-card .mini-card {
      width: 72px;
      height: 110px;
      flex-shrink: 0;
    }

    .meaning-body h3 {
      font-size: 1.02rem;
      font-weight: 600;
      color: var(--gold-soft);
      margin-bottom: 0.35rem;
    }

    .meaning-body .arcana-tag {
      font-size: 0.72rem;
      color: var(--text-muted);
      margin-bottom: 0.55rem;
      display: inline-block;
    }

    .meaning-body p {
      font-size: 0.9rem;
      color: var(--text);
      line-height: 1.75;
      font-weight: 400;
    }

    /* Deck */
    .deck-panel {
      margin-top: 0.5rem;
    }

    .deck-head {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 1.15rem;
    }

    .deck-head h2 {
      font-size: 0.98rem;
      font-weight: 500;
      color: var(--text-muted);
    }

    .deck-head .count {
      font-size: 0.8rem;
      color: var(--gold-soft);
      background: rgba(92,45,145,0.25);
      padding: 0.22rem 0.8rem;
      border-radius: 999px;
      border: 1px solid rgba(123,75,184,0.25);
    }

    .cards-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(118px, 1fr));
      gap: 1.15rem;
      justify-items: center;
    }

    /* ===== Card component ===== */
    .card {
      width: 118px;
      height: 182px;
      perspective: 1200px;
      cursor: pointer;
      position: relative;
      transition: transform 0.28s ease;
    }

    .card:hover:not(.is-selected):not(.tray) {
      transform: translateY(-8px) scale(1.04);
    }

    .card.is-selected {
      opacity: 0.38;
      pointer-events: none;
      filter: grayscale(0.35) brightness(0.85);
    }

    .card.tray {
      width: 105px;
      height: 162px;
      flex-shrink: 0;
      cursor: default;
    }

    .card.tray:hover { transform: none; }

    .card-inner {
      width: 100%;
      height: 100%;
      position: relative;
      transform-style: preserve-3d;
      transition: transform 0.7s cubic-bezier(0.4, 0.15, 0.2, 1);
      border-radius: 12px;
    }

    .card.flipped .card-inner,
    .card.tray .card-inner {
      transform: rotateY(180deg);
    }

    .card.tray .card-inner { transform: none; }

    .face {
      position: absolute;
      inset: 0;
      backface-visibility: hidden;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 6px 22px rgba(0,0,0,0.5);
    }

    /* Back */
    .face.back {
      background:
        linear-gradient(145deg, #1a1028 0%, #2a1840 45%, #150e22 100%);
      border: 2px solid var(--gold-deep);
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .face.back::before {
      content: '';
      position: absolute;
      inset: 7px;
      border: 1px solid rgba(201,162,39,0.32);
      border-radius: 8px;
    }

    .face.back::after {
      content: '';
      position: absolute;
      inset: 14px;
      border: 1px solid rgba(201,162,39,0.12);
      border-radius: 5px;
      background:
        radial-gradient(circle at center, transparent 30%, rgba(201,162,39,0.05) 31%, transparent 55%),
        repeating-linear-gradient(45deg, transparent 0 7px, rgba(201,162,39,0.035) 7px 8px);
    }

    .back-mark {
      width: 48px;
      height: 48px;
      border: 2px solid var(--gold);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.35rem;
      color: var(--gold);
      background: rgba(0,0,0,0.4);
      box-shadow: 0 0 18px rgba(201,162,39,0.22);
      z-index: 2;
      position: relative;
    }

    /* Front */
    .face.front {
      background: linear-gradient(168deg, #1c1330 0%, #2d1c48 48%, #161022 100%);
      border: 2px solid var(--gold);
      transform: rotateY(180deg);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-between;
      padding: 10px 8px 12px;
      text-align: center;
    }

    .card.tray .face.front {
      transform: none;
      position: relative;
      width: 100%;
      height: 100%;
    }

    .card.tray .face.back { display: none; }

    .face.front.major {
      background: linear-gradient(168deg, #251840 0%, #3a2460 48%, #1a1230 100%);
      border-color: var(--gold-soft);
    }

    .c-num {
      font-family: 'Cinzel', serif;
      font-size: 0.78rem;
      color: var(--gold);
      letter-spacing: 0.06em;
      opacity: 0.95;
    }

    .c-sym {
      font-size: 2.15rem;
      line-height: 1;
      margin: 6px 0;
      filter: drop-shadow(0 3px 6px rgba(0,0,0,0.45));
    }

    .c-name {
      font-size: 0.78rem;
      font-weight: 600;
      color: var(--text);
      line-height: 1.3;
    }

    .c-suit {
      font-size: 0.65rem;
      color: var(--text-muted);
      margin-top: 3px;
    }

    .suit-wands .c-sym { color: #e67e22; }
    .suit-cups .c-sym { color: #5dade2; }
    .suit-swords .c-sym { color: #aeb6bf; }
    .suit-pentacles .c-sym { color: #58d68d; }
    .suit-major .c-sym { color: var(--gold-soft); }

    /* Mini in meaning */
    .mini-card .face.front {
      transform: none;
      position: relative;
      width: 100%;
      height: 100%;
      border-radius: 8px;
      padding: 6px 4px 8px;
    }
    .mini-card .c-sym { font-size: 1.5rem; margin: 2px 0; }
    .mini-card .c-name { font-size: 0.62rem; }
    .mini-card .c-num { font-size: 0.65rem; }

    /* Toast */
    .toast {
      position: fixed;
      bottom: 1.8rem;
      left: 50%;
      transform: translateX(-50%) translateY(120%);
      background: linear-gradient(135deg, rgba(40,22,70,0.97), rgba(18,10,35,0.98));
      border: 1px solid var(--gold-deep);
      color: var(--gold-soft);
      padding: 0.75rem 1.5rem;
      border-radius: 999px;
      font-size: 0.88rem;
      box-shadow: 0 10px 32px rgba(0,0,0,0.5);
      opacity: 0;
      transition: all 0.4s ease;
      z-index: 50;
      pointer-events: none;
      white-space: nowrap;
    }
    .toast.show {
      opacity: 1;
      transform: translateX(-50%) translateY(0);
    }

    /* Stars */
    .stars { position: fixed; inset: 0; pointer-events: none; z-index: 0; overflow: hidden; }
    .star {
      position: absolute;
      width: 2px; height: 2px;
      background: var(--gold-soft);
      border-radius: 50%;
      opacity: 0.25;
      animation: twinkle 5s infinite ease-in-out;
    }
    @keyframes twinkle {
      0%, 100% { opacity: 0.15; transform: scale(1); }
      50% { opacity: 0.65; transform: scale(1.5); }
    }

    @media (max-width: 640px) {
      .cards-grid {
        grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
        gap: 0.9rem;
      }
      .card { width: 100px; height: 154px; }
      .card.tray { width: 90px; height: 138px; }
      .c-name { font-size: 0.7rem; }
      .c-sym { font-size: 1.85rem; }
      .meaning-card { grid-template-columns: 1fr; }
      .meaning-card .mini-card { display: none; }
    }

    /* Footer */
    .site-footer {
      text-align: center;
      padding: 2.5rem 1rem 1.5rem;
      margin-top: 2rem;
      font-size: 0.88rem;
      color: var(--text-muted);
      letter-spacing: 0.03em;
      opacity: 0.85;
      border-top: 1px solid rgba(201, 162, 39, 0.12);
    }
  </style>
</head>
<body>
  <div class="stars" id="stars"></div>

  <div class="wrap">
    <header>
      <h1>تـاروت</h1>
    </header>

    <div class="controls">
      <button class="btn" id="btnShuffle">
        <svg viewBox="0 0 24 24"><path d="M16 3h5v5M4 20L21 3M21 16v5h-5M15 15l6 6M4 4l5 5"/></svg>
        بر زدن
      </button>
      <button class="btn" id="btnRandom">
        <svg viewBox="0 0 24 24"><path d="M12 2a10 10 0 1 0 10 10A10 10 0 0 0 12 2zm0 18a8 8 0 1 1 8-8 8 8 0 0 1-8 8zm1-13h-2v6l5.2 3.2.8-1.3-4-2.4z"/></svg>
        کارت تصادفی
      </button>
      <button class="btn" id="btnReset">
        <svg viewBox="0 0 24 24"><path d="M12 5V1L7 6l5 5V7c3.3 0 6 2.7 6 6s-2.7 6-6 6-6-2.7-6-6H4c0 4.4 3.6 8 8 8s8-3.6 8-8-3.6-8-8-8z"/></svg>
        شروع مجدد
      </button>
    </div>

    <!-- Selected + Meanings -->
    <section class="selected-panel">
      <div class="panel-head">
        <h2>کارت‌های انتخاب‌شده</h2>
        <span class="badge" id="selectedCount">۰ کارت</span>
      </div>
      <div class="selected-row" id="selectedRow">
        <div class="empty-state">هنوز کارتی انتخاب نشده است. روی هر کارت کلیک کنید تا باز شود.</div>
      </div>

      <div class="meanings-block" id="meaningsBlock"></div>
    </section>

    <!-- Deck -->
    <section class="deck-panel">
      <div class="deck-head">
        <h2>دسته کامل کارت‌ها</h2>
        <span class="count" id="remainingCount">۷۸ باقی‌مانده</span>
      </div>
      <div class="cards-grid" id="cardsGrid"></div>
    </section>

    <footer class="site-footer">
      ساخته شده با عشق توسط Rania💜
    </footer>
  </div>

  <div class="toast" id="toast"></div>

  <script>
    // ========== داده‌های کامل کارت‌ها با تفسیر حرفه‌ای ==========
    const majorArcana = [
      { id:'m0', name:'ابله', number:'۰', symbol:'🃏', suit:'major', meaning:'آغازی تازه و بی‌قید. روح هنوز سنگین نشده و آمادهٔ پرش به ناشناخته است. این کارت دعوت می‌کند به اعتماد به مسیر، حتی اگر نقشهٔ روشنی در دست نباشد. جسارت کودکانه و ایمان به جریان زندگی، کلید این مرحله است.' },
      { id:'m1', name:'جادوگر', number:'I', symbol:'🪄', suit:'major', meaning:'قدرت تجلی و تمرکز اراده. همهٔ ابزارها روی میز است و اکنون زمان عمل آگاهانه فرا رسیده. جادوگر به تو می‌گوید منابع درونی‌ات کافی‌اند؛ فقط باید آن‌ها را با وضوح و نیت خالص به کار بگیری.' },
      { id:'m2', name:'کاهنه اعظم', number:'II', symbol:'🌙', suit:'major', meaning:'سکوت و شهود. دانشی که با عقل صرف به دست نمی‌آید، در عمق ناخودآگاه منتظر است. این کارت از تو می‌خواهد به ندای درونی گوش بسپاری و رازهایی را که هنوز آشکار نشده‌اند، با صبر بپذیری.' },
      { id:'m3', name:'امپراتریس', number:'III', symbol:'👑', suit:'major', meaning:'فراوانی، پرورش و زیبایی طبیعی. انرژی مادرانهٔ کیهان در حال جاری شدن است. زمان رشد، خلاقیت و مراقبت از آنچه دوست می‌داری. زمین حاصلخیز است؛ بذرها را با عشق بکار.' },
      { id:'m4', name:'امپراتور', number:'IV', symbol:'🦁', suit:'major', meaning:'ساختار، اقتدار و ثبات. این کارت نظم و رهبری مسئولانه را یادآوری می‌کند. مرزها را مشخص کن، پایه‌ها را محکم بساز و با انضباط به سوی هدف حرکت کن. قدرت واقعی در ثبات و مسئولیت است.' },
      { id:'m5', name:'هیروفانت', number:'V', symbol:'⛪', suit:'major', meaning:'سنت، آموزش و مسیر معنوی تثبیت‌شده. دانشی که از نسل‌ها به تو رسیده، اکنون راهنماست. احترام به آیین، معلم یا ارزش‌های پایدار می‌تواند راه را روشن کند. گاهی حکمت در پیروی آگاهانه نهفته است.' },
      { id:'m6', name:'عشاق', number:'VI', symbol:'💕', suit:'major', meaning:'انتخاب قلب و اتحاد. این کارت فراتر از عشق رمانتیک است؛ دربارهٔ هم‌راستایی ارزش‌ها و تصمیم‌هایی است که روح را به سوی هماهنگی می‌برد. انتخابی که از عمق وجود برمی‌خیزد، مسیر را تغییر می‌دهد.' },
      { id:'m7', name:'ارابه', number:'VII', symbol:'🏛️', suit:'major', meaning:'ارادهٔ متمرکز و پیشروی. دو نیروی متضاد را با عزم و کنترل هدایت می‌کنی. پیروزی از طریق انضباط و جهت‌گیری روشن به دست می‌آید. اکنون زمان حرکت قاطع است، نه تردید.' },
      { id:'m8', name:'قدرت', number:'VIII', symbol:'💪', suit:'major', meaning:'قدرت نرم و شجاعت درونی. نه زور، بلکه مهربانی و تسلط بر غرایز. این کارت می‌گوید نیروی واقعی از شفقت و آرامش در برابر چالش‌ها می‌آید. شیر درون را با لطافت رام کن.' },
      { id:'m9', name:'زاهد', number:'IX', symbol:'🕯️', suit:'major', meaning:'خلوت و جست‌وجوی حقیقت درونی. زمان کناره‌گیری موقت از هیاهو برای شنیدن صدای خود است. نور فانوس زاهد، راه را در تاریکی نشان می‌دهد. خرد در سکوت و تأمل عمیق رشد می‌کند.' },
      { id:'m10', name:'چرخ اقبال', number:'X', symbol:'☸️', suit:'major', meaning:'چرخش تقدیر و تغییر اجتناب‌ناپذیر. چرخ می‌چرخد و موقعیت‌ها دگرگون می‌شوند. این کارت یادآور می‌شود که هیچ حالتی دائمی نیست. با جریان همراه شو و از فرصت‌هایی که چرخش می‌آورد، بهره بگیر.' },
      { id:'m11', name:'عدالت', number:'XI', symbol:'⚖️', suit:'major', meaning:'تعادل، حقیقت و پیامد اعمال. ترازو بی‌طرف است و هر عملی نتیجهٔ خود را دارد. این کارت دعوت به صداقت، مسئولیت‌پذیری و تصمیم‌گیری بر پایهٔ انصاف است. آنچه کاشته‌ای، اکنون درو می‌شود.' },
      { id:'m12', name:'مرد آویخته', number:'XII', symbol:'🙃', suit:'major', meaning:'تسلیم آگاهانه و تغییر دیدگاه. گاهی پیشرفت در رها کردن و دیدن دنیا از زاویهٔ دیگر است. این کارت صبر و پذیرش را می‌طلبد. با معلق ماندن، بینشی تازه به دست می‌آید که قبلاً پنهان بود.' },
      { id:'m13', name:'مرگ', number:'XIII', symbol:'💀', suit:'major', meaning:'پایان یک چرخه و تحول عمیق. نه لزوماً مرگ فیزیکی، بلکه رها شدن از آنچه کهنه شده. فضای تازه فقط با بستن درهای قدیمی ایجاد می‌شود. این کارت نوید تولد دوباره پس از عبور از تاریکی است.' },
      { id:'m14', name:'اعتدال', number:'XIV', symbol:'⚗️', suit:'major', meaning:'هماهنگی و میانه‌روی. ترکیب هوشمندانهٔ عناصر متضاد برای رسیدن به تعادل. این کارت صبر، انعطاف و جریان ملایم را می‌ستاید. عجله نکن؛ اجازه بده چیزها با ریتم طبیعی خود مخلوط شوند.' },
      { id:'m15', name:'شیطان', number:'XV', symbol:'😈', suit:'major', meaning:'اسارت در بندهای خودساخته. وابستگی، ترس یا الگوی تکراری که آزادی را محدود کرده. این کارت آینه است: زنجیرها اغلب در ذهن‌اند. آگاهی از سایه، نخستین گام رهایی است.' },
      { id:'m16', name:'برج', number:'XVI', symbol:'🗼', suit:'major', meaning:'فروپاشی ناگهانی ساختارهای دروغین. آنچه بر پایهٔ سست بنا شده بود، فرو می‌ریزد تا حقیقت نمایان شود. شوک می‌تواند دردناک باشد، اما فضای پاکی برای ساختن واقعی‌تر ایجاد می‌کند.' },
      { id:'m17', name:'ستاره', number:'XVII', symbol:'⭐', suit:'major', meaning:'امید، الهام و شفای آرام. پس از طوفان، نور ملایم ستاره بازمی‌گردد. این کارت ایمان به آینده و اتصال به منبع بالاتر را زنده می‌کند. زخم‌ها در حال التیام‌اند؛ به جریان شفابخش اعتماد کن.' },
      { id:'m18', name:'ماه', number:'XVIII', symbol:'🌕', suit:'major', meaning:'قلمرو وهم، ترس و ناخودآگاه. مسیر مبهم است و سایه‌ها بازی می‌کنند. این کارت هشدار می‌دهد که همه چیز آن‌طور که به نظر می‌رسد نیست. شهود را تقویت کن و از فریب‌های ذهن آگاه باش.' },
      { id:'m19', name:'خورشید', number:'XIX', symbol:'☀️', suit:'major', meaning:'شادی، وضوح و حیات. نور کامل بر همه چیز می‌تابد و حقیقت ساده آشکار می‌شود. این کارت انرژی کودکانه، موفقیت و گرمای درونی را می‌آورد. زمان جشن گرفتن زندگی و درخشیدن است.' },
      { id:'m20', name:'قضاوت', number:'XX', symbol:'📯', suit:'major', meaning:'بیداری و فراخوان به سطح بالاتر. گذشته ارزیابی می‌شود و دعوت به رستاخیز درونی می‌رسد. این کارت لحظهٔ تصمیم بزرگ و پاسخ به ندای روح است. آمادهٔ تولد دوبارهٔ آگاهی باش.' },
      { id:'m21', name:'جهان', number:'XXI', symbol:'🌍', suit:'major', meaning:'تکمیل چرخه و یکپارچگی. سفر به مقصد رسیده و همهٔ درس‌ها در یک کل هماهنگ جمع شده‌اند. این کارت موفقیت کامل، حس تعلق به کیهان و آمادگی برای آغاز دور جدید را نوید می‌دهد.' }
    ];

    const suitsData = [
      { key:'wands', name:'چوب‌دستی', symbol:'🔥', element:'آتش' },
      { key:'cups', name:'جام', symbol:'💧', element:'آب' },
      { key:'swords', name:'شمشیر', symbol:'⚔️', element:'هوا' },
      { key:'pentacles', name:'سکه', symbol:'🌿', element:'زمین' }
    ];

    const rankMeanings = {
      wands: {
        'آس': 'جرقهٔ خلاقیت و انگیزهٔ تازه. انرژی آتشین برای آغاز یک پروژه یا مسیر پرشور آماده است. این فرصت را با شجاعت بگیر.',
        '۲': 'نگاه به افق و برنامه‌ریزی. جهان در برابر توست و باید جهت را انتخاب کنی. جاه‌طلبی همراه با دوراندیشی نتیجه می‌دهد.',
        '۳': 'گسترش و انتظار ثمربخش. بذرهایی که کاشته‌ای در حال رشدند. صبر کن و افق‌های وسیع‌تر را ببین.',
        '۴': 'جشن و ثبات پس از تلاش. خانه‌ای امن یا لحظه‌ای از آرامش جمعی. موفقیت را با دیگران شریک شو.',
        '۵': 'رقابت و چالش‌های پراکنده. انرژی‌ها در تضادند. با مهارت و انعطاف، آشوب را به رشد تبدیل کن.',
        '۶': 'پیروزی و شناخته شدن. تلاش‌هایت دیده می‌شود. با افتخار اما فروتنی پیش برو.',
        '۷': 'دفاع از موقعیت. چالش‌هایی از پایین می‌آیند. استقامت و ایمان به مسیر، تو را نگه می‌دارد.',
        '۸': 'سرعت و حرکت سریع رویدادها. پیام‌ها و تغییرات با شتاب می‌رسند. آمادهٔ واکنش سریع باش.',
        '۹': 'مقاومت و آمادگی نهایی. خسته اما هنوز ایستاده‌ای. آخرین تلاش‌ها پیش از استراحت لازم است.',
        '۱۰': 'بار سنگین مسئولیت. بیش از حد بر دوش گرفته‌ای. زمان واگذاری بخشی از بار و سبک شدن است.',
        'جوان': 'پیام‌آور شور و ایدهٔ تازه. کنجکاوی آتشین و میل به کشف. با اشتیاق اما بدون عجله پیش برو.',
        'شوالیه': 'اقدام پرشور و ماجراجویی. انرژی پرشتاب که می‌تواند الهام‌بخش یا بی‌پروا باشد. جهت را حفظ کن.',
        'ملکه': 'اعتماد به نفس خلاق و گرمای رهبری. زنی که ایده‌ها را با جذابیت و استقلال می‌پروراند.',
        'پادشاه': 'رهبری با چشم‌انداز و کاریزما. تسلط بر انرژی آتش و تبدیل آن به دستاوردهای بزرگ.'
      },
      cups: {
        'آس': 'جریان تازهٔ احساسات و عشق. قلب باز می‌شود و هدیه‌ای عاطفی یا معنوی می‌رسد. بپذیر و جاری شو.',
        '۲': 'پیوند و تبادل احساسی. دو روح در حال شناخت عمیق یکدیگرند. تعادل دادن و گرفتن، کلید است.',
        '۳': 'شادی جمعی و دوستی. جشن، حمایت و لحظات شیرین با دیگران. روابط را گرامی بدار.',
        '۴': 'بی‌میلی و جست‌وجوی معنا. فرصت‌هایی هست اما روح هنوز سیراب نشده. به درون نگاه کن.',
        '۵': 'اندوه و تمرکز بر از دست‌رفته‌ها. سه جام ریخته اما دو جام هنوز ایستاده‌اند. روی آنچه باقی است تمرکز کن.',
        '۶': 'خاطرات شیرین و معصومیت گذشته. بازگشت به ریشه‌ها یا هدیهٔ بی‌چشم‌داشت. گرمای قدیم را احساس کن.',
        '۷': 'خیال و انتخاب‌های متعدد. وسوسه‌های رویایی که ممکن است واقعی نباشند. وضوح را حفظ کن.',
        '۸': 'ترک آنچه دیگر سیراب نمی‌کند. حرکت به سوی عمق بیشتر، حتی اگر مسیر تنهایی باشد.',
        '۹': 'رضایت و آرزوهای برآورده‌شده. لحظهٔ قدردانی از آنچه داری. شادی درونی را جشن بگیر.',
        '۱۰': 'هماهنگی خانوادگی و عشق کامل. دایرهٔ احساسی بسته و امن است. خانهٔ روح پیدا شده.',
        'جوان': 'پیام‌آور احساسات لطیف و شهود. قلب باز و کنجکاو برای تجربه‌های عاطفی تازه.',
        'شوالیه': 'جست‌وجوی رمانتیک و ایده‌آل‌گرایی. حرکت به سوی آنچه قلب می‌خواهد، با کمی رؤیاپردازی.',
        'ملکه': 'همدلی عمیق و مراقبت عاطفی. کسی که فضا را با درک و محبت پر می‌کند.',
        'پادشاه': 'تسلط بالغ بر احساسات. رهبری با قلبی آرام و خردمند که دیگران را حمایت می‌کند.'
      },
      swords: {
        'آس': 'وضوح ذهنی و حقیقت برنده. شمشیر از ابرها پایین می‌آید و راه را روشن می‌کند. تصمیم قاطع بگیر.',
        '۲': 'بن‌بست و نیاز به انتخاب. دو مسیر در تعادل معلق‌اند. چشم‌ها را ببند و با شهود تصمیم بگیر.',
        '۳': 'درد قلبی و جدایی. شمشیرها قلب را شکسته‌اند. این رنج، بخشی از فرآیند شفاست.',
        '۴': 'استراحت و بازیابی نیرو. پس از نبرد، سکوت و ترمیم لازم است. به خودت فرصت بده.',
        '۵': 'پیروزی توخالی و درگیری بیهوده. ممکن است برنده شوی اما با هزینهٔ روابط. عاقلانه‌تر عمل کن.',
        '۶': 'گذار به سوی آرامش. قایق از آب‌های متلاطم دور می‌شود. تغییر تدریجی به سوی بهتر.',
        '۷': 'استراتژی و پنهان‌کاری. گاهی باید هوشمندانه و بی‌سروصدا حرکت کرد. نیت را پاک نگه دار.',
        '۸': 'احساس گرفتاری و محدودیت ذهنی. بندها اغلب در فکر ساخته شده‌اند. راه خروج وجود دارد.',
        '۹': 'اضطراب شبانه و نگرانی‌های تکراری. ذهن در حال بازی با ترس‌هاست. صبح نزدیک است.',
        '۱۰': 'پایان دردناک یک چرخهٔ ذهنی. بدترین گذشته و اکنون فضا برای شروع تازه باز است.',
        'جوان': 'ذهن تیز و کنجکاو. پیام‌های تازه و نگاه پرسشگر. مراقب باش کلمات زخم نزنند.',
        'شوالیه': 'عمل سریع و قاطع ذهنی. شجاعت فکری که گاهی بی‌ملاحظه می‌شود. جهت را دقیق نگه دار.',
        'ملکه': 'وضوح، استقلال فکری و صداقت تند. زنی که حقیقت را بدون پرده‌پوشی می‌بیند و می‌گوید.',
        'پادشاه': 'اقتدار عقلانی و عدالت ذهنی. رهبری با منطق روشن و تصمیم‌های منصفانه.'
      },
      pentacles: {
        'آس': 'فرصت مادی و بذر ثروت. هدیه‌ای از زمین برای ساختن امنیت و رشد پایدار. آن را با دقت پرورش بده.',
        '۲': 'تعادل در مدیریت منابع. جادوگری که سکه‌ها را در هوا نگه می‌دارد. انعطاف و سازگاری لازم است.',
        '۳': 'کار تیمی و مهارت. ساختن چیزی با همکاری و تخصص. نتیجهٔ کار جمعی باکیفیت است.',
        '۴': 'حفظ و احتیاط بیش از حد. ترس از دست دادن می‌تواند جریان را متوقف کند. کمی بازتر باش.',
        '۵': 'سختی مادی و احساس بیرون‌ماندگی. حمایت هست اما شاید ندیده‌ای. کمک بخواه و امید را حفظ کن.',
        '۶': 'بخشش و دریافت متعادل. جریان سخاوت که هم به تو و هم از تو جاری می‌شود. عدالت در منابع.',
        '۷': 'صبر و ارزیابی رشد. بذرها کاشته شده‌اند؛ اکنون باید منتظر ثمربخشی باشی. عجله نکن.',
        '۸': 'تسلط بر مهارت و کار دقیق. شاگردی که به استاد تبدیل می‌شود. تمرکز و تمرین مداوم.',
        '۹': 'استقلال و لذت از دستاوردها. باغی که خودت ساخته‌ای و اکنون از آن لذت می‌بری.',
        '۱۰': 'ثروت خانوادگی و امنیت نسلی. موفقیت پایدار که به دیگران نیز منتقل می‌شود. میراث.',
        'جوان': 'دانش‌آموز عمل‌گرا و فرصت‌های زمینی. پیام‌های مربوط به کار، پول یا یادگیری عملی.',
        'شوالیه': 'پشتکار قابل اعتماد و حرکت آهسته اما مطمئن. کسی که قول می‌دهد و عمل می‌کند.',
        'ملکه': 'پرورش امنیت و فراوانی با گرمی. کسی که خانه و منابع را با مراقبت رشد می‌دهد.',
        'پادشاه': 'استاد مدیریت منابع و موفقیت مادی. رهبری با ثبات، سخاوت و خرد عملی.'
      }
    };

    const ranks = ['آس','۲','۳','۴','۵','۶','۷','۸','۹','۱۰','جوان','شوالیه','ملکه','پادشاه'];
    const rankSymbols = ['A','2','3','4','5','6','7','8','9','10','P','Kn','Q','K'];

    // ساخت دسته کامل
    let allCards = [...majorArcana];
    suitsData.forEach(suit => {
      ranks.forEach((rank, i) => {
        allCards.push({
          id: `${suit.key}-${i}`,
          name: `${rank} ${suit.name}`,
          number: rankSymbols[i],
          symbol: suit.symbol,
          suit: suit.key,
          meaning: rankMeanings[suit.key][rank]
        });
      });
    });

    // State
    let selectedIds = [];
    let deckOrder = allCards.map(c => c.id);

    // DOM
    const cardsGrid = document.getElementById('cardsGrid');
    const selectedRow = document.getElementById('selectedRow');
    const meaningsBlock = document.getElementById('meaningsBlock');
    const selectedCountEl = document.getElementById('selectedCount');
    const remainingCountEl = document.getElementById('remainingCount');
    const toastEl = document.getElementById('toast');

    function showToast(msg) {
      toastEl.textContent = msg;
      toastEl.classList.add('show');
      clearTimeout(showToast.t);
      showToast.t = setTimeout(() => toastEl.classList.remove('show'), 2400);
    }

    function getCard(id) {
      return allCards.find(c => c.id === id);
    }

    function createCardHTML(card, extraClass = '') {
      const suitClass = card.suit === 'major' ? 'suit-major major' : `suit-${card.suit}`;
      return `
        <div class="card ${extraClass}" data-id="${card.id}">
          <div class="card-inner">
            <div class="face back">
              <div class="back-mark">✦</div>
            </div>
            <div class="face front ${suitClass}">
              <div class="c-num">${card.number}</div>
              <div class="c-sym">${card.symbol}</div>
              <div>
                <div class="c-name">${card.name}</div>
                ${card.suit !== 'major' ? `<div class="c-suit">${suitsData.find(s=>s.key===card.suit)?.name || ''}</div>` : ''}
              </div>
            </div>
          </div>
        </div>`;
    }

    function renderDeck() {
      cardsGrid.innerHTML = '';
      deckOrder.forEach(id => {
        const card = getCard(id);
        if (!card) return;
        const isSel = selectedIds.includes(id);
        const wrapper = document.createElement('div');
        wrapper.innerHTML = createCardHTML(card, isSel ? 'flipped is-selected' : '');
        const el = wrapper.firstElementChild;
        if (!isSel) {
          el.addEventListener('click', () => selectCard(id));
        }
        cardsGrid.appendChild(el);
      });
      updateCounts();
    }

    function renderSelected() {
      if (selectedIds.length === 0) {
        selectedRow.innerHTML = '<div class="empty-state">هنوز کارتی انتخاب نشده است. روی هر کارت کلیک کنید تا باز شود.</div>';
        meaningsBlock.innerHTML = '';
        updateCounts();
        return;
      }

      selectedRow.innerHTML = selectedIds.map(id => {
        const card = getCard(id);
        return createCardHTML(card, 'tray flipped');
      }).join('');

      meaningsBlock.innerHTML = selectedIds.map(id => {
        const card = getCard(id);
        const arcana = card.suit === 'major' ? 'آرکانای کبیر' : `آرکانای صغیر • ${suitsData.find(s=>s.key===card.suit)?.name}`;
        return `
          <div class="meaning-card">
            <div class="mini-card">
              ${createCardHTML(card, 'tray flipped').replace('class="card tray flipped"', 'class="card tray flipped" style="width:72px;height:110px"')}
            </div>
            <div class="meaning-body">
              <h3>${card.name}</h3>
              <span class="arcana-tag">${arcana}</span>
              <p>${card.meaning}</p>
            </div>
          </div>`;
      }).join('');

      updateCounts();
    }

    function updateCounts() {
      const n = selectedIds.length;
      selectedCountEl.textContent = n === 0 ? '۰ کارت' : `${n.toLocaleString('fa-IR')} کارت`;
      remainingCountEl.textContent = `${(78 - n).toLocaleString('fa-IR')} باقی‌مانده`;
    }

    function selectCard(id) {
      if (selectedIds.includes(id)) return;
      selectedIds.push(id);

      const deckEl = cardsGrid.querySelector(`[data-id="${id}"]`);
      if (deckEl) {
        deckEl.classList.add('flipped');
        setTimeout(() => {
          deckEl.classList.add('is-selected');
        }, 450);
      }

      renderSelected();
      const card = getCard(id);
      showToast(`«${card.name}» انتخاب شد`);

      // scroll last meaning into view
      setTimeout(() => {
        const last = meaningsBlock.lastElementChild;
        if (last) last.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
      }, 100);
    }

    function shuffleDeck() {
      for (let i = deckOrder.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [deckOrder[i], deckOrder[j]] = [deckOrder[j], deckOrder[i]];
      }
      renderDeck();
      showToast('کارت‌ها بر زده شدند');
    }

    function randomCard() {
      const available = deckOrder.filter(id => !selectedIds.includes(id));
      if (!available.length) {
        showToast('همه کارت‌ها انتخاب شده‌اند');
        return;
      }
      const pick = available[Math.floor(Math.random() * available.length)];
      selectCard(pick);
    }

    function resetAll() {
      selectedIds = [];
      deckOrder = allCards.map(c => c.id);
      // shuffle
      for (let i = deckOrder.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [deckOrder[i], deckOrder[j]] = [deckOrder[j], deckOrder[i]];
      }
      renderDeck();
      renderSelected();
      showToast('دسته از نو آغاز شد');
    }

    function createStars() {
      const box = document.getElementById('stars');
      for (let i = 0; i < 55; i++) {
        const s = document.createElement('div');
        s.className = 'star';
        s.style.left = Math.random() * 100 + '%';
        s.style.top = Math.random() * 100 + '%';
        s.style.animationDelay = Math.random() * 5 + 's';
        s.style.animationDuration = (3.5 + Math.random() * 3) + 's';
        box.appendChild(s);
      }
    }

    // Events
    document.getElementById('btnShuffle').addEventListener('click', shuffleDeck);
    document.getElementById('btnRandom').addEventListener('click', randomCard);
    document.getElementById('btnReset').addEventListener('click', resetAll);

    // Init
    createStars();
    shuffleDeck();
    renderSelected();
  </script>
</body>
</html>

