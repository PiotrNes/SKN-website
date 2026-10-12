
<html lang="pl" class="dark scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>SKN Energy Team | Akademia Leona Koźmińskiego</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        energy: {
                            navy: '#070b12',
                            darkCard: '#0f172a',
                            emerald: '#00ff88',
                            cyan: '#00f0ff',
                            blue: '#3b82f6',
                            purple: '#a855f7',
                            pink: '#ec4899',
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                    animation: {
                        'pulse-slow': 'pulseGlow 4s infinite alternate',
                        'float': 'float 5s ease-in-out infinite',
                    },
                    keyframes: {
                        pulseGlow: {
                            '0%': { filter: 'drop-shadow(0 0 15px rgba(0,255,136,0.25))' },
                            '100%': { filter: 'drop-shadow(0 0 35px rgba(0,240,255,0.5))' }
                        },
                        float: {
                            '0%, 100%': { transform: 'translateY(0px)' },
                            '50%': { transform: 'translateY(-8px)' }
                        }
                    }
                }
            }
        }
    </script>
    <!-- Lucide Icons & Google Fonts -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #070b12;
            color: #f3f4f6;
            overflow-x: hidden;
            width: 100%;
        }
        .glass-panel {
            background: rgba(15, 23, 42, 0.85);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }
        .glass-panel-hover {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        @media (min-width: 768px) {
            .glass-panel-hover:hover {
                border-color: rgba(0, 240, 255, 0.4);
                transform: translateY(-4px);
                box-shadow: 0 12px 30px -10px rgba(0, 240, 255, 0.2);
            }
        }
        .text-gradient {
            background: linear-gradient(135deg, #00ff88 0%, #00f0ff 50%, #3b82f6 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .bg-gradient-btn {
            background: linear-gradient(135deg, #00ff88 0%, #00f0ff 100%);
            transition: all 0.3s ease;
        }
        .bg-gradient-btn:active, .bg-gradient-btn:hover {
            opacity: 0.95;
            transform: translateY(-1px);
            box-shadow: 0 8px 20px -5px rgba(0, 255, 136, 0.4);
        }
        /* Mobile touch friendly targets */
        button, a, input, select, textarea {
            touch-action: manipulation;
        }
        ::-webkit-scrollbar {
            width: 6px;
        }
        ::-webkit-scrollbar-track {
            background: #070b12;
        }
        ::-webkit-scrollbar-thumb {
            background: #1e293b;
            border-radius: 4px;
        }
    </style>
</head>
<body class="min-h-screen flex flex-col justify-between selection:bg-energy-emerald selection:text-black">

    <!-- Navigation Header -->
    <header class="sticky top-0 z-50 glass-panel border-b border-white/10 px-3 sm:px-6 py-3 transition-all">
        <div class="max-w-7xl mx-auto flex items-center justify-between">
            <a href="#" class="flex items-center gap-2.5 group">
                <div class="relative w-9 h-9 sm:w-10 sm:h-10 rounded-xl bg-gradient-to-br from-energy-emerald via-energy-cyan to-energy-blue p-[2px] shrink-0">
                    <div class="w-full h-full bg-energy-navy rounded-[10px] flex items-center justify-center">
                        <i data-lucide="zap" class="w-4 h-4 sm:w-5 sm:h-5 text-energy-emerald"></i>
                    </div>
                </div>
                <div>
                    <span class="font-extrabold text-sm sm:text-lg tracking-wider text-white block leading-tight">SKN ENERGY TEAM</span>
                    <span class="text-[9px] sm:text-[10px] text-gray-400 font-medium tracking-widest uppercase block">Kozminski University</span>
                </div>
            </a>

            <!-- Desktop Nav Links -->
            <nav class="hidden lg:flex items-center gap-6 text-sm font-medium text-gray-300">
                <a href="#sekcje" class="hover:text-energy-emerald transition-colors">Sekcje</a>
                <a href="#quiz" class="hover:text-energy-emerald transition-colors flex items-center gap-1.5">
                    <span class="relative flex h-2 w-2">
                        <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-energy-emerald opacity-75"></span>
                        <span class="relative inline-flex rounded-full h-2 w-2 bg-energy-emerald"></span>
                    </span>
                    Quiz Rekrutacyjny
                </a>
                <a href="#kalkulator" class="hover:text-energy-emerald transition-colors">Symulator OZE</a>
                <a href="#rekrutacja" class="hover:text-energy-emerald transition-colors">Aplikuj</a>
            </nav>

            <div class="flex items-center gap-2 sm:gap-3">
                <a href="https://instagram.com/kozminskienergy" target="_blank" rel="noopener noreferrer" 
                   class="hidden sm:flex items-center gap-2 px-3 py-2 rounded-lg text-xs font-semibold glass-panel border border-pink-500/30 text-pink-400 hover:bg-pink-500/10 transition-all">
                    <i data-lucide="instagram" class="w-4 h-4"></i>
                    <span>@kozminskienergy</span>
                </a>
                
                <a href="#rekrutacja" class="hidden sm:inline-flex items-center gap-2 px-4 py-2 rounded-lg text-xs font-bold text-black bg-gradient-btn shadow-lg">
                    <span>Dołącz do nas</span>
                    <i data-lucide="arrow-right" class="w-4 h-4"></i>
                </a>

                <!-- Mobile Hamburger Toggle Button -->
                <button id="mobile-menu-btn" onclick="toggleMobileMenu()" class="lg:hidden p-2.5 rounded-xl bg-white/5 border border-white/10 text-gray-200 hover:text-white focus:outline-none min-h-[44px] min-w-[44px] flex items-center justify-center">
                    <i data-lucide="menu" id="menu-icon" class="w-6 h-6"></i>
                </button>
            </div>
        </div>

        <!-- Mobile Slide-down Overlay Navigation Menu -->
        <div id="mobile-menu" class="hidden lg:hidden pt-4 pb-2 border-t border-white/10 mt-3 space-y-2">
            <a href="#sekcje" onclick="toggleMobileMenu()" class="block px-4 py-3 rounded-xl hover:bg-white/5 text-sm font-semibold text-gray-200">
                <div class="flex items-center gap-3"><i data-lucide="layers" class="w-4 h-4 text-energy-cyan"></i> 4 Sekcje Koła</div>
            </a>
            <a href="#quiz" onclick="toggleMobileMenu()" class="block px-4 py-3 rounded-xl hover:bg-white/5 text-sm font-semibold text-gray-200">
                <div class="flex items-center gap-3"><i data-lucide="award" class="w-4 h-4 text-energy-emerald"></i> Quiz Rekrutacyjny (10 Pytania)</div>
            </a>
            <a href="#kalkulator" onclick="toggleMobileMenu()" class="block px-4 py-3 rounded-xl hover:bg-white/5 text-sm font-semibold text-gray-200">
                <div class="flex items-center gap-3"><i data-lucide="sliders" class="w-4 h-4 text-energy-blue"></i> Symulator Transformacji ESG</div>
            </a>
            <a href="#rekrutacja" onclick="toggleMobileMenu()" class="block px-4 py-3 rounded-xl hover:bg-white/5 text-sm font-semibold text-gray-200">
                <div class="flex items-center gap-3"><i data-lucide="send" class="w-4 h-4 text-energy-pink"></i> Formularz Aplikacyjny</div>
            </a>
            <a href="https://instagram.com/kozminskienergy" target="_blank" class="block px-4 py-3 rounded-xl bg-pink-500/10 border border-pink-500/30 text-pink-400 text-sm font-bold text-center">
                <div class="flex items-center justify-center gap-2"><i data-lucide="instagram" class="w-4 h-4"></i> Obserwuj @kozminskienergy</div>
            </a>
        </div>
    </header>

    <!-- Hero Banner -->
    <section class="relative pt-8 sm:pt-16 pb-16 sm:pb-24 px-4 overflow-hidden">
        <div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[300px] sm:w-[600px] h-[300px] sm:h-[600px] bg-energy-cyan/15 rounded-full blur-[100px] sm:blur-[140px] pointer-events-none"></div>

        <div class="max-w-5xl mx-auto text-center relative z-10">
            <div class="inline-flex items-center gap-2 px-3.5 py-1.5 sm:px-4 sm:py-2 rounded-full glass-panel border border-energy-emerald/30 text-energy-emerald text-[11px] sm:text-xs font-semibold mb-6 max-w-full text-left sm:text-center">
                <i data-lucide="sparkles" class="w-4 h-4 shrink-0"></i>
                <span class="truncate">Rekrutacja 2026/2027 • Zgłoś się już dziś!</span>
            </div>

            <h1 class="text-3xl sm:text-5xl md:text-7xl font-black text-white tracking-tight leading-tight sm:leading-none mb-5">
                Napędzaj Przyszłość Energii z <br class="hidden sm:block">
                <span class="text-gradient">SKN Energy Team</span>
            </h1>

            <p class="text-gray-300 text-sm sm:text-base md:text-lg max-w-2xl mx-auto mb-8 font-normal leading-relaxed px-2">
                Koło naukowe Akademii Leona Koźmińskiego skupiające pasjonatów OZE, rynków energii, ESG i innowacji. Wybierz swoją sekcję i dołącz do nas!
            </p>

            <div class="flex flex-col sm:flex-row items-stretch sm:items-center justify-center gap-3.5 max-w-md mx-auto sm:max-w-none">
                <a href="#quiz" class="w-full sm:w-auto px-6 py-4 rounded-xl font-bold text-black bg-gradient-btn shadow-xl flex items-center justify-center gap-2.5 text-sm sm:text-base min-h-[48px]">
                    <i data-lucide="award" class="w-5 h-5 text-black shrink-0"></i>
                    <span>Quiz Rekrutacyjny</span>
                    <i data-lucide="arrow-right" class="w-4 h-4 shrink-0"></i>
                </a>
                <a href="#sekcje" class="w-full sm:w-auto px-6 py-4 rounded-xl font-semibold text-white glass-panel hover:bg-white/5 flex items-center justify-center gap-2 text-sm sm:text-base transition-all min-h-[48px]">
                    <i data-lucide="layers" class="w-5 h-5 text-energy-cyan shrink-0"></i>
                    <span>Poznaj 4 Sekcje</span>
                </a>
            </div>

            <!-- Stats Badge Bar -->
            <div class="grid grid-cols-2 md:grid-cols-4 gap-3 sm:gap-4 mt-12 sm:mt-16 text-left max-w-4xl mx-auto">
                <div class="glass-panel p-3.5 sm:p-4 rounded-xl border-l-4 border-l-energy-emerald">
                    <div class="text-xl sm:text-2xl font-black text-white">4 Sekcje</div>
                    <div class="text-[11px] sm:text-xs text-gray-400">Różnorodne obszary</div>
                </div>
                <div class="glass-panel p-3.5 sm:p-4 rounded-xl border-l-4 border-l-energy-cyan">
                    <div class="text-xl sm:text-2xl font-bold text-white">OZE & ESG</div>
                    <div class="text-[11px] sm:text-xs text-gray-400">Nowoczesne trendy</div>
                </div>
                <div class="glass-panel p-3.5 sm:p-4 rounded-xl border-l-4 border-l-energy-blue">
                    <div class="text-xl sm:text-2xl font-bold text-white">Networking</div>
                    <div class="text-[11px] sm:text-xs text-gray-400">Wizyty w firmach</div>
                </div>
                <div class="glass-panel p-3.5 sm:p-4 rounded-xl border-l-4 border-l-energy-pink">
                    <div class="text-xl sm:text-2xl font-bold text-white">@kozminski</div>
                    <div class="text-[11px] sm:text-xs text-gray-400">Instagram i LinkedIn</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Sekcje Koła (4 Core Divisions) -->
    <section id="sekcje" class="py-14 sm:py-20 px-4 relative bg-energy-darkCard/40 border-y border-white/5">
        <div class="max-w-6xl mx-auto">
            <div class="text-center mb-10 sm:mb-14">
                <span class="text-energy-cyan text-xs font-bold uppercase tracking-widest">Struktura Koła</span>
                <h2 class="text-2xl sm:text-4xl font-black text-white mt-1">Wybierz Swoją Sekcję w SKN Energy Team</h2>
                <p class="text-gray-400 text-xs sm:text-sm mt-2 max-w-2xl mx-auto">
                    Każda z naszych 4 sekcji odpowiada za inny obszar działalności koła. Zobacz, gdzie najlepiej wykorzystasz swoje umiejętności!
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-4 sm:gap-6">
                
                <!-- Sekcja 1: Współpraca -->
                <div class="glass-panel p-5 sm:p-7 rounded-2xl glass-panel-hover border border-white/10 relative overflow-hidden">
                    <div class="flex items-center gap-3.5 mb-3.5">
                        <div class="w-11 h-11 sm:w-12 sm:h-12 rounded-xl bg-energy-emerald/15 text-energy-emerald flex items-center justify-center border border-energy-emerald/30 shrink-0">
                            <i data-lucide="handshake" class="w-5 h-5 sm:w-6 sm:h-6"></i>
                        </div>
                        <div>
                            <h3 class="text-lg sm:text-xl font-bold text-white">Sekcja Współpraca</h3>
                            <span class="text-[11px] sm:text-xs text-energy-emerald font-semibold uppercase tracking-wider block">Partnerstwa & Wizyty Studyjne</span>
                        </div>
                    </div>
                    <p class="text-gray-300 text-xs sm:text-sm leading-relaxed mb-4">
                        Pozyskiwanie partnerów strategicznych, nawiązywanie relacji z liderami sektora OZE/ESG, budowanie sieci kontaktów biznesowych oraz organizowanie wizyt studyjnych w spółkach energetycznych.
                    </p>
                    <div class="space-y-2 border-t border-white/10 pt-3 text-xs text-gray-300">
                        <div class="flex items-start gap-2"><i data-lucide="check" class="w-4 h-4 text-energy-emerald shrink-0 mt-0.5"></i> Pozyskiwanie sponsorów i partnerów wydarzeń</div>
                        <div class="flex items-start gap-2"><i data-lucide="check" class="w-4 h-4 text-energy-emerald shrink-0 mt-0.5"></i> Wyjazdy i wizyty studyjne w firmach branżowych</div>
                    </div>
                </div>

                <!-- Sekcja 2: Dydaktyczno-Naukowa -->
                <div class="glass-panel p-5 sm:p-7 rounded-2xl glass-panel-hover border border-white/10 relative overflow-hidden">
                    <div class="flex items-center gap-3.5 mb-3.5">
                        <div class="w-11 h-11 sm:w-12 sm:h-12 rounded-xl bg-energy-cyan/15 text-energy-cyan flex items-center justify-center border border-energy-cyan/30 shrink-0">
                            <i data-lucide="book-open-check" class="w-5 h-5 sm:w-6 sm:h-6"></i>
                        </div>
                        <div>
                            <h3 class="text-lg sm:text-xl font-bold text-white">Sekcja Dydaktyczno-Naukowa</h3>
                            <span class="text-[11px] sm:text-xs text-energy-cyan font-semibold uppercase tracking-wider block">Raporty & Analizy Rynku</span>
                        </div>
                    </div>
                    <p class="text-gray-300 text-xs sm:text-sm leading-relaxed mb-4">
                        Tworzenie specjalistycznych raportów i analiz rynkowych, publikacja artykułów, badania trendów dekarbonizacyjnych, prelekcje eksperckie oraz udział w konferencjach naukowych.
                    </p>
                    <div class="space-y-2 border-t border-white/10 pt-3 text-xs text-gray-300">
                        <div class="flex items-start gap-2"><i data-lucide="check" class="w-4 h-4 text-energy-cyan shrink-0 mt-0.5"></i> Opracowywanie raportów ESG i OZE</div>
                        <div class="flex items-start gap-2"><i data-lucide="check" class="w-4 h-4 text-energy-cyan shrink-0 mt-0.5"></i> Pisanie artykułów branżowych i wystąpienia</div>
                    </div>
                </div>

                <!-- Sekcja 3: HR -->
                <div class="glass-panel p-5 sm:p-7 rounded-2xl glass-panel-hover border border-white/10 relative overflow-hidden">
                    <div class="flex items-center gap-3.5 mb-3.5">
                        <div class="w-11 h-11 sm:w-12 sm:h-12 rounded-xl bg-energy-purple/15 text-energy-purple flex items-center justify-center border border-energy-purple/30 shrink-0">
                            <i data-lucide="users" class="w-5 h-5 sm:w-6 sm:h-6"></i>
                        </div>
                        <div>
                            <h3 class="text-lg sm:text-xl font-bold text-white">Sekcja HR</h3>
                            <span class="text-[11px] sm:text-xs text-energy-purple font-semibold uppercase tracking-wider block">Rekrutacja & Integracja Zespołu</span>
                        </div>
                    </div>
                    <p class="text-gray-300 text-xs sm:text-sm leading-relaxed mb-4">
                        Prowadzenie procesów rekrutacyjnych, dbanie o sprawny onboarding nowych członków, organizacja warsztatów wewnętrznych oraz dbaniem o integrację zespołu SKN Energy Team.
                    </p>
                    <div class="space-y-2 border-t border-white/10 pt-3 text-xs text-gray-300">
                        <div class="flex items-start gap-2"><i data-lucide="check" class="w-4 h-4 text-energy-purple shrink-0 mt-0.5"></i> Zarządzanie rekrutacją i onboardingiem</div>
                        <div class="flex items-start gap-2"><i data-lucide="check" class="w-4 h-4 text-energy-purple shrink-0 mt-0.5"></i> Spotkania integracyjne i szkolenia wewnętrzne</div>
                    </div>
                </div>

                <!-- Sekcja 4: Social Media -->
                <div class="glass-panel p-5 sm:p-7 rounded-2xl glass-panel-hover border border-white/10 relative overflow-hidden">
                    <div class="flex items-center gap-3.5 mb-3.5">
                        <div class="w-11 h-11 sm:w-12 sm:h-12 rounded-xl bg-energy-pink/15 text-pink-400 flex items-center justify-center border border-pink-500/30 shrink-0">
                            <i data-lucide="share-2" class="w-5 h-5 sm:w-6 sm:h-6"></i>
                        </div>
                        <div>
                            <h3 class="text-lg sm:text-xl font-bold text-white">Sekcja Social Media</h3>
                            <span class="text-[11px] sm:text-xs text-pink-400 font-semibold uppercase tracking-wider block">Marketing & Branding (@kozminskienergy)</span>
                        </div>
                    </div>
                    <p class="text-gray-300 text-xs sm:text-sm leading-relaxed mb-4">
                        Zarządzanie profilami na Instagramie i LinkedInie, produkcja atrakcyjnych materiałów wizualnych, edycja wideo, tworzenie kreacji graficznych oraz promocja wydarzeń.
                    </p>
                    <div class="space-y-2 border-t border-white/10 pt-3 text-xs text-gray-300">
                        <div class="flex items-start gap-2"><i data-lucide="check" class="w-4 h-4 text-pink-400 shrink-0 mt-0.5"></i> Kreacja grafik i treści na Instagram oraz LinkedIn</div>
                        <div class="flex items-start gap-2"><i data-lucide="check" class="w-4 h-4 text-pink-400 shrink-0 mt-0.5"></i> Kampanie promocyjne i budowanie marki koła</div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- Interactive 10-Question Recruitment Quiz Section -->
    <section id="quiz" class="py-14 sm:py-20 px-3 sm:px-4 relative">
        <div class="max-w-3xl mx-auto">
            <div class="text-center mb-8 sm:mb-10">
                <span class="text-energy-emerald text-xs font-bold uppercase tracking-widest">Interaktywny Test</span>
                <h2 class="text-2xl sm:text-3xl font-extrabold text-white mt-1">Quiz Rekrutacyjny SKN Energy Team</h2>
                <p class="text-gray-400 text-xs sm:text-sm mt-1.5 px-2">Sprawdź swoją wiedzę i dowiedz się, która z 4 sekcji najlepiej odpowiada Twoim pasjom!</p>
            </div>

            <div class="glass-panel rounded-2xl p-4 sm:p-7 border border-white/10 relative overflow-hidden shadow-2xl">
                
                <!-- Progress Header -->
                <div id="quiz-progress-container" class="mb-5">
                    <div class="flex justify-between items-center text-xs text-gray-400 mb-2">
                        <span id="question-tracker">Pytanie 1 z 10</span>
                        <span id="score-tracker" class="font-bold text-energy-emerald">Wynik: 0 pkt</span>
                    </div>
                    <div class="w-full bg-gray-800 rounded-full h-2 overflow-hidden">
                        <div id="progress-bar" class="bg-gradient-to-r from-energy-emerald via-energy-cyan to-energy-blue h-full w-[10%] transition-all duration-300"></div>
                    </div>
                </div>

                <!-- Active Question Container -->
                <div id="question-box">
                    <h3 id="question-text" class="text-base sm:text-lg md:text-xl font-bold text-white mb-5 leading-snug">
                        Ładowanie pytania...
                    </h3>

                    <div id="options-container" class="space-y-2.5 mb-5">
                        <!-- Dynamic Options injected here -->
                    </div>

                    <!-- Instant Feedback explanation -->
                    <div id="feedback-box" class="hidden p-3.5 sm:p-4 rounded-xl mb-5 text-xs sm:text-sm font-medium border flex items-start gap-2.5">
                        <i id="feedback-icon" data-lucide="info" class="w-4 h-4 sm:w-5 sm:h-5 shrink-0 mt-0.5"></i>
                        <span id="feedback-text" class="leading-relaxed"></span>
                    </div>

                    <button id="next-btn" onclick="nextQuestion()" disabled class="w-full py-3.5 px-5 rounded-xl font-bold text-gray-500 bg-gray-800 cursor-not-allowed transition-all flex items-center justify-center gap-2 min-h-[48px]">
                        <span>Następne pytanie</span>
                        <i data-lucide="arrow-right" class="w-4 h-4"></i>
                    </button>
                </div>

                <!-- Quiz Completion Screen -->
                <div id="result-box" class="hidden text-center py-2 sm:py-4">
                    <div class="w-14 h-14 sm:w-16 sm:h-16 bg-energy-emerald/20 text-energy-emerald rounded-full flex items-center justify-center mx-auto mb-3 border border-energy-emerald/40">
                        <i data-lucide="trophy" class="w-7 h-7 sm:w-8 sm:h-8"></i>
                    </div>

                    <h3 class="text-xl sm:text-2xl font-black text-white mb-1">Quiz Ukończony!</h3>
                    <p class="text-xs sm:text-sm text-gray-300 mb-4">Twój wynik: <span id="final-score" class="font-extrabold text-energy-emerald text-base sm:text-lg">0/10</span></p>

                    <!-- Matching Section Recommendation -->
                    <div class="p-4 sm:p-5 rounded-2xl glass-panel border border-energy-cyan/40 mb-5 text-left">
                        <div class="text-[10px] sm:text-xs text-gray-400 font-semibold uppercase mb-1">Rekomendowana sekcja:</div>
                        <div id="recommended-section-title" class="text-lg sm:text-xl font-extrabold text-gradient mb-1.5">Sekcja Dydaktyczno-Naukowa</div>
                        <p id="recommended-section-desc" class="text-xs text-gray-300 leading-relaxed">
                            Twój profil pasuje do prowadzenia analiz, tworzenia raportów rynkowych i udziału w konferencjach!
                        </p>
                    </div>

                    <a href="#rekrutacja" onclick="preselectSectionInForm()" class="w-full py-3.5 sm:py-4 rounded-xl font-bold text-black bg-gradient-btn flex items-center justify-center gap-2 text-xs sm:text-sm shadow-xl mb-3 min-h-[48px]">
                        <i data-lucide="send" class="w-4 h-4 text-black"></i>
                        <span>Aplikuj do rekomendowanej sekcji</span>
                    </a>

                    <button onclick="restartQuiz()" class="text-xs text-gray-400 hover:text-white underline inline-flex items-center gap-1.5 py-2">
                        <i data-lucide="rotate-ccw" class="w-3.5 h-3.5"></i>
                        Rozwiąż quiz ponownie
                    </button>
                </div>

            </div>
        </div>
    </section>

    <!-- Interactive Energy & ESG Calculator / Simulator Section -->
    <section id="kalkulator" class="py-14 sm:py-20 px-3 sm:px-4 bg-energy-darkCard/30 border-y border-white/5">
        <div class="max-w-5xl mx-auto">
            <div class="text-center mb-8 sm:mb-12">
                <span class="text-energy-cyan text-xs font-bold uppercase tracking-widest">Interaktywne Narzędzie</span>
                <h2 class="text-2xl sm:text-3xl font-extrabold text-white mt-1">Symulator Transformacji Energetycznej & ESG</h2>
                <p class="text-gray-400 text-xs sm:text-sm mt-1.5 max-w-xl mx-auto px-2">
                    Przesuwaj suwaki, aby symulować wpływ inwestycji w OZE oraz zielony wodór na redukcję emisji CO₂.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-12 gap-6 items-center">
                <!-- Sliders Control Panel -->
                <div class="lg:col-span-6 glass-panel p-4 sm:p-6 rounded-2xl space-y-5 border border-white/10">
                    <div>
                        <div class="flex justify-between text-xs sm:text-sm font-semibold mb-2">
                            <span class="text-gray-300">Udział OZE w Miksie (PV & Wiatr):</span>
                            <span id="renewables-value" class="text-energy-emerald font-bold">50%</span>
                        </div>
                        <input type="range" id="renewables-range" min="10" max="100" value="50" class="w-full h-3 bg-gray-800 rounded-lg appearance-none cursor-pointer accent-energy-emerald" oninput="updateCalculator()">
                    </div>

                    <div>
                        <div class="flex justify-between text-xs sm:text-sm font-semibold mb-2">
                            <span class="text-gray-300">Cel Redukcji CO₂ (Rocznie):</span>
                            <span id="co2-value" class="text-energy-cyan font-bold">100,000 t</span>
                        </div>
                        <input type="range" id="co2-range" min="10000" max="500000" step="10000" value="100000" class="w-full h-3 bg-gray-800 rounded-lg appearance-none cursor-pointer accent-energy-cyan" oninput="updateCalculator()">
                    </div>

                    <div>
                        <div class="flex justify-between text-xs sm:text-sm font-semibold mb-2">
                            <span class="text-gray-300">Moc Elektrolizerów Wodoru (H₂):</span>
                            <span id="h2-value" class="text-energy-blue font-bold">25 MW</span>
                        </div>
                        <input type="range" id="h2-range" min="0" max="100" value="25" class="w-full h-3 bg-gray-800 rounded-lg appearance-none cursor-pointer accent-energy-blue" oninput="updateCalculator()">
                    </div>

                    <div class="p-3.5 bg-energy-navy/80 rounded-xl border border-white/5 text-xs text-gray-400">
                        <p class="font-semibold text-gray-200 mb-1 flex items-center gap-1.5">
                            <i data-lucide="lightbulb" class="w-4 h-4 text-energy-emerald shrink-0"></i>
                            Ciekawostka Branżowa:
                        </p>
                        <p id="calc-fact" class="leading-relaxed">
                            Wyprodukowanie 1 tony zielonego wodoru wymaga ok. 50 MWh czystej energii z OZE i pozwala zastąpić paliwa kopalne w przemyśle.
                        </p>
                    </div>
                </div>

                <!-- Live Dynamic Output Metrics -->
                <div class="lg:col-span-6 grid grid-cols-2 gap-3 sm:gap-4">
                    <div class="glass-panel p-4 rounded-2xl text-center border-t-2 border-t-energy-emerald">
                        <i data-lucide="zap" class="w-6 h-6 text-energy-emerald mx-auto mb-1.5"></i>
                        <div id="out-power" class="text-lg sm:text-2xl font-black text-white">140,845 MWh</div>
                        <div class="text-[10px] sm:text-xs text-gray-400 mt-0.5">Czysta energia / rok</div>
                    </div>

                    <div class="glass-panel p-4 rounded-2xl text-center border-t-2 border-t-energy-cyan">
                        <i data-lucide="trees" class="w-6 h-6 text-energy-cyan mx-auto mb-1.5"></i>
                        <div id="out-trees" class="text-lg sm:text-2xl font-black text-white">4.5 mln</div>
                        <div class="text-[10px] sm:text-xs text-gray-400 mt-0.5">Zasadzone drzewa</div>
                    </div>

                    <div class="glass-panel p-4 rounded-2xl text-center border-t-2 border-t-energy-blue">
                        <i data-lucide="flame" class="w-6 h-6 text-energy-blue mx-auto mb-1.5"></i>
                        <div id="out-coal" class="text-lg sm:text-2xl font-black text-white">56,338 t</div>
                        <div class="text-[10px] sm:text-xs text-gray-400 mt-0.5">Zastąpiony węgiel</div>
                    </div>

                    <div class="glass-panel p-4 rounded-2xl text-center border-t-2 border-t-pink-500">
                        <i data-lucide="droplet" class="w-6 h-6 text-pink-400 mx-auto mb-1.5"></i>
                        <div id="out-h2-prod" class="text-lg sm:text-2xl font-black text-white">2,190 t</div>
                        <div class="text-[10px] sm:text-xs text-gray-400 mt-0.5">Zielony Wodór (H₂) / rok</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Direct Recruitment Form Section -->
    <section id="rekrutacja" class="py-14 sm:py-20 px-3 sm:px-4 relative">
        <div class="max-w-2xl mx-auto">
            <div class="text-center mb-8 sm:mb-10">
                <span class="text-pink-400 text-xs font-bold uppercase tracking-widest">Aplikuj Do Koła</span>
                <h2 class="text-2xl sm:text-3xl font-extrabold text-white mt-1">Formularz Rekrutacyjny</h2>
                <p class="text-gray-400 text-xs sm:text-sm mt-1.5 px-2">
                    Dołącz do SKN Energy Team w Akademii Leona Koźmińskiego!
                </p>
            </div>

            <div class="glass-panel rounded-2xl p-4 sm:p-8 border border-white/10 shadow-2xl">
                <form id="application-form" onsubmit="handleFormSubmit(event)" class="space-y-4">
                    <div>
                        <label class="block text-xs font-medium text-gray-300 mb-1">Imię i Nazwisko *</label>
                        <input type="text" required id="form-name" placeholder="np. Jan Kowalski" class="w-full px-3.5 py-3 rounded-xl bg-energy-navy/90 border border-white/10 text-white text-sm focus:outline-none focus:border-energy-emerald transition-colors min-h-[48px]">
                    </div>

                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-xs font-medium text-gray-300 mb-1">E-mail (Uczelniany / Prywatny) *</label>
                            <input type="email" required id="form-email" placeholder="np. 12345@kozminski.edu.pl" class="w-full px-3.5 py-3 rounded-xl bg-energy-navy/90 border border-white/10 text-white text-sm focus:outline-none focus:border-energy-emerald transition-colors min-h-[48px]">
                        </div>
                        <div>
                            <label class="block text-xs font-medium text-gray-300 mb-1">Poziom i Rok Studiów ALK *</label>
                            <select id="form-year" required class="w-full px-3.5 py-3 rounded-xl bg-energy-navy/90 border border-white/10 text-white text-sm focus:outline-none focus:border-energy-emerald transition-colors font-medium min-h-[48px]">
                                <option value="" disabled selected>Wybierz tryb i rok</option>
                                <optgroup label="Jednolite Studia Magisterskie (5-letnie)">
                                    <option value="1 Rok Jednolite Magisterskie">1 Rok - Jednolite Magisterskie</option>
                                    <option value="2 Rok Jednolite Magisterskie">2 Rok - Jednolite Magisterskie</option>
                                    <option value="3 Rok Jednolite Magisterskie">3 Rok - Jednolite Magisterskie</option>
                                    <option value="4 Rok Jednolite Magisterskie">4 Rok - Jednolite Magisterskie</option>
                                    <option value="5 Rok Jednolite Magisterskie">5 Rok - Jednolite Magisterskie</option>
                                </optgroup>
                                <optgroup label="Studia I Stopnia (Licencjackie / Inżynierskie)">
                                    <option value="1 Rok Licencjat">1 Rok - Licencjat / Inżynier</option>
                                    <option value="2 Rok Licencjat">2 Rok - Licencjat / Inżynier</option>
                                    <option value="3 Rok Licencjat">3 Rok - Licencjat / Inżynier</option>
                                </optgroup>
                                <optgroup label="Studia II Stopnia (Magisterskie)">
                                    <option value="1 Rok Magister">1 Rok - Magisterskie</option>
                                    <option value="2 Rok Magister">2 Rok - Magisterskie</option>
                                </optgroup>
                            </select>
                        </div>
                    </div>

                    <div>
                        <label class="block text-xs font-medium text-gray-300 mb-1">Wybierz Sekcję, do której aplikujesz *</label>
                        <select id="form-section" required class="w-full px-3.5 py-3 rounded-xl bg-energy-navy/90 border border-white/10 text-white text-sm focus:outline-none focus:border-energy-emerald transition-colors font-semibold min-h-[48px]">
                            <option value="Współpraca">Sekcja Współpraca (Partnerzy & Wizyty Studyjne)</option>
                            <option value="Dydaktyczno-Naukowa">Sekcja Dydaktyczno-Naukowa (Raporty & Konferencje)</option>
                            <option value="HR">Sekcja HR (Rekrutacja & Onboarding)</option>
                            <option value="Social Media">Sekcja Social Media (@kozminskienergy)</option>
                        </select>
                    </div>

                    <div>
                        <label class="block text-xs font-medium text-gray-300 mb-1">Krótka motywacja / profil Instagram (opcjonalnie)</label>
                        <textarea id="form-message" rows="3" placeholder="Dlaczego chcesz dołączyć? Twój nick na IG..." class="w-full px-3.5 py-3 rounded-xl bg-energy-navy/90 border border-white/10 text-white text-sm focus:outline-none focus:border-energy-emerald transition-colors resize-none"></textarea>
                    </div>

                    <button type="submit" class="w-full py-4 rounded-xl font-bold text-black bg-gradient-btn shadow-xl flex items-center justify-center gap-2 text-sm transition-all mt-3 min-h-[48px]">
                        <i data-lucide="send" class="w-4 h-4 text-black"></i>
                        <span>Wyślij Zgłoszenie Rekrutacyjne</span>
                    </button>
                </form>

                <!-- Success Confirmation Box -->
                <div id="form-success" class="hidden text-center py-6">
                    <div class="w-14 h-14 bg-energy-emerald/20 text-energy-emerald rounded-full flex items-center justify-center mx-auto mb-3 border border-energy-emerald/40">
                        <i data-lucide="check-circle-2" class="w-7 h-7"></i>
                    </div>
                    <h3 class="text-lg sm:text-xl font-bold text-white mb-2">Zgłoszenie Przyjęte!</h3>
                    <p class="text-xs sm:text-sm text-gray-300 mb-6 max-w-md mx-auto leading-relaxed">
                        Dziękujemy za zgłoszenie do <span id="success-section-name" class="font-bold text-energy-emerald">SKN Energy Team</span>. Skontaktujemy się z Tobą drogą mailową!
                    </p>
                    <a href="https://instagram.com/kozminskienergy" target="_blank" class="inline-flex items-center justify-center gap-2 px-5 py-3 rounded-xl font-bold text-white bg-gradient-to-r from-purple-600 to-pink-600 hover:opacity-90 transition-all text-xs min-h-[48px] w-full sm:w-auto">
                        <i data-lucide="instagram" class="w-4 h-4"></i>
                        <span>Obserwuj nas na Instagramie @kozminskienergy</span>
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="glass-panel border-t border-white/10 py-8 px-4 text-xs text-gray-400">
        <div class="max-w-6xl mx-auto flex flex-col md:flex-row items-center justify-between gap-4 text-center md:text-left">
            <div class="flex items-center gap-3">
                <div class="w-8 h-8 rounded-xl bg-energy-emerald/20 text-energy-emerald flex items-center justify-center font-bold border border-energy-emerald/30 shrink-0">
                    <i data-lucide="zap" class="w-4 h-4"></i>
                </div>
                <div>
                    <div class="text-white font-bold text-xs sm:text-sm">SKN Energy Team</div>
                    <div class="text-gray-400 text-[11px]">Akademia Leona Koźmińskiego w Warszawie</div>
                </div>
            </div>

            <div class="flex flex-wrap items-center justify-center gap-4 text-gray-300 font-medium text-xs">
                <a href="#sekcje" class="hover:text-energy-emerald transition-colors">Sekcje</a>
                <a href="#quiz" class="hover:text-energy-emerald transition-colors">Quiz</a>
                <a href="#kalkulator" class="hover:text-energy-emerald transition-colors">Symulator OZE</a>
                <a href="https://instagram.com/kozminskienergy" target="_blank" class="text-pink-400 hover:text-pink-300 transition-colors flex items-center gap-1">
                    <i data-lucide="instagram" class="w-3.5 h-3.5"></i>
                    <span>@kozminskienergy</span>
                </a>
            </div>

            <div class="text-gray-500 text-[11px]">
                &copy; 2026 SKN Energy Team Kozminski. Wszystkie prawa zastrzeżone.
            </div>
        </div>
    </footer>

    <!-- Application Logic Javascript -->
    <script>
        // Toggle mobile hamburger navigation overlay
        function toggleMobileMenu() {
            const menu = document.getElementById('mobile-menu');
            const icon = document.getElementById('menu-icon');
            const isHidden = menu.classList.contains('hidden');

            if (isHidden) {
                menu.classList.remove('hidden');
                icon.setAttribute('data-lucide', 'x');
            } else {
                menu.classList.add('hidden');
                icon.setAttribute('data-lucide', 'menu');
            }
            lucide.createIcons();
        }

        // 10 Recruitment Questions Mapping to the 4 Core Sections
        const quizQuestions = [
            {
                question: "Które źródło energii charakteryzuje się tzw. „efektem niestabilności produkcyjnej” zależnym bezpośrednio od warunków meteorologicznych w czasie rzeczywistym?",
                options: [
                    "Elektrownie atomowe i elektrociepłownie",
                    "Elektrownie fotowoltaiczne i farmy wiatrowe",
                    "Elektrownie wodne przepływowe",
                    "Elektrownie na biogaz rolniczy"
                ],
                correct: 1,
                sectionMatch: "Dydaktyczno-Naukowa",
                explanation: "Fotowoltaika i wiatr są źródłami pogodowo-zależnymi (OZE wariabilne), co wymaga bilansowania sieci."
            },
            {
                question: "Co oznacza skrót ESG w kontekście współczesnego biznesu energetycznego i finansów zrównoważonego rozwoju?",
                options: [
                    "Energy, Sustainability, and Green",
                    "Environmental, Social, and Governance",
                    "Ecological Standards and Growth",
                    "European Smart Grid"
                ],
                correct: 1,
                sectionMatch: "Dydaktyczno-Naukowa",
                explanation: "ESG to kryteria oceny przedsiębiorstw pod kątem Ochrony Środowiska, Odpowiedzialności Społecznej i Ładu Korporacyjnego."
            },
            {
                question: "Czym charakteryzują się umowy typu PPA (Power Purchase Agreement) na rynku energii?",
                options: [
                    "To krótkoterminowe pożyczki na budowę domowych mikroinstalacji",
                    "Są to długoterminowe umowy zakupu energii bezpośrednio między wytwórcą OZE a odbiorcą przemysłowym",
                    "To dotacje rządowe na wymianę pieców",
                    "To roczne umowy na prąd dla gospodarstw domowych"
                ],
                correct: 1,
                sectionMatch: "Współpraca",
                explanation: "Umowy PPA łączą wytwórców energii OZE z dużym biznesem przemysłowym i stanowią fundament finansowania OZE."
            },
            {
                question: "Jakie jest główne zadanie odpowiedzialnego zespołu HR podczas onboarding kandydata do koła naukowego?",
                options: [
                    "Stworzenie grafiki na Instagrama",
                    "Sprawne wprowadzenie w struktury, przydzielenie opiekuna i integracja z zespołem",
                    "Napisanie raportu rynkowego",
                    "Negocjacja umowy sponsorskiej"
                ],
                correct: 1,
                sectionMatch: "HR",
                explanation: "HR dba o to, aby każdy nowy członek koła szybko poczuł się częścią zespołu i wiedział, jakie ma zadania."
            },
            {
                question: "Jaki format materiałów wideo osiąga obecnie największe organiczne zasięgi w promocji wydarzeń studenckich na Instagramie?",
                options: [
                    "Prywatna wiadomość e-mail",
                    "Krótkie, dynamiczne wideo typu Reels / Rolki ze ścieżką dźwiękową",
                    "Długi plik PDF",
                    "Post tekstowy bez grafiki"
                ],
                correct: 1,
                sectionMatch: "Social Media",
                explanation: "Rolki na Instagramie (@kozminskienergy) pozwalają dotrzeć do tysięcy studentów zainteresowanych energią i OZE."
            },
            {
                question: "Co jest głównym celem organizacji wizyt studyjnych w spółkach energetycznych (np. PGE, Orlen, Veolia)?",
                options: [
                    "Tylko zrobienie pamiątkowego zdjęcia",
                    "Poznanie praktycznych aspektów funkcjonowania infrastruktury oraz budowanie relacji z partnerami",
                    "Weryfikacja biletów na uczelni",
                    "Zakup akcji na giełdzie"
                ],
                correct: 1,
                sectionMatch: "Współpraca",
                explanation: "Wizyty studyjne pozwalają członkom SKN zobaczyć od kulis najnowocześniejsze obiekty energetyczne w Polsce."
            },
            {
                question: "Co oznacza pojęcie „dekarbonizacja gospodarki”?",
                options: [
                    "Zakaz używania diamentów i grafitu w przemyśle",
                    "Systematyczne ograniczanie emisji gazów cieplarnianych, ze szczególnym uwzględnieniem CO2",
                    "Zamknięcie wszystkich fabryk chemicznych",
                    "Przejście na rozliczenia gotówkowe"
                ],
                correct: 1,
                sectionMatch: "Dydaktyczno-Naukowa",
                explanation: "Dekarbonizacja to proces przechodzenia na nisko- i zeroemisyjne źródła w przemyśle i energetyce."
            },
            {
                question: "Czym jest tzw. „zielony wodór” (H₂) produkowany w procesie elektrolizy?",
                options: [
                    "Wodorem wydobywanym ze złóż geologicznych",
                    "Wodorem otrzymywanym z wody przy użyciu energii elektrycznej pochodzącej ze źródeł odnawialnych",
                    "Wodorem barwionym barwnikiem organicznym",
                    "Gazem z wysypisk śmieci"
                ],
                correct: 1,
                sectionMatch: "Dydaktyczno-Naukowa",
                explanation: "Zielony wodór powstaje w procesie elektrolizy wody zasilanej wyłącznie czystą energią z OZE."
            },
            {
                question: "Które narzędzie jest kluczowe w pracy zespołu Social Media przy planowaniu spójnego wizerunku koła?",
                options: [
                    "Kalkulator CO2",
                    "Harmonogram publikacji (Content Plan) i identyfikacja wizualna w Canvie/Adobe",
                    "Umowa cywilnoprawna",
                    "Giełda Towarowa"
                ],
                correct: 1,
                sectionMatch: "Social Media",
                explanation: "Content plan pozwala regularnie edukować obserwujących na profilu @kozminskienergy."
            },
            {
                question: "Co jest kluczowe dla budowania zaangażowania i dobrej atmosfery wewnątrz SKN Energy Team?",
                options: [
                    "Brak komunikacji między sekcjami",
                    "Regularne spotkania integracyjne, warsztaty i jasny feedback ze strony Sekcji HR",
                    "Praca wyłącznie indywidualna",
                    "Anulowanie zebrań"
                ],
                correct: 1,
                sectionMatch: "HR",
                explanation: "Dobra atmosfera i dbanie o potrzeby członków zespołu gwarantują sukces i wysokie morale w kole."
            }
        ];

        // Quiz State
        let currentQIndex = 0;
        let quizScore = 0;
        let selectedChoice = null;
        let sectionScores = {
            "Współpraca": 0,
            "Dydaktyczno-Naukowa": 0,
            "HR": 0,
            "Social Media": 0
        };

        window.onload = function() {
            lucide.createIcons();
            loadQuizQuestion();
            updateCalculator();
        };

        function loadQuizQuestion() {
            const q = quizQuestions[currentQIndex];
            selectedChoice = null;

            document.getElementById('question-tracker').innerText = `Pytanie ${currentQIndex + 1} z ${quizQuestions.length}`;
            document.getElementById('score-tracker').innerText = `Wynik: ${quizScore} pkt`;
            document.getElementById('progress-bar').style.width = `${((currentQIndex + 1) / quizQuestions.length) * 100}%`;

            document.getElementById('question-text').innerText = q.question;
            document.getElementById('feedback-box').classList.add('hidden');

            const nextBtn = document.getElementById('next-btn');
            nextBtn.disabled = true;
            nextBtn.className = "w-full py-3.5 px-5 rounded-xl font-bold text-gray-500 bg-gray-800 cursor-not-allowed transition-all flex items-center justify-center gap-2 min-h-[48px]";

            const optionsContainer = document.getElementById('options-container');
            optionsContainer.innerHTML = '';

            q.options.forEach((opt, idx) => {
                const btn = document.createElement('button');
                btn.className = `w-full text-left p-3.5 sm:p-4 rounded-xl text-xs sm:text-sm font-medium border border-white/10 bg-energy-navy/60 text-gray-200 hover:border-energy-cyan hover:bg-white/5 transition-all flex items-center justify-between gap-2 group min-h-[48px]`;
                btn.onclick = () => selectQuizChoice(idx);
                btn.innerHTML = `
                    <span class="flex items-center gap-2.5">
                        <span class="w-5 h-5 sm:w-6 sm:h-6 rounded-full bg-white/5 border border-white/20 text-[11px] sm:text-xs flex items-center justify-center group-hover:border-energy-cyan text-gray-400 font-bold shrink-0">${String.fromCharCode(65 + idx)}</span>
                        <span class="leading-tight">${opt}</span>
                    </span>
                    <i data-lucide="circle" class="w-4 h-4 text-gray-500 opacity-50 shrink-0"></i>
                `;
                optionsContainer.appendChild(btn);
            });

            lucide.createIcons();
        }

        function selectQuizChoice(idx) {
            if (selectedChoice !== null) return;
            selectedChoice = idx;

            const q = quizQuestions[currentQIndex];
            const options = document.getElementById('options-container').children;
            const feedbackBox = document.getElementById('feedback-box');
            const feedbackText = document.getElementById('feedback-text');

            if (idx === q.correct) {
                quizScore++;
                sectionScores[q.sectionMatch] = (sectionScores[q.sectionMatch] || 0) + 1;

                options[idx].className = "w-full text-left p-3.5 sm:p-4 rounded-xl text-xs sm:text-sm font-medium border-2 border-energy-emerald bg-energy-emerald/10 text-white flex items-center justify-between gap-2 min-h-[48px]";
                options[idx].querySelector('[data-lucide]').setAttribute('data-lucide', 'check-circle-2');
                options[idx].querySelector('[data-lucide]').className = "w-4 h-4 sm:w-5 sm:h-5 text-energy-emerald shrink-0";

                feedbackBox.className = "p-3.5 sm:p-4 rounded-xl mb-5 text-xs sm:text-sm font-medium border border-energy-emerald/30 bg-energy-emerald/10 text-energy-emerald flex items-start gap-2.5";
                feedbackText.innerText = `Świetnie! ${q.explanation}`;
            } else {
                options[idx].className = "w-full text-left p-3.5 sm:p-4 rounded-xl text-xs sm:text-sm font-medium border-2 border-red-500 bg-red-500/10 text-white flex items-center justify-between gap-2 min-h-[48px]";
                options[idx].querySelector('[data-lucide]').setAttribute('data-lucide', 'x-circle');
                options[idx].querySelector('[data-lucide]').className = "w-4 h-4 sm:w-5 sm:h-5 text-red-400 shrink-0";

                options[q.correct].className = "w-full text-left p-3.5 sm:p-4 rounded-xl text-xs sm:text-sm font-medium border border-energy-emerald/60 bg-energy-emerald/5 text-gray-200 flex items-center justify-between gap-2 min-h-[48px]";

                feedbackBox.className = "p-3.5 sm:p-4 rounded-xl mb-5 text-xs sm:text-sm font-medium border border-red-500/30 bg-red-500/10 text-red-300 flex items-start gap-2.5";
                feedbackText.innerText = `Odpowiedź niepoprawna. Prawidłowa: "${q.options[q.correct]}". ${q.explanation}`;
            }

            feedbackBox.classList.remove('hidden');

            const nextBtn = document.getElementById('next-btn');
            nextBtn.disabled = false;
            nextBtn.className = "w-full py-3.5 px-5 rounded-xl font-bold text-black bg-gradient-btn hover:opacity-95 shadow-lg transition-all flex items-center justify-center gap-2 cursor-pointer min-h-[48px]";

            document.getElementById('score-tracker').innerText = `Wynik: ${quizScore} pkt`;
            lucide.createIcons();
        }

        function nextQuestion() {
            if (currentQIndex < quizQuestions.length - 1) {
                currentQIndex++;
                loadQuizQuestion();
            } else {
                finishQuiz();
            }
        }

        function finishQuiz() {
            document.getElementById('question-box').classList.add('hidden');
            document.getElementById('quiz-progress-container').classList.add('hidden');
            document.getElementById('result-box').classList.remove('hidden');

            document.getElementById('final-score').innerText = `${quizScore} / ${quizQuestions.length}`;

            // Find best matching section
            let bestSection = "Dydaktyczno-Naukowa";
            let maxVal = -1;
            for (const [sec, val] of Object.entries(sectionScores)) {
                if (val > maxVal) {
                    maxVal = val;
                    bestSection = sec;
                }
            }

            const titleEl = document.getElementById('recommended-section-title');
            const descEl = document.getElementById('recommended-section-desc');

            if (bestSection === "Współpraca") {
                titleEl.innerText = "Sekcja Współpraca";
                descEl.innerText = "Twoje odpowiedzi wskazują na talent do budowania relacji biznesowych, organizowania wizyt studyjnych i pozyskiwania partnerów!";
            } else if (bestSection === "HR") {
                titleEl.innerText = "Sekcja HR";
                descEl.innerText = "Doskonale czujesz potrzeby zespołu! Świetnie sprawdzisz się w rekrutacji, onboardingu i integracji nowych członków SKN Energy Team.";
            } else if (bestSection === "Social Media") {
                titleEl.innerText = "Sekcja Social Media";
                descEl.innerText = "Masz zmysł marketingowy i wizualny! Idealnie pasujesz do prowadzenia profilu @kozminskienergy na Instagramie i tworzenia kreacji.";
            } else {
                titleEl.innerText = "Sekcja Dydaktyczno-Naukowa";
                descEl.innerText = "Twoje analityczne podejście czyni Cię idealnym kandydatem do opracowywania raportów rynkowych OZE/ESG i udziału w konferencjach.";
            }
        }

        function preselectSectionInForm() {
            const recommendedTitle = document.getElementById('recommended-section-title').innerText;
            const selectEl = document.getElementById('form-section');
            if (recommendedTitle.includes("Współpraca")) selectEl.value = "Współpraca";
            else if (recommendedTitle.includes("HR")) selectEl.value = "HR";
            else if (recommendedTitle.includes("Social")) selectEl.value = "Social Media";
            else selectEl.value = "Dydaktyczno-Naukowa";
        }

        function restartQuiz() {
            currentQIndex = 0;
            quizScore = 0;
            sectionScores = { "Współpraca": 0, "Dydaktyczno-Naukowa": 0, "HR": 0, "Social Media": 0 };
            document.getElementById('result-box').classList.add('hidden');
            document.getElementById('question-box').classList.remove('hidden');
            document.getElementById('quiz-progress-container').classList.remove('hidden');
            loadQuizQuestion();
        }

        // Interactive Simulator Logic
        function updateCalculator() {
            const renewables = parseInt(document.getElementById('renewables-range').value);
            const co2Goal = parseInt(document.getElementById('co2-range').value);
            const h2MW = parseInt(document.getElementById('h2-range').value);

            document.getElementById('renewables-value').innerText = `${renewables}%`;
            document.getElementById('co2-value').innerText = `${co2Goal.toLocaleString()} t`;
            document.getElementById('h2-value').innerText = `${h2MW} MW`;

            // Calculations
            const powerMWh = Math.round((co2Goal / 0.71) * (renewables / 50));
            const treesMillion = ((co2Goal * 45) / 1000000).toFixed(1);
            const coalTons = Math.round(powerMWh * 0.4);
            const h2Tons = Math.round((h2MW * 8760 * 0.6) / 50);

            document.getElementById('out-power').innerText = `${powerMWh.toLocaleString()} MWh`;
            document.getElementById('out-trees').innerText = `${treesMillion} mln`;
            document.getElementById('out-coal').innerText = `${coalTons.toLocaleString()} t`;
            document.getElementById('out-h2-prod').innerText = `${h2Tons.toLocaleString()} t`;
        }

        // Recruitment Form Submission
        function handleFormSubmit(e) {
            e.preventDefault();
            const section = document.getElementById('form-section').value;
            document.getElementById('success-section-name').innerText = `Sekcji ${section}`;
            document.getElementById('application-form').classList.add('hidden');
            document.getElementById('form-success').classList.remove('hidden');
        }
    </script>
</body>
</html>
