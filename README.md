!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>OSF Link - ì˜¤ëšœê¸°SF í’ˆì§ˆí”Œëž«í¼</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        
        :root {
            /* ë” ìžì—°ìŠ¤ëŸ½ê³  ì„ ëª…í•œ ì˜¤ëšœê¸° ì»¬ëŸ¬ */
            --primary: #E53E3E;         /* ì˜¤ëšœê¸° ë ˆë“œ */
            --primary-light: #FC8181;   /* ë°ì€ ë ˆë“œ */
            --primary-dark: #C53030;    /* ê¹Šì€ ë ˆë“œ */
            --accent: #FDB02C;          /* ì˜¤ëšœê¸° ì˜ë¡œìš° */
            --secondary: #ED8936;       /* ì˜¤ë Œì§€ */
            --success: #38A169;         /* ì„±ê³µ ê·¸ë¦° */
            --cream: #FFFAF0;           /* í¬ë¦¼ ë°°ê²½ */
            --warm-white: #FFFFFF;      /* ìˆœë°±ìƒ‰ */
            --text-dark: #2D3748;       /* ë‹¤í¬ í…ìŠ¤íŠ¸ */
            --text-light: #4A5568;      /* ë¼ì´íŠ¸ í…ìŠ¤íŠ¸ */
        }
        
        body { 
            font-family: 'Inter', sans-serif;
            background: var(--cream);
        }
        
        .hidden { display: none !important; }
        
        /* ê·¸ë¼ë°ì´ì…˜ ì œê±°, ë‹¨ìƒ‰ ì‚¬ìš© */
        .bg-primary { background-color: var(--primary); }
        .bg-primary-light { background-color: var(--primary-light); }
        .bg-accent { background-color: var(--accent); }
        .bg-secondary { background-color: var(--secondary); }
        .bg-success { background-color: var(--success); }
        
        /* ê°„ì†Œí™”ëœ ê·¸ë¦¼ìž */
        .shadow-soft {
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
        }
        
        .shadow-medium {
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
        }
        
        /* í€´ì¦ˆ ì˜µì…˜ ìŠ¤íƒ€ì¼ */
        .quiz-option.selected { 
            background-color: #FEF5E7;
            border: 2px solid var(--accent);
            color: var(--text-dark);
        }
        .quiz-option.correct { 
            background-color: var(--success);
            border: 2px solid var(--success);
            color: white;
        }
        .quiz-option.wrong { 
            background-color: #FED7D7;
            border: 2px solid #E53E3E;
            color: #E53E3E;
        }
        
        /* ê°„ì†Œí™”ëœ í˜¸ë²„ íš¨ê³¼ */
        .hover-lift:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.12);
        }
        
        /* ë²„íŠ¼ ìŠ¤íƒ€ì¼ */
        .btn-primary {
            background-color: var(--primary);
            color: white;
            font-weight: 600;
            transition: all 0.2s ease;
        }
        
        .btn-primary:hover {
            background-color: var(--primary-dark);
            transform: translateY(-1px);
        }
        
        .btn-accent {
            background-color: var(--accent);
            color: var(--text-dark);
            font-weight: 600;
        }
        
        .btn-success {
            background-color: var(--success);
            color: white;
            font-weight: 600;
        }
        
        .btn-secondary {
            background-color: var(--secondary);
            color: white;
            font-weight: 600;
        }
        
        /* ìƒíƒœ ë°°ì§€ */
        .badge-completed {
            background-color: var(--success);
            color: white;
        }
        
        .badge-progress {
            background-color: var(--accent);
            color: var(--text-dark);
        }
        
        .badge-admin {
            background-color: var(--primary);
            color: white;
        }
        
        /* ì¹´ë“œ ìŠ¤íƒ€ì¼ */
        .card {
            background: white;
            border: 1px solid #E2E8F0;
            border-radius: 16px;
        }
        
        /* ê°„ì†Œí™”ëœ ì• ë‹ˆë©”ì´ì…˜ */
        .fade-in {
            animation: fadeIn 0.3s ease-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* ì˜¤ëšœê¸° ë¡œê³  ìŠ¤íƒ€ì¼ */
        .ottogi-logo {
            width: 60px;
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .ottogi-logo-large {
            width: 80px;
            height: 80px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .ottogi-svg {
            width: 100%;
            height: 100%;
        }
    </style>
</head>
<body>
    <!-- ë¡œê·¸ì¸ í™”ë©´ -->
    <div id="loginScreen" class="min-h-screen flex flex-col justify-center items-center px-8">
        <div class="w-full max-w-md fade-in">
            <div class="text-center mb-12">
                <div class="ottogi-logo-large mx-auto mb-8 shadow-medium">
                    <img src="https://www.otoki.com/images/common/logo.png" alt="ì˜¤ëšœê¸° ë¡œê³ " class="w-full h-full object-contain"
                         onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                    <!-- ë°±ì—… SVG ë¡œê³  -->
                    <svg class="ottogi-svg" style="display: none;" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                        <circle cx="50" cy="50" r="48" fill="#E53E3E" stroke="#C53030" stroke-width="2"/>
                        <circle cx="50" cy="50" r="35" fill="white"/>
                        <circle cx="50" cy="40" r="18" fill="#E53E3E"/>
                        <circle cx="50" cy="40" r="15" fill="white"/>
                        <path d="M44 37 Q46 35 48 37" stroke="#E53E3E" stroke-width="2" fill="none"/>
                        <path d="M52 37 Q54 35 56 37" stroke="#E53E3E" stroke-width="2" fill="none"/>
                        <circle cx="50" cy="40" r="1.5" fill="#E53E3E"/>
                        <path d="M46 43 Q50 46 54 43" stroke="#E53E3E" stroke-width="2" fill="none"/>
                        <path d="M42 32 Q45 28 50 30 Q55 28 58 32" stroke="#E53E3E" stroke-width="2" fill="none"/>
                        <rect x="30" y="55" width="40" height="20" rx="10" fill="white" stroke="#E53E3E" stroke-width="1"/>
                        <text x="50" y="67" font-family="Arial, sans-serif" font-size="8" font-weight="bold" fill="#E53E3E" text-anchor="middle">ì˜¤ëšœê¸°</text>
                    </svg>
                </div>
                <h1 class="text-5xl font-bold text-gray-800 mb-3">OSF Link</h1>
                <p class="text-gray-600 text-lg font-medium">ì˜¤ëšœê¸°SF í’ˆì§ˆí”Œëž«í¼</p>
                <div class="w-16 h-1 bg-primary rounded-full mx-auto mt-4"></div>
            </div>
            
            <div class="card shadow-medium p-10 space-y-6">
                <input
                    id="employeeId"
                    type="text"
                    placeholder="ì‚¬ë²ˆì„ ìž…ë ¥í•˜ì„¸ìš”"
                    class="w-full px-6 py-4 border-2 border-gray-200 rounded-xl text-gray-700 bg-white focus:border-red-400 focus:outline-none transition-colors"
                />
                <input
                    id="password"
                    type="password"
                    placeholder="íŒ¨ìŠ¤ì›Œë“œë¥¼ ìž…ë ¥í•˜ì„¸ìš”"
                    class="w-full px-6 py-4 border-2 border-gray-200 rounded-xl text-gray-700 bg-white focus:border-red-400 focus:outline-none transition-colors"
                />
                <button
                    onclick="handleLogin()"
                    class="w-full btn-primary py-4 rounded-xl text-lg shadow-soft"
                >
                    ë¡œê·¸ì¸
                </button>
            </div>
        </div>
    </div>

    <!-- ë©”ì¸ í™”ë©´ -->
    <div id="mainScreen" class="hidden min-h-screen">
        <div class="bg-primary text-white py-8 px-6 shadow-medium">
            <div class="flex items-center justify-between">
                <div class="flex items-center space-x-4">
                    <div class="ottogi-logo">
                        <img src="https://www.otoki.com/images/common/logo.png" alt="ì˜¤ëšœê¸° ë¡œê³ " class="w-full h-full object-contain"
                             onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                        <!-- ë°±ì—… SVG ë¡œê³  -->
                        <svg class="ottogi-svg" style="display: none;" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                            <circle cx="50" cy="50" r="48" fill="#E53E3E" stroke="#C53030" stroke-width="2"/>
                            <circle cx="50" cy="50" r="35" fill="white"/>
                            <circle cx="50" cy="40" r="18" fill="#E53E3E"/>
                            <circle cx="50" cy="40" r="15" fill="white"/>
                            <path d="M44 37 Q46 35 48 37" stroke="#E53E3E" stroke-width="2" fill="none"/>
                            <path d="M52 37 Q54 35 56 37" stroke="#E53E3E" stroke-width="2" fill="none"/>
                            <circle cx="50" cy="40" r="1.5" fill="#E53E3E"/>
                            <path d="M46 43 Q50 46 54 43" stroke="#E53E3E" stroke-width="2" fill="none"/>
                            <path d="M42 32 Q45 28 50 30 Q55 28 58 32" stroke="#E53E3E" stroke-width="2" fill="none"/>
                            <rect x="30" y="55" width="40" height="20" rx="10" fill="white" stroke="#E53E3E" stroke-width="1"/>
                            <text x="50" y="67" font-family="Arial, sans-serif" font-size="8" font-weight="bold" fill="#E53E3E" text-anchor="middle">ì˜¤ëšœê¸°</text>
                        </svg>
                    </div>
                    <div>
                        <h1 class="text-3xl font-bold">OSF Link</h1>
                        <p id="adminMode" class="text-sm text-red-100 hidden font-medium">âš¡ ê´€ë¦¬ìž ëª¨ë“œ</p>
                    </div>
                </div>
                <div class="flex items-center space-x-4">
                    <button id="saveAllBtn" onclick="saveAllFiles()" class="hidden btn-success px-4 py-3 rounded-xl transition-all flex items-center space-x-2 shadow-soft">
                        <span class="text-xl">ðŸ’¾</span>
                        <span class="text-sm">ëª¨ë‘ ì €ìž¥</span>
                    </button>
                </div>
            </div>
        </div>
        
        <div class="p-8">
            <div class="grid grid-cols-1 gap-6">
                <!-- ì›”ë³„êµìœ¡ -->
                <div onclick="showScreen('education')" class="card shadow-soft p-8 cursor-pointer hover-lift transition-all duration-200">
                    <div class="flex items-center justify-between">
                        <div class="flex items-center space-x-6">
                            <div class="w-16 h-16 bg-primary rounded-xl flex items-center justify-center shadow-soft">
                                <span class="text-white text-2xl">ðŸ“š</span>
                            </div>
                            <div>
                                <h3 class="text-xl font-bold text-gray-800 mb-1">ì›”ë³„êµìœ¡</h3>
                                <p class="text-gray-600 font-medium">êµìœ¡ê³¼ì • ë° í€´ì¦ˆ í‰ê°€</p>
                            </div>
                        </div>
                        <span class="text-gray-400 text-2xl">â€º</span>
                    </div>
                </div>

                <!-- ê³µì§€ì‚¬í•­ -->
                <div onclick="showScreen('notice')" class="card shadow-soft p-8 cursor-pointer hover-lift transition-all duration-200">
                    <div class="flex items-center justify-between">
                        <div class="flex items-center space-x-6">
                            <div class="w-16 h-16 bg-accent rounded-xl flex items-center justify-center shadow-soft">
                                <span class="text-gray-800 text-2xl">ðŸ“¢</span>
                            </div>
                            <div>
                                <h3 class="text-xl font-bold text-gray-800 mb-1">ê³µì§€ì‚¬í•­</h3>
                                <p class="text-gray-600 font-medium">ì¤‘ìš”í•œ ì•Œë¦¼ ë° ê³µì§€</p>
                            </div>
                        </div>
                        <span class="text-gray-400 text-2xl">â€º</span>
                    </div>
                </div>

                <!-- ê±´ì˜í•¨ -->
                <div onclick="showScreen('suggestion')" class="card shadow-soft p-8 cursor-pointer hover-lift transition-all duration-200">
                    <div class="flex items-center justify-between">
                        <div class="flex items-center space-x-6">
                            <div class="w-16 h-16 bg-success rounded-xl flex items-center justify-center shadow-soft">
                                <span class="text-white text-2xl">ðŸ’¡</span>
                            </div>
                            <div>
                                <h3 class="text-xl font-bold text-gray-800 mb-1">ì‹í’ˆì•ˆì „ ë° í’ˆì§ˆê°œì„  ê±´ì˜í•¨</h3>
                                <p class="text-gray-600 font-medium">ê°œì„ ì‚¬í•­ ì œì•ˆ ë° ì•„ì´ë””ì–´</p>
                            </div>
                        </div>
                        <span class="text-gray-400 text-2xl">â€º</span>
                    </div>
                </div>

                <!-- ì„¤ì • -->
                <div onclick="showScreen('settings')" class="card shadow-soft p-8 cursor-pointer hover-lift transition-all duration-200">
                    <div class="flex items-center justify-between">
                        <div class="flex items-center space-x-6">
                            <div class="w-16 h-16 bg-secondary rounded-xl flex items-center justify-center shadow-soft">
                                <span class="text-white text-2xl">âš™ï¸</span>
                            </div>
                            <div>
                                <h3 class="text-xl font-bold text-gray-800 mb-1">ì„¤ì •</h3>
                                <p class="text-gray-600 font-medium">í”„ë¡œí•„ ë° ì•± í™˜ê²½ì„¤ì •</p>
                            </div>
                        </div>
                        <span class="text-gray-400 text-2xl">â€º</span>
                    </div>
                </div>

                <!-- ê´€ë¦¬ìž ì „ìš© ì‚¬ìš©ìž ê´€ë¦¬ -->
                <div id="userManagementMenu" onclick="showScreen('userManagement')" class="hidden card shadow-soft p-8 cursor-pointer hover-lift transition-all duration-200 border border-orange-200">
                    <div class="flex items-center justify-between">
                        <div class="flex items-center space-x-6">
                            <div class="w-16 h-16 bg-primary rounded-xl flex items-center justify-center shadow-soft">
                                <span class="text-white text-2xl">ðŸ‘¥</span>
                            </div>
                            <div>
                                <h3 class="text-xl font-bold text-gray-800 mb-1">ì‚¬ìš©ìž ê´€ë¦¬</h3>
                                <p class="text-gray-600 font-medium">ì§„ë„ í˜„í™© ë° í€´ì¦ˆ ì ìˆ˜ ê´€ë¦¬</p>
                            </div>
                        </div>
                        <div class="flex items-center space-x-3">
                            <span class="badge-admin text-xs px-3 py-2 rounded-full font-bold">ADMIN</span>
                            <span class="text-gray-400 text-2xl">â€º</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- ì›”ë³„êµìœ¡ í™”ë©´ -->
    <div id="educationScreen" class="hidden min-h-screen">
        <div class="bg-primary text-white py-6 px-6 flex items-center justify-between shadow-medium">
            <div class="flex items-center">
                <button onclick="showScreen('main')" class="mr-6 text-white hover:text-red-200 transition-colors text-3xl">â†</button>
                <div class="flex items-center space-x-4">
                    <span class="text-3xl">ðŸ“š</span>
                    <h1 class="text-3xl font-bold">ì›”ë³„êµìœ¡</h1>
                </div>
            </div>
        </div>
        
        <div class="p-8">
            <div class="space-y-6" id="educationList">
                <!-- êµìœ¡ ëª©ë¡ì´ ì—¬ê¸°ì— ë™ì ìœ¼ë¡œ ìƒì„±ë©ë‹ˆë‹¤ -->
            </div>
        </div>
    </div>

    <!-- ê³µì§€ì‚¬í•­ í™”ë©´ -->
    <div id="noticeScreen" class="hidden min-h-screen">
        <div class="bg-primary text-white py-6 px-6 flex items-center justify-between shadow-medium">
            <div class="flex items-center">
                <button onclick="showScreen('main')" class="mr-6 text-white hover:text-red-200 transition-colors text-3xl">â†</button>
                <div class="flex items-center space-x-4">
                    <span class="text-3xl">ðŸ“¢</span>
                    <h1 class="text-3xl font-bold">ê³µì§€ì‚¬í•­</h1>
                </div>
            </div>
            <button id="writeNoticeBtn" onclick="toggleNoticeForm()" class="hidden bg-white bg-opacity-20 hover:bg-opacity-30 px-6 py-3 rounded-xl transition-all font-medium">
                âœï¸ ìž‘ì„±
            </button>
        </div>
        
        <div class="p-8">
            <!-- ê³µì§€ì‚¬í•­ ìž‘ì„± í¼ -->
            <div id="noticeForm" class="hidden card shadow-soft p-8 mb-8">
                <h3 class="text-2xl font-bold text-gray-800 mb-6">ðŸ“ ê³µì§€ì‚¬í•­ ìž‘ì„±</h3>
                <input
                    id="noticeTitle"
                    type="text"
                    placeholder="ì œëª©ì„ ìž…ë ¥í•˜ì„¸ìš”"
                    class="w-full px-6 py-4 border-2 border-gray-200 rounded-xl text-gray-800 bg-white focus:border-red-400 focus:outline-none transition-all mb-6"
                />
                <textarea
                    id="noticeContent"
                    placeholder="ë‚´ìš©ì„ ìž…ë ¥í•˜ì„¸ìš”"
                    rows="6"
                    class="w-full px-6 py-4 border-2 border-gray-200 rounded-xl text-gray-800 bg-white focus:border-red-400 focus:outline-none transition-all mb-6"
                ></textarea>
                <button
                    onclick="addNotice()"
                    class="btn-primary px-8 py-4 rounded-xl shadow-soft"
                >
                    ðŸ“¤ ë“±ë¡í•˜ê¸°
                </button>
            </div>

            <div id="noticeList">
                <div class="card shadow-soft p-12 text-center">
                    <span class="text-6xl mb-6 block">ðŸ“¢</span>
                    <span class="text-gray-600 text-xl font-medium">ê³µì§€ì‚¬í•­ì´ ì—†ìŠµë‹ˆë‹¤.</span>
                </div>
            </div>
        </div>
    </div>

    <!-- ê±´ì˜í•¨ í™”ë©´ -->
    <div id="suggestionScreen" class="hidden min-h-screen">
        <div class="bg-primary text-white py-6 px-6 flex items-center shadow-medium">
            <button onclick="showScreen('main')" class="mr-6 text-white hover:text-red-200 transition-colors text-3xl">â†</button>
            <div class="flex items-center space-x-4">
                <span class="text-3xl">ðŸ’¡</span>
                <h1 class="text-3xl font-bold">ì‹í’ˆì•ˆì „ ë° í’ˆì§ˆê°œì„  ê±´ì˜í•¨</h1>
            </div>
        </div>
        
        <div class="p-8">
            <div class="card shadow-medium p-12 text-center">
                <div class="w-20 h-20 bg-success rounded-full mx-auto mb-8 flex items-center justify-center shadow-soft">
                    <span class="text-4xl">ðŸ“</span>
                </div>
                <h3 class="text-2xl font-bold text-gray-800 mb-6">ê±´ì˜ì‚¬í•­ì„ ìž‘ì„±í•´ì£¼ì„¸ìš”</h3>
                <p class="text-gray-600 mb-8 text-lg font-medium">ë§í¬ë¥¼ í†µí•´ ê±´ì˜ì‚¬í•­ì„ ì œì¶œí•˜ì‹¤ ìˆ˜ ìžˆìŠµë‹ˆë‹¤.</p>
                <button
                    onclick="openGoogleForm()"
                    class="btn-success px-10 py-4 rounded-xl hover-lift transition-all shadow-soft flex items-center space-x-3 mx-auto text-lg"
                >
                    <span class="text-2xl">ðŸ”—</span>
                    <span>ê±´ì˜í•¨ ì—´ê¸°</span>
                </button>
            </div>
        </div>
    </div>

    <!-- ì„¤ì • í™”ë©´ -->
    <div id="settingsScreen" class="hidden min-h-screen">
        <div class="bg-primary text-white py-6 px-6 flex items-center shadow-medium">
            <button onclick="showScreen('main')" class="mr-6 text-white hover:text-red-200 transition-colors text-3xl">â†</button>
            <div class="flex items-center space-x-4">
                <span class="text-3xl">âš™ï¸</span>
                <h1 class="text-3xl font-bold">ì„¤ì •</h1>
            </div>
        </div>
        
        <div class="p-8">
            <div class="space-y-6">
                <div onclick="openProfileModal()" class="card shadow-soft p-6 cursor-pointer hover-lift transition-all duration-200">
                    <div class="flex items-center justify-between">
                        <div class="flex items-center space-x-6">
                            <div class="w-14 h-14 bg-primary rounded-xl flex items-center justify-center shadow-soft">
                                <span class="text-2xl">ðŸ‘¤</span>
                            </div>
                            <span class="text-xl font-bold text-gray-800">ë‚´ í”„ë¡œí•„</span>
                        </div>
                        <span class="text-gray-400 text-2xl">â€º</span>
                    </div>
                </div>

                <div onclick="openNotificationModal()" class="card shadow-soft p-6 cursor-pointer hover-lift transition-all duration-200">
                    <div class="flex items-center justify-between">
                        <div class="flex items-center space-x-6">
                            <div class="w-14 h-14 bg-accent rounded-xl flex items-center justify-center shadow-soft">
                                <span class="text-2xl">ðŸ””</span>
                            </div>
                            <span class="text-xl font-bold text-gray-800">ì•Œë¦¼ì„¤ì •</span>
                        </div>
                        <span class="text-gray-400 text-2xl">â€º</span>
                    </div>
                </div>

                <div class="card shadow-soft p-6 cursor-pointer hover-lift transition-all duration-200" onclick="handleLogout()">
                    <div class="flex items-center justify-between">
                        <div class="flex items-center space-x-6">
                            <div class="w-14 h-14 bg-red-500 rounded-xl flex items-center justify-center shadow-soft">
                                <span class="text-2xl">ðŸšª</span>
                            </div>
                            <span class="text-xl font-bold text-red-600">ë¡œê·¸ì•„ì›ƒ</span>
                        </div>
                        <span class="text-red-400 text-2xl">â€º</span>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- ì‚¬ìš©ìž ê´€ë¦¬ í™”ë©´ (ê´€ë¦¬ìž ì „ìš©) -->
    <div id="userManagementScreen" class="hidden min-h-screen">
        <div class="bg-primary text-white py-6 px-6 flex items-center shadow-medium">
            <button onclick="showScreen('main')" class="mr-6 text-white hover:text-red-200 transition-colors text-3xl">â†</button>
            <div class="flex items-center space-x-4">
                <span class="text-3xl">ðŸ‘¥</span>
                <h1 class="text-3xl font-bold">ì‚¬ìš©ìž ê´€ë¦¬</h1>
                <span class="badge-admin text-sm px-3 py-2 rounded-full font-bold">ADMIN ONLY</span>
            </div>
        </div>
        
        <div class="p-8">
            <div id="userProgressList" class="grid grid-cols-1 gap-6">
                <!-- ì‚¬ìš©ìž ì§„ë„ ëª©ë¡ì´ ì—¬ê¸°ì— ë™ì ìœ¼ë¡œ ìƒì„±ë©ë‹ˆë‹¤ -->
            </div>
        </div>
    </div>

    <!-- í€´ì¦ˆ ëª¨ë‹¬ -->
    <div id="quizModal" class="hidden fixed inset-0 bg-black bg-opacity-60 flex items-center justify-center z-50 p-4">
        <div class="card shadow-medium w-full max-w-3xl max-h-[90vh] overflow-auto">
            <div class="p-8">
                <div class="text-center mb-8">
                    <div class="w-20 h-20 bg-primary rounded-full mx-auto mb-6 flex items-center justify-center shadow-soft">
                        <span class="text-4xl">â“</span>
                    </div>
                    <h3 id="quizTitle" class="text-2xl font-bold text-gray-800 mb-3">2025ë…„ 07ì›” êµìœ¡ ìžë£Œ ì‹œí—˜ ë¬¸ì œ</h3>
                    <div id="quizScore" class="hidden text-xl font-bold"></div>
                </div>
                
                <div id="quizQuestions" class="space-y-8">
                    <!-- í€´ì¦ˆ ë¬¸ì œë“¤ì´ ì—¬ê¸°ì— ë™ì ìœ¼ë¡œ ìƒì„±ë©ë‹ˆë‹¤ -->
                </div>
                
                <div class="flex space-x-4 mt-8">
                    <button onclick="closeQuiz()" class="flex-1 px-6 py-4 border-2 border-gray-300 rounded-xl text-gray-600 hover:bg-gray-50 transition-all font-semibold">
                        <span id="quizCloseText">ì·¨ì†Œ</span>
                    </button>
                    <button id="submitQuizBtn" onclick="submitQuiz()" class="flex-1 px-6 py-4 btn-primary rounded-xl transition-all disabled:opacity-50 disabled:cursor-not-allowed font-semibold shadow-soft">
                        ì œì¶œí•˜ê¸°
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- ì„œëª… ëª¨ë‹¬ -->
    <div id="signatureModal" class="hidden fixed inset-0 bg-black bg-opacity-60 flex items-center justify-center z-50 p-4">
        <div class="card shadow-medium w-full max-w-md">
            <div class="p-8">
                <div class="text-center mb-8">
                    <div class="w-20 h-20 bg-success rounded-full mx-auto mb-6 flex items-center justify-center shadow-soft">
                        <span class="text-4xl">âœï¸</span>
                    </div>
                    <h3 class="text-2xl font-bold text-gray-800 mb-3">êµìœ¡ ì™„ë£Œ ì„œëª…</h3>
                    <p id="signatureModalText" class="text-gray-600 font-medium">êµìœ¡ì„ ì™„ë£Œí•˜ì˜€ìŒì„ í™•ì¸í•©ë‹ˆë‹¤.</p>
                </div>
                
                <div class="mb-8">
                    <label class="block text-lg font-bold text-gray-700 mb-4">ì„œëª… (ì´ë¦„ì„ ìž…ë ¥í•´ì£¼ì„¸ìš”)</label>
                    <input
                        id="signatureInput"
                        type="text"
                        placeholder="í™ê¸¸ë™"
                        class="w-full px-6 py-4 border-2 border-gray-300 rounded-xl text-gray-800 bg-white focus:border-red-400 focus:outline-none transition-all text-center text-xl font-bold"
                    />
                </div>
                
                <div class="flex space-x-4">
                    <button onclick="closeSignatureModal()" class="flex-1 px-6 py-4 border-2 border-gray-300 rounded-xl text-gray-600 hover:bg-gray-50 transition-all font-semibold">
                        ì·¨ì†Œ
                    </button>
                    <button onclick="saveSignature()" class="flex-1 px-6 py-4 btn-success rounded-xl shadow-soft font-semibold">
                        âœ… ì„œëª… ì™„ë£Œ
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- ê³µì§€ì‚¬í•­ ìˆ˜ì • ëª¨ë‹¬ -->
    <div id="editNoticeModal" class="hidden fixed inset-0 bg-black bg-opacity-60 flex items-center justify-center z-50 p-4">
        <div class="card shadow-medium w-full max-w-2xl">
            <div class="p-8">
                <div class="text-center mb-8">
                    <div class="w-20 h-20 bg-accent rounded-full mx-auto mb-6 flex items-center justify-center shadow-soft">
                        <span class="text-4xl">âœï¸</span>
                    </div>
                    <h3 class="text-2xl font-bold text-gray-800 mb-3">ê³µì§€ì‚¬í•­ ìˆ˜ì •</h3>
                </div>
                
                <div class="space-y-6">
                    <input
                        id="editNoticeTitle"
                        type="text"
                        placeholder="ì œëª©ì„ ìž…ë ¥í•˜ì„¸ìš”"
                        class="w-full px-6 py-4 border-2 border-gray-200 rounded-xl text-gray-800 bg-white focus:border-red-400 focus:outline-none transition-all"
                    />
                    <textarea
                        id="editNoticeContent"
                        placeholder="ë‚´ìš©ì„ ìž…ë ¥í•˜ì„¸ìš”"
                        rows="6"
                        class="w-full px-6 py-4 border-2 border-gray-200 rounded-xl text-gray-800 bg-white focus:border-red-400 focus:outline-none transition-all"
                    ></textarea>
                </div>
                
                <div class="flex space-x-4 mt-8">
                    <button onclick="closeEditNoticeModal()" class="flex-1 px-6 py-4 border-2 border-gray-300 rounded-xl text-gray-600 hover:bg-gray-50 transition-all font-semibold">
                        ì·¨ì†Œ
                    </button>
                    <button onclick="updateNotice()" class="flex-1 px-6 py-4 btn-primary rounded-xl shadow-soft font-semibold">
                        âœ… ìˆ˜ì • ì™„ë£Œ
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- ì‚¬ìš©ìž ìƒì„¸ì •ë³´ ëª¨ë‹¬ -->
    <div id="userDetailModal" class="hidden fixed inset-0 bg-black bg-opacity-60 flex items-center justify-center z-50 p-4">
        <div class="card shadow-medium w-full max-w-md">
            <div class="p-8">
                <div class="text-center mb-8">
                    <div class="w-20 h-20 bg-primary rounded-full mx-auto mb-6 flex items-center justify-center shadow-soft">
                        <span class="text-4xl">ðŸ‘¤</span>
                    </div>
                    <h3 class="text-2xl font-bold text-gray-800 mb-3">ì‚¬ìš©ìž ìƒì„¸ì •ë³´</h3>
                </div>
                
                <div id="userDetailContent" class="space-y-4">
                    <!-- ì‚¬ìš©ìž ì •ë³´ê°€ ì—¬ê¸°ì— í‘œì‹œë©ë‹ˆë‹¤ -->
                </div>
                
                <div class="mt-8">
                    <button onclick="closeUserDetailModal()" class="w-full px-6 py-4 btn-primary rounded-xl shadow-soft font-semibold">
                        í™•ì¸
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- ë‚´ í”„ë¡œí•„ ëª¨ë‹¬ -->
    <div id="profileModal" class="hidden fixed inset-0 bg-black bg-opacity-60 flex items-center justify-center z-50 p-4">
        <div class="card shadow-medium w-full max-w-md">
            <div class="p-8">
                <div class="text-center mb-8">
                    <div class="w-20 h-20 bg-primary rounded-full mx-auto mb-6 flex items-center justify-center shadow-soft">
                        <span class="text-4xl">ðŸ‘¤</span>
                    </div>
                    <h3 class="text-2xl font-bold text-gray-800 mb-3">ë‚´ í”„ë¡œí•„</h3>
                </div>
                
                <div id="profileContent" class="space-y-6">
                    <div class="flex items-center justify-between p-4 bg-gray-50 rounded-xl">
                        <span class="font-bold text-gray-600">ðŸ†” ì‚¬ë²ˆ</span>
                        <span id="profileEmployeeId" class="text-gray-800 font-semibold">-</span>
                    </div>
                    <div class="flex items-center justify-between p-4 bg-gray-50 rounded-xl">
                        <span class="font-bold text-gray-600">ðŸ‘¤ ì´ë¦„</span>
                        <span id="profileName" class="text-gray-800 font-semibold">-</span>
                    </div>
                    <div class="flex items-center justify-between p-4 bg-gray-50 rounded-xl">
                        <span class="font-bold text-gray-600">ðŸ¢ ë¶€ì„œ</span>
                        <span id="profileDepartment" class="text-gray-800 font-semibold">-</span>
                    </div>
                    <div class="flex items-center justify-between p-4 bg-gray-50 rounded-xl">
                        <span class="font-bold text-gray-600">ðŸ“Š êµìœ¡ ì§„ë„</span>
                        <span id="profileProgress" class="text-gray-800 font-semibold">-</span>
                    </div>
                    <div class="flex items-center justify-between p-4 bg-gray-50 rounded-xl">
                        <span class="font-bold text-gray-600">ðŸŽ¯ í‰ê·  ì ìˆ˜</span>
                        <span id="profileScore" class="text-gray-800 font-semibold">-</span>
                    </div>
                </div>
                
                <div class="mt-8">
                    <button onclick="closeProfileModal()" class="w-full px-6 py-4 btn-primary rounded-xl shadow-soft font-semibold">
                        í™•ì¸
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- ì•Œë¦¼ì„¤ì • ëª¨ë‹¬ -->
    <div id="notificationModal" class="hidden fixed inset-0 bg-black bg-opacity-60 flex items-center justify-center z-50 p-4">
        <div class="card shadow-medium w-full max-w-md">
            <div class="p-8">
                <div class="text-center mb-8">
                    <div class="w-20 h-20 bg-accent rounded-full mx-auto mb-6 flex items-center justify-center shadow-soft">
                        <span class="text-4xl">ðŸ””</span>
                    </div>
                    <h3 class="text-2xl font-bold text-gray-800 mb-3">ì•Œë¦¼ ì„¤ì •</h3>
                </div>
                
                <div class="space-y-6">
                    <div class="flex items-center justify-between p-4 bg-gray-50 rounded-xl">
                        <div>
                            <span class="font-bold text-gray-800 block">ðŸ“š êµìœ¡ ì•Œë¦¼</span>
                            <span class="text-sm text-gray-600">ìƒˆë¡œìš´ êµìœ¡ì´ ë“±ë¡ë  ë•Œ</span>
                        </div>
                        <label class="relative inline-flex items-center cursor-pointer">
                            <input id="educationNotification" type="checkbox" class="sr-only peer" checked>
                            <div class="w-11 h-6 bg-gray-200 peer-focus:outline-none rounded-full peer peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:rounded-full after:h-5 after:w-5 after:transition-all peer-checked:bg-primary"></div>
                        </label>
                    </div>
                    
                    <div class="flex items-center justify-between p-4 bg-gray-50 rounded-xl">
                        <div>
                            <span class="font-bold text-gray-800 block">ðŸ“¢ ê³µì§€ì‚¬í•­ ì•Œë¦¼</span>
                            <span class="text-sm text-gray-600">ìƒˆë¡œìš´ ê³µì§€ì‚¬í•­ì´ ë“±ë¡ë  ë•Œ</span>
                        </div>
                        <label class="relative inline-flex items-center cursor-pointer">
                            <input id="noticeNotification" type="checkbox" class="sr-only peer" checked>
                            <div class="w-11 h-6 bg-gray-200 peer-focus:outline-none rounded-full peer peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:rounded-full after:h-5 after:w-5 after:transition-all peer-checked:bg-primary"></div>
                        </label>
                    </div>
                    
                    <div class="flex items-center justify-between p-4 bg-gray-50 rounded-xl">
                        <div>
                            <span class="font-bold text-gray-800 block">â° ë§ˆê°ì¼ ì•Œë¦¼</span>
                            <span class="text-sm text-gray-600">êµìœ¡ ë§ˆê°ì¼ 3ì¼ ì „</span>
                        </div>
                        <label class="relative inline-flex items-center cursor-pointer">
                            <input id="deadlineNotification" type="checkbox" class="sr-only peer" checked>
                            <div class="w-11 h-6 bg-gray-200 peer-focus:outline-none rounded-full peer peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:rounded-full after:h-5 after:w-5 after:transition-all peer-checked:bg-primary"></div>
                        </label>
                    </div>
                    
                    <div class="flex items-center justify-between p-4 bg-gray-50 rounded-xl">
                        <div>
                            <span class="font-bold text-gray-800 block">ðŸ”Š í‘¸ì‹œ ì•Œë¦¼</span>
                            <span class="text-sm text-gray-600">ì•± ì™¸ë¶€ì—ì„œë„ ì•Œë¦¼ ë°›ê¸°</span>
                        </div>
                        <label class="relative inline-flex items-center cursor-pointer">
                            <input id="pushNotification" type="checkbox" class="sr-only peer">
                            <div class="w-11 h-6 bg-gray-200 peer-focus:outline-none rounded-full peer peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:rounded-full after:h-5 after:w-5 after:transition-all peer-checked:bg-primary"></div>
                        </label>
                    </div>
                </div>
                
                <div class="flex space-x-4 mt-8">
                    <button onclick="closeNotificationModal()" class="flex-1 px-6 py-4 border-2 border-gray-300 rounded-xl text-gray-600 hover:bg-gray-50 transition-all font-semibold">
                        ì·¨ì†Œ
                    </button>
                    <button onclick="saveNotificationSettings()" class="flex-1 px-6 py-4 btn-primary rounded-xl shadow-soft font-semibold">
                        âœ… ì €ìž¥
                    </button>
                </div>
            </div>
        </div>
    </div>

    <script>
        // ì „ì—­ ë³€ìˆ˜
        let currentUser = null;
        let isAdmin = false;
        let notices = [];
        let signatures = {};
        let currentQuiz = null;
        let userAnswers = {};
        let quizSubmitted = false;
        let currentSignatureMonth = null;
        let editingNoticeId = null;

        // ì•Œë¦¼ ì„¤ì • ìƒíƒœ
        let notificationSettings = {
            education: true,
            notice: true,
            deadline: true,
            push: false
        };

        // ê´€ë¦¬ìž ê³„ì •
        const adminAccounts = {
            'K2020004': { name: 'ì†¡ì„œí˜„' },
            'K2024010': { name: 'ê¹€ì§€ì™„' }
        };

        // ì‚¬ìš©ìž ë”ë¯¸ ë°ì´í„°
        const userData = {
            'K2024001': { name: 'ê¹€ì² ìˆ˜', department: 'ìƒì‚°ê´€ë¦¬íŒ€', progress: 75, quizScore: 85 },
            'K2024002': { name: 'ì´ì˜í¬', department: 'í’ˆì§ˆê´€ë¦¬íŒ€', progress: 100, quizScore: 95 },
            'K2024003': { name: 'ë°•ë¯¼ìˆ˜', department: 'ì œì¡°1íŒ€', progress: 50, quizScore: 70 },
            'K2024004': { name: 'ì •ìˆ˜ì§„', department: 'ì—°êµ¬ê°œë°œíŒ€', progress: 90, quizScore: 88 }
        };

        // í€´ì¦ˆ ë°ì´í„°
        const quizData = {
            7: {
                title: '2025ë…„ 07ì›” êµìœ¡ ìžë£Œ ì‹œí—˜ ë¬¸ì œ',
                questions: [
                    {
                        id: 1,
                        question: 'ì„¸ì²™ì´ ë¯¸í¡í•˜ë”ë¼ë„ ê°•ë ¥í•œ ì†Œë…ì œ ì‚¬ìš©ë§Œìœ¼ë¡œ ì‹ì¤‘ë…ê· ì„ ì‚´ë©¸ì‹œí‚¬ ìˆ˜ ìžˆë‹¤.',
                        type: 'ox',
                        options: ['O', 'X'],
                        correctAnswer: 1,
                        explanation: 'ì„¸ì²™ì´ ìš°ì„ ë˜ì–´ì•¼ í•˜ë©°, ì†Œë…ì œë§Œìœ¼ë¡œëŠ” ë¶ˆì¶©ë¶„í•©ë‹ˆë‹¤.'
                    },
                    {
                        id: 2,
                        question: 'ì„¸ì²™Â·ì†Œë…ì œ ì‚¬ìš© ì‹œ ì£¼ì˜ì‚¬í•­ì— ëŒ€í•œ ì„¤ëª… ì¤‘ ë°”ë¥´ì§€ ì•Šì€ ê²ƒì€?',
                        type: 'multiple',
                        options: [
                            'ì†Œë…ì œì˜ í¬ì„ì•¡ ì œì¡° ì‹œ, ë‹¤ë¥¸ ì‚´ê· ì†Œë…ì œì™€ í˜¼í•©í•˜ì—¬ ì†Œë…íš¨ê³¼ì„±ì„ ë†’ì¸ë‹¤.',
                            'ë°˜ë“œì‹œ ì„¸ì²™ì œ ë° ì†Œë…ì œëŠ” ì‹ì•½ì²˜ í—ˆê°€ë¥¼ ë°›ì€ ì œí’ˆë§Œì„ ì‚¬ìš©í•œë‹¤.',
                            'ì†Œë…ì œ í¬ì„ì•¡ì€ ì¦‰ì‹œ ì‚¬ìš©í•˜ê³  ë‚¨ì€ í¬ì„ì•¡ì„ íê¸°í•œë‹¤.',
                            'ì‹ ì²´ì— ì†Œë…ì œ ì›ì•¡ ë“±ì´ ë¬»ì§€ ì•Šë„ë¡ ë§ˆìŠ¤í¬ ë“± ê°œì¸ ë³´í˜¸ìž¥ë¹„ë¥¼ ì°©ìš© í›„ ì‚¬ìš©í•œë‹¤.'
                        ],
                        correctAnswer: 0,
                        explanation: 'ë‹¤ë¥¸ ì‚´ê· ì†Œë…ì œì™€ í˜¼í•©í•˜ë©´ ìœ„í—˜í•  ìˆ˜ ìžˆìœ¼ë¯€ë¡œ í˜¼í•©í•˜ì§€ ì•Šì•„ì•¼ í•©ë‹ˆë‹¤.'
                    },
                    {
                        id: 3,
                        question: 'ì„¸ì²™ì œê°€ ìž”ë¥˜í•˜ì§€ ì•Šë„ë¡ ìŒìš©ì— ì í•©í•œ ë¬¼ë¡œ ì¶©ë¶„ížˆ í—¹êµ° í›„ ê±´ì¡°ì‹œì¼œì•¼ í•œë‹¤.',
                        type: 'ox',
                        options: ['O', 'X'],
                        correctAnswer: 0,
                        explanation: 'ì„¸ì²™ì œ ìž”ë¥˜ë¥¼ ë°©ì§€í•˜ê¸° ìœ„í•´ ì¶©ë¶„í•œ í—¹êµ¼ê³¼ ê±´ì¡°ê°€ í•„ìš”í•©ë‹ˆë‹¤.'
                    },
                    {
                        id: 4,
                        question: 'ë°”ë‹¥ìš©, ìž‘ì—…ëŒ€ìš©, ì„¤ë¹„ìš© ë“± ìš©ë„ë³„ë¡œ êµ¬ë¶„í•˜ì—¬ ì‚¬ìš©í•˜ë©°, ì ˆëŒ€ ê²¸ìš©í•˜ì—¬ ì‚¬ìš©í•˜ì§€ ì•ŠëŠ”ë‹¤.',
                        type: 'ox',
                        options: ['O', 'X'],
                        correctAnswer: 0,
                        explanation: 'êµì°¨ì˜¤ì—¼ ë°©ì§€ë¥¼ ìœ„í•´ ìš©ë„ë³„ë¡œ êµ¬ë¶„í•˜ì—¬ ì‚¬ìš©í•´ì•¼ í•©ë‹ˆë‹¤.'
                    }
                ]
            }
        };

        // êµìœ¡ ë°ì´í„° ìƒì„±
        function generateEducationData() {
            const currentYear = 2025;
            const months = [];
            for (let i = 1; i <= 12; i++) {
                const monthStr = i.toString().padStart(2, '0');
                const allCompleted = Math.random() > 0.3;
                months.push({
                    id: i,
                    title: `${currentYear}ë…„ ${monthStr}ì›” êµìœ¡`,
                    items: [
                        { id: 1, title: `${currentYear}ë…„ ${monthStr}ì›” êµìœ¡ë‚´ìš©`, type: 'content', completed: allCompleted },
                        { id: 2, title: `${currentYear}ë…„ ${monthStr}ì›” í€´ì¦ˆ`, type: 'quiz', completed: allCompleted }
                    ],
                    allCompleted: allCompleted
                });
            }
            return months;
        }

        const educationData = generateEducationData();

        // ë¡œê·¸ì¸ ì²˜ë¦¬
        function handleLogin() {
            const employeeId = document.getElementById('employeeId').value.trim();
            const password = document.getElementById('password').value.trim();
            
            if (!employeeId || !password) {
                alert('ì‚¬ë²ˆê³¼ íŒ¨ìŠ¤ì›Œë“œë¥¼ ëª¨ë‘ ìž…ë ¥í•´ì£¼ì„¸ìš”.');
                return;
            }
            
            currentUser = employeeId;
            
            // ê´€ë¦¬ìž ê¶Œí•œ í™•ì¸
            const upperEmployeeId = employeeId.toUpperCase();
            if (adminAccounts[upperEmployeeId]) {
                isAdmin = true;
                document.getElementById('adminMode').classList.remove('hidden');
                document.getElementById('userManagementMenu').classList.remove('hidden');
                document.getElementById('writeNoticeBtn').classList.remove('hidden');
                document.getElementById('saveAllBtn').classList.remove('hidden');
            } else {
                isAdmin = false;
                document.getElementById('adminMode').classList.add('hidden');
                document.getElementById('userManagementMenu').classList.add('hidden');
                document.getElementById('writeNoticeBtn').classList.add('hidden');
                document.getElementById('saveAllBtn').classList.add('hidden');
            }
            
            showScreen('main');
        }

        // ë¡œê·¸ì•„ì›ƒ ì²˜ë¦¬
        function handleLogout() {
            currentUser = null;
            isAdmin = false;
            notices = [];
            signatures = {};
            
            document.getElementById('adminMode').classList.add('hidden');
            document.getElementById('userManagementMenu').classList.add('hidden');
            document.getElementById('writeNoticeBtn').classList.add('hidden');
            document.getElementById('saveAllBtn').classList.add('hidden');
            
            document.getElementById('employeeId').value = '';
            document.getElementById('password').value = '';
            
            showScreen('login');
        }

        // í™”ë©´ ì „í™˜
        function showScreen(screenName) {
            const screens = ['loginScreen', 'mainScreen', 'educationScreen', 'noticeScreen', 'suggestionScreen', 'settingsScreen', 'userManagementScreen'];
            screens.forEach(screen => {
                document.getElementById(screen).classList.add('hidden');
            });
            
            if (screenName === 'login') {
                document.getElementById('loginScreen').classList.remove('hidden');
            } else if (screenName === 'main') {
                document.getElementById('mainScreen').classList.remove('hidden');
            } else if (screenName === 'education') {
                document.getElementById('educationScreen').classList.remove('hidden');
                renderEducationList();
            } else if (screenName === 'notice') {
                document.getElementById('noticeScreen').classList.remove('hidden');
                renderNoticeList();
            } else if (screenName === 'suggestion') {
                document.getElementById('suggestionScreen').classList.remove('hidden');
            } else if (screenName === 'settings') {
                document.getElementById('settingsScreen').classList.remove('hidden');
            } else if (screenName === 'userManagement' && isAdmin) {
                document.getElementById('userManagementScreen').classList.remove('hidden');
                renderUserProgress();
            }
        }

        // êµìœ¡ ëª©ë¡ ë Œë”ë§
        function renderEducationList() {
            const container = document.getElementById('educationList');
            
            container.innerHTML = educationData.map((month, index) => {
                const statusBadge = month.allCompleted 
                    ? '<span class="badge-completed text-sm px-4 py-2 rounded-full font-bold">âœ… ì™„ë£Œ</span>'
                    : '<span class="badge-progress text-sm px-4 py-2 rounded-full font-bold">â³ ì§„í–‰ì¤‘</span>';
                
                const isSignatureExists = signatures[month.id];
                const signatureButton = month.allCompleted && !isSignatureExists
                    ? `<button onclick="openSignatureModal(${month.id})" class="btn-success px-6 py-3 rounded-xl font-semibold shadow-soft hover-lift transition-all">âœï¸ ì„œëª…í•˜ê¸°</button>`
                    : isSignatureExists
                    ? `<div class="text-green-600 font-bold text-lg">âœ… ì„œëª…ì™„ë£Œ (${isSignatureExists.signature})</div>`
                    : '';

                return `
                    <div class="card shadow-soft overflow-hidden fade-in">
                        <div class="p-8 cursor-pointer hover-lift transition-all duration-200" onclick="toggleMonth(${month.id})">
                            <div class="flex items-center justify-between">
                                <div class="flex items-center space-x-6">
                                    <div class="w-16 h-16 bg-primary rounded-xl flex items-center justify-center shadow-soft">
                                        <span class="text-white text-2xl font-bold">${month.id.toString().padStart(2, '0')}</span>
                                    </div>
                                    <div>
                                        <h3 class="text-2xl font-bold text-gray-800">${month.title}</h3>
                                        <p class="text-gray-600 font-medium text-lg">${month.items.length}ê°œ í•™ìŠµê³¼ì •</p>
                                    </div>
                                </div>
                                <div class="flex items-center space-x-4">
                                    ${statusBadge}
                                    <span id="chevron-${month.id}" class="text-gray-400 text-3xl transition-transform duration-200">â€º</span>
                                </div>
                            </div>
                        </div>
                        
                        <div id="month-content-${month.id}" class="hidden border-t border-gray-100 px-8 py-6 bg-gray-50">
                            <div class="space-y-4">
                                ${month.items.map(item => `
                                    <div class="flex items-center justify-between bg-white rounded-xl p-6 border border-gray-200 shadow-soft hover-lift transition-all duration-200">
                                        <div class="flex items-center space-x-4">
                                            <div class="w-12 h-12 rounded-full ${item.completed ? 'bg-success' : 'bg-gray-100'} flex items-center justify-center shadow-soft">
                                                <span class="text-xl">${item.completed ? 'âœ…' : item.type === 'quiz' ? 'â“' : 'ðŸ“„'}</span>
                                            </div>
                                            <span class="text-gray-800 text-lg font-semibold">${item.title}</span>
                                        </div>
                                        <div class="flex items-center space-x-3">
                                            ${item.completed 
                                                ? '<span class="badge-completed text-sm px-4 py-2 rounded-full font-bold">ì™„ë£Œ</span>' 
                                                : item.type === 'quiz' 
                                                ? `<button onclick="startQuiz(${month.id})" class="btn-primary px-6 py-3 rounded-xl font-semibold shadow-soft hover-lift transition-all">ðŸš€ ì‹œìž‘í•˜ê¸°</button>`
                                                : '<span class="text-gray-400 font-medium">ì¤€ë¹„ì¤‘</span>'
                                            }
                                        </div>
                                    </div>
                                `).join('')}
                                
                                ${signatureButton ? `<div class="mt-6 text-center bg-white rounded-xl p-6">${signatureButton}</div>` : ''}
                            </div>
                        </div>
                    </div>
                `;
            }).join('');
        }

        // í€´ì¦ˆ ë Œë”ë§
        function renderQuiz(monthId) {
            const quiz = quizData[monthId];
            if (!quiz) {
                document.getElementById('quizQuestions').innerHTML = '<p class="text-center text-gray-500 text-lg">í€´ì¦ˆ ë°ì´í„°ê°€ ì—†ìŠµë‹ˆë‹¤.</p>';
                return;
            }

            const questionsHtml = quiz.questions.map((question, index) => `
                <div class="bg-gray-50 rounded-xl p-8 border border-gray-200 shadow-soft">
                    <h4 class="text-xl font-bold text-gray-800 mb-6">ë¬¸ì œ ${question.id}. ${question.question}</h4>
                    <div class="space-y-4">
                        ${question.options.map((option, optionIndex) => `
                            <div id="option-${question.id}-${optionIndex}" 
                                 onclick="selectAnswer(${question.id}, ${optionIndex})" 
                                 class="quiz-option p-6 border-2 border-gray-200 rounded-xl cursor-pointer hover:bg-gray-50 transition-all duration-200 font-medium text-lg shadow-soft">
                                ${question.type === 'ox' ? `<span class="text-2xl font-bold">${option}</span>` : `<span class="font-bold mr-2">${optionIndex + 1}.</span> ${option}`}
                            </div>
                        `).join('')}
                    </div>
                    <div id="explanation-${question.id}" class="hidden mt-6 p-6 bg-blue-50 border border-blue-200 rounded-xl shadow-soft">
                        <p class="text-blue-800 font-medium text-lg"><span class="font-bold">ðŸ’¡ í•´ì„¤:</span> ${question.explanation}</p>
                    </div>
                </div>
            `).join('');

            document.getElementById('quizQuestions').innerHTML = questionsHtml;
        }

        // ì›”ë³„ êµìœ¡ í† ê¸€
        function toggleMonth(monthId) {
            const content = document.getElementById(`month-content-${monthId}`);
            const chevron = document.getElementById(`chevron-${monthId}`);
            
            if (content.classList.contains('hidden')) {
                content.classList.remove('hidden');
                chevron.style.transform = 'rotate(90deg)';
            } else {
                content.classList.add('hidden');
                chevron.style.transform = 'rotate(0deg)';
            }
        }

        // í€´ì¦ˆ ì‹œìž‘
        function startQuiz(monthId) {
            currentQuiz = monthId;
            userAnswers = {};
            quizSubmitted = false;
            
            document.getElementById('quizTitle').textContent = quizData[monthId]?.title || `2025ë…„ ${String(monthId).padStart(2, '0')}ì›” êµìœ¡ ìžë£Œ ì‹œí—˜ ë¬¸ì œ`;
            document.getElementById('quizScore').classList.add('hidden');
            document.getElementById('submitQuizBtn').disabled = false;
            document.getElementById('submitQuizBtn').textContent = 'ì œì¶œí•˜ê¸°';
            document.getElementById('quizCloseText').textContent = 'ì·¨ì†Œ';
            
            renderQuiz(monthId);
            document.getElementById('quizModal').classList.remove('hidden');
        }

        // í€´ì¦ˆ ë‹µì•ˆ ì„ íƒ
        function selectAnswer(questionId, answerIndex) {
            if (quizSubmitted) return;
            
            userAnswers[questionId] = answerIndex;
            
            const options = document.querySelectorAll(`[id^="option-${questionId}-"]`);
            options.forEach((option, index) => {
                if (index === answerIndex) {
                    option.classList.add('selected');
                } else {
                    option.classList.remove('selected');
                }
            });
        }

        // í€´ì¦ˆ ì œì¶œ
        function submitQuiz() {
            if (quizSubmitted) return;
            
            const quiz = quizData[currentQuiz];
            if (!quiz) return;
            
            let correctCount = 0;
            
            quiz.questions.forEach(question => {
                const userAnswer = userAnswers[question.id];
                const isCorrect = userAnswer === question.correctAnswer;
                
                if (isCorrect) correctCount++;
                
                const options = document.querySelectorAll(`[id^="option-${question.id}-"]`);
                options.forEach((option, index) => {
                    option.classList.remove('selected');
                    if (index === question.correctAnswer) {
                        option.classList.add('correct');
                    } else if (index === userAnswer && !isCorrect) {
                        option.classList.add('wrong');
                    }
                });
                
                document.getElementById(`explanation-${question.id}`).classList.remove('hidden');
            });
            
            const score = Math.round((correctCount / quiz.questions.length) * 100);
            const scoreColor = score >= 80 ? 'text-green-600' : score >= 60 ? 'text-yellow-600' : 'text-red-600';
            document.getElementById('quizScore').innerHTML = `<span class="${scoreColor}">ðŸŽ¯ ì ìˆ˜: ${score}ì  (${correctCount}/${quiz.questions.length}ë¬¸ì œ ì •ë‹µ)</span>`;
            document.getElementById('quizScore').classList.remove('hidden');
            
            document.getElementById('submitQuizBtn').disabled = true;
            document.getElementById('submitQuizBtn').textContent = 'âœ… ì œì¶œ ì™„ë£Œ';
            document.getElementById('quizCloseText').textContent = 'ë‹«ê¸°';
            
            quizSubmitted = true;
            
            const monthData = educationData.find(m => m.id === currentQuiz);
            if (monthData) {
                monthData.items.forEach(item => item.completed = true);
                monthData.allCompleted = true;
            }
        }

        // í€´ì¦ˆ ë‹«ê¸°
        function closeQuiz() {
            document.getElementById('quizModal').classList.add('hidden');
            if (quizSubmitted) {
                renderEducationList();
            }
        }

        // ì„œëª… ëª¨ë‹¬ ì—´ê¸°
        function openSignatureModal(monthId) {
            currentSignatureMonth = monthId;
            document.getElementById('signatureInput').value = '';
            document.getElementById('signatureModal').classList.remove('hidden');
        }

        // ì„œëª… ëª¨ë‹¬ ë‹«ê¸°
        function closeSignatureModal() {
            document.getElementById('signatureModal').classList.add('hidden');
        }

        // ì„œëª… ì €ìž¥
        function saveSignature() {
            const signature = document.getElementById('signatureInput').value.trim();
            
            if (!signature) {
                alert('ì„œëª…ì„ ìž…ë ¥í•´ì£¼ì„¸ìš”.');
                return;
            }
            
            const now = new Date();
            signatures[currentSignatureMonth] = {
                signature: signature,
                employeeId: currentUser,
                employeeName: adminAccounts[currentUser.toUpperCase()]?.name || 'ì¼ë°˜ì‚¬ìš©ìž',
                date: now.toLocaleDateString('ko-KR'),
                time: now.toLocaleTimeString('ko-KR', { hour: '2-digit', minute: '2-digit' })
            };
            
            closeSignatureModal();
            renderEducationList();
        }

        // Google Form ì—´ê¸°
        function openGoogleForm() {
            window.open('https://forms.google.com', '_blank');
        }

        // ê³µì§€ì‚¬í•­ í† ê¸€
        function toggleNoticeForm() {
            const form = document.getElementById('noticeForm');
            form.classList.toggle('hidden');
        }

        // ê³µì§€ì‚¬í•­ ì¶”ê°€
        function addNotice() {
            const title = document.getElementById('noticeTitle').value.trim();
            const content = document.getElementById('noticeContent').value.trim();
            
            if (!title || !content) {
                alert('ì œëª©ê³¼ ë‚´ìš©ì„ ëª¨ë‘ ìž…ë ¥í•´ì£¼ì„¸ìš”.');
                return;
            }
            
            notices.unshift({
                id: Date.now(),
                title: title,
                content: content,
                author: adminAccounts[currentUser.toUpperCase()]?.name || 'ê´€ë¦¬ìž',
                date: new Date().toLocaleDateString('ko-KR')
            });
            
            document.getElementById('noticeTitle').value = '';
            document.getElementById('noticeContent').value = '';
            toggleNoticeForm();
            renderNoticeList();
        }

        // ê³µì§€ì‚¬í•­ ìˆ˜ì • ëª¨ë‹¬ ì—´ê¸°
        function openEditNoticeModal(noticeId) {
            const notice = notices.find(n => n.id === noticeId);
            if (!notice) return;
            
            editingNoticeId = noticeId;
            document.getElementById('editNoticeTitle').value = notice.title;
            document.getElementById('editNoticeContent').value = notice.content;
            document.getElementById('editNoticeModal').classList.remove('hidden');
        }

        // ê³µì§€ì‚¬í•­ ìˆ˜ì • ëª¨ë‹¬ ë‹«ê¸°
        function closeEditNoticeModal() {
            document.getElementById('editNoticeModal').classList.add('hidden');
            editingNoticeId = null;
        }

        // ê³µì§€ì‚¬í•­ ìˆ˜ì •
        function updateNotice() {
            if (!editingNoticeId) return;
            
            const title = document.getElementById('editNoticeTitle').value.trim();
            const content = document.getElementById('editNoticeContent').value.trim();
            
            if (!title || !content) {
                alert('ì œëª©ê³¼ ë‚´ìš©ì„ ëª¨ë‘ ìž…ë ¥í•´ì£¼ì„¸ìš”.');
                return;
            }
            
            const noticeIndex = notices.findIndex(n => n.id === editingNoticeId);
            if (noticeIndex !== -1) {
                notices[noticeIndex].title = title;
                notices[noticeIndex].content = content;
            }
            
            closeEditNoticeModal();
            renderNoticeList();
        }

        // ê³µì§€ì‚¬í•­ ì‚­ì œ
        function deleteNotice(noticeId) {
            if (confirm('ì •ë§ë¡œ ì´ ê³µì§€ì‚¬í•­ì„ ì‚­ì œí•˜ì‹œê² ìŠµë‹ˆê¹Œ?')) {
                notices = notices.filter(n => n.id !== noticeId);
                renderNoticeList();
            }
        }

        // ê³µì§€ì‚¬í•­ ëª©ë¡ ë Œë”ë§
        function renderNoticeList() {
            const container = document.getElementById('noticeList');
            
            if (notices.length === 0) {
                container.innerHTML = `
                    <div class="card shadow-soft p-12 text-center">
                        <span class="text-6xl mb-6 block">ðŸ“¢</span>
                        <span class="text-gray-600 text-xl font-medium">ê³µì§€ì‚¬í•­ì´ ì—†ìŠµë‹ˆë‹¤.</span>
                    </div>
                `;
                return;
            }
            
            container.innerHTML = notices.map((notice, index) => `
                <div class="card shadow-soft p-8 mb-6 hover-lift transition-all duration-200 fade-in">
                    <div class="flex items-start justify-between mb-4">
                        <h3 class="text-2xl font-bold text-gray-800">ðŸ“Œ ${notice.title}</h3>
                        ${isAdmin ? `
                            <div class="flex items-center space-x-2">
                                <button onclick="openEditNoticeModal(${notice.id})" class="btn-secondary px-3 py-1 rounded-lg text-sm shadow-soft">
                                    âœï¸ ìˆ˜ì •
                                </button>
                                <button onclick="deleteNotice(${notice.id})" class="bg-red-500 text-white px-3 py-1 rounded-lg text-sm shadow-soft hover:bg-red-600 transition-colors">
                                    ðŸ—‘ï¸ ì‚­ì œ
                                </button>
                            </div>
                        ` : ''}
                    </div>
                    <p class="text-gray-600 mb-6 text-lg leading-relaxed">${notice.content}</p>
                    <div class="flex items-center justify-between text-gray-500 font-medium">
                        <span>ðŸ‘¤ ${notice.author}</span>
                        <span>ðŸ“… ${notice.date}</span>
                    </div>
                </div>
            `).join('');
        }

        // ì‚¬ìš©ìž ìƒì„¸ì •ë³´ ëª¨ë‹¬ ì—´ê¸°
        function openUserDetailModal(userId) {
            const user = userData[userId];
            if (!user) return;
            
            document.getElementById('userDetailContent').innerHTML = `
                <div class="space-y-4">
                    <div class="flex items-center justify-between p-4 bg-gray-50 rounded-xl">
                        <span class="font-bold text-gray-600">ðŸ‘¤ ì´ë¦„</span>
                        <span class="text-gray-800 font-semibold">${user.name}</span>
                    </div>
                    <div class="flex items-center justify-between p-4 bg-gray-50 rounded-xl">
                        <span class="font-bold text-gray-600">ðŸ¢ ë¶€ì„œëª…</span>
                        <span class="text-gray-800 font-semibold">${user.department}</span>
                    </div>
                    <div class="flex items-center justify-between p-4 bg-gray-50 rounded-xl">
                        <span class="font-bold text-gray-600">ðŸ†” ì‚¬ë²ˆ</span>
                        <span class="text-gray-800 font-semibold">${userId}</span>
                    </div>
                </div>
            `;
            
            document.getElementById('userDetailModal').classList.remove('hidden');
        }

        // ì‚¬ìš©ìž ìƒì„¸ì •ë³´ ëª¨ë‹¬ ë‹«ê¸°
        function closeUserDetailModal() {
            document.getElementById('userDetailModal').classList.add('hidden');
        }

        // ì‚¬ìš©ìž ì§„ë„ ë Œë”ë§ (ê´€ë¦¬ìžìš©)
        function renderUserProgress() {
            const container = document.getElementById('userProgressList');
            
            container.innerHTML = Object.keys(userData).map((userId, index) => {
                const user = userData[userId];
                return `
                    <div onclick="openUserDetailModal('${userId}')" class="card shadow-soft p-8 hover-lift transition-all duration-200 fade-in cursor-pointer">
                        <div class="flex items-center justify-between mb-6">
                            <div class="flex items-center space-x-4">
                                <div class="w-16 h-16 bg-primary rounded-full flex items-center justify-center shadow-soft">
                                    <span class="text-white text-2xl">ðŸ‘¤</span>
                                </div>
                                <div>
                                    <h3 class="text-2xl font-bold text-gray-800">${user.name}</h3>
                                    <p class="text-gray-600 font-medium text-lg">${user.department}</p>
                                    <p class="text-gray-500 text-sm">${userId}</p>
                                </div>
                            </div>
                            <div class="text-right">
                                <p class="text-gray-600 font-medium text-lg">í€´ì¦ˆ í‰ê· ì ìˆ˜</p>
                                <p class="text-4xl font-bold ${user.quizScore >= 80 ? 'text-green-600' : 'text-yellow-600'}">${user.quizScore}ì </p>
                            </div>
                        </div>
                        <div>
                            <div class="flex items-center justify-between mb-3">
                                <span class="text-gray-700 font-bold text-lg">ðŸ“Š êµìœ¡ ì§„ë„</span>
                                <span class="font-bold text-gray-800 text-xl">${user.progress}%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-4">
                                <div class="bg-primary h-4 rounded-full shadow-soft transition-all duration-1000" style="width: ${user.progress}%"></div>
                            </div>
                        </div>
                    </div>
                `;
            }).join('');
        }

        // ë‚´ í”„ë¡œí•„ ëª¨ë‹¬ ì—´ê¸°
        function openProfileModal() {
            // í˜„ìž¬ ì‚¬ìš©ìž ì •ë³´ ì„¤ì •
            const upperEmployeeId = currentUser.toUpperCase();
            const isAdminUser = adminAccounts[upperEmployeeId];
            const userInfo = userData[currentUser] || {};
            
            document.getElementById('profileEmployeeId').textContent = currentUser;
            document.getElementById('profileName').textContent = isAdminUser ? isAdminUser.name : (userInfo.name || 'ì‚¬ìš©ìž');
            document.getElementById('profileDepartment').textContent = isAdminUser ? 'ê´€ë¦¬íŒ€' : (userInfo.department || 'ì¼ë°˜ë¶€ì„œ');
            document.getElementById('profileProgress').textContent = isAdminUser ? '100%' : (userInfo.progress ? userInfo.progress + '%' : '0%');
            document.getElementById('profileScore').textContent = isAdminUser ? '100ì ' : (userInfo.quizScore ? userInfo.quizScore + 'ì ' : '0ì ');
            
            document.getElementById('profileModal').classList.remove('hidden');
        }

        // ë‚´ í”„ë¡œí•„ ëª¨ë‹¬ ë‹«ê¸°
        function closeProfileModal() {
            document.getElementById('profileModal').classList.add('hidden');
        }

        // ì•Œë¦¼ì„¤ì • ëª¨ë‹¬ ì—´ê¸°
        function openNotificationModal() {
            // í˜„ìž¬ ì„¤ì •ê°’ìœ¼ë¡œ ì´ˆê¸°í™”
            document.getElementById('educationNotification').checked = notificationSettings.education;
            document.getElementById('noticeNotification').checked = notificationSettings.notice;
            document.getElementById('deadlineNotification').checked = notificationSettings.deadline;
            document.getElementById('pushNotification').checked = notificationSettings.push;
            
            document.getElementById('notificationModal').classList.remove('hidden');
        }

        // ì•Œë¦¼ì„¤ì • ëª¨ë‹¬ ë‹«ê¸°
        function closeNotificationModal() {
            document.getElementById('notificationModal').classList.add('hidden');
        }

        // ì•Œë¦¼ì„¤ì • ì €ìž¥
        function saveNotificationSettings() {
            notificationSettings.education = document.getElementById('educationNotification').checked;
            notificationSettings.notice = document.getElementById('noticeNotification').checked;
            notificationSettings.deadline = document.getElementById('deadlineNotification').checked;
            notificationSettings.push = document.getElementById('pushNotification').checked;
            
            alert('ì•Œë¦¼ ì„¤ì •ì´ ì €ìž¥ë˜ì—ˆìŠµë‹ˆë‹¤.');
            closeNotificationModal();
        }

        // ëª¨ë“  íŒŒì¼ ì €ìž¥ (ê´€ë¦¬ìžìš©)
        function saveAllFiles() {
            alert('ðŸ’¾ ë°ì´í„° ì €ìž¥ ê¸°ëŠ¥ì€ ì¤€ë¹„ ì¤‘ìž…ë‹ˆë‹¤.');
        }

        // Enter í‚¤ë¡œ ë¡œê·¸ì¸
        document.addEventListener('DOMContentLoaded', function() {
            const passwordInput = document.getElementById('password');
            const employeeIdInput = document.getElementById('employeeId');
            
            passwordInput.addEventListener('keypress', function(e) {
                if (e.key === 'Enter') {
                    handleLogin();
                }
            });
            
            employeeIdInput.addEventListener('keypress', function(e) {
                if (e.key === 'Enter') {
                    passwordInput.focus();
                }
            });
        });
    </script>
</body>
</html>
