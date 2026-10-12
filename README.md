
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SKN Energy Team | Kozminski University</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-dark: #090d16;
            --bg-card: rgba(18, 26, 43, 0.7);
            --bg-card-hover: rgba(28, 40, 65, 0.8);
            --accent-green: #00ffaa;
            --accent-blue: #00b8ff;
            --accent-glow: rgba(0, 255, 170, 0.25);
            --text-main: #f1f5f9;
            --text-muted: #94a3b8;
            --border-color: rgba(255, 255, 255, 0.08);
            --border-highlight: rgba(0, 255, 170, 0.3);
            --nav-height: 80px;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Plus Jakarta Sans', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            line-height: 1.6;
            overflow-x: hidden;
            background-image: 
                radial-gradient(circle at 10% 20%, rgba(0, 184, 255, 0.08) 0%, transparent 40%),
                radial-gradient(circle at 90% 80%, rgba(0, 255, 170, 0.08) 0%, transparent 40%);
            background-attachment: fixed;
        }

        /* --- NAVBAR --- */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: var(--nav-height);
            z-index: 1000;
            background: rgba(9, 13, 22, 0.85);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border-bottom: 1px solid var(--border-color);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 24px;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo-group {
            display: flex;
            align-items: center;
            gap: 12px;
            text-decoration: none;
            color: var(--text-main);
        }

        .logo-icon {
            width: 42px;
            height: 42px;
            background: linear-gradient(135deg, var(--accent-green), var(--accent-blue));
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 22px;
            font-weight: bold;
            color: #090d16;
            box-shadow: 0 0 15px var(--accent-glow);
        }

        .logo-text h1 {
            font-size: 1.1rem;
            font-weight: 800;
            letter-spacing: -0.5px;
            text-transform: uppercase;
        }

        .logo-text span {
            font-size: 0.72rem;
            color: var(--accent-blue);
            font-weight: 600;
            letter-spacing: 1px;
            display: block;
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 32px;
            list-style: none;
        }

        .nav-links a {
            color: var(--text-muted);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.95rem;
            transition: all 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--accent-green);
        }

        .btn-nav {
            background: linear-gradient(135deg, var(--accent-green), var(--accent-blue));
            color: #090d16 !important;
            padding: 10px 22px;
            border-radius: 30px;
            font-weight: 700 !important;
            box-shadow: 0 0 20px var(--accent-glow);
            transition: transform 0.3s ease, box-shadow 0.3s ease !important;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .btn-nav:hover {
            transform: translateY(-2px);
            box-shadow: 0 0 30px rgba(0, 255, 170, 0.4);
        }

        .hamburger {
            display: none;
            cursor: pointer;
            background: none;
            border: none;
            color: var(--text-main);
            font-size: 28px;
        }

        /* --- HERO SECTION --- */
        .hero {
            padding-top: calc(var(--nav-height) + 60px);
            padding-bottom: 80px;
            text-align: center;
            max-width: 1000px;
            margin: 0 auto;
            padding-left: 24px;
            padding-right: 24px;
        }

        .badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: rgba(0, 255, 170, 0.1);
            border: 1px solid var(--border-highlight);
            color: var(--accent-green);
            padding: 6px 18px;
            border-radius: 30px;
            font-size: 0.85rem;
            font-weight: 600;
            margin-bottom: 24px;
        }

        .badge-dot {
            width: 8px;
            height: 8px;
            background-color: var(--accent-green);
            border-radius: 50%;
            box-shadow: 0 0 8px var(--accent-green);
        }

        .hero h2 {
            font-size: clamp(2.2rem, 5vw, 3.8rem);
            font-weight: 800;
            line-height: 1.15;
            letter-spacing: -1px;
            margin-bottom: 24px;
        }

        .gradient-text {
            background: linear-gradient(135deg, var(--accent-green), var(--accent-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero p {
            font-size: 1.15rem;
            color: var(--text-muted);
            max-width: 750px;
            margin: 0 auto 36px auto;
        }

        .hero-actions {
            display: flex;
            gap: 16px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--accent-green), var(--accent-blue));
            color: #090d16;
            padding: 16px 36px;
            border-radius: 30px;
            font-weight: 700;
            font-size: 1rem;
            text-decoration: none;
            box-shadow: 0 0 25px var(--accent-glow);
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 0 35px rgba(0, 255, 170, 0.5);
        }

        .btn-secondary {
            background: rgba(255, 255, 255, 0.05);
            color: var(--text-main);
            border: 1px solid var(--border-color);
            padding: 16px 36px;
            border-radius: 30px;
            font-weight: 600;
            font-size: 1rem;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.1);
            border-color: var(--text-muted);
        }

        /* --- SEKCJE / SECTIONS GRID --- */
        .section-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 80px 24px;
        }

        .section-header {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-header h3 {
            font-size: 2.2rem;
            font-weight: 800;
            margin-bottom: 12px;
        }

        .section-header p {
            color: var(--text-muted);
            font-size: 1.05rem;
        }

        .divisions-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 24px;
        }

        .division-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 20px;
            padding: 30px;
            transition: all 0.3s ease;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .division-card:hover {
            background: var(--bg-card-hover);
            border-color: var(--border-highlight);
            transform: translateY(-5px);
        }

        .div-icon {
            width: 50px;
            height: 50px;
            border-radius: 12px;
            background: rgba(0, 255, 170, 0.1);
            color: var(--accent-green);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            margin-bottom: 20px;
        }

        .division-card h4 {
            font-size: 1.3rem;
            margin-bottom: 12px;
        }

        .division-card p {
            color: var(--text-muted);
            font-size: 0.95rem;
            line-height: 1.5;
        }

        /* --- HYPERLINK RECRUITMENT BANNER --- */
        .recruit-banner {
            background: linear-gradient(135deg, rgba(18, 26, 43, 0.9), rgba(9, 13, 22, 0.95));
            border: 1px solid var(--border-highlight);
            border-radius: 28px;
            padding: 60px 40px;
            text-align: center;
            position: relative;
            overflow: hidden;
            box-shadow: 0 0 40px rgba(0, 255, 170, 0.1);
        }

        .recruit-banner::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(0, 255, 170, 0.05) 0%, transparent 60%);
            pointer-events: none;
        }

        .recruit-banner h3 {
            font-size: 2.4rem;
            font-weight: 800;
            margin-bottom: 16px;
        }

        .recruit-banner p {
            color: var(--text-muted);
            font-size: 1.1rem;
            max-width: 650px;
            margin: 0 auto 36px auto;
        }

        .forms-link-btn {
            display: inline-flex;
            align-items: center;
            gap: 14px;
            background: linear-gradient(135deg, var(--accent-green), var(--accent-blue));
            color: #090d16;
            font-size: 1.2rem;
            font-weight: 800;
            padding: 20px 48px;
            border-radius: 40px;
            text-decoration: none;
            box-shadow: 0 0 30px var(--accent-glow);
            transition: all 0.3s ease;
        }

        .forms-link-btn:hover {
            transform: scale(1.04) translateY(-3px);
            box-shadow: 0 0 45px rgba(0, 255, 170, 0.6);
        }

        /* --- QUIZ & SIMULATOR --- */
        .interactive-box {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 24px;
            padding: 40px;
            margin-bottom: 40px;
        }

        .quiz-option {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid var(--border-color);
            padding: 16px 20px;
            border-radius: 12px;
            margin-bottom: 12px;
            cursor: pointer;
            transition: all 0.2s ease;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .quiz-option:hover {
            background: rgba(0, 255, 170, 0.08);
            border-color: var(--border-highlight);
        }

        .quiz-option.selected {
            background: rgba(0, 255, 170, 0.15);
            border-color: var(--accent-green);
        }

        .sim-slider {
            width: 100%;
            height: 12px;
            border-radius: 6px;
            background: #1e293b;
            outline: none;
            margin: 24px 0;
            accent-color: var(--accent-green);
        }

        .stat-badge {
            font-size: 2.4rem;
            font-weight: 800;
            color: var(--accent-green);
        }

        /* --- FOOTER --- */
        footer {
            border-top: 1px solid var(--border-color);
            padding: 40px 24px;
            text-align: center;
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        footer a {
            color: var(--accent-blue);
            text-decoration: none;
        }

        /* RESPONSIVE MOBILE */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
                position: absolute;
                top: var(--nav-height);
                left: 0;
                width: 100%;
                background: rgba(9, 13, 22, 0.98);
                flex-direction: column;
                padding: 30px 24px;
                gap: 20px;
                border-bottom: 1px solid var(--border-color);
            }

            .nav-links.active {
                display: flex;
            }

            .hamburger {
                display: block;
            }

            .recruit-banner {
                padding: 40px 20px;
            }

            .forms-link-btn {
                width: 100%;
                justify-content: center;
                padding: 18px 24px;
                font-size: 1rem;
            }

            .hero h2 {
                font-size: 2.1rem;
            }
        }
    </style>
</head>
<body>

    <!-- NAVBAR -->
    <header>
        <div class="nav-container">
            <a href="#" class="logo-group">
                <div class="logo-icon">⚡</div>
                <div class="logo-text">
                    <h1>SKN Energy Team</h1>
                    <span>KOZMINSKI UNIVERSITY</span>
                </div>
            </a>
            
            <button class="hamburger" id="hamburgerBtn">☰</button>

            <ul class="nav-links" id="navLinks">
                <li><a href="#sekcje">Sekcje</a></li>
                <li><a href="#quiz">Quiz OZE</a></li>
                <li><a href="#symulator">Symulator</a></li>
                <li><a href="https://forms.cloud.microsoft/e/YEAW18jFCf" target="_blank" class="btn-nav">Aplikuj Do Nas ↗</a></li>
            </ul>
        </div>
    </header>

    <!-- HERO SECTION -->
    <section class="hero">
        <div class="badge">
            <span class="badge-dot"></span> Rekrutacja 2026/2027 • Otwarta
        </div>
        <h2>Napędzaj Przyszłość Energii z <br><span class="gradient-text">SKN Energy Team</span></h2>
        <p>Dołącz do czołowego koła naukowego Akademii Leona Koźmińskiego. Zdobądź doświadczenie w OZE, analizach rynku energii oraz raportowaniu ESG.</p>
        
        <div class="hero-actions">
            <a href="https://forms.cloud.microsoft/e/YEAW18jFCf" target="_blank" class="btn-primary">Wypełnij Formularz Rekrutacyjny ↗</a>
            <a href="#sekcje" class="btn-secondary">Poznaj 4 Sekcje</a>
        </div>
    </section>

    <!-- 4 SEKCJE -->
    <section class="section-container" id="sekcje">
        <div class="section-header">
            <h3>Nasze Sekcje</h3>
            <p>Wybierz obszar, w którym chcesz rozwijać swoje kompetencje</p>
        </div>

        <div class="divisions-grid">
            <div class="division-card">
                <div>
                    <div class="div-icon">🤝</div>
                    <h4>Współpraca</h4>
                    <p>Pozyskiwanie partnerów biznesowych, organizacja wizyt studyjnych w firmach z sektora OZE oraz budowanie relacji z liderami rynku energii.</p>
                </div>
            </div>

            <div class="division-card">
                <div>
                    <div class="div-icon">📚</div>
                    <h4>Dydaktyczno-Naukowa</h4>
                    <p>Tworzenie raportów rynkowych, publikowanie artykułów o transformacji energetycznej, udział w konferencjach oraz analizy ESG.</p>
                </div>
            </div>

            <div class="division-card">
                <div>
                    <div class="div-icon">👥</div>
                    <h4>HR i Integracja</h4>
                    <p>Rekrutacja nowych członków, onboarding, organizacja wewnętrznych warsztatów szkoleniowych oraz dbanie o świetną atmosferę w zespole.</p>
                </div>
            </div>

            <div class="division-card">
                <div>
                    <div class="div-icon">📱</div>
                    <h4>Social Media</h4>
                    <p>Kreowanie wizerunku koła w mediach społecznościowych (@kozminskienergy), tworzenie grafik, materiałów wideo oraz prowadzenie kampanii.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- BANER REKRUTACYJNY (HYPERLINK DO FORMS) -->
    <section class="section-container" id="rekrutacja">
        <div class="recruit-banner">
            <h3>Dołącz do Zespołu SKN Energy Team</h3>
            <p>Kliknij poniższy przycisk, aby przejść do oficjalnego formularza rekrutacyjnego Microsoft Forms. Wypełnienie zgłoszenia zajmuje tylko 2 minuty!</p>
            
            <a href="https://forms.cloud.microsoft/e/YEAW18jFCf" target="_blank" class="forms-link-btn">
                ⚡ Otwórz Formularz Rekrutacyjny (Microsoft Forms) ↗
            </a>
        </div>
    </section>

    <!-- INTERAKTYWNY QUIZ -->
    <section class="section-container" id="quiz">
        <div class="interactive-box">
            <div class="section-header" style="margin-bottom: 30px;">
                <h3>Sprawdź swoją wiedzę OZE & ESG</h3>
                <p>Rozwiąż mini-quiz rekrutacyjny i sprawdź, ile wiesz o transformacji energetycznej!</p>
            </div>
            
            <div id="quizContainer">
                <div id="questionCounter" style="color: var(--accent-blue); font-weight: 600; margin-bottom: 8px; font-size: 0.9rem;">Pytanie 1 z 4</div>
                <p style="font-weight: 700; font-size: 1.1rem; margin-bottom: 20px;" id="quizQuestion">Ładowanie...</p>
                <div id="optionsContainer"></div>
                <div id="quizResult" style="margin-top: 20px; font-weight: 700; font-size: 1rem;"></div>
                <button id="nextBtn" style="display: none; margin-top: 24px; background: var(--accent-green); color: #090d16; border: none; padding: 12px 28px; border-radius: 20px; font-weight: 700; cursor: pointer;" onclick="nextQuestion()">Następne pytanie ➔</button>
            </div>
        </div>
    </section>

    <!-- SYMULATOR OZE -->
    <section class="section-container" id="symulator">
        <div class="interactive-box">
            <div class="section-header" style="margin-bottom: 30px;">
                <h3>Kalkulator Wpływu OZE</h3>
                <p>Przesuń suwak, aby oszacować roczną redukcję emisji CO2 przy instalacji fotowoltaicznej</p>
            </div>

            <label style="font-weight: 700; font-size: 1.1rem;">Moc instalacji PV (kWp): <span id="powerVal" style="color: var(--accent-green); font-size: 1.3rem;">50</span> kWp</label>
            <input type="range" min="10" max="500" value="50" class="sim-slider" id="pvSlider" oninput="updateSim()">

            <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 24px; margin-top: 35px; text-align: center;">
                <div style="background: rgba(255,255,255,0.04); padding: 28px; border-radius: 20px; border: 1px solid var(--border-color);">
                    <div class="stat-badge" id="mwhVal">50 MWh</div>
                    <div style="color: var(--text-muted); font-size: 1rem; margin-top: 8px;">Roczna produkcja zielonej energii</div>
                </div>
                <div style="background: rgba(255,255,255,0.04); padding: 28px; border-radius: 20px; border: 1px solid var(--border-color);">
                    <div class="stat-badge" id="co2Val">35 ton</div>
                    <div style="color: var(--text-muted); font-size: 1rem; margin-top: 8px;">Oszczędzona emisja CO2</div>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <p>&copy; 2026 SKN Energy Team – Kozminski University. Wszelkie prawa zastrzeżone.</p>
        <p style="margin-top: 8px;">Obserwuj nas na Instagramie: <a href="https://instagram.com/kozminskienergy" target="_blank">@kozminskienergy</a></p>
    </footer>

    <!-- SKRYPTY JS -->
    <script>
        // Menu mobilne
        const hamburgerBtn = document.getElementById('hamburgerBtn');
        const navLinks = document.getElementById('navLinks');

        hamburgerBtn.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // BAZA PYTAŃ DO QUIZU
        const quizData = [
            {
                question: "1. Co oznacza skrót ESG w biznesie?",
                options: [
                    "A) Energy, Sustainability, and Green",
                    "B) Environmental, Social, and Governance",
                    "C) Ecological Standards and Growth"
                ],
                correct: 1
            },
            {
                question: "2. Które źródło energii jest zaliczane do OZE (Odnawialnych Źródeł Energii)?",
                options: [
                    "A) Gaz ziemny",
                    "B) Węgiel kamienny",
                    "C) Energetyka wiatrowa"
                ],
                correct: 2
            },
            {
                question: "3. Głównym celem polityki Europejskiego Zielonego Ładu (European Green Deal) jest:",
                options: [
                    "A) Osiągnięcie neutralności klimatycznej UE do 2050 roku",
                    "B) Całkowite zamknięcie sektora przemysłowego w Europie",
                    "C) Zwiększenie importu węgla kamiennego"
                ],
                correct: 0
            },
            {
                question: "4. Do której sekcji w SKN Energy Team powinieneś dołączyć, jeśli pasjonujesz się tworzeniem grafik, rolek i prowadzeniem Instagrama?",
                options: [
                    "A) Współpraca",
                    "B) Dydaktyczno-Naukowa",
                    "C) Social Media"
                ],
                correct: 2
            }
        ];

        let currentQuestionIndex = 0;
        let score = 0;
        let answered = false;

        function loadQuiz() {
            answered = false;
            const q = quizData[currentQuestionIndex];
            document.getElementById('questionCounter').innerText = `Pytanie ${currentQuestionIndex + 1} z ${quizData.length}`;
            document.getElementById('quizQuestion').innerText = q.question;
            
            const optionsContainer = document.getElementById('optionsContainer');
            optionsContainer.innerHTML = '';
            
            q.options.forEach((opt, index) => {
                const div = document.createElement('div');
                div.className = 'quiz-option';
                div.innerText = opt;
                div.onclick = () => selectAnswer(index, div);
                optionsContainer.appendChild(div);
            });

            document.getElementById('quizResult').innerText = '';
            document.getElementById('nextBtn').style.display = 'none';
        }

        function selectAnswer(selectedIndex, element) {
            if (answered) return;
            answered = true;

            const q = quizData[currentQuestionIndex];
            const options = document.querySelectorAll('.quiz-option');
            
            if (selectedIndex === q.correct) {
                element.classList.add('selected');
                element.style.borderColor = 'var(--accent-green)';
                element.style.background = 'rgba(0, 255, 170, 0.15)';
                document.getElementById('quizResult').innerText = "Dobra odpowiedź!";
                document.getElementById('quizResult').style.color = "var(--accent-green)";
                score++;
            } else {
                element.style.borderColor = '#ff4757';
                element.style.background = 'rgba(255, 71, 87, 0.15)';
                options[q.correct].style.borderColor = 'var(--accent-green)';
                options[q.correct].style.background = 'rgba(0, 255, 170, 0.15)';
                document.getElementById('quizResult').innerText = "Błędne, poprawna to: " + q.options[q.correct];
                document.getElementById('quizResult').style.color = "#ff4757";
            }

            document.getElementById('nextBtn').style.display = 'inline-block';
        }

        function nextQuestion() {
            currentQuestionIndex++;
            if (currentQuestionIndex < quizData.length) {
                loadQuiz();
            } else {
                document.getElementById('quizContainer').innerHTML = `
                    <div style="text-align: center; padding: 20px;">
                        <h3 style="font-size: 1.8rem; margin-bottom: 12px;" class="gradient-text">Quiz ukończony!</h3>
                        <p style="font-size: 1.1rem; color: var(--text-muted); margin-bottom: 24px;">Twój wynik: <strong>${score} / ${quizData.length}</strong></p>
                        <a href="https://forms.cloud.microsoft/e/YEAW18jFCf" target="_blank" class="forms-link-btn" style="padding: 14px 32px; font-size: 1rem;">
                            Przejdź do formularza rekrutacyjnego ↗
                        </a>
                    </div>
                `;
            }
        }

        // Symulator
        function updateSim() {
            const val = document.getElementById('pvSlider').value;
            document.getElementById('powerVal').innerText = val;
            document.getElementById('mwhVal').innerText = (val * 1.0).toFixed(0) + " MWh";
            document.getElementById('co2Val').innerText = (val * 0.7).toFixed(0) + " ton";
        }

        // Uruchomienie quizu na starcie
        loadQuiz();
    </script>
</body>
</html>
