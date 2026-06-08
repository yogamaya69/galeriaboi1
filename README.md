<html lang="pt-BR" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Galeria Boi | Apresentação</title>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500&family=Playfair+Display:ital,wght@0,400;0,600;1,400&display=swap" rel="stylesheet">
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        serif: ['Playfair Display', 'serif'],
                    },
                    colors: {
                        'gallery-white': '#fcfcfc',
                        'gallery-offwhite': '#f5f5f5',
                        'gallery-black': '#111111',
                        'gallery-gray': '#888888',
                    }
                }
            }
        }
    </script>

    <style>
        /* --- HACKS ANTI-JEKYLL PARA O GITHUB PAGES --- */
        body, html {
            margin: 0 !important;
            padding: 0 !important;
            max-width: 100% !important;
            background-color: #fcfcfc;
            color: #111111;
            overflow-x: hidden;
        }
        .wrapper, .container-lg, main.page-content, .markdown-body, .main-content { 
            max-width: 100% !important; 
            margin: 0 !important; 
            padding: 0 !important; 
            background: transparent !important;
            border: none !important;
        }
        .site-header, .site-footer, header.header, .page-header, body > header { 
            display: none !important; 
        }
        .markdown-body h1:first-child, .markdown-body > h1:first-of-type, #project_title {
            display: none !important;
        }

        /* --- CORREÇÃO DEFINITIVA DA LOGO --- */
        .logo-safe {
            background-color: transparent !important;
            mix-blend-mode: normal !important;
            -webkit-transform: translateZ(0); 
        }
        .logo-white {
            filter: brightness(0) invert(1) !important;
        }
        .logo-original {
            filter: none !important;
        }

        /* --- Custom Scrollbar --- */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #fcfcfc;
        }
        ::-webkit-scrollbar-thumb {
            background: #d1d5db;
            border-radius: 10px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #9ca3af;
        }

        /* --- Animações de entrada --- */
        .reveal-up {
            opacity: 0;
            transform: translateY(40px);
            transition: all 1s cubic-bezier(0.16, 1, 0.3, 1);
        }
        .reveal-up.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* --- Hero Image Parallax Box --- */
        .hero-img-container {
            clip-path: inset(0);
        }
        .hero-img {
            position: absolute;
            top: -10%;
            left: 0;
            width: 100%;
            height: 120%;
            object-fit: cover;
            transform-origin: center;
            will-change: transform;
        }
    </style>
</head>
<body class="antialiased selection:bg-gallery-black selection:text-white">

    <!-- Navegação -->
    <nav id="navbar" class="fixed top-0 w-full z-[99] transition-all duration-300 pointer-events-none">
        <div id="nav-container" class="flex justify-between items-center px-6 py-5 md:px-12 md:py-8 w-full transition-all duration-300 pointer-events-auto">
            
            <!-- Logo blindada -->
            <img id="main-logo" src="./logoboi.svg" alt="Galeria Boi" class="h-12 md:h-20 w-auto object-contain cursor-pointer transition-all duration-300 origin-left logo-safe logo-white" onclick="window.scrollTo(0,0)">
            
            <!-- Desktop Links -->
            <div id="desktop-links" class="hidden md:flex gap-8 text-sm font-sans tracking-widest uppercase text-white transition-colors duration-300">
                <a href="#apresentacao" class="hover:opacity-60 transition-opacity">A Galeria</a>
                <a href="#diretor" class="hover:opacity-60 transition-opacity">O Diretor</a>
                <a href="#contato" class="hover:opacity-60 transition-opacity">Contato</a>
            </div>
            
            <!-- Mobile Menu Button -->
            <div id="mobile-btn" class="md:hidden text-white transition-colors duration-300">
                <button onclick="toggleMobileMenu()" class="uppercase text-xs tracking-widest hover:opacity-70 transition-opacity">Menu</button>
            </div>
        </div>
    </nav>

    <!-- Menu Mobile Overlay -->
    <div id="mobile-menu" class="hidden-menu fixed inset-0 z-[100] bg-gallery-black text-white flex flex-col justify-center items-center opacity-0 invisible transition-all duration-300">
        <button onclick="toggleMobileMenu()" class="absolute top-6 right-6 p-4 uppercase text-xs tracking-widest opacity-70 hover:opacity-100">Fechar</button>
        <div class="flex flex-col gap-10 text-center font-serif text-3xl">
            <a href="#apresentacao" onclick="toggleMobileMenu()" class="hover:text-gallery-gray transition-colors">A Galeria</a>
            <a href="#diretor" onclick="toggleMobileMenu()" class="hover:text-gallery-gray transition-colors">O Diretor</a>
            <a href="#contato" onclick="toggleMobileMenu()" class="hover:text-gallery-gray transition-colors">Contato</a>
        </div>
    </div>

    <!-- Hero Section -->
    <section id="hero" class="w-full min-h-screen flex flex-col lg:flex-row relative bg-gallery-white">
        <!-- Lado do Texto -->
        <div class="w-full lg:w-1/2 flex flex-col justify-center px-8 md:px-16 lg:px-24 pt-32 pb-16 lg:py-0 z-10 min-h-[60vh] lg:min-h-screen">
            <div class="max-w-xl reveal-up active mx-auto lg:mx-0 w-full">
                <p class="text-gallery-gray text-sm md:text-base tracking-[0.2em] uppercase mb-6 font-medium">Sobre Nós</p>
                <h1 class="text-6xl md:text-7xl lg:text-[5.5rem] font-serif leading-none mb-10">NOVA FORNOS</h1>
                <p class="font-sans text-gallery-gray font-light leading-relaxed mb-12 text-base md:text-lg">
                    Um espaço de pesquisa, documentação, fomento e exibição da produção artística contemporânea. Deslize para baixo para conhecer a nossa história e missão.
                </p>
                <a href="#apresentacao" class="inline-flex items-center gap-4 text-sm uppercase tracking-widest font-medium group pb-2 border-b border-gallery-black/20 hover:border-gallery-black transition-colors">
                    Conhecer a Galeria
                    <span class="transform transition-transform group-hover:translate-y-1">↓</span>
                </a>
            </div>
        </div>

        <!-- Lado da Imagem com o ficheiro galeria.jpg -->
        <div class="w-full lg:w-1/2 h-[50vh] lg:h-screen relative overflow-hidden bg-gray-100 hero-img-container">
            <img src="./galeria.jpg" 
                 alt="Interior da Galeria de Arte" 
                 class="hero-img" 
                 id="heroImage">
        </div>
    </section>

    <!-- Seção de Apresentação da Galeria -->
    <section id="apresentacao" class="py-24 md:py-32 bg-gallery-white w-full">
        <div class="max-w-7xl mx-auto px-6 md:px-16 flex flex-col lg:flex-row gap-16 lg:gap-24 items-center">
            
            <div class="w-full lg:w-1/2 reveal-up">
                <div class="aspect-square w-full bg-gray-100 overflow-hidden relative rounded-sm">
                    <!-- Removido o filtro grayscale desta imagem -->
                    <img src="./2galeria.webp" alt="Espaço da Galeria Boi" class="w-full h-full object-cover transition-all duration-700">
                </div>
            </div>

            <div class="w-full lg:w-1/2 reveal-up flex flex-col justify-center">
                <h2 class="text-4xl md:text-5xl font-serif mb-8 text-gallery-black">O Espaço</h2>
                <div class="w-12 h-px bg-gallery-black mb-8"></div>
                <div class="space-y-6 text-gallery-gray font-sans font-light leading-relaxed text-lg">
                    <p>
                        Fundada em 2021 em Caruaru, a Galeria Boi é um espaço de pesquisa, documentação, fomento e exibição da produção artística contemporânea. Propõe estratégias curatoriais colaborativas que fomentem o diálogo entre diferentes gerações e distintas perspectivas culturais. 
                    </p>
                    <p>
                        Mantém como diretriz principal o estímulo às práticas artísticas caracterizadas pelo conceitualismo, pela ênfase nos processos e pela postura crítica, muitas vezes subversiva.
                    </p>
                    <p>
                        A Galeria desenvolve um programa especial de investigação em torno da produção de jovens bem como de renomados artistas, flexionando o anagrama <strong>AGRESTE_RESGATE</strong>, referência à região onde acontece a Bienal do Barro e funciona a sede da Galeria, o Agreste Pernambucano. 
                    </p>
                    <p>
                        Diferencia-se promovendo uma atualização histórica de processos desenvolvidos a partir de forte resistência intelectual e geopolítica, cujo desafio e compromisso é o contra-hegemônico, promovendo a transformação dos agentes do mercado de arte no país, cuja atuação foi exclusivamente no Sudeste ao longo das últimas décadas.
                    </p>
                </div>
            </div>

        </div>
    </section>

    <!-- Seção do Diretor -->
    <section id="diretor" class="py-24 md:py-32 bg-gallery-offwhite w-full">
        <div class="max-w-7xl mx-auto px-6 md:px-16 flex flex-col-reverse lg:flex-row gap-16 lg:gap-24 items-center">
            
            <div class="w-full lg:w-1/2 reveal-up flex flex-col justify-center">
                <p class="text-xs tracking-widest uppercase mb-4 text-gallery-gray font-semibold">Diretor & Idealizador</p>
                <h2 class="text-4xl md:text-5xl font-serif mb-8 text-gallery-black">Carlos Mélo</h2>
                <div class="w-12 h-px bg-gallery-black mb-8"></div>
                <div class="space-y-6 text-gallery-gray font-sans font-light leading-relaxed text-lg">
                    <p>
                        A Galeria Boi é uma extensão visceral da <strong>Primeira Bienal do Barro do Brasil</strong>, concebida e idealizada pelo artista e diretor da galeria, Carlos Mélo.
                    </p>
                    <p>
                        Com uma visão focada na descentralização da arte contemporânea, Carlos busca resgatar a potência do Agreste Pernambucano, transformando-o num polo ativo de reflexão, criação e exibição artística que desafia as narrativas tradicionais do eixo hegemônico.
                    </p>
                </div>
            </div>

            <div class="w-full lg:w-1/2 reveal-up">
                <!-- Mantido o alinhamento perfeito à esquerda com o texto e o filtro grayscale aqui -->
                <div class="aspect-[3/4] w-full max-w-[240px] md:max-w-[280px] lg:ml-auto bg-gray-200 overflow-hidden relative rounded-sm shadow-sm">
                    <img src="./carlos.webp" alt="Retrato de Carlos Mélo" class="w-full h-full object-cover filter grayscale hover:grayscale-0 transition-all duration-700">
                </div>
            </div>

        </div>
    </section>

    <!-- Rodapé PRETO com Contatos Atualizados -->
    <footer id="contato" class="bg-gallery-black text-white py-24 px-8 md:px-16 w-full">
        <div class="max-w-screen-2xl mx-auto grid grid-cols-1 md:grid-cols-4 gap-12 font-sans">
            <div class="md:col-span-2">
                <!-- Logo no Rodapé blindada (logo-safe + logo-white) -->
                <img src="./logoboi.svg" alt="Logo Galeria Boi" class="h-16 md:h-24 w-auto mb-8 object-contain origin-left logo-safe logo-white">
                <p class="text-base text-gray-400 font-light max-w-lg leading-relaxed">
                    Galeria Boi é uma extensão da Primeira Bienal do Barro do Brasil. Um espaço de pesquisa, fomento e exibição da produção artística contemporânea, operando na interseção do conceitualismo, processos críticos e resistência geopolítica.
                </p>
            </div>
            
            <div class="md:col-span-1 flex flex-col items-start text-left w-full">
                <h4 class="uppercase tracking-widest text-xs font-semibold mb-6 text-white w-full">Localização</h4>
                <p class="text-sm text-gray-400 font-light leading-relaxed w-full">
                    Travessa Mestre Vitalino, 9α<br>
                    Alto do Moura, Caruaru - PE<br>
                    CEP: 55000-000<br>
                    Ter - Sáb, 11h às 19h
                </p>
            </div>
            
            <div class="md:col-span-1 flex flex-col items-start text-left w-full">
                <h4 class="uppercase tracking-widest text-xs font-semibold mb-6 text-white w-full">Contato</h4>
                <ul class="text-sm text-gray-400 font-light space-y-3 w-full p-0 m-0">
                    <li><a href="mailto:gaaleriaboi@gmail.com" class="hover:text-white transition-colors">gaaleriaboi@gmail.com</a></li>
                    <li><a href="tel:+5581997186677" class="hover:text-white transition-colors">+55 81 9 9718 6677</a></li>
                    <li><a href="https://www.instagram.com/galeriaboi/" target="_blank" rel="noopener noreferrer" class="hover:text-white transition-colors">@galeriaboi</a></li>
                </ul>
            </div>
        </div>
        <div class="max-w-screen-2xl mx-auto mt-24 pt-8 border-t border-gray-800 text-xs text-gray-500 flex flex-col md:flex-row justify-between items-center gap-4">
            <p>&copy; 2026 Galeria Boi. Todos os direitos reservados.</p>
            <p>Design web otimizado</p>
        </div>
    </footer>

    <!-- JAVASCRIPT SIMPLIFICADO E LIMPO -->
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            
            // --- 1. MENU MOBILE ---
            const mobileMenu = document.getElementById('mobile-menu');
            window.toggleMobileMenu = function() {
                if(mobileMenu.classList.contains('opacity-0')) {
                    mobileMenu.classList.remove('opacity-0', 'invisible');
                    document.body.style.overflow = 'hidden';
                } else {
                    mobileMenu.classList.add('opacity-0', 'invisible');
                    document.body.style.overflow = '';
                }
            }

            // --- 2. OBSERVER PARA ANIMAÇÕES DE ENTRADA ---
            const revealElements = document.querySelectorAll('.reveal-up');
            const revealObserver = new IntersectionObserver((entries, observer) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('active');
                        observer.unobserve(entry.target);
                    }
                });
            }, { root: null, threshold: 0.1, rootMargin: "0px 0px -50px 0px" });

            revealElements.forEach(el => revealObserver.observe(el));

            // --- 3. EFEITO DA NAVBAR E PARALLAX ---
            const heroImage = document.getElementById('heroImage');
            const navbar = document.getElementById('navbar');
            const navContainer = document.getElementById('nav-container');
            const desktopLinks = document.getElementById('desktop-links');
            const mobileBtn = document.getElementById('mobile-btn');
            const mainLogo = document.getElementById('main-logo');
            let ticking = false;

            window.addEventListener('scroll', () => {
                if (!ticking) {
                    window.requestAnimationFrame(() => {
                        const scrollY = window.scrollY;

                        // Efeito Navbar
                        if (scrollY > 50) {
                            navbar.classList.add('bg-white/90', 'backdrop-blur-md', 'border-b', 'border-gray-200', 'shadow-sm');
                            
                            navContainer.classList.remove('py-5', 'md:py-8');
                            navContainer.classList.add('py-3', 'md:py-4');
                            
                            desktopLinks.classList.remove('text-white');
                            desktopLinks.classList.add('text-gallery-black');
                            
                            mobileBtn.classList.remove('text-white');
                            mobileBtn.classList.add('text-gallery-black');

                            // Logo volta para a cor original (preto)
                            mainLogo.classList.remove('logo-white');
                            mainLogo.classList.add('logo-original');
                        } else {
                            navbar.classList.remove('bg-white/90', 'backdrop-blur-md', 'border-b', 'border-gray-200', 'shadow-sm');
                            
                            navContainer.classList.add('py-5', 'md:py-8');
                            navContainer.classList.remove('py-3', 'md:py-4');
                            
                            desktopLinks.classList.add('text-white');
                            desktopLinks.classList.remove('text-gallery-black');
                            
                            mobileBtn.classList.add('text-white');
                            mobileBtn.classList.remove('text-gallery-black');

                            // Logo volta a ficar branca
                            mainLogo.classList.remove('logo-original');
                            mainLogo.classList.add('logo-white');
                        }

                        // Parallax da Hero Image
                        if (scrollY < window.innerHeight) {
                            heroImage.style.transform = `translateY(${scrollY * 0.25}px)`;
                        }
                        ticking = false;
                    });
                    ticking = true;
                }
            });
        });
    </script>
</body>
</html>
