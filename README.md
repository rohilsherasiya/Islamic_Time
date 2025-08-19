<html lang="en" dir="ltr">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Al‑Noor • Islamic Center</title>
    <meta name="description"
        content="A clean, responsive Islamic website template: prayer times, Qur'an, Hadith, events, articles, contact, and donation." />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link
        href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Noto+Naskh+Arabic:wght@500;700&display=swap"
        rel="stylesheet">
    <style>
        :root {
            --bg: #0b0f0c;
            --surface: #0f1712;
            --card: #121c16;
            --muted: #99a39b;
            --text: #ecf1ed;
            --brand: #1dbf73;
            --brand-2: #0b8f56;
            --gold: #f0c36c;
            --radius: 18px;
            --shadow: 0 12px 30px rgba(0, 0, 0, .25)
        }

        * {
            box-sizing: border-box
        }

        html,
        body {
            margin: 0;
            padding: 0;
            font-family: Inter, system-ui, Segoe UI, Roboto, Arial;
            background: linear-gradient(180deg, #0a120e, #0b0f0c 35%, #0d150f);
            color: var(--text)
        }

        a {
            color: inherit;
            text-decoration: none
        }

        img {
            max-width: 100%;
            display: block
        }

        .container {
            width: min(1200px, 100%);
            margin-inline: auto;
            padding: 0 16px
        }

        /* Header/Nav */
        header {
            position: sticky;
            top: 0;
            z-index: 40;
            backdrop-filter: saturate(1.1) blur(6px);
            background: rgba(10, 16, 12, .6);
            border-bottom: 1px solid #1b251e
        }

        .nav {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 16px;
            padding: 12px 0
        }

        .brand {
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: 800;
            letter-spacing: .4px
        }

        .brand .logo {
            width: 28px;
            height: 28px;
            border-radius: 50%;
            background: radial-gradient(circle at 60% 40%, #ffd27a, #f0c36c 45%, #b68d3a);
            position: relative;
            box-shadow: 0 0 18px rgba(240, 195, 108, .35)
        }

        .brand .logo::after {
            content: "";
            position: absolute;
            inset: 6px 10px auto auto;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: var(--bg)
        }

        .links {
            display: flex;
            gap: 14px;
            flex-wrap: wrap
        }

        .links a {
            padding: 8px 12px;
            border-radius: 12px;
            color: #dfe7e2
        }

        .links a:hover {
            background: #152018
        }

        .cta {
            display: flex;
            gap: 10px;
            align-items: center
        }

        .btn {
            border: 1px solid #254030;
            background: #152018;
            padding: 10px 14px;
            border-radius: 12px;
            cursor: pointer;
            color: var(--text)
        }

        .btn.brand {
            background: linear-gradient(135deg, var(--brand), var(--brand-2));
            border: 0;
            box-shadow: var(--shadow)
        }

        .menu {
            display: none
        }

        @media (max-width:900px) {
            .links {
                display: none
            }

            .menu {
                display: block
            }
        }

        /* Hero */
        .hero {
            position: relative;
            overflow: hidden
        }

        .hero .wrap {
            display: grid;
            grid-template-columns: 1.2fr .8fr;
            gap: 22px;
            align-items: center;
            padding: 30px 0
        }

        @media (max-width:900px) {
            .hero .wrap {
                grid-template-columns: 1fr
            }
        }

        .hero-card {
            background: linear-gradient(160deg, #0e1913 0%, #0c1711 60%, rgba(20, 33, 25, .6));
            border: 1px solid #1a2a20;
            border-radius: var(--radius);
            padding: 26px;
            box-shadow: var(--shadow)
        }

        .hero h1 {
            font-size: clamp(28px, 4vw, 48px);
            line-height: 1.15;
            margin: 0 0 8px
        }

        .hero p {
            color: #b6c0b8;
            margin: 0 0 18px
        }

        .pill {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            font-size: 13px;
            color: #d6e0d9;
            background: #0d2317;
            border: 1px solid #1f3a2a;
            padding: 6px 10px;
            border-radius: 999px
        }

        .arabic {
            font-family: 'Noto Naskh Arabic', system-ui;
            font-size: 28px;
            color: var(--gold)
        }

        .stat {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 12px;
            margin-top: 18px
        }

        .stat .kpi {
            background: #0e1a14;
            border: 1px solid #1a2a20;
            border-radius: 14px;
            padding: 14px
        }

        .kpi b {
            font-size: 20px
        }

        /* Sections */
        section {
            padding: 36px 0
        }

        .section-head {
            display: flex;
            align-items: end;
            justify-content: space-between;
            gap: 12px;
            margin: 0 0 14px
        }

        .title {
            font-size: clamp(20px, 2.6vw, 28px);
            margin: 0
        }

        .subtitle {
            color: var(--muted)
        }

        /* Cards & grids */
        .grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 16px
        }

        @media (max-width:1000px) {
            .grid {
                grid-template-columns: repeat(2, 1fr)
            }
        }

        @media (max-width:620px) {
            .grid {
                grid-template-columns: 1fr
            }
        }

        .card {
            background: var(--card);
            border: 1px solid #1a2a20;
            border-radius: 16px;
            padding: 16px;
            box-shadow: var(--shadow)
        }

        .card h3 {
            margin: 0 0 8px
        }

        /* Prayer times */
        .times {
            display: grid;
            grid-template-columns: repeat(6, 1fr);
            gap: 10px
        }

        @media (max-width:900px) {
            .times {
                grid-template-columns: repeat(3, 1fr)
            }
        }

        @media (max-width:520px) {
            .times {
                grid-template-columns: repeat(2, 1fr)
            }
        }

        .time {
            background: #0e1a14;
            border: 1px solid #1b2c21;
            border-radius: 14px;
            padding: 12px;
            text-align: center
        }

        .time b {
            display: block;
            font-size: 14px;
            color: #cfe6da
        }

        .time .value {
            font-size: 20px;
            font-weight: 700
        }

        /* Quran list */
        .surah-list {
            max-height: 360px;
            overflow: auto;
            border: 1px solid #1a2a20;
            border-radius: 14px
        }

        .surah {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 8px;
            padding: 10px 12px;
            border-bottom: 1px solid #1a2a20;
            cursor: pointer
        }

        .surah:hover {
            background: #132118
        }

        .surah:last-child {
            border-bottom: 0
        }

        .ayah {
            background: #0e1a14;
            border: 1px solid #1c2d22;
            border-radius: 14px;
            padding: 16px
        }

        /* Hadith carousel */
        .carousel {
            position: relative
        }

        .carousel .slide {
            display: none
        }

        .carousel .slide.active {
            display: block
        }

        .carousel .dotbar {
            display: flex;
            gap: 6px;
            justify-content: center;
            margin-top: 10px
        }

        .dot {
            width: 8px;
            height: 8px;
            border-radius: 50%;
            background: #274b37;
            border: 1px solid #305a43;
            cursor: pointer
        }

        .dot.active {
            background: var(--brand)
        }

        /* Articles */
        .article {
            display: flex;
            gap: 12px;
            align-items: flex-start
        }

        .badge {
            display: inline-block;
            font-size: 12px;
            padding: 4px 8px;
            border-radius: 999px;
            background: #123622;
            border: 1px solid #1d4a32;
            color: #cfe6da
        }

        /* Footer */
        footer {
            margin-top: 40px;
            background: #0a120d;
            border-top: 1px solid #1b251e
        }

        .footer {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 18px;
            padding: 22px 0
        }

        @media (max-width:900px) {
            .footer {
                grid-template-columns: 1fr 1fr
            }
        }

        @media (max-width:560px) {
            .footer {
                grid-template-columns: 1fr
            }
        }

        .small {
            color: #93a398;
            font-size: 13px
        }

        /* Utilities */
        .row {
            display: flex;
            gap: 10px;
            align-items: center;
            flex-wrap: wrap
        }

        .input {
            background: #0c1611;
            border: 1px solid #1e2f24;
            color: var(--text);
            padding: 10px 12px;
            border-radius: 12px;
            outline: none;
            width: 100%
        }

        .select {
            appearance: none
        }

        .sep {
            height: 1px;
            background: #1a2a20;
            margin: 12px 0
        }

        .sr {
            position: absolute;
            width: 1px;
            height: 1px;
            padding: 0;
            margin: -1px;
            overflow: hidden;
            clip: rect(0, 0, 0, 0);
            border: 0
        }

        /* RTL toggle */
        .rtl body {
            direction: rtl
        }
    </style>
</head>

<body>
    <!-- Header / Navbar -->
    <header>
        <div class="container nav">
            <a class="brand" href="#home" aria-label="Al-Noor Home">
                <span class="logo" aria-hidden="true"></span>
                <span>Al‑Noor</span>
            </a>
            <nav class="links" aria-label="Primary">
                <a href="#home">Home</a>
                <a href="#prayer">Prayer Times</a>
                <a href="#quran">Qur'an</a>
                <a href="#hadith">Hadith</a>
                <a href="#articles">Articles</a>
                <a href="#events">Events</a>
                <a href="#donate">Donate</a>
                <a href="#contact">Contact</a>
            </nav>
            <div class="cta">
                <button id="rtlBtn" class="btn" title="Toggle RTL">RTL</button>
                <button id="themeBtn" class="btn">Theme</button>
                <button class="btn brand"
                    onclick="document.getElementById('donate').scrollIntoView({behavior:'smooth'})">Donate</button>
                <button class="menu btn" id="menuBtn">Menu</button>
            </div>
        </div>
    </header>

    <!-- Mobile links -->
    <div id="mobileNav" class="container" style="display:none; padding:8px 0">
        <div class="row" style="justify-content:space-between">
            <a class="btn" href="#home">Home</a>
            <a class="btn" href="#prayer">Prayer</a>
            <a class="btn" href="#quran">Qur'an</a>
            <a class="btn" href="#hadith">Hadith</a>
            <a class="btn" href="#events">Events</a>
        </div>
    </div>

    <!-- Hero -->
    <section id="home" class="hero">
        <div class="container wrap">
            <div class="hero-card">
                <span class="pill">السلام عليكم • Peace & Guidance</span>
                <h1>Welcome to <span style="color:var(--brand)">Al‑Noor</span> Islamic Center</h1>
                <p>Daily prayers, Qur'an circles, community events, and knowledge for hearts seeking light.</p>
                <div class="arabic" aria-label="Bismillah">بِسْمِ اللّٰهِ الرَّحْمٰنِ الرَّحِيْمِ</div>
                <div class="stat">
                    <div class="kpi"><b id="todayName">Friday</b>
                        <div class="small" id="todayDate">—</div>
                    </div>
                    <div class="kpi"><b>Next Jumu'ah</b>
                        <div class="small" id="jumuTime">1:30 PM</div>
                    </div>
                    <div class="kpi"><b>Visitors online</b>
                        <div class="small" id="visitors">—</div>
                    </div>
                </div>
            </div>
            <div class="hero-card" aria-label="Masjid illustration">
                <svg viewBox="0 0 400 260" role="img" aria-label="Masjid silhouette"
                    style="width:100%; border-radius:14px; background:linear-gradient(180deg,#0b1720,#081014)">
                    <defs>
                        <linearGradient id="g" x1="0" x2="0" y1="0" y2="1">
                            <stop offset="0%" stop-color="#143b2a" />
                            <stop offset="100%" stop-color="#0b1913" />
                        </linearGradient>
                    </defs>
                    <rect x="0" y="0" width="400" height="260" fill="url(#g)" />
                    <circle cx="320" cy="60" r="24" fill="#f0c36c" />
                    <path
                        d="M40 220 L360 220 L360 200 L300 200 L300 170 Q260 140 220 170 L220 200 L180 200 L180 170 Q140 140 100 170 L100 200 L40 200 Z"
                        fill="#183f2a" />
                    <rect x="76" y="180" width="40" height="40" fill="#1a4a32" />
                    <rect x="180" y="180" width="40" height="40" fill="#1a4a32" />
                    <rect x="284" y="180" width="40" height="40" fill="#1a4a32" />
                    <path d="M200 120 L230 140 L170 140 Z" fill="#1b5a3a" />
                    <rect x="192" y="140" width="16" height="60" fill="#1a4a32" />
                </svg>
                <div class="small">“Indeed, in the remembrance of Allah do hearts find rest.” — Qur'an 13:28</div>
            </div>
        </div>
    </section>

    <!-- Prayer Times -->
    <section id="prayer">
        <div class="container">
            <div class="section-head">
                <h2 class="title">Prayer Times</h2>
                <div class="subtitle">Quick view for your city (demo data; replace with your official times)</div>
            </div>
            <div class="card">
                <div class="row">
                    <input id="city" class="input" style="max-width:260px" placeholder="Enter city (e.g., Ahmedabad)" />
                    <select id="method" class="input select" style="max-width:240px">
                        <option value="demo">Demo Method</option>
                        <option value="custom">Custom (enter manually)</option>
                    </select>
                    <button id="loadTimes" class="btn">Load Times</button>
                    <button id="manualBtn" class="btn">Manual Edit</button>
                </div>
                <div class="sep"></div>
                <div class="times" id="times"></div>
                <div class="small" style="margin-top:8px">Note: For accuracy, replace demo logic with an API like your
                    masjid timetable or a recognized prayer time service.</div>
            </div>
        </div>
    </section>

    <!-- Qur'an -->
    <section id="quran">
        <div class="container">
            <div class="section-head">
                <h2 class="title">Qur'an Explorer</h2>
                <div class="subtitle">Browse Surahs • Arabic + English names</div>
            </div>
            <div class="grid">
                <div class="card">
                    <div class="row">
                        <input id="surahSearch" class="input" placeholder="Search Surah (name/number)" />
                    </div>
                    <div class="surah-list" id="surahList" aria-label="Surah list"></div>
                </div>
                <div class="card" style="grid-column:span 2">
                    <h3 id="surahTitle">Select a Surah</h3>
                    <div class="ayah" id="ayahBox">
                        <div class="arabic" id="ayahArabic" style="font-size:26px; line-height:1.8"></div>
                        <div class="sep"></div>
                        <div id="ayahTrans" class="small"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Hadith -->
    <section id="hadith">
        <div class="container">
            <div class="section-head">
                <h2 class="title">Hadith of the Day</h2>
                <div class="subtitle">Short reminders (authentic collections)</div>
            </div>
            <div class="card carousel" id="hadithCarousel">
                <div class="slide active">
                    <div class="arabic">إِنَّمَا الأَعْمَالُ بِالنِّيَّاتِ</div>
                    <div class="small">“Actions are by intentions.” — Bukhari & Muslim</div>
                </div>
                <div class="slide">
                    <div class="arabic">الدِّينُ النَّصِيحَةُ</div>
                    <div class="small">“Religion is sincere advice.” — Muslim</div>
                </div>
                <div class="slide">
                    <div class="arabic">مَنْ صَمَتَ نَجَا</div>
                    <div class="small">“Whoever remains silent is saved.” — Tirmidhi (hasan)</div>
                </div>
                <div class="dotbar" aria-label="slides">
                    <span class="dot active" data-i="0"></span>
                    <span class="dot" data-i="1"></span>
                    <span class="dot" data-i="2"></span>
                </div>
            </div>
        </div>
    </section>

    <!-- Articles / Events -->
    <section id="articles">
        <div class="container">
            <div class="section-head">
                <h2 class="title">Articles</h2>
                <div class="subtitle">Study notes and community posts</div>
            </div>
            <div class="grid">
                <div class="card article">
                    <div>
                        <div class="badge">Fiqh</div>
                        <h3>Preparing for Jumu'ah</h3>
                        <p class="small">Etiquettes of Friday prayer: ghusl, clean clothes, early arrival, listening to
                            the khutbah attentively.</p>
                    </div>
                </div>
                <div class="card article">
                    <div>
                        <div class="badge">Akhlaq</div>
                        <h3>Guarding the Tongue</h3>
                        <p class="small">Speak good or remain silent. Tips to avoid backbiting and maintain a soft
                            heart.</p>
                    </div>
                </div>
                <div class="card article">
                    <div>
                        <div class="badge">Seerah</div>
                        <h3>Mercy of the Prophet ﷺ</h3>
                        <p class="small">Brief reflections on compassion, patience, and service to others.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="events">
        <div class="container">
            <div class="section-head">
                <h2 class="title">Events</h2>
                <div class="subtitle">Weekly & monthly gatherings</div>
            </div>
            <div class="grid">
                <div class="card">
                    <h3>Jumu'ah Prayer</h3>
                    <p class="small">Khutbah 1:15 PM • Salah 1:45 PM</p>
                </div>
                <div class="card">
                    <h3>Qur'an Circle</h3>
                    <p class="small">Saturdays after Maghrib • Tajwid & Tafsir</p>
                </div>
                <div class="card">
                    <h3>Family Night</h3>
                    <p class="small">Last Friday of the month • Potluck & talk</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Donate -->
    <section id="donate">
        <div class="container">
            <div class="section-head">
                <h2 class="title">Support the Masjid</h2>
                <div class="subtitle">Zakat • Sadaqah • General Fund</div>
            </div>
            <div class="grid">
                <div class="card">
                    <h3>Give Online</h3>
                    <p class="small">Use your preferred payment gateway.</p>
                    <div class="row">
                        <input class="input" id="amount" type="number" min="1" placeholder="Amount (₹)"
                            style="max-width:220px" />
                        <button class="btn brand" id="giveBtn">Donate</button>
                    </div>
                    <div id="donateMsg" class="small" style="margin-top:8px"></div>
                </div>
                <div class="card">
                    <h3>Bank Transfer</h3>
                    <p class="small">Account: Al‑Noor Welfare Trust<br>IFSC: ALNO0123456<br>UPI: alnoor@upi</p>
                </div>
                <div class="card">
                    <h3>Volunteer</h3>
                    <p class="small">Join our events, setup, or media teams.</p>
                    <button class="btn"
                        onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">Contact
                        Us</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact -->
    <section id="contact">
        <div class="container">
            <div class="section-head">
                <h2 class="title">Contact</h2>
                <div class="subtitle">We'd love to hear from you</div>
            </div>
            <div class="grid">
                <form class="card" onsubmit="event.preventDefault(); submitContact();">
                    <div class="row">
                        <input id="name" class="input" placeholder="Your name" required />
                        <input id="email" class="input" type="email" placeholder="Email" required />
                    </div>
                    <textarea id="msg" class="input" rows="5" placeholder="Message"></textarea>
                    <button class="btn brand" type="submit">Send</button>
                    <div id="contactNote" class="small" style="margin-top:8px"></div>
                </form>
                <div class="card">
                    <h3>Visit Us</h3>
                    <p class="small">Al‑Noor Islamic Center<br>Park View Road, Ahmedabad, IN</p>
                    <div class="sep"></div>
                    <h3>Hours</h3>
                    <p class="small">Fajr to Isha • Office Mon–Sat 10am–5pm</p>
                </div>
                <div class="card">
                    <h3>Newsletter</h3>
                    <p class="small">Get monthly updates.</p>
                    <div class="row">
                        <input id="newsEmail" class="input" type="email" placeholder="Email address" />
                        <button class="btn" id="newsBtn">Subscribe</button>
                    </div>
                    <div id="newsMsg" class="small" style="margin-top:8px"></div>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container footer">
            <div>
                <div class="brand"><span class="logo"></span><span>Al‑Noor</span></div>
                <p class="small">A community hub for prayer, learning, and service. May Allah accept.</p>
            </div>
            <div>
                <h4>Quick Links</h4>
                <p class="small"><a href="#prayer">Prayer Times</a><br><a href="#quran">Qur'an</a><br><a
                        href="#events">Events</a></p>
            </div>
            <div>
                <h4>Contact</h4>
                <p class="small">Rohil Sherasiya<br>+91 79846 57804</p>
            </div>
            <div>
                <h4>Follow</h4>
                <p class="small">YouTube • Instagram • </p>
            </div>
        </div>
        <div class="container" style="padding:10px 0; border-top:1px solid #1b251e">
            <div class="small">© <span id="year"></span> Al‑Noor. Built with ❤️</div>
        </div>
    </footer>

    <script>
        // --- Date, visitors (mock), theme/rtl, menu ---
        const $ = (id) => document.getElementById(id);
        const fmt = new Intl.DateTimeFormat(undefined, { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' });
        const now = new Date();
        $('todayName').textContent = new Intl.DateTimeFormat(undefined, { weekday: 'long' }).format(now);
        $('todayDate').textContent = fmt.format(now);
        $('visitors').textContent = Math.floor(10 + Math.random() * 90) + ' online';
        $('year').textContent = now.getFullYear();

        $('themeBtn').addEventListener('click', () => {
            const isDark = getComputedStyle(document.documentElement).getPropertyValue('--bg').trim() === '#0b0f0c';
            if (isDark) {
                document.documentElement.style.setProperty('--bg', '#f4f7f5');
                document.documentElement.style.setProperty('--surface', '#ffffff');
                document.documentElement.style.setProperty('--card', '#ffffff');
                document.documentElement.style.setProperty('--text', '#0b0f0c');
                document.documentElement.style.setProperty('--muted', '#5b6a60');
            } else {
                document.documentElement.style.setProperty('--bg', '#0b0f0c');
                document.documentElement.style.setProperty('--surface', '#0f1712');
                document.documentElement.style.setProperty('--card', '#121c16');
                document.documentElement.style.setProperty('--text', '#ecf1ed');
                document.documentElement.style.setProperty('--muted', '#99a39b');
            }
        });
        $('rtlBtn').addEventListener('click', () => {
            const isLTR = document.documentElement.getAttribute('dir') !== 'rtl';
            document.documentElement.setAttribute('dir', isLTR ? 'rtl' : 'ltr');
        });
        $('menuBtn').addEventListener('click', () => {
            const el = $('mobileNav'); el.style.display = el.style.display === 'none' ? 'block' : 'none';
        });

        // --- Prayer times (demo) ---
        const demoTimes = {
            'ahmedabad': { Fajr: '05:12', Dhuhr: '12:45', Asr: '16:10', Maghrib: '19:08', Isha: '20:26', Jumuah: '13:30' },
            'mumbai': { Fajr: '05:20', Dhuhr: '12:50', Asr: '16:20', Maghrib: '19:10', Isha: '20:30', Jumuah: '13:30' },
            'delhi': { Fajr: '04:58', Dhuhr: '12:40', Asr: '16:05', Maghrib: '19:02', Isha: '20:20', Jumuah: '13:15' }
        };
        function renderTimes(t) {
            const names = ['Fajr', 'Dhuhr', 'Asr', 'Maghrib', 'Isha', 'Jumuah'];
            $('times').innerHTML = names.map(n => `<div class="time"><b>${n}</b><div class="value">${t[n] || '—'}</div></div>`).join('');
        }
        function loadDemo(city) {
            const t = demoTimes[city.toLowerCase()] || { Fajr: '05:10', Dhuhr: '12:45', Asr: '16:10', Maghrib: '19:05', Isha: '20:25', Jumuah: '13:30' };
            renderTimes(t);
        }
        $('loadTimes').addEventListener('click', () => {
            const city = $('city').value.trim() || 'Ahmedabad';
            const method = $('method').value;
            if (method === 'demo') loadDemo(city); else editManual();
        });
        $('manualBtn').addEventListener('click', editManual);
        function editManual() {
            const fields = ['Fajr', 'Dhuhr', 'Asr', 'Maghrib', 'Isha', 'Jumuah'];
            $('times').innerHTML = fields.map(n => `<label class="time" style="text-align:left"><b>${n}</b><input class="input" style="margin-top:6px" id="i_${n}" placeholder="HH:MM" /></label>`).join('');
            const save = document.createElement('button');
            save.className = 'btn brand'; save.textContent = 'Save Times'; save.style.marginTop = '10px';
            save.onclick = () => {
                const t = {}; fields.forEach(n => t[n] = (document.getElementById('i_' + n).value || '—'));
                renderTimes(t);
            };
            $('times').after(save);
        }

        // --- Jumu'ah countdown (simple next Friday at 13:30 local) ---
        (function () {
            const target = new Date();
            const day = target.getDay(); // 0 Sun ... 5 Fri ... 6 Sat
            const diff = (5 - day + 7) % 7 || (target.getHours() > 13 || (target.getHours() === 13 && target.getMinutes() >= 30) ? 7 : 0);
            target.setDate(target.getDate() + diff);
            target.setHours(13, 30, 0, 0);
            function tick() {
                const now = new Date();
                const ms = target - now; if (ms <= 0) { $('jumuTime').textContent = 'In progress'; return; }
                const h = Math.floor(ms / 3.6e6), m = Math.floor((ms % 3.6e6) / 6e4);
                $('jumuTime').textContent = `${h}h ${m}m`;
                requestAnimationFrame(() => setTimeout(tick, 1000));
            }
            tick();
        })();

        // --- Qur'an simple data (first 10 surahs + first ayah) ---
        const surahs = [
            { n: 1, en: 'Al-Fatihah', ar: 'ٱلْفَاتِحَة', bism: true, ayah: 'بِسْمِ اللّٰهِ الرَّحْمٰنِ الرَّحِيْمِ', tr: 'In the Name of Allah—the Most Compassionate, Most Merciful.' },
            { n: 2, en: 'Al-Baqarah', ar: 'ٱلْبَقَرَة', bism: true, ayah: 'الم', tr: 'Alif-Lam-Meem.' },
            { n: 3, en: 'Ali Imran', ar: 'آلِ عِمْرَان', bism: true, ayah: 'اللَّهُ لَا إِلَٰهَ إِلَّا هُوَ الْحَيُّ الْقَيُّومُ', tr: 'Allah! There is no god except Him, the Ever-Living, Sustainer.' },
            { n: 4, en: 'An-Nisa', ar: 'ٱلنِّسَاء', bism: true, ayah: 'يَا أَيُّهَا النَّاسُ اتَّقُوا رَبَّكُمُ', tr: 'O humanity! Be mindful of your Lord…' },
            { n: 5, en: 'Al-Ma’idah', ar: 'ٱلْمَائِدَة', bism: true, ayah: 'يَا أَيُّهَا الَّذِينَ آمَنُوا أَوْفُوا بِالْعُقُودِ', tr: 'O believers! Honor your obligations…' },
            { n: 6, en: 'Al-An’am', ar: 'ٱلْأَنْعَام', bism: true, ayah: 'الْحَمْدُ لِلَّهِ الَّذِي خَلَقَ السَّمَاوَاتِ وَالْأَرْضَ', tr: 'All praise is for Allah Who created the heavens and the earth…' },
            { n: 7, en: 'Al-A’raf', ar: 'ٱلْأَعْرَاف', bism: true, ayah: 'كِتَابٌ أُنْزِلَ إِلَيْكَ', tr: 'A Book revealed to you…' },
            { n: 8, en: 'Al-Anfal', ar: 'ٱلْأَنْفَال', bism: true, ayah: 'يَسْأَلُونَكَ عَنِ الْأَنْفَالِ', tr: 'They ask you concerning the spoils…' },
            { n: 9, en: 'At-Tawbah', ar: 'ٱلتَّوْبَة', bism: false, ayah: 'بَرَاءَةٌ مِنَ اللَّهِ وَرَسُولِهِ', tr: 'A declaration of disassociation from Allah and His Messenger…' },
            { n: 10, en: 'Yunus', ar: 'يُونُس', bism: true, ayah: 'الر', tr: 'Alif-Lam-Ra.' }
        ];
        function renderSurahList(list) {
            $('surahList').innerHTML = list.map(s => `<div class="surah" data-n="${s.n}"><span>#${s.n} • ${s.en}</span><span class="arabic">${s.ar}</span></div>`).join('');
        }
        function showSurah(n) {
            const s = surahs.find(x => x.n == n); if (!s) return;
            $('surahTitle').textContent = `#${s.n} ${s.en} — ${s.ar}`;
            $('ayahArabic').textContent = (s.bism ? 'بِسْمِ اللّٰهِ الرَّحْمٰنِ الرَّحِيْمِ\n' : '') + s.ayah;
            $('ayahTrans').textContent = s.tr;
        }
        renderSurahList(surahs);
        $('surahList').addEventListener('click', (e) => {
            const el = e.target.closest('.surah'); if (!el) return; showSurah(el.dataset.n);
        });
        $('surahSearch').addEventListener('input', (e) => {
            const q = e.target.value.toLowerCase();
            const list = surahs.filter(s => String(s.n).includes(q) || s.en.toLowerCase().includes(q) || s.ar.includes(q));
            renderSurahList(list);
        });

        // --- Hadith carousel ---
        const slides = [...document.querySelectorAll('#hadithCarousel .slide')];
        const dots = [...document.querySelectorAll('#hadithCarousel .dot')];
        function go(i) { slides.forEach((s, idx) => s.classList.toggle('active', idx == i)); dots.forEach((d, idx) => d.classList.toggle('active', idx == i)); }
        dots.forEach(d => d.addEventListener('click', () => go(Number(d.dataset.i))));
        let i = 0; setInterval(() => { i = (i + 1) % slides.length; go(i); }, 7000);

        // --- Donate / Contact ---
        $('giveBtn').addEventListener('click', () => {
            const v = Number($('amount').value || 0); if (v <= 0) { $('donateMsg').textContent = 'Please enter a valid amount.'; return; }
            $('donateMsg').textContent = `Thank you! You pledged ₹${v.toFixed(0)} (demo).`;
        });
        function submitContact() {
            $('contactNote').textContent = 'JazakAllahu khairan! We will reply soon (demo).';
        }
        $('newsBtn').addEventListener('click', () => {
            const e = $('newsEmail').value.trim();
            $('newsMsg').textContent = e ? 'Subscribed (demo).' : 'Enter a valid email.';
        });
    </script>
    
</body>

</html>
