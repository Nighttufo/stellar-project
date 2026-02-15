<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stellar Project | Mapas Mentais</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Ícones Lucide -->
    <script src="https://unpkg.com/lucide@latest"></script>

    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;600;700&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">

    <style>
        :root {
            --space-dark: #050505;
            --nebula-purple: #6d28d9;
            --nebula-blue: #1e40af;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--space-dark);
            color: #e2e8f0;
            overflow-x: hidden;
        }

        h1, h2, h3, .font-space {
            font-family: 'Space Grotesk', sans-serif;
        }

        /* Animação de Fundo de Estrelas */
        #stars-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            background: radial-gradient(circle at center, #111 0%, #050505 100%);
        }

        .star {
            position: absolute;
            background: white;
            border-radius: 50%;
            opacity: 0.5;
            animation: twinkle var(--duration) infinite ease-in-out;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0.3; transform: scale(1); }
            50% { opacity: 1; transform: scale(1.2); }
        }

        /* Efeito de Nebulosa */
        .nebula {
            position: fixed;
            width: 600px;
            height: 600px;
            border-radius: 50%;
            filter: blur(120px);
            z-index: 1;
            opacity: 0.15;
            pointer-events: none;
        }

        /* Botão Estelar Animado */
        .btn-stellar {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .btn-stellar:hover {
            background: rgba(255, 255, 255, 0.1);
            border-color: #818cf8;
            transform: translateY(-5px) scale(1.02);
            box-shadow: 0 0 20px rgba(99, 102, 241, 0.4);
        }

        .glass-card {
            background: rgba(15, 15, 25, 0.7);
            backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }
    </style>
</head>
<body class="antialiased flex flex-col min-h-screen">

    <!-- Fundo Animado -->
    <div id="stars-container"></div>
    <div class="nebula bg-purple-600 top-[-10%] left-[-10%]"></div>
    <div class="nebula bg-blue-600 bottom-[-10%] right-[-10%]"></div>

    <!-- Hero Section -->
    <header class="relative z-10 pt-20 pb-16 px-6 text-center">
        <div class="container mx-auto">
            <div class="inline-block px-4 py-1.5 mb-6 border border-indigo-500/30 rounded-full bg-indigo-500/10 backdrop-blur-md">
                <span class="text-xs font-bold tracking-[0.2em] text-indigo-300 uppercase">Stellar Project</span>
            </div>
            
            <h1 class="text-5xl md:text-7xl font-bold mb-6 bg-clip-text text-transparent bg-gradient-to-b from-white to-gray-500">
                Mapeie seu Universo <br> de Ideias
            </h1>
            
            <p class="text-lg md:text-xl text-gray-400 max-w-2xl mx-auto leading-relaxed">
                Transforme pensamentos complexos em galáxias visuais. A ferramenta definitiva da <strong>Stellar Project</strong> para criar mapas mentais intuitivos e expansivos.
            </p>
        </div>
    </header>

    <!-- Seção de Ação -->
    <main class="relative z-10 container mx-auto px-6 pb-24">
        
        <!-- Grid de Botões Principais -->
        <div class="grid md:grid-cols-2 gap-8 max-w-4xl mx-auto mb-20">
            
            <!-- Link Desktop -->
            <a href="https://nighttufo.github.io/estelar/" target="_blank" class="btn-stellar glass-card rounded-2xl p-8 flex flex-col items-center text-center">
                <div class="w-16 h-16 bg-indigo-500/20 rounded-full flex items-center justify-center mb-6">
                    <i data-lucide="monitor" class="w-8 h-8 text-indigo-400"></i>
                </div>
                <h3 class="text-2xl font-bold mb-3">Versão Desktop</h3>
                <p class="text-gray-400 mb-6">A experiência completa de mapeamento para o seu navegador no PC.</p>
                <span class="mt-auto inline-flex items-center text-indigo-400 font-semibold group">
                    Explorar no PC <i data-lucide="external-link" class="ml-2 w-4 h-4"></i>
                </span>
            </a>

            <!-- Link Mobile -->
            <a href="https://nighttufo.github.io/estelar-mobile/" target="_blank" class="btn-stellar glass-card rounded-2xl p-8 flex flex-col items-center text-center">
                <div class="w-16 h-16 bg-purple-500/20 rounded-full flex items-center justify-center mb-6">
                    <i data-lucide="smartphone" class="w-8 h-8 text-purple-400"></i>
                </div>
                <h3 class="text-2xl font-bold mb-3">Versão Mobile</h3>
                <p class="text-gray-400 mb-6">Leve suas ideias no bolso com a interface otimizada para smartphones.</p>
                <span class="mt-auto inline-flex items-center text-purple-400 font-semibold group">
                    Abrir no Celular <i data-lucide="external-link" class="ml-2 w-4 h-4"></i>
                </span>
            </a>

        </div>

        <!-- Card de Propósito -->
        <div class="glass-card rounded-3xl p-10 max-w-4xl mx-auto">
            <div class="flex flex-col md:flex-row gap-10 items-center">
                <div class="w-full md:w-1/2">
                    <h2 class="text-3xl font-bold mb-6 text-white">Nossa Visão</h2>
                    <p class="text-gray-400 mb-4 leading-relaxed">
                        A **Stellar Project** nasceu da necessidade de organizar o caos criativo. Acreditamos que cada ideia é uma estrela que, quando conectada, forma uma constelação de conhecimento.
                    </p>
                    <p class="text-gray-400 leading-relaxed">
                        Nossa ferramenta de mapas mentais foi desenhada para ser fluida, rápida e visualmente gratificante, permitindo que você navegue pelo seu cérebro como se estivesse explorando o espaço.
                    </p>
                </div>
                <div class="w-full md:w-1/2 grid grid-cols-2 gap-4">
                    <div class="p-4 bg-white/5 rounded-xl border border-white/10">
                        <i data-lucide="brain-circuit" class="w-6 h-6 text-indigo-400 mb-2"></i>
                        <h4 class="font-bold text-sm">Intuitivo</h4>
                    </div>
                    <div class="p-4 bg-white/5 rounded-xl border border-white/10">
                        <i data-lucide="rocket" class="w-6 h-6 text-orange-400 mb-2"></i>
                        <h4 class="font-bold text-sm">Rápido</h4>
                    </div>
                    <div class="p-4 bg-white/5 rounded-xl border border-white/10">
                        <i data-lucide="cloud" class="w-6 h-6 text-blue-400 mb-2"></i>
                        <h4 class="font-bold text-sm">Cloud Ready</h4>
                    </div>
                    <div class="p-4 bg-white/5 rounded-xl border border-white/10">
                        <i data-lucide="share-2" class="w-6 h-6 text-green-400 mb-2"></i>
                        <h4 class="font-bold text-sm">Colaborativo</h4>
                    </div>
                </div>
            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer class="relative z-10 border-t border-white/5 mt-auto py-12">
        <div class="container mx-auto px-6 text-center">
            <h2 class="font-space text-2xl font-bold tracking-tighter mb-4">STELLAR PROJECT</h2>
            <p class="text-gray-500 text-sm mb-6">Inovação em mapeamento mental.</p>
            <div class="flex justify-center space-x-8">
                <!-- GitHub Link -->
                <a href="https://github.com/Nighttufo" target="_blank" class="text-gray-400 hover:text-white transition-colors flex flex-col items-center">
                    <i data-lucide="github" class="w-6 h-6 mb-1"></i>
                    <span class="text-[10px] uppercase tracking-widest">GitHub</span>
                </a>
                <!-- TikTok Link -->
                <a href="https://tiktok.com/@stellarproject.com" target="_blank" class="text-gray-400 hover:text-white transition-colors flex flex-col items-center">
                    <!-- Custom SVG para TikTok já que Lucide às vezes não tem nativo -->
                    <svg class="w-6 h-6 mb-1 fill-current" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path d="M12.525.02c1.31-.02 2.61-.01 3.91-.02.08 1.53.63 3.09 1.75 4.17 1.12 1.11 2.7 1.62 4.24 1.79v4.03c-1.44-.17-2.89-.6-4.13-1.47V15.5c0 1.93-.75 3.81-2.11 5.17-1.36 1.36-3.24 2.11-5.17 2.11-1.93 0-3.81-.75-5.17-2.11-1.36-1.36-2.11-3.24-2.11-5.17 0-1.93.75-3.81 2.11-5.17 1.36-1.36 3.24-2.11 5.17-2.11.37 0 .73.03 1.09.09V12.4c-.36-.05-.72-.07-1.09-.07-1.18 0-2.31.47-3.14 1.31-.84.83-1.31 1.96-1.31 3.14 0 1.18.47 2.31 1.31 3.14.83.84 1.96 1.31 3.14 1.31 1.18 0 2.31-.47 3.14-1.31.84-.83 1.31-1.96 1.31-3.14V.02z"/>
                    </svg>
                    <span class="text-[10px] uppercase tracking-widest">TikTok</span>
                </a>
            </div>
        </div>
    </footer>

    <script>
        // Inicializar ícones
        lucide.createIcons();

        // Gerar estrelas dinamicamente
        const container = document.getElementById('stars-container');
        const starCount = 150;

        for (let i = 0; i < starCount; i++) {
            const star = document.createElement('div');
            star.className = 'star';
            
            // Posição aleatória
            const x = Math.random() * 100;
            const y = Math.random() * 100;
            
            // Tamanho aleatório
            const size = Math.random() * 3;
            
            // Duração da animação aleatória
            const duration = 2 + Math.random() * 4;
            
            star.style.left = `${x}%`;
            star.style.top = `${y}%`;
            star.style.width = `${size}px`;
            star.style.height = `${size}px`;
            star.style.setProperty('--duration', `${duration}s`);
            
            container.appendChild(star);
        }

        // Efeito parallax leve no mouse
        document.addEventListener('mousemove', (e) => {
            const mouseX = e.clientX / window.innerWidth;
            const mouseY = e.clientY / window.innerHeight;
            
            container.style.transform = `translate(${mouseX * 20}px, ${mouseY * 20}px)`;
        });
    </script>
</body>
</html>
