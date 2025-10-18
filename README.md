[index.html](https://github.com/user-attachments/files/22981883/index.html)<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rodízios - Restaurante Japonês</title>
    <style>
        body {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #1a1a1a 0%, #2d1810 100%);
            color: #ffffff;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            text-align: center;
            padding: 60px 0;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><rect fill="%23d4af37" width="100" height="100" opacity="0.1"/></svg>');
        }

        .logo {
            font-size: 3.5rem;
            font-weight: 300;
            color: #d4af37;
            margin-bottom: 10px;
            text-shadow: 
                0 0 10px rgba(212, 175, 55, 0.8),
                0 0 20px rgba(212, 175, 55, 0.6),
                0 0 30px rgba(212, 175, 55, 0.4),
                2px 2px 8px rgba(0,0,0,0.8);
            letter-spacing: 8px;
            font-family: 'Georgia', 'Times New Roman', serif;
            position: relative;
            background: linear-gradient(45deg, #d4af37, #f4e4a6, #d4af37, #b8941f);
            background-size: 300% 300%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: shimmer 3s ease-in-out infinite;
        }

        @keyframes shimmer {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }

        .logo::before {
            content: '';
            position: absolute;
            top: -10px;
            left: -20px;
            right: -20px;
            bottom: -10px;
            background: linear-gradient(45deg, transparent, rgba(212, 175, 55, 0.1), transparent);
            border-radius: 15px;
            z-index: -1;
        }

        .subtitle {
            font-size: 1.2rem;
            color: #cccccc;
            margin-bottom: 40px;
        }

        .rodizios-section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            color: #d4af37;
            margin-bottom: 60px;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: #d4af37;
        }

        .rodizios-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
            gap: 40px;
            margin-top: 60px;
        }

        .rodizio-card {
            background: linear-gradient(145deg, #2a2a2a, #1f1f1f);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
            border: 2px solid #d4af37;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .rodizio-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(90deg, #d4af37, #f4e4a6, #d4af37);
        }

        .rodizio-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 30px 60px rgba(212, 175, 55, 0.2);
        }

        .rodizio-type {
            font-size: 2rem;
            font-weight: bold;
            color: #d4af37;
            margin-bottom: 20px;
            text-align: center;
        }

        .price {
            font-size: 2.5rem;
            font-weight: bold;
            color: #ffffff;
            text-align: center;
            margin-bottom: 30px;
        }

        .price-period {
            font-size: 1rem;
            color: #cccccc;
            font-weight: normal;
        }

        .sushibar-subtitle {
            text-align: left;
            font-size: 1.3rem;
            color: #888888;
            margin-bottom: 20px;
            font-weight: 700;
            margin-left: 20px;
            text-transform: uppercase;
            letter-spacing: 2px;
            text-shadow: none;
            border: 2px solid #d4af37;
            border-radius: 25px;
            padding: 8px 16px;
            display: inline-block;
        }

        .features-list {
            list-style: none;
            padding: 0;
            margin: 30px 0;
        }

        .features-list li {
            padding: 12px 0;
            border-bottom: 1px solid #333;
            position: relative;
            padding-left: 30px;
        }

        .features-list li::before {
            content: '—';
            color: #d4af37;
            font-weight: bold;
            position: absolute;
            left: 0;
            top: 12px;
        }

        .features-list li:last-child {
            border-bottom: none;
        }

        .cta-button {
            background: linear-gradient(45deg, #d4af37, #f4e4a6);
            color: #1a1a1a;
            border: none;
            padding: 15px 30px;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            width: 100%;
            margin-top: 30px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .cta-button:hover {
            background: linear-gradient(45deg, #f4e4a6, #d4af37);
            transform: scale(1.05);
            box-shadow: 0 10px 20px rgba(212, 175, 55, 0.3);
        }

        .info-section {
            background: rgba(42, 42, 42, 0.8);
            padding: 60px 0;
            margin-top: 80px;
            text-align: center;
        }

        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmin(250px, 1fr));
            gap: 40px;
            margin-top: 40px;
        }

        .info-item {
            padding: 30px;
            background: rgba(212, 175, 55, 0.1);
            border-radius: 15px;
            border: 1px solid rgba(212, 175, 55, 0.3);
        }

        .info-icon {
            font-size: 3rem;
            margin-bottom: 20px;
        }

        .info-title {
            font-size: 1.3rem;
            font-weight: bold;
            color: #d4af37;
            margin-bottom: 15px;
        }

        footer {
            background: #1a1a1a;
            padding: 40px 0;
            text-align: center;
            border-top: 2px solid #d4af37;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 40px;
            flex-wrap: wrap;
            margin-bottom: 20px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
            color: #cccccc;
        }



        @media (max-width: 768px) {
            .rodizios-grid {
                grid-template-columns: 1fr;
            }
            
            .logo {
                font-size: 2rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .rodizio-card {
                padding: 30px 20px;
            }
            
            .contact-info {
                flex-direction: column;
                gap: 20px;
            }


        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="logo">O CHEF SUSHI</div>
            <div class="subtitle">Tradição, Elegância e Sabor Inigualável</div>
        </div>
    </header>

    <main>
        <section class="rodizios-section">
            <div class="container">
                <h1 class="section-title">Nossos Rodízios</h1>
                
                <div class="rodizios-grid">
                    <!-- Rodízio Tradicional -->
                    <div class="rodizio-card">
                        <h2 class="rodizio-type">Rodízio Tradicional</h2>
                        <div class="price">
                            R$ 120,00
                            <span class="price-period">por pessoa</span>
                        </div>
                        
                        <div class="sushibar-subtitle">Sushibar</div>
                        
                        <ul class="features-list">
                            <li>Sashimis (atum, salmão e peixe branco)</li>
                            <li>Sushis especiais da casa (joy, niguiri, uramaki, triplex, hossomaki etc.)</li>
                            <li>Temakis (salmão, atum, peixe branco, california, skin e salmão grelhado)</li>
                            <li>Ceviche, carpaccio, camarão empanado na laranja, hot roll</li>
                        </ul>
                        
                        <div class="sushibar-subtitle">Cozinha</div>
                        
                        <ul class="features-list">
                            <li>Shimeji negro, sunomono, gohan, robata grelhada, missoshiro</li>
                            <li>Guioza (bovina, suína e vegetariana)</li>
                            <li>Harumaki (queijo e legumes)</li>
                            <li>Tempura (salmão e legumes)</li>
                        </ul>
                        
                        <div class="sushibar-subtitle">Sobremesa</div>
                        
                        <ul class="features-list">
                            <li>Banana flambada com sorvete de creme</li>
                            <li>Abacaxi flambado com sorvete de creme</li>
                            <li>Harumaki (chocolate e doce de leite)</li>
                        </ul>
                    </div>

                    <!-- Rodízio Premium -->
                    <div class="rodizio-card">
                        <h2 class="rodizio-type">Rodízio Premium</h2>
                        <div class="price">
                            R$ 160,00
                            <span class="price-period">por pessoa</span>
                        </div>
                        
                        <div class="sushibar-subtitle">Sushibar</div>
                        
                        <ul class="features-list">
                            <li>Sashimis (salmão, atum, peixe branco e polvo)</li>
                            <li>Iguarias (unagui, foie gras, vieira, niguiri de camarão, uramaki de camarão com abacate, joy viagra, niguiri de polvo)</li>
                            <li>Temakis (temaki fabi, temaki fabi crisp, temaki ebitem, temaki spice tuna, temaki shimeji)</li>
                            <li>Ceviche com camarão e polvo, carpaccio, camarão empanado na laranja, hot roll</li>
                        </ul>
                        
                        <div class="sushibar-subtitle">Cozinha</div>
                        
                        <ul class="features-list">
                            <li>Shimeji com camarão, shitake, robata de salmão grelhada</li>
                            <li>Sunomono, gohan, missoshiro, edamame</li>
                            <li>Guioza (bovina, suína e vegetariana)</li>
                            <li>Harumaki (queijo e legumes)</li>
                            <li>Tempura (salmão, legumes, camarão, misto)</li>
                            <li>Yakisoba (carne, frango e vegetariano)</li>
                        </ul>
                        
                        <div class="sushibar-subtitle">Sobremesa</div>
                        
                        <ul class="features-list">
                            <li>Petit gateau com sorvete de creme</li>
                            <li>Banana flambada com sorvete de creme</li>
                            <li>Abacaxi flambado com sorvete de creme</li>
                            <li>Harumaki (chocolate e doce de leite)</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <section class="info-section">
            <div class="container">
                <h2 class="section-title">Por que escolher nossos rodízios?</h2>
                
                <div class="info-grid">
                    <div class="info-item">
                        <div class="info-icon">🐟</div>
                        <div class="info-title">Peixes Frescos</div>
                        <p>Selecionamos diariamente os melhores peixes e frutos do mar para garantir máxima qualidade e sabor.</p>
                    </div>
                    
                    <div class="info-item">
                        <div class="info-icon">👨‍🍳</div>
                        <div class="info-title">Chefs Especializados</div>
                        <p>Nossa equipe possui anos de experiência na culinária japonesa tradicional e contemporânea.</p>
                    </div>
                    

                    
                    <div class="info-item">
                        <div class="info-icon">⏰</div>
                        <div class="info-title">Sem Pressa</div>
                        <p>Aproveite seu rodízio sem limite de tempo. Queremos que você tenha a melhor experiência possível.</p>
                    </div>
                </div>
            </div>
        </section>


    </main>

    <footer>
        <div class="container">
            <div class="contact-info">
                <div class="contact-item">
                    <span>📍</span>
                    <span>Estrada das Lágrimas, 1744</span>
                </div>
                <div class="contact-item">
                    <span>📞</span>
                    <span>(11) 94909-7290</span>
                </div>
                <div class="contact-item">
                    <span>🕒</span>
                    <span>Seg-Dom: 12h às 22h30</span>
                </div>
            </div>
            <p>&copy; 2024 O Chef Sushi. Todos os direitos reservados.</p>
        </div>
    </footer>

    <script>
        function reservarMesa(tipoRodizio) {
            const mensagem = tipoRodizio === 'tradicional' 
                ? 'Gostaria de reservar uma mesa para o Rodízio Tradicional (R$ 120,00)' 
                : 'Gostaria de reservar uma mesa para o Rodízio Premium (R$ 160,00)';
            
            const telefone = '5511949097290';
            const url = https://wa.me/${telefone}?text=${encodeURIComponent(mensagem)};
            
            window.open(url, '_blank', 'noopener,noreferrer');
        }



        // Animação suave ao rolar a página
        window.addEventListener('scroll', () => {
            const cards = document.querySelectorAll('.rodizio-card');
            cards.forEach(card => {
                const rect = card.getBoundingClientRect();
                const isVisible = rect.top < window.innerHeight && rect.bottom > 0;
                
                if (isVisible) {
                    card.style.opacity = '1';
                    card.style.transform = 'translateY(0)';
                }
            });
        });

        // Inicializar animações
        document.addEventListener('DOMContentLoaded', () => {
            const cards = document.querySelectorAll('.rodizio-card');
            cards.forEach((card, index) => {
                card.style.opacity = '0';
                card.style.transform = 'translateY(50px)';
                card.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
                
                setTimeout(() => {
                    card.style.opacity = '1';
                    card.style.transform = 'translateY(0)';
                }, index * 200);
            });
        });
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'98fb6ed511c000e0',t:'MTc2MDY1ODM1OC4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>in
