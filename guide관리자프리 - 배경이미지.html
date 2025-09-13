<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>채굴테크 - 암호화폐 채굴대행 서비스</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap');
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0d1117; /* Fallback color */
            color: #e6edf3;
        }
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            background-image: url('https://images.unsplash.com/photo-1639322537228-f710d846310a?q=80&w=1920&auto=format&fit=crop');
            background-size: cover;
            background-position: center;
            filter: blur(5px) brightness(0.4); /* 이미지 흐림 및 밝기 조절 */
            z-index: -1; /* 콘텐츠 뒤에 배경 배치 */
        }
        .gradient-bg {
            background: linear-gradient(135deg, #1d2b3a 0%, #0d1117 100%);
        }
        .card {
            background-color: #161b22;
            border: 1px solid #30363d;
        }
        .btn {
            transition: all 0.3s ease;
        }
        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            display: none;
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }
        .modal-content {
            background-color: #161b22;
            padding: 2rem;
            border-radius: 12px;
            border: 1px solid #30363d;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
            width: 90%;
            max-width: 400px;
        }
        .form-input {
            width: 100%;
            padding: 0.75rem;
            background-color: #0d1117;
            border: 1px solid #30363d;
            border-radius: 8px;
            color: #e6edf3;
        }
        .trade-table th, .trade-table td {
            padding: 12px;
            border-bottom: 1px solid #30363d;
        }
        .hidden-page {
            display: none;
        }
        .loader {
            border: 4px solid #f3f3f3;
            border-top: 4px solid #3498db;
            border-radius: 50%;
            width: 24px;
            height: 24px;
            animation: spin 1s linear infinite;
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        /* Admin page specific styles */
        .admin-table th, .admin-table td {
            padding: 12px;
            border-bottom: 1px solid #30363d;
        }
        /* Mining Farm table style */
        .mining-farm-table th, .mining-farm-table td {
            padding: 12px;
            border-bottom: 1px solid #30363d;
        }
    </style>
</head>
<body class="antialiased">
    <!-- Header -->
    <header class="p-4 md:p-6 flex items-center justify-between border-b border-gray-700 relative">
        <div class="flex items-center space-x-2">
            <svg class="w-8 h-8 text-yellow-400" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 15.93v-2.88c0-.66.54-1.2 1.2-1.2s1.2.54 1.2 1.2v2.88c0 .66-.54 1.2-1.2 1.2s-1.2-.54-1.2-1.2zm1.2-4.8c-.66 0-1.2-.54-1.2-1.2v-2.88c0-.66.54-1.2 1.2-1.2s1.2.54 1.2 1.2v2.88c0 .66-.54 1.2-1.2 1.2zm1.2-4.8c-.66 0-1.2-.54-1.2-1.2V5.07c0-.66.54-1.2 1.2-1.2s1.2.54 1.2 1.2v2.88c0 .66-.54 1.2-1.2 1.2z"/>
            </svg>
            <span class="text-xl md:text-2xl font-bold">Coin Farm</span>
        </div>
        <nav class="hidden md:flex space-x-10">
            <button class="hover:text-yellow-400" data-page="home">HOME</button>
            <button class="hover:text-yellow-400" data-page="howToMine">채굴장 이용방법</button>
            <button class="hover:text-yellow-400" data-page="openMiningFarm">채굴장 개설</button>
            <button class="hover:text-yellow-400" data-page="myMiningFarm">내채굴장</button>
            <button class="hover:text-yellow-400" data-page="coinWallet">내지갑</button>
            <button class="hover:text-yellow-400" data-page="withdrawalRequest">출금요청</button>
            <button class="hover:text-yellow-400" data-page="customerService">고객센터</button>
        </nav>
        <div class="flex items-center space-x-2">
            <div id="desktop-auth-buttons" class="hidden md:flex items-center space-x-4">
                <span id="user-info" class="hidden text-gray-400 text-sm md:text-base"></span>
                <button id="login-btn" class="bg-gray-800 text-gray-200 px-4 py-2 rounded-lg hover:bg-gray-700 transition">로그인</button>
                <button id="signup-btn" class="bg-yellow-500 text-gray-900 px-4 py-2 rounded-lg font-bold hover:bg-yellow-400 transition">회원가입</button>
                <button id="member-info-btn" class="hidden bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700 transition">회원정보</button>
                <button id="logout-btn" class="hidden bg-red-600 text-white px-4 py-2 rounded-lg hover:bg-red-700 transition">로그아웃</button>
            </div>
             <!-- Mobile Menu Button -->
            <button id="mobile-menu-button" class="md:hidden p-2 rounded-md text-gray-400 hover:text-white hover:bg-gray-700 flex items-center space-x-2">
                <svg class="h-6 w-6" stroke="currentColor" fill="none" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
                </svg>
                <span>메뉴버튼</span>
            </button>
        </div>
    </header>

    <!-- Mobile Menu -->
    <div id="mobile-menu" class="hidden md:hidden fixed inset-0 bg-gray-900 bg-opacity-95 z-50">
        <div class="flex justify-end p-4">
            <button id="close-mobile-menu">
                <svg class="h-8 w-8 text-white" stroke="currentColor" fill="none" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                </svg>
            </button>
        </div>
        <nav class="flex flex-col items-center space-y-6 mt-10 text-xl">
            <button class="hover:text-yellow-400" data-page="home">HOME</button>
            <button class="hover:text-yellow-400" data-page="howToMine">채굴장 이용방법</button>
            <button class="hover:text-yellow-400" data-page="openMiningFarm">채굴장 개설</button>
            <button class="hover:text-yellow-400" data-page="myMiningFarm">내채굴장</button>
            <button class="hover:text-yellow-400" data-page="coinWallet">내지갑</button>
            <button class="hover:text-yellow-400" data-page="withdrawalRequest">출금요청</button>
            <button class="hover:text-yellow-400" data-page="customerService">고객센터</button>
            <div class="pt-6 border-t border-gray-700 w-3/4 text-center space-y-4">
                 <div id="mobile-auth-buttons">
                    <!-- Mobile auth buttons will be cloned here -->
                 </div>
            </div>
        </nav>
    </div>


    <!-- Main Content Wrapper -->
    <div id="content-container">
        <!-- Home Page -->
        <main id="home-page" class="container mx-auto p-4 md:p-8">
            <!-- Hero Section -->
            <section class="text-center py-16 md:py-10">
                <h1 class="text-3xl md:text-5xl font-bold leading-tight mb-8">
                    전자 화폐 <span class="text-yellow-400">코인 채굴대행 사업</span>
                </h1>
                <p class="text-gray-400 text-lg md:text-xl max-w-2xl mx-auto">
                    채굴테크 암호화폐 채굴대행 서비스를 통해 장비 관리부터 수익 정산까지
                <p class="text-gray-400 text-lg md:text-xl max-w-2xl mx-auto mb-8">    
                    신경쓰지 않고, 편안하게 안정적으로 수익을 창출하세요.
                </p>
                <div class="flex flex-col md:flex-row justify-center space-y-4 md:space-y-0 md:space-x-4">
                </div>
            </section>

            <!-- About Section -->
            <section id="about-section" class="py-26">
                <div class="card p-8 rounded-xl">
                    <h2 class="text-3xl font-bold text-yellow-400 mb-8 text-center">사업 소개</h2>
                    <p class="text-lg text-gray-300 leading-relaxed mb-8">
                        코인 채굴의 난이도 상승에 따라 개인 채굴의 어려움 발생하고 있이며 채굴 풀(Mining Pool)로 채굴을 하며, 전문분석가가 선별한 수익성 있는 코인을 유동성 있게 채굴하여 고수익을 얻고있으며, 
                        당사에 채굴장을 보유하신 채굴장 등급에 따라 채굴 수익을 배분하는 시스템 입니다..
                    </p>
                    <p class="text-lg text-gray-300 leading-relaxed mb-6">
                        최신 채굴 장비와 코인의 동향을 전문적으로 파악하는 기술팀을 바탕으로 효율성을 극대화하고, 투명한 수익 분배 시스템을 통해 고객과의 신뢰를 최우선으로 생각합니다. 또한, 이용자의 편의를 위해 출금 요청 시 USDT테더로 지급하고 있습니다 
                    </p>
                </div>
            </section>

            <!-- Crypto Prices Section -->
            <section id="crypto-prices" class="py-16">
                <div class="flex justify-between items-center mb-8">
                    <div class="flex items-center space-x-4">
                        <h2 class="text-3xl font-bold">코인 시세</h2>
                        <p id="last-updated-time" class="text-m text-gray-400"></p>
                    </div>
                    <button id="analyze-market-btn" class="bg-blue-600 text-white font-bold py-2 px-6 rounded-full btn">
                        시장 분석
                    </button>
                </div>
                <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-6 gap-6">
                    <!-- Bitcoin Card -->
                    <div class="card p-6 rounded-xl flex items-center justify-between">
                        <div>
                            <div class="text-lg text-gray-400">Bitcoin</div>
                            <div id="price-bitcoin" class="text-lg font-bold mt-1">₩0</div>
                        </div>
                        <div class=></div>
                    </div>
                    <!-- USDT Tether Card -->
                    <div class="card p-6 rounded-xl flex items-center justify-between">
                        <div>
                            <div class="text-lg text-gray-400">USDT Tether</div>
                            <div id="price-tether" class="text-lg font-bold mt-1">₩0</div>
                        </div>
                        <div class=></div>
                    </div>
                    <!-- Ethereum Card -->
                    <div class="card p-6 rounded-xl flex items-center justify-between">
                        <div>
                            <div class="text-lg text-gray-400">Ethereum</div>
                            <div id="price-ethereum" class="text-lg font-bold mt-1">₩0</div>
                        </div>
                        <div class=></div>
                    </div>
                    <!-- Dollars Card -->
                    <div class="card p-6 rounded-xl flex items-center justify-between">
                        <div>
                            <div class="text-lg text-gray-400">Dollars</div>
                            <div id="price-dollars" class="text-lg font-bold mt-1">₩0</div>
                        </div>
                        <div class=></div>
                    </div>
                    <!-- Solana Card -->
                    <div class="card p-6 rounded-xl flex items-center justify-between">
                        <div>
                            <div class="text-lg text-gray-400">Solana</div>
                            <div id="price-solana" class="text-lg font-bold mt-1">₩0</div>
                        </div>
                        <div class=></div>
                    </div>
                    <!-- Dogecoin Card -->
                    <div class="card p-6 rounded-xl flex items-center justify-between">
                        <div>
                            <div class="text-lg text-gray-400">Dogecoin</div>
                            <div id="price-dogecoin" class="text-lg font-bold mt-1">₩0</div>
                        </div>
                        <div class=></div>
                    </div>
                </div>
                <!-- Crypto analysis result section -->
                <div id="crypto-analysis-result" class="card p-6 mt-8 rounded-xl hidden">
                    <h3 class="text-xl font-bold text-yellow-400 mb-2">시장 분석 결과</h3>
                    <p id="analysis-text" class="text-gray-300"></p>
                    <div id="analysis-loader" class="flex justify-center mt-4 hidden">
                        <div class="loader"></div>
                    </div>
                </div>
            </section>

            <!-- Mining Plans Section -->
            <section id="plans" class="py-6">
                <h2 class="text-3xl font-bold text-center mb-8">☆ 채굴장 등급 ☆</h2>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <!-- Silver Plan -->
                    <div class="card p-8 rounded-xl text-center border-2 border-yellow-400">
                        <h3 class="text-2xl font-bold text-yellow-400 mb-2">SILVER MINES</h3>
                        <p class="text-lg text-gray-400 mb-2">₩5,000,000</p>
                        <p class="text-gray-300 mb-6">암호화폐 채굴을 처음 시작하는 초급자를 위한 등급입니다. 안정적인 채굴 시스템을 통해 부담 없이 시작할 수 있습니다.</p>
                        </a>
                    </div>
                    <!-- Gold Plan -->
                    <div class="card p-8 rounded-xl text-center border-2 border-yellow-400">
                        <h3 class="text-2xl font-bold text-yellow-400 mb-2">GOLD MINES</h3>
                        <p class="text-lg text-gray-400 mb-2">₩10,000,000</p>
                        <p class="text-gray-300 mb-6">더 높은 수익률을 목표로 하는 중급 채굴자에게 적합합니다. 효율적인 장비로 채굴 속도를 향상시킵니다.</p>
                        </a>
                    </div>
                    <!-- Diamond Plan -->
                    <div class="card p-8 rounded-xl text-center border-2 border-yellow-400">
                        <h3 class="text-2xl font-bold text-yellow-400 mb-2">DIAMOND MINES</h3>
                        <p class="text-lg text-gray-400 mb-2">₩15,000,000</p>
                        <p class="text-gray-300 mb-6">최고의 성능과 최대 수익을 원하는 전문가를 위한 등급입니다. 프리미엄 장비로 최상의 채굴 효율을 경험하세요.</p>
                        </a>
                    </div>
                </div>
            </section>
        </main>

        <!-- How to Mine Page -->
        <main id="howToMine-page" class="container mx-auto p-4 md:p-8 py-16 hidden-page">
            <h1 class="text-3xl md:text-5xl font-bold text-center text-yellow-400 mb-8">채굴장 이용방법</h1>
            <div class="card p-8 rounded-xl max-w-3xl mx-auto space-y-6">
                <p class="text-lg text-gray-300">
                    저희 채굴장 이용은 아주 간단합니다. 아래 단계를 따라 암호화폐 채굴을 시작해 보세요.
                </p>
                <div class="space-y-4">
                    <div class="flex items-start space-x-4">
                        <span class="flex-shrink-0 w-8 h-8 flex items-center justify-center rounded-full bg-yellow-500 text-gray-900 font-bold">1</span>
                        <div>
                            <h3 class="font-bold text-xl">회원가입 및 로그인</h3>
                            <p class="text-gray-400">
                                먼저 웹사이트 상단에서 회원가입을 하고 로그인합니다.
                            </p>
                        </div>
                    </div>
                    <div class="flex items-start space-x-4">
                        <span class="flex-shrink-0 w-8 h-8 flex items-center justify-center rounded-full bg-yellow-500 text-gray-900 font-bold">2</span>
                        <div>
                            <h3 class="font-bold text-xl">채굴장 개설 및 채굴</h3>
                            <p class="text-gray-400">
                                1-초기자금 부담없이 시작하는 실버 채굴장부터 최대 수익성을 보장하는 다이아몬드 채굴장까지, 원하시는 채굴장과 수량을 선택하고 구매신청을 한다.
                            <p class="text-gray-400">    
                                2-고객센터에 개설관련을 선택하고 채굴장 개설 입금계좌를 문의 및 결재 후 내 채굴장에 구매한 채굴장이 활성화 되면 채굴시작을 누른다.
                            </p>
                        </div>
                    </div>
                    <div class="flex items-start space-x-4">
                        <span class="flex-shrink-0 w-8 h-8 flex items-center justify-center rounded-full bg-yellow-500 text-gray-900 font-bold">3</span>
                        <div>
                            <h3 class="font-bold text-xl">출금 요청</h3>
                            <p class="text-gray-400">
                                1-채굴이 시작되면 보유하고 있는 모든 채굴장의 코인이 USDT테더로 환산되어 코인 지갑으로 실시간 저장됩니다.
                            <p class="text-gray-400">
                                2-출금을 할때는 출금요청 페이지에서 양식에 맞게 작성후 고객센터에 출금관련을 선택하고 출금 금액을 기입하고 요청을 보내면 된다.   (최소 출금액은 35 USDT입니다.)
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </main>
        
        <!-- Open Mining Farm Page -->
        <main id="openMiningFarm-page" class="container mx-auto p-4 md:p-8 py-16 hidden-page">
            <h1 class="text-3xl md:text-5xl font-bold text-center text-yellow-400 mb-8">채굴장 개설</h1>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-5xl mx-auto">
                <!-- Silver Plan -->
                <div class="card p-8 rounded-xl text-center border-2 border-yellow-400">
                    <h3 class="text-2xl font-bold text-yellow-400 mb-2">SILVER MINES</h3>
                    <p class="text-lg text-red-400 mb-2">₩5,000,000</p>
                    <p class="text-gray-400 text-sm mb-2">입문자에게 추천!</p>
                    <p class="text-gray-400 text-sm mb-6">안정적인 수익을 체험.</p>
                    <div class="flex flex-col items-center space-y-4">
                        <div class="flex items-center space-x-2">
                            <span class="text-gray-400">수량:</span>
                            <input type="number" value="1" min="1" class="w-16 form-input text-center" />
                        </div>
                        <button class="w-full bg-yellow-500 text-gray-900 font-bold py-3 rounded-full btn" data-type="SILVER MINES">
                            구매하기
                        </button>
                    </div>
                </div>
                <!-- Gold Plan -->
                <div class="card p-8 rounded-xl text-center border-2 border-yellow-400">
                    <h3 class="text-2xl font-bold text-yellow-400 mb-2">GOLD MINES</h3>
                    <p class="text-lg text-red-400 mb-2">₩10,000,000</p>
                    <p class="text-gray-400 text-sm mb-2">중급자에게 적합!</p>
                    <p class="text-gray-400 text-sm mb-6">빨라진 채굴속도와 향상된 수익.</p>
                    <div class="flex flex-col items-center space-y-4">
                        <div class="flex items-center space-x-2">
                            <span class="text-gray-400">수량:</span>
                            <input type="number" value="1" min="1" class="w-16 form-input text-center" />
                        </div>
                        <button class="w-full bg-yellow-500 text-gray-900 font-bold py-3 rounded-full btn" data-type="GOLD MINES">
                            구매하기
                        </button>
                    </div>
                </div>
                <!-- Diamond Plan -->
                <div class="card p-8 rounded-xl text-center border-2 border-yellow-400">
                    <h3 class="text-2xl font-bold text-yellow-400 mb-2">DIAMOND MINES</h3>
                    <p class="text-lg text-red-400 mb-2">₩15,000,000</p>
                    <p class="text-gray-400 text-sm mb-2">높은 수익을 위한 등급!</p>
                    <p class="text-gray-400 text-sm mb-6">최고의 장비로 최대 수익.</p>
                    <div class="flex flex-col items-center space-y-4">
                        <div class="flex items-center space-x-1">
                            <span class="text-gray-400">수량:</span>
                            <input type="number" value="1" min="1" class="w-16 form-input text-center" />
                        </div>
                        <button class="w-full bg-yellow-500 text-gray-900 font-bold py-3 rounded-full btn" data-type="DIAMOND MINES">
                            구매하기
                        </button>
                    </div>
                </div>
            </div>
        </main>

        <!-- My Mining Farm Page -->
        <main id="myMiningFarm-page" class="container mx-auto p-4 md:p-8 py-16 hidden-page">
            <h1 class="text-3xl md:text-5xl font-bold text-center text-yellow-400 mb-8">내 채굴장 현황</h1>
            <div class="card p-8 rounded-xl max-w-5xl mx-auto space-y-6">
                <p class="text-lg text-gray-300">
                    회원님이 보유한 채굴장 현황입니다.
                </p>
                <div id="my-mining-farms-container" class="space-y-8">
                    <!-- Mining farm data will be populated here by grade -->
                </div>
            </div>
        </main>
        
        <!-- Coin Wallet Page -->
        <main id="coinWallet-page" class="container mx-auto p-4 md:p-8 py-16 hidden-page">
            <h1 class="text-3xl md:text-5xl font-bold text-center text-yellow-400 mb-8">코인 지갑</h1>
            <div class="card p-8 rounded-xl max-w-2xl mx-auto space-y-6">
                <div class="text-center">
                    <p class="text-lg text-gray-400">총 보유 채굴량</p>
                    <h2 id="total-mined-usdt" class="text-5xl font-bold text-green-400 mt-2">0.000000 USDT</h2>
                </div>
            </div>
        </main>

        <!-- Withdrawal Request Page -->
        <main id="withdrawalRequest-page" class="container mx-auto p-4 md:p-8 py-16 hidden-page">
            <h1 class="text-3xl md:text-5xl font-bold text-center text-yellow-400 mb-8">출금 요청</h1>
            <div class="max-w-7xl mx-auto flex flex-col lg:flex-row gap-8">
                <!-- Left Column: Withdrawal Form -->
                <div class="lg:w-7/12 card p-8 rounded-xl space-y-6">
                    <p class="text-lg text-gray-300">
                        출금 요청을 하려면 아래 정보를 입력해주세요.
                    </p>
                    <div class="flex items-center justify-between mb-4">
                        <p class="text-gray-400">사용 가능 USDT:</p>
                        <span id="available-usdt" class="text-xl font-bold text-green-400">0.000000 USDT</span>
                    </div>
                    <form id="withdrawal-form" class="space-y-4">
                        <div>
                            <label for="withdrawal-amount" class="block text-gray-400 mb-1">출금 금액 (USDT)</label>
                            <input type="number" id="withdrawal-amount" class="form-input" placeholder="최소 35 USDT" min="35" step="0.000001" required>
                        </div>
                        <div>
                            <label for="wallet-address" class="block text-gray-400 mb-1">지갑 주소</label>
                            <input type="text" id="wallet-address" class="form-input" placeholder="출금받을 지갑 주소 입력" required>
                        </div>
                        <button type="submit" class="w-full bg-yellow-500 text-gray-900 font-bold py-3 rounded-lg btn">
                            출금 요청하기
                        </button>
                    </form>
                </div>
                <!-- Right Column: Withdrawal History -->
                <div class="lg:w-5/12 card p-8 rounded-xl space-y-4">
                    <h2 class="text-2xl font-bold text-yellow-400">출금 요청 내역</h2>
                    <div class="overflow-x-auto">
                        <table class="w-full text-left admin-table">
                            <thead>
                                <tr class="text-gray-400 uppercase text-sm">
                                    <th class="font-normal">요청일</th>
                                    <th class="font-normal">금액 (USDT)</th>
                                    <th class="font-normal">상태</th>
                                </tr>
                            </thead>
                            <tbody id="withdrawal-history-table-body">
                                <!-- History will be populated here -->
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>
        </main>

        <!-- Customer Service Page -->
        <main id="customerService-page" class="container mx-auto p-4 md:p-8 py-16 hidden-page">
            <h1 class="text-3xl md:text-5xl font-bold text-center text-yellow-400 mb-8">고객 센터</h1>
            <div class="max-w-4xl mx-auto">
                <div class="flex justify-end mb-6">
                    <button id="show-inquiry-form-btn" class="bg-yellow-500 text-gray-900 font-bold py-2 px-6 rounded-lg btn">문의하기</button>
                </div>

                <!-- New Inquiry Form -->
                <div id="inquiry-form-container" class="card p-8 rounded-xl mb-8 hidden">
                    <h2 class="text-2xl font-bold mb-4">새 문의 작성</h2>
                    <form id="inquiry-form" class="space-y-4">
                        <div>
                            <label for="inquiry-category" class="block text-gray-400 mb-1">카테고리</label>
                            <select id="inquiry-category" class="form-input" required>
                                <option value="" disabled selected>카테고리를 선택하세요</option>
                                <option value="이용관련">이용관련</option>
                                <option value="개설관련">개설관련</option>
                                <option value="출금관련">출금관련</option>
                                <option value="기타관련">기타관련</option>
                            </select>
                        </div>
                        <div>
                            <label for="inquiry-title" class="block text-gray-400 mb-1">제목</label>
                            <input type="text" id="inquiry-title" class="form-input" required>
                        </div>
                        <div>
                            <label for="inquiry-question" class="block text-gray-400 mb-1">내용</label>
                            <textarea id="inquiry-question" rows="5" class="form-input" required></textarea>
                        </div>
                        <div class="flex justify-end space-x-4">
                             <button type="button" id="cancel-inquiry-btn" class="bg-gray-600 text-white font-bold py-2 px-6 rounded-lg btn">취소</button>
                            <button type="submit" class="bg-blue-600 text-white font-bold py-2 px-6 rounded-lg btn">제출하기</button>
                        </div>
                    </form>
                </div>
                
                <!-- Inquiries List -->
                <div id="inquiries-list" class="space-y-4">
                    <!-- Inquiry items will be populated here -->
                </div>
            </div>
        </main>


        <!-- Admin Page -->
        <main id="admin-page" class="container mx-auto p-4 md:p-8 py-16 hidden-page">
            <h1 class="text-3xl md:text-5xl font-bold text-center text-yellow-400 mb-8">관리자 대시보드</h1>
            
            <div id="admin-dashboard-area">
                <div class="card p-4 rounded-xl mb-8 flex justify-between items-center overflow-x-auto">
                    <button class="flex-shrink-0 px-4 py-2 bg-gray-800 text-gray-300 rounded-lg hover:bg-gray-700 transition" data-section="users">가입회원 정보</button>
                    <button class="flex-shrink-0 px-4 py-2 bg-gray-800 text-gray-300 rounded-lg hover:bg-gray-700 transition" data-section="mining">사용자 채굴현황</button>
                    <button class="flex-shrink-0 px-4 py-2 bg-gray-800 text-gray-300 rounded-lg hover:bg-gray-700 transition" data-section="purchase">채굴장 개설요청</button>
                    <button class="flex-shrink-0 px-4 py-2 bg-gray-800 text-gray-300 rounded-lg hover:bg-gray-700 transition" data-section="withdrawals">출금요청 내역</button>
                    <button class="flex-shrink-0 px-4 py-2 bg-gray-800 text-gray-300 rounded-lg hover:bg-gray-700 transition" data-section="inquiries">고객센터 문의</button>
                </div>

                <div id="mining-input-section" class="card p-8 rounded-xl mb-8">
                    <h2 class="text-2xl font-bold mb-4">등급별 채굴량 입력 (분당)</h2>
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                        <div>
                            <label for="silver-rate" class="block text-gray-400">SILVER MINES (USDT)</label>
                            <input type="number" id="silver-rate" class="form-input mt-1" placeholder="분당 채굴량 입력">
                        </div>
                        <div>
                            <label for="gold-rate" class="block text-gray-400">GOLD MINES (USDT)</label>
                            <input type="number" id="gold-rate" class="form-input mt-1" placeholder="분당 채굴량 입력">
                        </div>
                        <div>
                            <label for="diamond-rate" class="block text-gray-400">DIAMOND MINES (USDT)</label>
                            <input type="number" id="diamond-rate" class="form-input mt-1" placeholder="분당 채굴량 입력">
                        </div>
                    </div>
                    <button id="update-mining-rate-btn" class="mt-6 w-full bg-blue-600 text-white font-bold py-3 rounded-lg btn">채굴량 업데이트</button>
                    <p id="mining-rate-message" class="text-green-400 text-center mt-4 hidden"></p>
                </div>
                
                <section id="users-section">
                    <h2 class="text-2xl font-bold mb-4">가입회원 정보</h2>
                    <div class="mb-4 flex items-center gap-2">
                        <select id="user-search-category" class="form-input w-48 bg-gray-800 border-gray-600">
                            <option value="id">가입번호</option>
                            <option value="username">사용자 아이디</option>
                        </select>
                        <input type="text" id="user-search-input" class="form-input flex-grow" placeholder="검색어 입력...">
                        <button id="user-search-btn" class="bg-blue-600 text-white font-bold py-2 px-4 rounded-lg btn">검색</button>
                    </div>
                    <div class="card p-8 rounded-xl">
                        <div class="overflow-x-auto">
                            <table class="w-full text-left admin-table">
                                <thead>
                                    <tr class="text-gray-400 uppercase text-sm">
                                        <th class="font-normal">가입번호</th>
                                        <th class="font-normal">사용자 아이디</th>
                                        <th class="font-normal">전화번호</th>
                                        <th class="font-normal">가입일</th>
                                        <th class="font-normal">관리</th>
                                    </tr>
                                </thead>
                                <tbody id="users-table-body">
                                    <!-- User data will be populated here -->
                                </tbody>
                            </table>
                        </div>
                    </div>
                </section>

                <section id="mining-section" class="hidden-page">
                    <h2 class="text-2xl font-bold mb-4">사용자 채굴현황</h2>
                    <div class="card p-8 rounded-xl">
                        <div class="overflow-x-auto">
                            <table class="w-full text-left admin-table">
                                <thead>
                                    <tr class="text-gray-400 uppercase text-sm">
                                        <th class="font-normal">가입번호</th>
                                        <th class="font-normal">사용자 아이디</th>
                                        <th class="font-normal">보유 채굴장</th>
                                        <th class="font-normal">총 채굴량 (USDT)</th>
                                    </tr>
                                </thead>
                                <tbody id="mining-table-body">
                                    <!-- Mining data will be populated here -->
                                </tbody>
                            </table>
                        </div>
                    </div>
                </section>

                <section id="purchase-section" class="hidden-page">
                    <h2 class="text-2xl font-bold mb-4">채굴장 개설요청</h2>
                    <div class="card p-8 rounded-xl">
                        <div class="overflow-x-auto">
                            <table class="w-full text-left admin-table">
                                <thead>
                                    <tr class="text-gray-400 uppercase text-sm">
                                        <th class="font-normal">가입번호</th>
                                        <th class="font-normal">사용자 아이디</th>
                                        <th class="font-normal">신청 등급</th>
                                        <th class="font-normal">수량</th>
                                        <th class="font-normal">상태</th>
                                        <th class="font-normal">관리</th>
                                    </tr>
                                </thead>
                                <tbody id="purchase-table-body">
                                    <!-- Purchase data will be populated here -->
                                </tbody>
                            </table>
                        </div>
                    </div>
                </section>

                <section id="withdrawals-section" class="hidden-page">
                    <h2 class="text-2xl font-bold mb-4">출금요청 내역</h2>
                    <div class="card p-8 rounded-xl">
                        <div class="overflow-x-auto">
                            <table class="w-full text-left admin-table">
                                <thead>
                                    <tr class="text-gray-400 uppercase text-sm">
                                        <th class="font-normal">가입번호</th>
                                        <th class="font-normal">사용자 아이디</th>
                                        <th class="font-normal">요청 금액 (USDT)</th>
                                        <th class="font-normal">지갑 주소</th>
                                        <th class="font-normal">상태</th>
                                        <th class="font-normal">요청일</th>
                                        <th class="font-normal">관리</th>
                                    </tr>
                                </thead>
                                <tbody id="withdrawals-table-body">
                                    <!-- Withdrawal data will be populated here -->
                                </tbody>
                            </table>
                        </div>
                    </div>
                </section>
                
                <section id="inquiries-section" class="hidden-page">
                    <h2 class="text-2xl font-bold mb-4">고객센터 문의</h2>
                    <div class="mb-4 flex flex-wrap gap-2" id="admin-inquiry-filters">
                        <button class="bg-blue-600 text-white font-bold py-2 px-4 rounded-lg btn" data-category="전체">전체</button>
                        <button class="bg-gray-700 text-gray-300 font-bold py-2 px-4 rounded-lg btn" data-category="이용관련">이용관련</button>
                        <button class="bg-gray-700 text-gray-300 font-bold py-2 px-4 rounded-lg btn" data-category="개설관련">개설관련</button>
                        <button class="bg-gray-700 text-gray-300 font-bold py-2 px-4 rounded-lg btn" data-category="출금관련">출금관련</button>
                        <button class="bg-gray-700 text-gray-300 font-bold py-2 px-4 rounded-lg btn" data-category="기타관련">기타관련</button>
                    </div>
                    <div id="admin-inquiries-list" class="space-y-4">
                       <!-- Admin inquiries will be populated here -->
                    </div>
                </section>
            </div>
        </main>

    </div>

    <!-- Footer -->
    <footer class="text-center py-6 border-t border-gray-700">
        <p class="text-gray-400 text-sm">
            © 2025 LIVIKA LP. All rights reserved.
        </p>
        <p class="text-gray-500 text-xs mt-1">
            * Crypto currency mining은 외국인을 위한 서비스를 제공하지 않습니다.
        </p>
        <button id="admin-page-link" class="text-blue-400 hover:underline mt-2">관리자 페이지</button>
    </footer>

    <!-- Auth Modal -->
    <div id="auth-modal" class="modal-overlay">
        <div class="modal-content">
            <div class="flex justify-between items-center mb-4">
                <h3 id="modal-title" class="text-2xl font-bold text-yellow-400">로그인</h3>
                <button id="close-modal" class="text-gray-400 hover:text-gray-200 text-2xl font-bold">&times;</button>
            </div>
            <!-- Login Form -->
            <form id="login-form" class="space-y-4">
                <input id="login-username" type="text" placeholder="사용자 아이디" class="form-input" required>
                <input id="login-password" type="password" placeholder="비밀번호" class="form-input" required>
                <button type="submit" class="w-full bg-yellow-500 text-gray-900 font-bold py-3 rounded-lg btn">로그인</button>
            </form>
            <!-- Signup Form -->
            <form id="signup-form" class="space-y-4 hidden">
                <input id="signup-username" type="text" placeholder="사용자 아이디" class="form-input" required>
                <input id="signup-password" type="password" placeholder="비밀번호" class="form-input" required>
                <input id="signup-password-confirm" type="password" placeholder="비밀번호 확인" class="form-input" required>
                <input id="signup-phone" type="tel" placeholder="휴대전화번호" class="form-input" required>
                <button type="submit" class="w-full bg-yellow-500 text-gray-900 font-bold py-3 rounded-lg btn">가입하기</button>
            </form>
            <p id="modal-message" class="text-center text-red-400 mt-4 hidden"></p>
        </div>
    </div>

    <!-- User Details Modal -->
    <div id="user-details-modal" class="modal-overlay">
        <div class="modal-content" style="max-width: 600px;">
            <div class="flex justify-between items-center mb-3">
                <h3 class="text-xl font-bold text-yellow-400">회원 상세 정보</h3>
                <button id="close-user-details-modal" class="text-gray-400 hover:text-gray-200 text-2xl font-bold">&times;</button>
            </div>
            <div id="user-details-content" class="space-y-3 text-gray-300 pr-2">
                <!-- Basic Info -->
                <div class="border-b border-gray-700 pb-2">
                    <h4 class="text-lg font-bold text-yellow-400 mb-1">기본 정보</h4>
                    <p class="text-sm"><strong>사용자 아이디:</strong> <span id="detail-username"></span></p>
                    <p class="text-sm"><strong>비밀번호:</strong> <span id="detail-password"></span></p>
                    <p class="text-sm"><strong>전화번호:</strong> <span id="detail-phone"></span></p>
                    <p class="text-sm"><strong>가입일:</strong> <span id="detail-signup-date"></span></p>
                </div>
                <!-- Mining Info -->
                <div class="border-b border-gray-700 pb-2">
                    <h4 class="text-lg font-bold text-yellow-400 mb-1">채굴장 현황</h4>
                    <div id="detail-farms"></div>
                </div>
                <!-- Coin Info -->
                <div class="border-b border-gray-700 pb-2">
                    <h4 class="text-lg font-bold text-yellow-400 mb-1">코인 현황 (USDT)</h4>
                    <p class="text-sm"><strong>누적 채굴량:</strong> <span id="detail-total-mined"></span></p>
                    <p class="text-sm"><strong>누적 출금액:</strong> <span id="detail-total-withdrawn" class="font-bold text-red-400"></span></p>
                    <p class="font-bold text-green-400 text-base"><strong>잔여 코인:</strong> <span id="detail-balance"></span></p>
                </div>
                <!-- Password Change Section -->
                <div>
                    <h4 class="text-lg font-bold text-yellow-400 mb-1">비밀번호 변경</h4>
                     <div class="space-y-2">
                        <input type="hidden" id="password-change-user-id">
                        <input type="password" id="new-password" class="form-input text-sm" placeholder="새 비밀번호">
                        <input type="password" id="confirm-new-password" class="form-input text-sm" placeholder="새 비밀번호 확인">
                        <button id="change-password-btn" class="w-full bg-yellow-500 text-gray-900 font-bold py-2 rounded-lg btn">변경하기</button>
                        <p id="password-change-message" class="text-center text-xs mt-2 hidden"></p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Message Modal -->
    <div id="message-modal" class="modal-overlay">
        <div class="modal-content">
            <div class="flex justify-between items-center mb-4">
                <h3 id="message-modal-title" class="text-2xl font-bold text-yellow-400">알림</h3>
                <button id="message-modal-close" class="text-gray-400 hover:text-gray-200 text-2xl font-bold">&times;</button>
            </div>
            <p id="message-modal-content" class="text-gray-300 text-center"></p>
            <div class="mt-6 text-center">
                <button id="message-modal-confirm-btn" class="bg-yellow-500 text-gray-900 font-bold py-2 px-8 rounded-lg btn">확인</button>
            </div>
        </div>
    </div>

    <!-- Admin Login Modal -->
    <div id="admin-login-modal" class="modal-overlay">
        <div class="modal-content">
            <div class="flex justify-between items-center mb-4">
                <h3 class="text-2xl font-bold text-yellow-400">관리자 로그인</h3>
                <button id="close-admin-modal" class="text-gray-400 hover:text-gray-200 text-2xl font-bold">&times;</button>
            </div>
            <form id="admin-login-form" class="space-y-4">
                <input id="admin-login-username" type="text" placeholder="관리자 아이디" class="form-input" required>
                <input id="admin-login-password" type="password" placeholder="비밀번호" class="form-input" required>
                <button type="submit" class="w-full bg-red-600 text-white font-bold py-3 rounded-lg btn">로그인</button>
            </form>
            <p id="admin-modal-message" class="text-center text-red-400 mt-4 hidden"></p>
        </div>
    </div>

    <script>
        const pages = ['home', 'howToMine', 'openMiningFarm', 'myMiningFarm', 'coinWallet', 'withdrawalRequest', 'admin', 'customerService'];
        const pageElements = pages.reduce((acc, page) => {
            acc[page] = document.getElementById(`${page}-page`);
            return acc;
        }, {});
        
        const contentContainer = document.getElementById('content-container');
        const loginBtn = document.getElementById('login-btn');
        const signupBtn = document.getElementById('signup-btn');
        const logoutBtn = document.getElementById('logout-btn');
        const userInfoSpan = document.getElementById('user-info');
        const authModal = document.getElementById('auth-modal');
        const closeModalBtn = document.getElementById('close-modal');
        const loginForm = document.getElementById('login-form');
        const signupForm = document.getElementById('signup-form');
        const modalTitle = document.getElementById('modal-title');
        const modalMessage = document.getElementById('modal-message');
        const adminPageLink = document.getElementById('admin-page-link');
        const adminSections = ['users', 'mining', 'purchase', 'withdrawals', 'inquiries'];
        const adminLoginModal = document.getElementById('admin-login-modal');
        const closeAdminModalBtn = document.getElementById('close-admin-modal');
        const adminLoginForm = document.getElementById('admin-login-form');
        const userDetailsModal = document.getElementById('user-details-modal');
        const closeUserDetailsModalBtn = document.getElementById('close-user-details-modal');
        const memberInfoBtn = document.getElementById('member-info-btn');
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');
        const closeMobileMenu = document.getElementById('close-mobile-menu');

        let isLoggedIn = false;
        let currentUser = null;
        let globalMiningInterval = null; // Variable to hold the global mining interval
        let activePage = 'home'; // Variable to track the currently active page
        let miningRates = {
            'SILVER MINES': 0,
            'GOLD MINES': 0,
            'DIAMOND MINES': 0
        };

        // --- Initialize Admin Account ---
        const initializeAdminAccount = () => {
            const users = getUsers();
            const adminExists = users.some(user => user.username === 'admin');
            
            if (!adminExists) {
                const adminUser = {
                    id: generateNewUserId(),
                    username: 'admin',
                    password: 'admin12',
                    phone: '000-0000-0000',
                    signupDate: new Date().toLocaleDateString('ko-KR'),
                    isAdmin: true
                };
                users.push(adminUser);
                saveUsers(users);
            }
        };

        // --- LocalStorage Data Management ---
        const getUsers = () => JSON.parse(localStorage.getItem('users')) || [];
        const saveUsers = (users) => localStorage.setItem('users', JSON.stringify(users));
        const getPurchases = () => JSON.parse(localStorage.getItem('purchases')) || [];
        const savePurchases = (purchases) => localStorage.setItem('purchases', JSON.stringify(purchases));
        const getWithdrawalRequests = () => JSON.parse(localStorage.getItem('withdrawalRequests')) || [];
        const saveWithdrawalRequests = (requests) => localStorage.setItem('withdrawalRequests', JSON.stringify(requests));
        const getMyMiningFarms = () => JSON.parse(localStorage.getItem('miningFarms')) || [];
        const saveMiningFarms = (farms) => localStorage.setItem('miningFarms', JSON.stringify(farms));
        const getMiningRates = () => JSON.parse(localStorage.getItem('miningRates')) || miningRates;
        const saveMiningRates = (rates) => localStorage.setItem('miningRates', JSON.stringify(rates));
        const getInquiries = () => JSON.parse(localStorage.getItem('inquiries')) || [];
        const saveInquiries = (inquiries) => localStorage.setItem('inquiries', JSON.stringify(inquiries));
        const getCryptoPrices = () => JSON.parse(localStorage.getItem('cryptoPrices'));
        const saveCryptoPrices = (data) => localStorage.setItem('cryptoPrices', JSON.stringify(data));

        // Helper to format currency
        const formatCurrency = (amount) => {
            return `₩${Math.round(amount).toLocaleString('ko-KR')}`;
        };

        // Helper to format date
        const formatDateTime = (date) => {
            if (!date) return '미기록';
            const d = new Date(date);
            return `${d.toLocaleDateString()} ${d.toLocaleTimeString()}`;
        };
        
        // Helper to format duration
        const formatDuration = (milliseconds) => {
            if (milliseconds < 0) return '0초';
            const seconds = Math.floor(milliseconds / 1000);
            const minutes = Math.floor(seconds / 60);
            const hours = Math.floor(minutes / 60);
            const days = Math.floor(hours / 24);
            
            let parts = [];
            if (days > 0) parts.push(`${days}일`);
            if (hours % 24 > 0) parts.push(`${hours % 24}시간`);
            if (minutes % 60 > 0) parts.push(`${minutes % 60}분`);
            if (seconds % 60 > 0) parts.push(`${seconds % 60}초`);
            
            return parts.length > 0 ? parts.join(' ') : '0초';
        };

        // Generate new user ID based on signup date and sequence
        const generateNewUserId = () => {
            const now = new Date();
            const year = now.getFullYear().toString().slice(-2);
            const month = (now.getMonth() + 1).toString().padStart(2, '0');
            const day = now.getDate().toString().padStart(2, '0');
            const datePrefix = `${year}${month}${day}`;

            let counterData = JSON.parse(localStorage.getItem('userCounter')) || {};
            let sequence = 1;

            if (counterData.date === datePrefix) {
                sequence = counterData.sequence + 1;
            }

            localStorage.setItem('userCounter', JSON.stringify({ date: datePrefix, sequence: sequence }));

            const sequenceString = sequence.toString().padStart(2, '0');
            return `${datePrefix}${sequenceString}`;
        };
        
        // ---- Crypto Price Update Logic ----
        const renderCryptoPrices = () => {
            const cryptoData = getCryptoPrices();
            if (!cryptoData) return;

            document.getElementById('price-bitcoin').textContent = formatCurrency(cryptoData.prices.bitcoin);
            document.getElementById('price-tether').textContent = formatCurrency(cryptoData.prices.tether);
            document.getElementById('price-ethereum').textContent = formatCurrency(cryptoData.prices.ethereum);
            document.getElementById('price-dollars').textContent = formatCurrency(cryptoData.prices.dollars);
            document.getElementById('price-solana').textContent = formatCurrency(cryptoData.prices.solana);
            document.getElementById('price-dogecoin').textContent = formatCurrency(cryptoData.prices.dogecoin);
            
            const lastUpdatedElement = document.getElementById('last-updated-time');
            lastUpdatedElement.textContent = `(마지막 업데이트: ${formatDateTime(cryptoData.lastUpdated)})`;
        };

        const updateCryptoPrices = () => {
            // Base prices are updated to reflect current market rates from sources like Google Finance.
            // Direct scraping from external sites is blocked by browser security (CORS), so we simulate real-time fluctuation.
            const basePrices = {
                bitcoin: 97092000,
                tether: 1390,
                ethereum: 4894000,
                dollars: 1390, // Represents USD/KRW exchange rate
                solana: 229600,
                dogecoin: 209
            };

            // Simulate price fluctuation by +/- 5%
            const fluctuate = (price) => {
                const changePercent = (Math.random() - 0.5) * 0.10; 
                return price * (1 + changePercent);
            };

            const newPrices = {
                bitcoin: fluctuate(basePrices.bitcoin),
                tether: fluctuate(basePrices.tether),
                ethereum: fluctuate(basePrices.ethereum),
                dollars: fluctuate(basePrices.dollars),
                solana: fluctuate(basePrices.solana),
                dogecoin: fluctuate(basePrices.dogecoin)
            };

            const cryptoData = {
                lastUpdated: Date.now(),
                prices: newPrices
            };

            saveCryptoPrices(cryptoData);
            renderCryptoPrices();
        };

        const initCryptoPrices = () => {
            // To meet the request of updating on every refresh, we call the update function directly.
            // This simulates fetching new data each time the page loads.
            updateCryptoPrices();

            // Set an interval to also update prices periodically while the page is open.
            const sixHours = 6 * 60 * 60 * 1000;
            setInterval(updateCryptoPrices, sixHours);
        };

        // Show a page and hide others
        const showPage = (pageId) => {
            if (pageId === 'admin' && (!isLoggedIn || !currentUser || !currentUser.isAdmin)) {
                adminLoginModal.style.display = 'flex';
                return;
            }
            activePage = pageId; // Update the active page tracker
            pages.forEach(page => {
                if (pageElements[page]) {
                    pageElements[page].classList.add('hidden-page');
                }
            });
            if (pageElements[pageId]) {
                pageElements[pageId].classList.remove('hidden-page');
            }

            // Perform an initial render of the page's content
            if (pageId === 'admin') {
                document.getElementById('user-search-input').value = ''; // Reset search field
                renderAdminUsers();
                renderAdminPurchases();
                renderAdminWithdrawals();
                renderAdminInquiries();
                renderAdminMiningStatus();
            } else if (pageId === 'myMiningFarm') {
                renderMyMiningFarms();
            } else if (pageId === 'coinWallet') {
                renderCoinWallet();
            } else if (pageId === 'withdrawalRequest') {
                renderWithdrawalRequest();
            } else if (pageId === 'customerService') {
                renderCustomerServicePage();
            }
        };
        
        const startGlobalMiningInterval = () => {
            if (globalMiningInterval) clearInterval(globalMiningInterval);

            globalMiningInterval = setInterval(() => {
                if (!isLoggedIn || !currentUser) return;

                const allFarms = getMyMiningFarms();
                const rates = getMiningRates();
                let hasChanges = false;

                // --- Data Calculation ---
                const userActiveFarms = allFarms.filter(farm => farm.userId === currentUser.id && farm.isMining);
                if (userActiveFarms.length === 0) return;

                const groupedFarms = userActiveFarms.reduce((acc, farm) => {
                    (acc[farm.miningType] = acc[farm.miningType] || []).push(farm);
                    return acc;
                }, {});

                for (const type in groupedFarms) {
                    if (rates[type] && rates[type] > 0) {
                        const totalRateForType = rates[type];
                        const count = groupedFarms[type].length;
                        const individualRate = count > 0 ? totalRateForType / count : 0;
                        
                        groupedFarms[type].forEach(farm => {
                            const now = Date.now();
                            const lastUpdate = new Date(farm.lastUpdateTime).getTime() || now;
                            const elapsedTime = now - lastUpdate;
                            if (elapsedTime > 0) {
                                farm.minedAmount += (elapsedTime / (1000 * 60)) * individualRate;
                                farm.lastUpdateTime = new Date().toISOString();
                                hasChanges = true;
                            }
                        });
                    }
                }

                if (hasChanges) {
                    saveMiningFarms(allFarms);
                }
                
                // --- UI Rendering based on active page ---
                if (activePage === 'myMiningFarm') {
                    renderMyMiningFarms();
                } else if (activePage === 'coinWallet') {
                    renderCoinWallet();
                } else if (activePage === 'withdrawalRequest') {
                    renderWithdrawalRequest();
                }
            }, 1000);
        };
        
        const stopGlobalMiningInterval = () => {
            if (globalMiningInterval) {
                clearInterval(globalMiningInterval);
                globalMiningInterval = null;
            }
        };

        // Show a custom message modal
        const showMessageModal = (title, message) => {
            const messageModal = document.getElementById('message-modal');
            const messageTitle = document.getElementById('message-modal-title');
            const messageContent = document.getElementById('message-modal-content');

            messageTitle.textContent = title;
            messageContent.textContent = message;
            messageModal.style.display = 'flex';
        };

        const handleUserSearch = () => {
            const category = document.getElementById('user-search-category').value;
            const searchTerm = document.getElementById('user-search-input').value.toLowerCase().trim();
            const allUsers = getUsers();

            if (!searchTerm) {
                renderAdminUsers(allUsers);
                return;
            }

            const filteredUsers = allUsers.filter(user => {
                if (category === 'id') {
                    return user.id.toString().toLowerCase().includes(searchTerm);
                } else if (category === 'username') {
                    return user.username.toLowerCase().includes(searchTerm);
                }
                return false;
            });

            renderAdminUsers(filteredUsers);
        };

        const closeMessageModal = () => {
            const messageModal = document.getElementById('message-modal');
            messageModal.style.display = 'none';
        };

        const showUserDetails = (userId) => {
            const users = getUsers();
            const user = users.find(u => u.id === userId);
            if (!user) return;

            // Clear previous state and set the user ID for the password change form
            document.getElementById('password-change-user-id').value = userId;
            document.getElementById('new-password').value = '';
            document.getElementById('confirm-new-password').value = '';
            document.getElementById('password-change-message').classList.add('hidden');

            // Basic Info
            document.getElementById('detail-username').textContent = user.username;
            document.getElementById('detail-password').textContent = user.password;
            document.getElementById('detail-phone').textContent = user.phone;
            document.getElementById('detail-signup-date').textContent = user.signupDate;

            // Farm Info
            const allFarms = getMyMiningFarms();
            const userFarms = allFarms.filter(farm => farm.userId === userId);
            const farmsContainer = document.getElementById('detail-farms');
            farmsContainer.innerHTML = ''; 

            const allPurchases = getPurchases();
            const farmsByGrade = {};
            userFarms.forEach(farm => {
                if (!farmsByGrade[farm.miningType]) {
                    farmsByGrade[farm.miningType] = [];
                }
                farmsByGrade[farm.miningType].push(farm);
            });

            const grades = ['SILVER MINES', 'GOLD MINES', 'DIAMOND MINES'];
            grades.forEach(grade => {
                const farms = farmsByGrade[grade] || [];
                const gradeDiv = document.createElement('div');
                gradeDiv.classList.add('mb-2');
                
                let farmListHtml = farms.map((farm, index) => {
                    const purchase = allPurchases.find(p => p.id === farm.purchaseId);
                    const openDate = purchase ? purchase.date : 'N/A';
                    const farmNumber = `${grade.split(' ')[0]}-${(index + 1).toString().padStart(2, '0')}`;
                    return `<li class="text-gray-400">채굴장 NO: ${farmNumber}, 개설일: ${openDate}</li>`;
                }).join('');
                
                gradeDiv.innerHTML = `
                    <p class="text-sm"><strong>${grade}:</strong> ${farms.length}개 보유</p>
                    ${farms.length > 0 ? `<ul class="list-disc list-inside text-sm pl-4">${farmListHtml}</ul>` : ''}
                `;
                farmsContainer.appendChild(gradeDiv);
            });

            // Coin Info
            const totalMined = userFarms.reduce((sum, farm) => sum + farm.minedAmount, 0);

            const allWithdrawals = getWithdrawalRequests();
            const userWithdrawals = allWithdrawals.filter(w => w.userId === userId);

            const totalWithdrawnApproved = userWithdrawals
                .filter(w => w.status === '승인 완료')
                .reduce((sum, req) => sum + req.amount, 0);
            
            const totalWithdrawnOrPending = userWithdrawals
                .reduce((sum, req) => sum + req.amount, 0);

            const balance = totalMined - totalWithdrawnOrPending;

            document.getElementById('detail-total-mined').textContent = `${totalMined.toFixed(6)} USDT`;
            document.getElementById('detail-total-withdrawn').textContent = `${totalWithdrawnApproved.toFixed(6)} USDT`;
            document.getElementById('detail-balance').textContent = `${balance.toFixed(6)} USDT`;

            userDetailsModal.style.display = 'flex';
        };

        // Event listeners for page navigation
        document.querySelectorAll('nav button').forEach(button => {
            button.addEventListener('click', () => {
                const pageId = button.dataset.page;
                if (!isLoggedIn && ['myMiningFarm', 'coinWallet', 'withdrawalRequest', 'customerService', 'openMiningFarm'].includes(pageId)) {
                    showMessageModal('알림', '로그인 후 이용 가능합니다.');
                    return;
                }
                showPage(pageId);
                // For mobile menu, also close the menu
                if (mobileMenu && !mobileMenu.classList.contains('hidden')) {
                    mobileMenu.classList.add('hidden');
                }
            });
        });
        
        closeUserDetailsModalBtn.addEventListener('click', () => {
            userDetailsModal.style.display = 'none';
        });

        memberInfoBtn.addEventListener('click', () => {
            if (isLoggedIn && currentUser) {
                showUserDetails(currentUser.id);
            }
        });

        document.getElementById('user-search-btn').addEventListener('click', handleUserSearch);
        document.getElementById('user-search-input').addEventListener('keyup', (e) => {
            if (e.key === 'Enter') {
                handleUserSearch();
            } else if (e.target.value === '') {
                handleUserSearch();
            }
        });

        // Event listener for admin page link
        adminPageLink.addEventListener('click', (e) => {
            e.preventDefault();
            showPage('admin');
        });

        // Event listeners for admin dashboard sections
        document.querySelectorAll('#admin-dashboard-area button[data-section]').forEach(button => {
            button.addEventListener('click', () => {
                const sectionId = button.dataset.section;
                adminSections.forEach(section => {
                    const sectionElement = document.getElementById(`${section}-section`);
                    if (sectionElement) {
                        sectionElement.classList.add('hidden-page');
                    }
                });
                const targetSection = document.getElementById(`${sectionId}-section`);
                if (targetSection) {
                    targetSection.classList.remove('hidden-page');
                }
                
                if (sectionId === 'users') renderAdminUsers();
                else if (sectionId === 'purchase') renderAdminPurchases();
                else if (sectionId === 'withdrawals') renderAdminWithdrawals();
                else if (sectionId === 'inquiries') renderAdminInquiries();
                else if (sectionId === 'mining') renderAdminMiningStatus();
            });
        });

        // Show auth modal
        loginBtn.addEventListener('click', () => {
            modalTitle.textContent = '로그인';
            loginForm.classList.remove('hidden');
            signupForm.classList.add('hidden');
            authModal.style.display = 'flex';
            modalMessage.classList.add('hidden');
        });

        signupBtn.addEventListener('click', () => {
            modalTitle.textContent = '회원가입';
            loginForm.classList.add('hidden');
            signupForm.classList.remove('hidden');
            authModal.style.display = 'flex';
            modalMessage.classList.add('hidden');
        });

        closeModalBtn.addEventListener('click', () => {
            authModal.style.display = 'none';
        });

        // Login logic
        loginForm.addEventListener('submit', (e) => {
            e.preventDefault();
            const username = document.getElementById('login-username').value;
            const password = document.getElementById('login-password').value;
            const users = getUsers();
            const user = users.find(u => u.username === username && u.password === password);
            if (user) {
                isLoggedIn = true;
                currentUser = user;
                updateAuthUI();
                authModal.style.display = 'none';
                showMessageModal('로그인 성공', '환영합니다!');
                startGlobalMiningInterval();
            } else {
                modalMessage.textContent = '아이디 또는 비밀번호가 올바르지 않습니다.';
                modalMessage.classList.remove('hidden');
            }
        });

        // Signup logic
        signupForm.addEventListener('submit', (e) => {
            e.preventDefault();
            const username = document.getElementById('signup-username').value;
            const password = document.getElementById('signup-password').value;
            const confirmPassword = document.getElementById('signup-password-confirm').value;
            const phone = document.getElementById('signup-phone').value;
            
            if (password !== confirmPassword) {
                modalMessage.textContent = '비밀번호가 일치하지 않습니다.';
                modalMessage.classList.remove('hidden');
                return;
            }

            if (username.toLowerCase() === 'admin') {
                modalMessage.textContent = '이 아이디는 사용할 수 없습니다.';
                modalMessage.classList.remove('hidden');
                return;
            }

            const users = getUsers();
            if (users.find(u => u.username === username)) {
                modalMessage.textContent = '이미 사용 중인 아이디입니다.';
                modalMessage.classList.remove('hidden');
                return;
            }
            
            const isAdmin = false; // Regular users cannot be admin

            const newUser = {
                id: generateNewUserId(),
                username,
                password,
                phone,
                signupDate: new Date().toLocaleDateString('ko-KR'),
                isAdmin: isAdmin
            };
            users.push(newUser);
            saveUsers(users);

            signupForm.classList.add('hidden');
            loginForm.classList.remove('hidden');
            modalTitle.textContent = '로그인';
            modalMessage.textContent = '회원가입이 완료되었습니다. 로그인 해주세요!';
            modalMessage.classList.remove('hidden');

            setTimeout(() => modalMessage.classList.add('hidden'), 3000);
        });

        // Logout logic
        logoutBtn.addEventListener('click', () => {
            isLoggedIn = false;
            currentUser = null;
            updateAuthUI();
            stopGlobalMiningInterval();
            showPage('home');
            showMessageModal('로그아웃', '성공적으로 로그아웃되었습니다.');
        });

        // New Admin Login Modal Logic
        closeAdminModalBtn.addEventListener('click', () => {
            adminLoginModal.style.display = 'none';
            document.getElementById('admin-modal-message').classList.add('hidden'); // Also hide message on close
        });

        adminLoginForm.addEventListener('submit', (e) => {
            e.preventDefault();
            const username = document.getElementById('admin-login-username').value;
            const password = document.getElementById('admin-login-password').value;
            const adminModalMessage = document.getElementById('admin-modal-message');

            const users = getUsers();
            const user = users.find(u => u.username === username && u.password === password);

            if (user && user.isAdmin) {
                isLoggedIn = true;
                currentUser = user;
                updateAuthUI();
                adminLoginModal.style.display = 'none';
                adminModalMessage.classList.add('hidden');
                showPage('admin');
                startGlobalMiningInterval();
            } else {
                adminModalMessage.textContent = '관리자 아이디 또는 비밀번호가 올바르지 않습니다.';
                adminModalMessage.classList.remove('hidden');
            }
        });

        // Update UI based on auth state
        const updateAuthUI = () => {
             const desktopAuthContainer = document.getElementById('desktop-auth-buttons');
             const mobileAuthContainer = document.getElementById('mobile-auth-buttons');
             
             // Clear previous buttons
             mobileAuthContainer.innerHTML = '';
             
             // Clone desktop buttons to mobile menu
             Array.from(desktopAuthContainer.children).forEach(node => {
                const clone = node.cloneNode(true);
                clone.id = `mobile-${node.id}`; // Ensure unique IDs
                clone.classList.remove('hidden', 'md:flex');
                clone.classList.add('w-full', 'block');
                mobileAuthContainer.appendChild(clone);
             });
             
             const mobileLoginBtn = document.getElementById('mobile-login-btn');
             const mobileSignupBtn = document.getElementById('mobile-signup-btn');
             const mobileMemberInfoBtn = document.getElementById('mobile-member-info-btn');
             const mobileLogoutBtn = document.getElementById('mobile-logout-btn');
             const mobileUserInfo = document.getElementById('mobile-user-info');
             
            if (isLoggedIn) {
                loginBtn.classList.add('hidden');
                signupBtn.classList.add('hidden');
                logoutBtn.classList.remove('hidden');
                memberInfoBtn.classList.remove('hidden');
                userInfoSpan.classList.remove('hidden');
                userInfoSpan.textContent = `${currentUser.username}님`;

                // Mobile view
                if(mobileLoginBtn) mobileLoginBtn.classList.add('hidden');
                if(mobileSignupBtn) mobileSignupBtn.classList.add('hidden');
                if(mobileLogoutBtn) mobileLogoutBtn.classList.remove('hidden');
                if(mobileMemberInfoBtn) mobileMemberInfoBtn.classList.remove('hidden');
                if(mobileUserInfo) {
                    mobileUserInfo.classList.remove('hidden');
                    mobileUserInfo.textContent = `${currentUser.username}님`;
                }

            } else {
                loginBtn.classList.remove('hidden');
                signupBtn.classList.remove('hidden');
                logoutBtn.classList.add('hidden');
                memberInfoBtn.classList.add('hidden');
                userInfoSpan.classList.add('hidden');

                // Mobile view
                if(mobileLoginBtn) mobileLoginBtn.classList.remove('hidden');
                if(mobileSignupBtn) mobileSignupBtn.classList.remove('hidden');
                if(mobileLogoutBtn) mobileLogoutBtn.classList.add('hidden');
                if(mobileMemberInfoBtn) mobileMemberInfoBtn.classList.add('hidden');
                if(mobileUserInfo) mobileUserInfo.classList.add('hidden');
            }
            
            // Re-attach event listeners for cloned mobile buttons
            if (mobileLoginBtn) {
                mobileLoginBtn.addEventListener('click', () => {
                    mobileMenu.classList.add('hidden');
                    loginBtn.click();
                });
            }
            if(mobileSignupBtn) {
                 mobileSignupBtn.addEventListener('click', () => {
                    mobileMenu.classList.add('hidden');
                    signupBtn.click();
                });
            }
            if(mobileMemberInfoBtn) {
                mobileMemberInfoBtn.addEventListener('click', () => {
                    mobileMenu.classList.add('hidden');
                    memberInfoBtn.click();
                });
            }
             if(mobileLogoutBtn) {
                mobileLogoutBtn.addEventListener('click', () => {
                    mobileMenu.classList.add('hidden');
                    logoutBtn.click();
                });
            }

        };
        
        // Handle purchase button clicks
        document.querySelectorAll('#openMiningFarm-page .btn').forEach(button => {
            button.addEventListener('click', (e) => {
                if (!isLoggedIn) {
                    showMessageModal('알림', '로그인 후 이용 가능합니다.');
                    return;
                }
                const card = e.target.closest('.card');
                const miningType = e.target.dataset.type;
                const quantity = parseInt(card.querySelector('input').value, 10);
                
                const newPurchaseId = Date.now().toString() + Math.random().toString(36).substring(2, 7);

                const purchases = getPurchases();
                purchases.push({
                    id: newPurchaseId,
                    userId: currentUser.id,
                    miningType,
                    quantity: quantity,
                    date: new Date().toLocaleDateString('ko-KR'),
                    status: '대기 중'
                });
                savePurchases(purchases);

                let miningFarms = getMyMiningFarms();
                for (let i = 0; i < quantity; i++) {
                    miningFarms.push({
                        id: `${miningType.charAt(0)}${Date.now().toString().slice(-4)}${i}`,
                        purchaseId: newPurchaseId,
                        userId: currentUser.id,
                        miningType: miningType,
                        minedAmount: 0.0,
                        isMining: false,
                        isApproved: false,
                        startTime: null,
                        stopTime: null,
                        lastUpdateTime: new Date().toISOString()
                    });
                }
                saveMiningFarms(miningFarms);

                showMessageModal('구매 신청 완료', `${miningType} ${quantity}개 구매 신청이 완료되었습니다.`);
            });
        });

        // Render user data on admin page
        const renderAdminUsers = (usersToRender) => {
            const users = usersToRender || getUsers();
            const tableBody = document.getElementById('users-table-body');
            tableBody.innerHTML = '';
            users.forEach(user => {
                const row = document.createElement('tr');

                let manageButtonHtml;
                if (user.isAdmin) {
                    manageButtonHtml = `<span class="bg-blue-600 text-white px-3 py-1 rounded-lg text-sm">관리자</span>`;
                } else {
                    manageButtonHtml = `<button class="bg-red-600 text-white px-3 py-1 rounded-lg text-sm delete-user-btn" data-user-id="${user.id}">삭제</button>`;
                }

                row.innerHTML = `
                    <td>${user.id}</td>
                    <td><button class="text-yellow-400 hover:underline user-detail-link" data-user-id="${user.id}">${user.username}</button></td>
                    <td>${user.phone}</td>
                    <td>${user.signupDate}</td>
                    <td>
                        ${manageButtonHtml}
                    </td>
                `;
                tableBody.appendChild(row);
            });
        };

        document.getElementById('users-table-body').addEventListener('click', (e) => {
            const target = e.target;
            if (target.classList.contains('user-detail-link')) {
                e.preventDefault();
                const userId = target.dataset.userId;
                showUserDetails(userId);
            } else if (target.classList.contains('delete-user-btn')) {
                const userId = target.dataset.userId;
                
                const users = getUsers();
                const userToDelete = users.find(u => u.id === userId);

                if (userToDelete && userToDelete.isAdmin) {
                    showMessageModal('삭제 불가', '관리자 계정은 삭제할 수 없습니다.');
                    return;
                }

                let updatedUsers = users.filter(user => user.id !== userId);
                saveUsers(updatedUsers);
                handleUserSearch(); 
                showMessageModal('회원 삭제', '회원 정보가 삭제되었습니다.');
            }
        });

        // Render purchase data on admin page
        const renderAdminPurchases = () => {
            const purchases = getPurchases();
            const users = getUsers();
            const tableBody = document.getElementById('purchase-table-body');
            tableBody.innerHTML = '';
            purchases.forEach(purchase => {
                const user = users.find(u => u.id === purchase.userId);
                const username = user ? user.username : '알 수 없음';
                const row = document.createElement('tr');
                let buttonHtml = (purchase.status === '대기 중') ?
                    `<button class="bg-blue-600 text-white px-3 py-1 rounded-lg text-sm" data-purchase-id="${purchase.id}" data-action="approve">승인</button>` :
                    `<span class="text-green-400">승인 완료</span>`;
                buttonHtml += ` <button class="bg-red-600 text-white px-3 py-1 rounded-lg text-sm" data-purchase-id="${purchase.id}" data-action="delete">삭제</button>`;

                row.innerHTML = `
                    <td>${purchase.userId}</td>
                    <td>${username}</td>
                    <td>${purchase.miningType}</td>
                    <td>${purchase.quantity}</td>
                    <td>${purchase.status}</td>
                    <td>${buttonHtml}</td>
                `;
                tableBody.appendChild(row);
            });
            
            document.querySelectorAll('#purchase-table-body button[data-action]').forEach(button => {
                button.addEventListener('click', (e) => {
                    const purchaseId = e.target.dataset.purchaseId;
                    const action = e.target.dataset.action;
                    let purchases = getPurchases();
                    const purchaseIndex = purchases.findIndex(p => p.id === purchaseId);
                    if (purchaseIndex > -1) {
                        if (action === 'approve') {
                            purchases[purchaseIndex].status = '승인 완료';
                            savePurchases(purchases);

                            let miningFarms = getMyMiningFarms();
                            miningFarms.forEach(farm => {
                                if (farm.purchaseId === purchaseId) {
                                    farm.isApproved = true;
                                }
                            });
                            saveMiningFarms(miningFarms);
                            
                            showMessageModal('승인', '구매 신청이 승인되었습니다.');
                        } else if (action === 'delete') {
                            const purchaseToDelete = purchases[purchaseIndex];
                            purchases.splice(purchaseIndex, 1);
                            savePurchases(purchases);

                            // Also delete the associated unapproved farms
                            let miningFarms = getMyMiningFarms();
                            const updatedFarms = miningFarms.filter(farm => farm.purchaseId !== purchaseToDelete.id);
                            saveMiningFarms(updatedFarms);
                            
                            showMessageModal('삭제', '구매 신청이 삭제되었습니다.');
                        }
                    }
                    renderAdminPurchases();
                });
            });
        };
        
        // Render withdrawal requests on admin page
        const renderAdminMiningStatus = () => {
            const users = getUsers();
            const allFarms = getMyMiningFarms();
            const tableBody = document.getElementById('mining-table-body');
            tableBody.innerHTML = '';

            users.forEach(user => {
                if (user.isAdmin) return; // Don't show admin in this list
                const userFarms = allFarms.filter(farm => farm.userId === user.id);
                const totalMined = userFarms.reduce((sum, farm) => sum + farm.minedAmount, 0);
                const farmCount = userFarms.length;

                const row = document.createElement('tr');
                row.innerHTML = `
                    <td>${user.id}</td>
                    <td>${user.username}</td>
                    <td>${farmCount} 개</td>
                    <td>${totalMined.toFixed(6)} USDT</td>
                `;
                tableBody.appendChild(row);
            });
        };

        const renderAdminWithdrawals = () => {
            const requests = getWithdrawalRequests();
            const users = getUsers();
            const tableBody = document.getElementById('withdrawals-table-body');
            tableBody.innerHTML = '';
            requests.forEach(req => {
                const user = users.find(u => u.id === req.userId);
                const username = user ? user.username : '알 수 없음';
                const row = document.createElement('tr');
                let buttonHtml = (req.status === '대기 중') ?
                    `<button class="bg-blue-600 text-white px-3 py-1 rounded-lg text-sm" data-req-id="${req.id}" data-action="approve">승인</button>` :
                    `<span class="text-green-400">승인 완료</span>`;
                
                row.innerHTML = `
                    <td>${req.userId}</td>
                    <td>${username}</td>
                    <td>${req.amount.toFixed(6)} USDT</td>
                    <td>${req.walletAddress}</td>
                    <td>${req.status}</td>
                    <td>${req.requestDate}</td>
                    <td>${buttonHtml}</td>
                `;
                tableBody.appendChild(row);
            });
            
            document.querySelectorAll('#withdrawals-table-body button[data-action]').forEach(button => {
                button.addEventListener('click', (e) => {
                    const reqId = e.target.dataset.reqId;
                    let requests = getWithdrawalRequests();
                    const reqIndex = requests.findIndex(r => r.id === reqId);
                    if (reqIndex > -1) {
                        requests[reqIndex].status = '승인 완료';
                        saveWithdrawalRequests(requests);
                        showMessageModal('승인', '출금 요청이 승인되었습니다.');
                    }
                    renderAdminWithdrawals();
                });
            });
        };

        // Render my mining farms on My Mining Farm page, grouped by type
        const renderMyMiningFarms = () => {
            const container = document.getElementById('my-mining-farms-container');
            container.innerHTML = '';

            if (!isLoggedIn) {
                container.innerHTML = `<p class="text-center text-gray-500">로그인 후 채굴장 현황을 확인하세요.</p>`;
                return;
            }

            const allFarms = getMyMiningFarms();
            const userFarms = allFarms.filter(farm => farm.userId === currentUser.id);

            const grades = ['SILVER MINES', 'GOLD MINES', 'DIAMOND MINES'];
            const gradeDisplayNames = {
                'SILVER MINES': 'SILVER 등급 채굴장',
                'GOLD MINES': 'GOLD 등급 채굴장',
                'DIAMOND MINES': 'DIAMOND 등급 채굴장'
            };

            grades.forEach(grade => {
                const gradeFarms = userFarms.filter(farm => farm.miningType === grade);
                const gradeSection = document.createElement('div');
                gradeSection.classList.add('space-y-4');
                
                const gradeHeaderDiv = document.createElement('div');
                gradeHeaderDiv.innerHTML = `
                    <h3 class="text-2xl font-bold text-yellow-400 border-b border-gray-700 pb-2 mb-4">${gradeDisplayNames[grade]}</h3>
                `;
                gradeSection.appendChild(gradeHeaderDiv);

                const tableContainer = document.createElement('div');
                tableContainer.classList.add('overflow-x-auto');

                const table = document.createElement('table');
                table.classList.add('w-full', 'text-left', 'mining-farm-table');

                const tableHeader = `
                    <thead>
                        <tr class="text-gray-400 uppercase text-sm">
                            <th class="font-normal">채굴장 NO</th>
                            <th class="font-normal">상태</th>
                            <th class="font-normal">총 채굴량 (USDT)</th>
                            <th class="font-normal">채굴 시간</th>
                            <th class="font-normal">시작 시간</th>
                            <th class="font-normal">중지 시간</th>
                            <th class="font-normal">관리</th>
                        </tr>
                    </thead>
                `;

                const tableBody = document.createElement('tbody');
                
                if (gradeFarms.length === 0) {
                    tableBody.innerHTML = `<tr><td colspan="7" class="text-center text-gray-500">보유 중인 채굴기가 없습니다.</td></tr>`;
                } else {
                    gradeFarms.forEach((farm, index) => {
                        let statusText, buttonHtml, miningTime = '0초';
                        
                        const farmNumber = `${grade.split(' ')[0]}-${(index + 1).toString().padStart(2, '0')}`;

                        if (!farm.isApproved) {
                             statusText = `<span class="text-yellow-400">입금대기</span>`;
                             buttonHtml = `<button class="bg-gray-600 text-gray-300 px-3 py-1 rounded-lg text-sm cursor-not-allowed" disabled>입금대기</button>`;
                        } else {
                            statusText = farm.isMining ? `<span class="text-green-400">채굴 중</span>` : `<span class="text-gray-500">중지됨</span>`;
                            if (farm.isMining) {
                                buttonHtml = `<button class="btn-stop bg-red-600 text-white px-3 py-1 rounded-lg text-sm" data-farm-id="${farm.id}">채굴 중지</button>`;
                                miningTime = formatDuration(Date.now() - new Date(farm.startTime).getTime());
                            } else {
                                buttonHtml = `<button class="btn-start bg-green-600 text-white px-3 py-1 rounded-lg text-sm" data-farm-id="${farm.id}">채굴 시작</button>`;
                                if (farm.stopTime && farm.startTime) {
                                     miningTime = formatDuration(new Date(farm.stopTime).getTime() - new Date(farm.startTime).getTime());
                                }
                            }
                        }
                        
                        const row = document.createElement('tr');
                        row.innerHTML = `
                            <td>${farmNumber}</td>
                            <td>${statusText}</td>
                            <td>${farm.minedAmount.toFixed(6)} USDT</td>
                            <td>${miningTime}</td>
                            <td>${farm.startTime ? formatDateTime(farm.startTime) : '미기록'}</td>
                            <td>${farm.stopTime ? formatDateTime(farm.stopTime) : '미기록'}</td>
                            <td>${buttonHtml}</td>
                        `;
                        tableBody.appendChild(row);
                    });
                }
                
                table.innerHTML = tableHeader;
                table.appendChild(tableBody);
                tableContainer.appendChild(table);
                gradeSection.appendChild(tableContainer);
                container.appendChild(gradeSection);
            });
        };

        // Render Coin Wallet page
        const renderCoinWallet = () => {
            const totalMinedElement = document.getElementById('total-mined-usdt');
            if (!isLoggedIn) {
                totalMinedElement.textContent = '로그인 후 확인 가능';
                return;
            }
            const allFarms = getMyMiningFarms();
            const userFarms = allFarms.filter(farm => farm.userId === currentUser.id);
            const totalMined = userFarms.reduce((sum, farm) => sum + farm.minedAmount, 0);
            
            totalMinedElement.textContent = `${totalMined.toFixed(6)} USDT`;
        };

        // Render Withdrawal Request page
        const renderWithdrawalRequest = () => {
            const availableUsdtElement = document.getElementById('available-usdt');
            const historyTableBody = document.getElementById('withdrawal-history-table-body');

            if (!isLoggedIn) {
                availableUsdtElement.textContent = '로그인 후 확인 가능';
                historyTableBody.innerHTML = `<tr><td colspan="3" class="text-center text-gray-500">로그인 후 확인 가능</td></tr>`;
                return;
            }

            // Calculate available USDT
            const allFarms = getMyMiningFarms();
            const userFarms = allFarms.filter(farm => farm.userId === currentUser.id);
            const totalMined = userFarms.reduce((sum, farm) => sum + farm.minedAmount, 0);

            const allRequests = getWithdrawalRequests();
            const userRequests = allRequests.filter(req => req.userId === currentUser.id);
            const totalWithdrawnOrPending = userRequests.reduce((sum, req) => sum + req.amount, 0);

            const availableBalance = totalMined - totalWithdrawnOrPending;
            
            availableUsdtElement.textContent = `${availableBalance.toFixed(6)} USDT`;

            // Update withdrawal history
            userRequests.reverse(); // Show recent first
            historyTableBody.innerHTML = '';
            if (userRequests.length === 0) {
                historyTableBody.innerHTML = `<tr><td colspan="3" class="text-center text-gray-500">출금 요청 내역이 없습니다.</td></tr>`;
            } else {
                userRequests.forEach(req => {
                    const statusClass = req.status === '승인 완료' ? 'text-green-400' : 'text-yellow-400';
                    const row = document.createElement('tr');
                    row.innerHTML = `
                        <td>${req.requestDate}</td>
                        <td>${req.amount.toFixed(6)}</td>
                        <td><span class="${statusClass}">${req.status}</span></td>
                    `;
                    historyTableBody.appendChild(row);
                });
            }
        };
        
        // Handle withdrawal request form submission
        document.getElementById('withdrawal-form').addEventListener('submit', (e) => {
            e.preventDefault();
            const amount = parseFloat(document.getElementById('withdrawal-amount').value);
            const walletAddress = document.getElementById('wallet-address').value;
            
            // Recalculate available balance for validation
            const allFarms = getMyMiningFarms();
            const userFarms = allFarms.filter(farm => farm.userId === currentUser.id);
            const totalMined = userFarms.reduce((sum, farm) => sum + farm.minedAmount, 0);
            const allRequests = getWithdrawalRequests();
            const userRequests = allRequests.filter(req => req.userId === currentUser.id);
            const totalWithdrawnOrPending = userRequests.reduce((sum, req) => sum + req.amount, 0);
            const availableBalance = totalMined - totalWithdrawnOrPending;
            
            if (amount < 35) {
                 showMessageModal('오류', '최소 출금 가능 금액은 35 USDT입니다.');
                 return;
            }

            if (amount > availableBalance) {
                showMessageModal('오류', '사용 가능 금액보다 많은 금액을 출금할 수 없습니다.');
                return;
            }

            const newRequest = {
                id: Date.now().toString(),
                userId: currentUser.id,
                amount,
                walletAddress,
                status: '대기 중',
                requestDate: new Date().toLocaleDateString('ko-KR')
            };

            const requests = getWithdrawalRequests();
            requests.push(newRequest);
            saveWithdrawalRequests(requests);
            
            showMessageModal('출금 요청 완료', '출금 요청이 성공적으로 접수되었습니다.');
            document.getElementById('withdrawal-form').reset();
            renderWithdrawalRequest();
        });

        document.addEventListener('click', (e) => {
            if (e.target.matches('.btn-start, .btn-stop')) {
                const farmId = e.target.dataset.farmId;
                const isStart = e.target.classList.contains('btn-start');
                const allFarms = getMyMiningFarms();
                const farmIndex = allFarms.findIndex(f => f.id === farmId);
                
                if (farmIndex > -1) {
                    const now = new Date().toISOString();
                    allFarms[farmIndex].isMining = isStart;
                    if (isStart) {
                        allFarms[farmIndex].startTime = now;
                        allFarms[farmIndex].stopTime = null;
                        allFarms[farmIndex].lastUpdateTime = now;
                    } else {
                        allFarms[farmIndex].stopTime = now;
                    }
                    saveMiningFarms(allFarms);
                    renderMyMiningFarms();
                }
            }
        });

        document.getElementById('update-mining-rate-btn').addEventListener('click', () => {
            const rates = {
                'SILVER MINES': parseFloat(document.getElementById('silver-rate').value) || 0,
                'GOLD MINES': parseFloat(document.getElementById('gold-rate').value) || 0,
                'DIAMOND MINES': parseFloat(document.getElementById('diamond-rate').value) || 0
            };
            saveMiningRates(rates);

            const message = document.getElementById('mining-rate-message');
            message.textContent = '채굴량이 성공적으로 업데이트되었습니다.';
            message.classList.remove('hidden');
            setTimeout(() => message.classList.add('hidden'), 3000);
        });

        document.getElementById('analyze-market-btn').addEventListener('click', () => {
            const analysisResultDiv = document.getElementById('crypto-analysis-result');
            const analysisText = document.getElementById('analysis-text');
            const loader = document.getElementById('analysis-loader');

            analysisResultDiv.classList.remove('hidden');
            analysisText.textContent = '';
            loader.classList.remove('hidden');

            setTimeout(() => {
                loader.classList.add('hidden');
                analysisText.textContent = "현재 코인 시장은 상승 추세를 보이고 있으며, 주요 코인들이 안정적인 상승세를 유지하고 있습니다. 단기적으로는 가격 변동성이 있을 수 있으나, 장기적인 전망은 긍정적입니다.";
            }, 2000);
        });

        document.getElementById('message-modal-close').addEventListener('click', closeMessageModal);

        document.getElementById('message-modal-confirm-btn').addEventListener('click', closeMessageModal);

        window.addEventListener('keydown', (e) => {
            const messageModal = document.getElementById('message-modal');
            if (messageModal.style.display === 'flex' && e.code === 'Space') {
                e.preventDefault();
                closeMessageModal();
            }
        });

        // --- Customer Service Logic ---
        const renderCustomerServicePage = () => {
            const inquiriesList = document.getElementById('inquiries-list');
            const formContainer = document.getElementById('inquiry-form-container');
            formContainer.classList.add('hidden');
            inquiriesList.innerHTML = '';
            
            if (!isLoggedIn) {
                inquiriesList.innerHTML = `<p class="text-center text-gray-500">로그인 후 문의 내역을 확인하거나 새 문의를 작성할 수 있습니다.</p>`;
                document.getElementById('show-inquiry-form-btn').classList.add('hidden');
                return;
            }
            document.getElementById('show-inquiry-form-btn').classList.remove('hidden');

            const allInquiries = getInquiries();
            const userInquiries = currentUser.isAdmin ? allInquiries : allInquiries.filter(inq => inq.userId === currentUser.id);

            if (userInquiries.length === 0) {
                 inquiriesList.innerHTML = `<p class="text-center text-gray-500">작성한 문의 내역이 없습니다.</p>`;
            }
            
            userInquiries.reverse().forEach(inquiry => { // Show recent first
                const inquiryCard = document.createElement('div');
                inquiryCard.className = 'card rounded-xl';

                const statusColor = inquiry.status === 'open' ? 'text-green-400' : 'text-gray-500';
                const statusText = inquiry.status === 'open' ? '답변 대기중' : '답변 완료';
                
                inquiryCard.innerHTML = `
                    <div class="p-4 border-b border-gray-700 flex justify-between items-center cursor-pointer inquiry-header" data-inquiry-id="${inquiry.id}">
                        <div>
                             <p class="font-bold"><span class="text-sm bg-gray-700 text-yellow-400 px-2 py-1 rounded-full mr-2">${inquiry.category}</span>${inquiry.title}</p>
                            <p class="text-sm text-gray-400 mt-1">작성자: ${inquiry.username} (${inquiry.userId}) | 날짜: ${inquiry.createdAt}</p>
                        </div>
                        <span class="font-bold ${statusColor}">${statusText}</span>
                    </div>
                    <div class="p-4 hidden inquiry-content bg-gray-900/20" data-inquiry-id="${inquiry.id}">
                        <p class="font-bold mb-2">질문 내용:</p>
                        <p class="text-gray-300 whitespace-pre-wrap mb-4">${inquiry.question}</p>
                        <div class="replies-container space-y-4">
                            ${inquiry.replies.map(reply => `
                                <div class="p-3 rounded-lg ${reply.isAdminReply ? 'bg-blue-900/50' : 'bg-gray-700/50'}">
                                    <p class="font-bold text-sm ${reply.isAdminReply ? 'text-blue-300' : 'text-yellow-300'}">${reply.username} (${reply.createdAt})</p>
                                    <p class="text-gray-300 whitespace-pre-wrap mt-1">${reply.text}</p>
                                </div>
                            `).join('')}
                        </div>
                        ${currentUser.isAdmin && inquiry.status === 'open' ? `
                            <form class="admin-reply-form mt-4 space-y-2" data-inquiry-id="${inquiry.id}">
                                <textarea class="form-input" rows="3" placeholder="답변을 입력하세요..." required></textarea>
                                <div class="flex justify-end space-x-2">
                                    <button type="submit" class="bg-blue-600 text-white font-bold py-2 px-4 rounded-lg btn">답변 등록</button>
                                    <button type="button" class="close-inquiry-btn bg-red-600 text-white font-bold py-2 px-4 rounded-lg btn" data-inquiry-id="${inquiry.id}">문의 종결</button>
                                </div>
                            </form>
                        ` : ''}
                    </div>
                `;
                inquiriesList.appendChild(inquiryCard);
            });
        };

        const renderAdminInquiries = (filterCategory = '전체') => {
            const container = document.getElementById('admin-inquiries-list');
            container.innerHTML = '';
            
            const allInquiries = getInquiries();
            const filteredInquiries = filterCategory === '전체'
                ? allInquiries
                : allInquiries.filter(inq => inq.category === filterCategory);

            if (filteredInquiries.length === 0) {
                container.innerHTML = `<p class="text-center text-gray-500">해당 카테고리에 문의 내역이 없습니다.</p>`;
                return;
            }

            filteredInquiries.reverse().forEach(inquiry => {
                const inquiryCard = document.createElement('div');
                inquiryCard.className = 'card rounded-xl mb-4';

                const statusColor = inquiry.status === 'open' ? 'text-green-400' : 'text-gray-500';
                const statusText = inquiry.status === 'open' ? '답변 대기중' : '답변 완료';
                
                inquiryCard.innerHTML = `
                    <div class="p-4 border-b border-gray-700 flex justify-between items-center">
                        <div class="cursor-pointer inquiry-header flex-grow" data-inquiry-id="${inquiry.id}">
                            <p class="font-bold"><span class="text-sm bg-gray-700 text-yellow-400 px-2 py-1 rounded-full mr-2">${inquiry.category}</span>${inquiry.title}</p>
                            <p class="text-sm text-gray-400 mt-1">작성자: ${inquiry.username} (${inquiry.userId}) | 날짜: ${inquiry.createdAt}</p>
                        </div>
                        <div class="flex items-center gap-4 ml-4">
                            <span class="font-bold ${statusColor}">${statusText}</span>
                            <button class="delete-inquiry-btn bg-red-800 text-white px-3 py-1 rounded-lg text-xs hover:bg-red-700 btn" data-inquiry-id="${inquiry.id}">삭제</button>
                        </div>
                    </div>
                    <div class="p-4 hidden inquiry-content bg-gray-900/20" data-inquiry-id="${inquiry.id}">
                        <p class="font-bold mb-2">질문 내용:</p>
                        <p class="text-gray-300 whitespace-pre-wrap mb-4">${inquiry.question}</p>
                        <div class="replies-container space-y-4">
                            ${inquiry.replies.map(reply => `
                                <div class="flex items-start justify-between p-3 rounded-lg ${reply.isAdminReply ? 'bg-blue-900/50' : 'bg-gray-700/50'}">
                                    <div>
                                        <p class="font-bold text-sm ${reply.isAdminReply ? 'text-blue-300' : 'text-yellow-300'}">${reply.username} (${reply.createdAt})</p>
                                        <p class="text-gray-300 whitespace-pre-wrap mt-1">${reply.text}</p>
                                    </div>
                                    <button class="delete-reply-btn text-red-500 hover:text-red-400 font-bold text-lg ml-4 flex-shrink-0" data-inquiry-id="${inquiry.id}" data-reply-created-at="${reply.createdAt}">&times;</button>
                                </div>
                            `).join('')}
                        </div>
                        ${inquiry.status === 'open' ? `
                            <form class="admin-reply-form mt-4 space-y-2" data-inquiry-id="${inquiry.id}">
                                <textarea class="form-input" rows="3" placeholder="답변을 입력하세요..." required></textarea>
                                <div class="flex justify-end space-x-2">
                                    <button type="submit" class="bg-blue-600 text-white font-bold py-2 px-4 rounded-lg btn">답변 등록</button>
                                    <button type="button" class="close-inquiry-btn bg-red-600 text-white font-bold py-2 px-4 rounded-lg btn" data-inquiry-id="${inquiry.id}">문의 종결</button>
                                </div>
                            </form>
                        ` : ''}
                    </div>
                `;
                container.appendChild(inquiryCard);
            });
        };
        
        document.getElementById('admin-inquiry-filters').addEventListener('click', (e) => {
            if (e.target.tagName === 'BUTTON') {
                const category = e.target.dataset.category;
                document.querySelectorAll('#admin-inquiry-filters button').forEach(btn => {
                    btn.classList.replace('bg-blue-600', 'bg-gray-700');
                    btn.classList.replace('text-white', 'text-gray-300');
                });
                e.target.classList.replace('bg-gray-700', 'bg-blue-600');
                e.target.classList.replace('text-gray-300', 'text-white');
                renderAdminInquiries(category);
            }
        });

        // Event delegation for customer service page
        document.getElementById('customerService-page').addEventListener('click', (e) => {
             // Toggle inquiry content visibility
            const header = e.target.closest('.inquiry-header');
            if(header) {
                const inquiryId = header.dataset.inquiryId;
                const content = document.querySelector(`#customerService-page .inquiry-content[data-inquiry-id="${inquiryId}"]`);
                content.classList.toggle('hidden');
            }
        });
        
        // Event delegation for admin page
        document.getElementById('admin-page').addEventListener('click', (e) => {
            const header = e.target.closest('.inquiry-header');
            if(header) {
                const inquiryId = header.dataset.inquiryId;
                const content = document.querySelector(`#admin-page .inquiry-content[data-inquiry-id="${inquiryId}"]`);
                if(content) content.classList.toggle('hidden');
            } else if (e.target.classList.contains('close-inquiry-btn')) {
                const inquiryId = e.target.dataset.inquiryId;
                let inquiries = getInquiries();
                const inquiryIndex = inquiries.findIndex(i => i.id === inquiryId);
                if (inquiryIndex > -1) {
                    inquiries[inquiryIndex].status = 'closed';
                    saveInquiries(inquiries);
                    const activeFilter = document.querySelector('#admin-inquiry-filters .bg-blue-600').dataset.category;
                    renderAdminInquiries(activeFilter);
                }
            } else if (e.target.classList.contains('delete-inquiry-btn')) {
                const inquiryId = e.target.dataset.inquiryId;
                let inquiries = getInquiries();
                const updatedInquiries = inquiries.filter(i => i.id !== inquiryId);
                saveInquiries(updatedInquiries);
                
                const activeFilter = document.querySelector('#admin-inquiry-filters .bg-blue-600').dataset.category;
                renderAdminInquiries(activeFilter);
                showMessageModal('삭제 완료', '문의 내역이 삭제되었습니다.');
            } else if (e.target.classList.contains('delete-reply-btn')) {
                const inquiryId = e.target.dataset.inquiryId;
                const replyCreatedAt = e.target.dataset.replyCreatedAt;
                
                let inquiries = getInquiries();
                const inquiryIndex = inquiries.findIndex(i => i.id === inquiryId);

                if (inquiryIndex > -1) {
                    inquiries[inquiryIndex].replies = inquiries[inquiryIndex].replies.filter(reply => reply.createdAt !== replyCreatedAt);
                    saveInquiries(inquiries);

                    const activeFilter = document.querySelector('#admin-inquiry-filters .bg-blue-600').dataset.category;
                    renderAdminInquiries(activeFilter);
                    showMessageModal('삭제 완료', '문의 답변이 삭제되었습니다.');
                }
            }
        });

        document.getElementById('change-password-btn').addEventListener('click', () => {
            const userId = document.getElementById('password-change-user-id').value;
            const newPassword = document.getElementById('new-password').value;
            const confirmPassword = document.getElementById('confirm-new-password').value;
            const messageEl = document.getElementById('password-change-message');

            if (!newPassword || !confirmPassword) {
                messageEl.textContent = '새 비밀번호를 입력해주세요.';
                messageEl.className = 'text-center text-sm mt-2 text-red-400';
                messageEl.classList.remove('hidden');
                return;
            }

            if (newPassword !== confirmPassword) {
                messageEl.textContent = '비밀번호가 일치하지 않습니다.';
                messageEl.className = 'text-center text-sm mt-2 text-red-400';
                messageEl.classList.remove('hidden');
                return;
            }

            let users = getUsers();
            const userIndex = users.findIndex(u => u.id === userId);

            if (userIndex > -1) {
                users[userIndex].password = newPassword;
                saveUsers(users);

                // Update the password displayed in the modal
                document.getElementById('detail-password').textContent = newPassword;

                // Show success message
                messageEl.textContent = '비밀번호가 성공적으로 변경되었습니다.';
                messageEl.className = 'text-center text-sm mt-2 text-green-400';
                messageEl.classList.remove('hidden');

                // Clear input fields
                document.getElementById('new-password').value = '';
                document.getElementById('confirm-new-password').value = '';

                // Hide message after a few seconds
                setTimeout(() => {
                    messageEl.classList.add('hidden');
                }, 3000);

            } else {
                messageEl.textContent = '사용자를 찾을 수 없습니다.';
                messageEl.className = 'text-center text-sm mt-2 text-red-400';
                messageEl.classList.remove('hidden');
            }
        });

        document.getElementById('admin-page').addEventListener('submit', (e) => {
            if (e.target.classList.contains('admin-reply-form')) {
                e.preventDefault();
                const inquiryId = e.target.dataset.inquiryId;
                const replyText = e.target.querySelector('textarea').value;
                let inquiries = getInquiries();
                const inquiryIndex = inquiries.findIndex(i => i.id === inquiryId);

                if (inquiryIndex > -1) {
                    inquiries[inquiryIndex].replies.push({
                        username: '관리자',
                        isAdminReply: true,
                        text: replyText,
                        createdAt: new Date().toLocaleDateString('ko-KR')
                    });
                    saveInquiries(inquiries);
                    const activeFilter = document.querySelector('#admin-inquiry-filters .bg-blue-600').dataset.category;
                    renderAdminInquiries(activeFilter);
                }
            }
        });


        // Show/hide new inquiry form
        document.getElementById('show-inquiry-form-btn').addEventListener('click', () => {
            document.getElementById('inquiry-form-container').classList.remove('hidden');
        });
        document.getElementById('cancel-inquiry-btn').addEventListener('click', () => {
             document.getElementById('inquiry-form-container').classList.add('hidden');
        });
        
        // Handle new inquiry submission
        document.getElementById('inquiry-form').addEventListener('submit', (e) => {
            e.preventDefault();
            const category = document.getElementById('inquiry-category').value;
            const title = document.getElementById('inquiry-title').value;
            const question = document.getElementById('inquiry-question').value;
            
            const newInquiry = {
                id: Date.now().toString(),
                userId: currentUser.id,
                username: currentUser.username,
                category,
                title,
                question,
                status: 'open',
                createdAt: new Date().toLocaleDateString('ko-KR'),
                replies: []
            };
            
            const inquiries = getInquiries();
            inquiries.push(newInquiry);
            saveInquiries(inquiries);

            showMessageModal('문의 접수', '새로운 문의가 성공적으로 접수되었습니다.');
            document.getElementById('inquiry-form').reset();
            document.getElementById('inquiry-form-container').classList.add('hidden');
            renderCustomerServicePage();
        });


        document.addEventListener('DOMContentLoaded', () => {
            initializeAdminAccount();
            showPage('home');
            updateAuthUI();
            initCryptoPrices();

            // Mobile Menu Logic
            mobileMenuButton.addEventListener('click', () => {
                mobileMenu.classList.remove('hidden');
            });
            closeMobileMenu.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });
    </script>
</body>
</html>


