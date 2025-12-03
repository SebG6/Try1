<!DOCTYPE html>
<html lang="fr" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sébastien Gourdin | Shaper Expert & Conducteur d'Engins Polyvalent</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Manrope:wght@300;400;700;800&display=swap" rel="stylesheet">
    
    <script src="https://cdn.tailwindcss.com"></script>

    <script>
        // CONFIGURATION TAILWIND (Couleurs)
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        'body': ['Manrope', 'sans-serif'],
                    },
                    colors: {
                        'light-bg': '#F5F5F5',      
                        'true-white': '#FFFFFF',
                        'dark-text': '#111111',
                        'mid-grey': '#333333',
                        'light-grey-border': '#E0E0E0',
                        'accent-dark': '#000000',
                    }
                }
            }
        }
    </script>
    
    <style>
        /* CSS Custom pour le style "Minimalist Light" */
        body {
            background-color: #F5F5F5;
            color: #111111;
            overflow-x: hidden;
            font-family: 'Manrope', sans-serif;
            letter-spacing: 0.02em; 
        }
        
        /* Images de Carte */
        .color-img-impact {
            filter: brightness(95%); 
            transition: filter 0.6s ease, transform 0.6s ease;
            border-radius: 0.25rem;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1); 
        }
        .image-container:hover .color-img-impact {
            filter: brightness(100%);
            transform: scale(1.02);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
        }

        /* CTA */
        .cta-minimal {
            transition: background-color 0.3s ease, color 0.3s ease;
            border: 1px solid #111111;
            background-color: #111111;
            color: #FFFFFF;
        }
        .cta-minimal:hover {
            background-color: #FFFFFF;
            color: #111111;
            border: 1px solid #111111;
        }
        
        /* Ligne de séparation élégante */
        .tech-line {
            height: 1px;
            background: #E0E0E0;
            width: 100%;
            margin: 3rem 0; 
        }
        
        /* Styles de l'Accordéon */
        .accordion-header {
            cursor: pointer;
            border-top: 1px solid #E0E0E0;
            transition: background-color 0.3s ease;
        }
        /* Style spécifique pour le header de l'accordéon noir */
        .accordion-item.bg-accent-dark .accordion-header {
             border-top: 1px solid #333333;
        }
        .accordion-header:hover {
            background-color: #FAFAFA;
        }
        .accordion-header.active {
            border-bottom: 1px solid #111111;
            background-color: #FFFFFF;
        }
        /* Adaptation active pour l'accordéon noir */
         .accordion-item.bg-accent-dark .accordion-header.active {
            border-bottom: 1px solid #FFFFFF;
            background-color: #000000;
        }
        .accordion-icon {
            transition: transform 0.3s ease;
        }
        .accordion-header.active .accordion-icon {
            transform: rotate(45deg); 
        }
        .accordion-content {
            background-color: #FFFFFF;
            overflow: hidden;
            transition: max-height 0.4s ease-out, opacity 0.4s ease-out;
            max-height: 0;
            opacity: 0;
            padding-top: 0;
            padding-bottom: 0;
            border-left: 5px solid #E0E0E0;
        }
        /* FIX DE BUG: Bordure latérale correcte pour la section Neige */
        .accordion-content#content-snow-eng {
            border-left: 5px solid #FFFFFF; /* Bordure blanche pour le contraste */
        }
        .accordion-content.open {
            opacity: 1;
            padding-top: 1.5rem; 
            padding-bottom: 1.5rem;
        }
        .accordion-content h5 {
            font-weight: 800;
            color: #111111;
            font-size: 1.125rem; 
            margin-top: 1.5rem;
            margin-bottom: 0.75rem;
            padding-bottom: 0.25rem;
            border-bottom: 1px dashed #E0E0E0;
        }


        /* Correction pour la navigation en mode "sticky" */
        .sticky-nav {
            position: sticky;
            top: 0;
            z-index: 50;
        }

        /* ------------------------------------------------------------------ */
        /* --- OPTIMISATIONS MOBILES (media queries) --- */
        /* ------------------------------------------------------------------ */
        @media (max-width: 640px) {
            .hero-title {
                font-size: 2.25rem; 
                line-height: 1.1;
            }
            .hero-subtitle {
                font-size: 1rem;
            }
             .mobile-hero-height { 
                height: 50vh !important; 
            }
            .mobile-image-first {
                order: -1; 
            }
            .accordion-content {
                padding-left: 1rem;
                padding-right: 1rem;
            }
        }

    </style>
</head>
<body class="selection:bg-mid-grey selection:text-true-white">

    <nav class="sticky-nav p-4 flex justify-between items-center bg-true-white/95 backdrop-blur-sm border-b border-light-grey-border">
        <div class="text-xl font-extrabold tracking-widest uppercase text-dark-text">S-PARK</div>
        <div class="flex items-center space-x-4 text-sm">
            <a href="#missions" class="hidden sm:inline-block text-mid-grey hover:text-dark-text transition-colors uppercase font-medium">Offres</a>
            <a href="#projets" class="hidden sm:inline-block text-mid-grey hover:text-dark-text transition-colors uppercase font-medium">Projets</a>
            <a href="#contact" class="px-3 py-1.5 text-true-white uppercase text-xs tracking-widest cta-minimal font-medium">CONTACT</a>
        </div>
    </nav>
    <header class="relative overflow-hidden bg-light-bg mobile-hero-height md:h-[60vh] flex items-center justify-center text-center">
        
        <div class="absolute inset-0 z-0">
            <img src="treuil2 (1).jpg" 
                 alt="Dameuse avec treuil au coucher de soleil sur la montagne" class="w-full h-full object-cover">
            <div class="absolute inset-0 bg-accent-dark/40"></div> 
        </div>

        <div class="relative z-10 px-4 text-true-white max-w-4xl text-center">
            <h1 class="text-5xl sm:text-7xl leading-none font-extrabold uppercase gs-reveal tracking-tight text-true-white mb-4 hero-title">
                Sculpteur de Terrain.<br>
                Expertise Alpine.
            </h1>
            
            <p class="text-lg sm:text-xl mt-2 gs-reveal font-light text-light-grey-border max-w-lg mx-auto hero-subtitle">
                Ingéniosité mécanique et rigueur opérationnelle au service de l'aménagement de montagne, été comme hiver.
            </p>

            <a href="#missions" class="mt-6 inline-block px-6 py-2 text-true-white uppercase text-xs tracking-wider font-medium" 
               style="border: 1px solid #FFFFFF; background-color: rgba(255, 255, 255, 0.1); backdrop-filter: blur(5px);">
                DÉCOUVRIR LES EXPERTISES
            </a>
        </div>
    </header>
    <section id="engagement" class="py-12 px-4 md:px-16 bg-true-white border-b border-light-grey-border">
        <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-6 items-center">
            
            <h2 class="text-2xl font-extrabold uppercase text-dark-text gs-reveal leading-snug">
                L'Expertise d'un **Rider-Shaper** aux commandes.
            </h2>
            
            <p class="text-base font-light text-mid-grey gs-reveal md:col-span-2">
                Mon profil unique combine la vision d'utilisateur pour des installations fluides, sécurisées et innovantes avec la rigueur technique et logistique nécessaire aux chantiers de Génie Civil les plus exigeants.
            </p>
            
        </div>
    </section>
    
    <section id="missions" class="py-16 px-4 md:px-16 bg-light-bg">
        <div class="max-w-7xl mx-auto">
            
            <h3 class="text-2xl font-extrabold uppercase text-dark-text gs-reveal mb-8 text-center tracking-widest">NOS DOMAINES D'INTERVENTION</h3>
            
            <div class="border-b border-E0E0E0">
                
                <div class="accordion-item">
                    <div class="accordion-header p-4 sm:p-6 flex justify-between items-center gs-reveal" onclick="toggleAccordion('content-1')">
                        <h4 class="text-lg sm:text-xl md:text-2xl font-extrabold uppercase text-dark-text">
                            ZONES LUDIQUES & FREESTYLE
                        </h4>
                        <span class="text-dark-text text-2xl accordion-icon">+</span>
                    </div>
                    <div id="content-1" class="accordion-content p-4 sm:p-8">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 sm:gap-8 items-start">
                            <div>
                                <p class="text-base font-light text-mid-grey mb-4">
                                    Conception, construction et exploitation de Snowparks, Skateparks ou Bike Parks. Un projet **Clé en main** du concept initial à la viabilité saisonnière.
                                </p>
                                <ul class="list-none space-y-3 pl-0 border-l-4 border-accent-dark pl-4 mt-4">
                                    <li class="text-sm text-dark-text font-semibold">Phase A : Expertise & Ingénierie</li>
                                    <li class="text-sm text-dark-text font-semibold">Phase B : Fabrication (Shaping, Terrassement spécifique, Modules)</li>
                                    <li class="text-sm text-dark-text font-semibold">Phase C : Exploitation & Maintenance (Équipes de Shapers, Suivi)</li>
                                </ul>
                            </div>
                            <div class="h-48 relative overflow-hidden image-container rounded-md mobile-image-first md:order-last">
                                <img src="snowpark1 (1).jpg" class="w-full h-full object-cover color-img-impact" alt="Vue large d'un snowpark avec télésièges">
                            </div>
                        </div>
                    </div>
                </div>

                <div class="accordion-item">
                    <div class="accordion-header p-4 sm:p-6 flex justify-between items-center gs-reveal" onclick="toggleAccordion('content-2')">
                        <h4 class="text-lg sm:text-xl md:text-2xl font-extrabold uppercase text-dark-text">
                            TERRASSEMENT & VRD
                        </h4>
                        <span class="text-dark-text text-2xl accordion-icon">+</span>
                    </div>
                    <div id="content-2" class="accordion-content p-4 sm:p-8">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 sm:gap-8 items-start">
                             <div class="h-48 relative overflow-hidden image-container rounded-md mobile-image-first md:order-first">
                                 <img src="IMG20220919172627 (1).jpg" class="w-full h-full object-cover color-img-impact" alt="Excavatrice en pleine construction de terrassement">
                            </div>
                            <div>
                                <p class="text-base font-light text-mid-grey mb-4">
                                    Nivellement et aménagement de terrains pour tous types de projets. De la maison individuelle aux infrastructures sportives complexes.
                                </p>
                                <ul class="list-none space-y-3 pl-0 border-l-4 border-accent-dark pl-4 mt-4">
                                    <li class="text-sm text-dark-text font-semibold">Phase A : Analyse Topographique & Étude des Sols</li>
                                    <li class="text-sm text-dark-text font-semibold">Phase B : Travaux de Terrassement (Décapage, Remblai, Compactage)</li>
                                    <li class="text-sm text-dark-text font-semibold">Phase C : Aménagements VRD (Réseaux, Assainissement, Finitions)</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="accordion-item">
                    <div class="accordion-header p-4 sm:p-6 flex justify-between items-center gs-reveal" onclick="toggleAccordion('content-4')">
                        <h4 class="text-lg sm:text-xl md:text-2xl font-extrabold uppercase text-dark-text">
                            GESTION ÉVÉNEMENTIELLE
                        </h4>
                        <span class="text-dark-text text-2xl accordion-icon">+</span>
                    </div>
                    <div id="content-4" class="accordion-content p-4 sm:p-8">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 sm:gap-8 items-start">
                            <div>
                                <p class="text-base font-light text-mid-grey mb-4">
                                    Organisation clé en main de manifestations sportives : SuperPark, compétitions, festivals. Notre équipe dédiée garantit logistique, sécurité et succès.
                                </p>
                                <ul class="list-none space-y-3 pl-0 border-l-4 border-accent-dark pl-4 mt-4">
                                    <li class="text-sm text-dark-text font-semibold">Concept & Design du Parcours Événementiel</li>
                                    <li class="text-sm text-dark-text font-semibold">Gestion Logistique, Sécurité et Encadrement</li>
                                    <li class="text-sm text-dark-text font-semibold">Mise en place de la Communication et des Partenariats</li>
                                </ul>
                            </div>
                            <div class="h-48 relative overflow-hidden image-container rounded-md mobile-image-first md:order-last">
                                <img src="modulepark1 (1).jpg" class="w-full h-full object-cover color-img-impact" alt="Shaping d'un module de park de nuit">
                            </div>
                        </div>
                    </div>
                </div>

                <div class="accordion-item">
                    <div class="accordion-header p-4 sm:p-6 flex justify-between items-center gs-reveal" onclick="toggleAccordion('content-5')">
                        <h4 class="text-lg sm:text-xl md:text-2xl font-extrabold uppercase text-dark-text">
                            PRODUCTION & MEDIA
                        </h4>
                        <span class="text-dark-text text-2xl accordion-icon">+</span>
                    </div>
                    <div id="content-5" class="accordion-content p-4 sm:p-8">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 sm:gap-8 items-start">
                            <div class="h-48 relative overflow-hidden image-container rounded-md mobile-image-first md:order-first">
                                <img src="snowbucket1 (1).jpg" class="w-full h-full object-cover color-img-impact" alt="Dameuse avec godet à neige à l'aube">
                            </div>
                            <div>
                                <p class="text-base font-light text-mid-grey mb-4">
                                    Création de spots de ride éphémères optimisés pour la captation vidéo/photo. Collaboration avec notre réseau d'experts du secteur.
                                </p>
                                <ul class="list-none space-y-3 pl-0 border-l-4 border-accent-dark pl-4 mt-4">
                                    <li class="text-sm text-dark-text font-semibold">Conception de Spots sur Mesure (neige ou terre)</li>
                                    <li class="text-sm text-dark-text font-semibold">Mise en Relation avec les Professionnels de l'Audiovisuel</li>
                                    <li class="text-sm text-dark-text font-semibold">Gestion du Site de Tournage et Logistique associée</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="accordion-item bg-accent-dark text-true-white">
                    <div class="accordion-header p-4 sm:p-6 flex justify-between items-center gs-reveal bg-accent-dark hover:bg-mid-grey" onclick="toggleAccordion('content-snow-eng')">
                        <h4 class="text-lg sm:text-xl md:text-2xl font-extrabold uppercase text-true-white">
                            INGÉNIERIE DE LA RESSOURCE NEIGE ❄️
                        </h4>
                        <span class="text-true-white text-2xl accordion-icon">+</span>
                    </div>
                    <div id="content-snow-eng" class="accordion-content p-4 sm:p-8 bg-true-white text-dark-text">
                        
                        <p class="text-base font-light text-mid-grey mb-6">
                            La maîtrise de la neige est essentielle pour la viabilité des installations. Notre expertise va de la production optimisée à l'aménagement technique du terrain pour garantir une saison réussie.
                        </p>

                        <div class="gs-reveal">
                            <h5>Engins de Damage : Puissance et Précision</h5>
                            <p class="text-base font-light text-mid-grey mb-4">Un **conducteur d'expérience** est requis. Construire des kickers ou des virages relevés n'est pas seulement une histoire de tas de neige, il faut avoir la vision d'ensemble afin de pouvoir optimiser le temps de travail et donc le temps de machine.</p>
                            <ul class="list-disc list-inside text-sm text-mid-grey space-y-1 pl-2">
                                <li>L'utilisation d'une machine spécialisée permet de sculpter la neige de manière plus efficace.</li>
                                <li>La dameuse équipée d'un **treuil** est un atout pour déplacer plus de neige et damer des réceptions supérieures à $35^\circ$.</li>
                            </ul>
                        </div>

                        <div class="gs-reveal">
                            <h5>Carrière à Neige : Piège à Flocons</h5>
                            <p class="text-base font-light text-mid-grey mb-4">Le principe consiste à définir une zone (si possible au-dessus du snowpark et exposée au vent dominant) où l'on va créer des lignes de neige pour **piéger la neige** pendant les tempêtes.</p>
                            <p class="text-sm font-semibold text-dark-text mt-3">⚠️ Précaution : Il est impératif de **compacter** au préalable toute la zone de la carrière afin d'avoir un fond sûr sur lequel la machine pourra travailler sans risque.</p>
                        </div>
                        
                        <div class="gs-reveal">
                            <h5>Canon à Neige : Stratégie de Production</h5>
                            <p class="text-base font-light text-mid-grey mb-4">L'implantation des canons à neige nécessite une étude rigoureuse de l'environnement (température, humidité, vent) pour maximiser le rendement.</p>
                            <ul class="list-disc list-inside text-sm text-mid-grey space-y-1 
