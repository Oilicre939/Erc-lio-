<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Megabytes Vodacom - Pacotes de Internet</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-red: #e4002b;
            --dark-red: #c40023;
            --white: #ffffff;
            --light-gray: #f5f5f5;
            --medium-gray: #e0e0e0;
            --dark-gray: #333333;
            --black: #111111;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a1a1a, #000);
            color: var(--white);
            line-height: 1.6;
            min-height: 100vh;
            background-attachment: fixed;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 1rem;
        }
        
        /* Header Compacto */
        .compact-header {
            background: linear-gradient(135deg, var(--primary-red), var(--dark-red));
            color: var(--white);
            padding: 0.8rem 1rem;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.4);
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 3px solid #ffcc00;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: bold;
            font-size: 1.3rem;
        }
        
        .logo i {
            font-size: 1.5rem;
            color: #ffcc00;
        }
        
        .whatsapp-btn {
            background: #25D366;
            color: white;
            padding: 0.6rem 1.2rem;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
        }
        
        .whatsapp-btn:hover {
            background: #128C7E;
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.4);
        }
        
        /* Main Content */
        .main-content {
            text-align: center;
            padding: 2rem 1rem;
        }
        
        .main-title {
            font-size: 2.2rem;
            margin-bottom: 1rem;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
            color: #ffcc00;
            position: relative;
            display: inline-block;
        }
        
        .main-title::after {
            content: "";
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 120px;
            height: 4px;
            background: var(--primary-red);
            border-radius: 2px;
        }
        
        .subtitle {
            font-size: 1.1rem;
            margin-bottom: 2rem;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
            color: #ddd;
        }
        
        /* Tabs */
        .tabs-container {
            margin: 2rem auto;
            max-width: 1000px;
        }
        
        .tabs {
            display: flex;
            justify-content: center;
            margin-bottom: 1.5rem;
            flex-wrap: wrap;
            gap: 8px;
        }
        
        .tab-btn {
            padding: 0.7rem 1.5rem;
            background: rgba(255, 255, 255, 0.1);
            border: none;
            border-radius: 30px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            color: #ddd;
            font-size: 0.95rem;
        }
        
        .tab-btn.active, .tab-btn:hover {
            background: var(--primary-red);
            color: var(--white);
            box-shadow: 0 4px 10px rgba(228, 0, 43, 0.4);
        }
        
        .tab-content {
            display: none;
            background: rgba(30, 30, 30, 0.7);
            border-radius: 12px;
            padding: 1.5rem;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.4);
            border: 1px solid rgba(228, 0, 43, 0.3);
        }
        
        .tab-content.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Package Table */
        .package-table {
            width: 100%;
            border-collapse: collapse;
            margin: 1rem 0;
        }
        
        .package-table th {
            background: var(--primary-red);
            padding: 1rem;
            text-align: center;
            font-size: 1.1rem;
        }
        
        .package-table td {
            padding: 1rem;
            text-align: center;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .package-table tr:nth-child(even) {
            background: rgba(50, 50, 50, 0.5);
        }
        
        .package-table tr:hover {
            background: rgba(228, 0, 43, 0.15);
        }
        
        .package-size {
            font-weight: bold;
            font-size: 1.1rem;
            color: #ffcc00;
        }
        
        .package-price {
            font-weight: bold;
            font-size: 1.1rem;
            color: var(--primary-red);
        }
        
        .buy-btn {
            background: rgba(228, 0, 43, 0.2);
            color: var(--white);
            border: 1px solid var(--primary-red);
            padding: 0.5rem 1rem;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: bold;
        }
        
        .buy-btn:hover {
            background: var(--primary-red);
            transform: translateY(-3px);
            box-shadow: 0 4px 10px rgba(228, 0, 43, 0.4);
        }
        
        /* Payment Section */
        .payment-section {
            background: rgba(30, 30, 30, 0.7);
            border-radius: 12px;
            padding: 1.5rem;
            margin: 2rem auto;
            max-width: 1000px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.4);
            border: 1px solid rgba(228, 0, 43, 0.3);
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 1.5rem;
            color: #ffcc00;
            font-size: 1.5rem;
        }
        
        .payment-options {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1.5rem;
            margin-top: 1.5rem;
        }
        
        .payment-card {
            background: rgba(40, 40, 40, 0.8);
            padding: 1.5rem;
            border-radius: 10px;
            flex-basis: 280px;
            text-align: center;
            border: 1px solid rgba(228, 0, 43, 0.3);
            transition: all 0.3s ease;
        }
        
        .payment-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(228, 0, 43, 0.3);
            border-color: var(--primary-red);
        }
        
        .payment-card h3 {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            margin-bottom: 1rem;
            color: var(--primary-red);
        }
        
        .payment-card .number {
            font-size: 1.4rem;
            font-weight: bold;
            margin: 0.8rem 0;
            color: #ffcc00;
        }
        
        .payment-card .name {
            font-size: 1rem;
            color: #ccc;
        }
        
        .cta-box {
            background: linear-gradient(135deg, var(--primary-red), var(--dark-red));
            border-radius: 12px;
            padding: 2rem;
            margin: 2rem auto;
            max-width: 1000px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(228, 0, 43, 0.4);
            border: 2px solid #ffcc00;
        }
        
        .cta-box h2 {
            font-size: 1.8rem;
            margin-bottom: 1rem;
            color: #ffcc00;
        }
        
        .cta-box p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .highlight {
            color: #ffcc00;
            font-weight: bold;
            text-shadow: 0 0 10px rgba(255, 204, 0, 0.5);
        }
        
        .pulse {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        footer {
            text-align: center;
            padding: 2rem 1rem;
            color: #aaa;
            font-size: 0.9rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            margin-top: 2rem;
        }
        
        /* Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.9);
            z-index: 1000;
            align-items: center;
            justify-content: center;
        }
        
        .modal-content {
            background: rgba(30, 30, 30, 0.95);
            border-radius: 12px;
            width: 90%;
            max-width: 500px;
            padding: 2rem;
            position: relative;
            animation: modalFadeIn 0.3s ease;
            border: 2px solid var(--primary-red);
            box-shadow: 0 0 30px rgba(228, 0, 43, 0.6);
        }
        
        @keyframes modalFadeIn {
            from { opacity: 0; transform: translateY(-50px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .close-modal {
            position: absolute;
            top: 15px;
            right: 15px;
            font-size: 1.8rem;
            cursor: pointer;
            color: #ccc;
            transition: color 0.3s;
        }
        
        .close-modal:hover {
            color: var(--primary-red);
        }
        
        .modal h3 {
            text-align: center;
            color: #ffcc00;
            margin-bottom: 1.5rem;
            font-size: 1.6rem;
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
            color: #ddd;
        }
        
        .form-group input, .form-group select {
            width: 100%;
            padding: 0.9rem;
            background: rgba(50, 50, 50, 0.7);
            border: 1px solid rgba(228, 0, 43, 0.5);
            border-radius: 8px;
            font-size: 1rem;
            color: white;
        }
        
        .selected-package {
            background: rgba(228, 0, 43, 0.15);
            padding: 1.2rem;
            border-radius: 8px;
            margin: 1.5rem 0;
            border-left: 4px solid var(--primary-red);
        }
        
        .selected-package p {
            margin: 0.5rem 0;
            font-size: 1.1rem;
        }
        
        .modal-btn {
            background: linear-gradient(135deg, var(--primary-red), var(--dark-red));
            color: white;
            width: 100%;
            padding: 1rem;
            border: none;
            border-radius: 8px;
            font-weight: bold;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            margin-top: 1rem;
        }
        
        .modal-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(228, 0, 43, 0.6);
        }
        
        /* Responsividade */
        @media (max-width: 768px) {
            .compact-header {
                flex-direction: column;
                gap: 10px;
                padding: 0.8rem;
            }
            
            .main-title {
                font-size: 1.8rem;
            }
            
            .package-table th, .package-table td {
                padding: 0.8rem 0.5rem;
                font-size: 0.9rem;
            }
            
            .package-size, .package-price {
                font-size: 1rem;
            }
            
            .buy-btn {
                padding: 0.4rem 0.8rem;
                font-size: 0.9rem;
            }
            
            .payment-options {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <!-- Header Compacto -->
    <header class="compact-header">
        <div class="logo">
            <i class="fas fa-bolt"></i>
            <span>MEGABYTES VODACOM</span>
        </div>
        <a href="https://wa.me/865627840" class="whatsapp-btn" target="_blank">
            <i class="fab fa-whatsapp"></i> Comprar Agora
        </a>
    </header>

    <!-- Conteúdo Principal -->
    <div class="container">
        <div class="main-content">
            <h1 class="main-title">🚨📢 MEGABYTES DA VODACOM 📢🚨</h1>
            <p class="subtitle">Adquira já os teus megas com segurança, confiança e rapidez! Navegue com a melhor internet e fale sem limites.</p>
            
            <div class="tabs-container">
                <div class="tabs">
                    <button class="tab-btn active" data-tab="diario">📦 PACOTE DIÁRIO</button>
                    <button class="tab-btn" data-tab="semanal">📦 PACOTE SEMANAL</button>
                    <button class="tab-btn" data-tab="mensal">📦 PACOTE MENSAL</button>
                    <button class="tab-btn" data-tab="ilimitado">♾️ TUDO TOP ILIMITADO</button>
                </div>
                
                <!-- Diário -->
                <div class="tab-content active" id="diario-content">
                    <table class="package-table">
                        <thead>
                            <tr>
                                <th>PACOTE</th>
                                <th>PREÇO</th>
                                <th>AÇÃO</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td class="package-size">🛜 256MB</td>
                                <td class="package-price">6 MT</td>
                                <td><button class="buy-btn" data-package="Diário 256MB" data-price="6MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">🛜 512MB</td>
                                <td class="package-price">10 MT</td>
                                <td><button class="buy-btn" data-package="Diário 512MB" data-price="10MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">🛜 1024MB</td>
                                <td class="package-price">20 MT</td>
                                <td><button class="buy-btn" data-package="Diário 1024MB" data-price="20MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">🛜 2048MB</td>
                                <td class="package-price">38 MT</td>
                                <td><button class="buy-btn" data-package="Diário 2048MB" data-price="38MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">🛜 3072MB</td>
                                <td class="package-price">57 MT</td>
                                <td><button class="buy-btn" data-package="Diário 3072MB" data-price="57MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">🛜 4096MB</td>
                                <td class="package-price">76 MT</td>
                                <td><button class="buy-btn" data-package="Diário 4096MB" data-price="76MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">🛜 5120MB</td>
                                <td class="package-price">95 MT</td>
                                <td><button class="buy-btn" data-package="Diário 5120MB" data-price="95MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">🛜 10240MB</td>
                                <td class="package-price">190 MT</td>
                                <td><button class="buy-btn" data-package="Diário 10240MB" data-price="190MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">🛜 20480MB</td>
                                <td class="package-price">380 MT</td>
                                <td><button class="buy-btn" data-package="Diário 20480MB" data-price="380MT">Comprar</button></td>
                            </tr>
                        </tbody>
                    </table>
                </div>
                
                <!-- Semanal -->
                <div class="tab-content" id="semanal-content">
                    <table class="package-table">
                        <thead>
                            <tr>
                                <th>PACOTE</th>
                                <th>PREÇO</th>
                                <th>AÇÃO</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td class="package-size">🛜 2.9GB</td>
                                <td class="package-price">85 MT</td>
                                <td><button class="buy-btn" data-package="Semanal 2.9GB" data-price="85MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">🛜 3.4GB</td>
                                <td class="package-price">95 MT</td>
                                <td><button class="buy-btn" data-package="Semanal 3.4GB" data-price="95MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">🛜 5.2GB</td>
                                <td class="package-price">145 MT</td>
                                <td><button class="buy-btn" data-package="Semanal 5.2GB" data-price="145MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">🛜 7.1GB</td>
                                <td class="package-price">195 MT</td>
                                <td><button class="buy-btn" data-package="Semanal 7.1GB" data-price="195MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">🛜 10.7GB</td>
                                <td class="package-price">295 MT</td>
                                <td><button class="buy-btn" data-package="Semanal 10.7GB" data-price="295MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">🛜 14.3GB</td>
                                <td class="package-price">395 MT</td>
                                <td><button class="buy-btn" data-package="Semanal 14.3GB" data-price="395MT">Comprar</button></td>
                            </tr>
                        </tbody>
                    </table>
                </div>
                
                <!-- Mensal -->
                <div class="tab-content" id="mensal-content">
                    <table class="package-table">
                        <thead>
                            <tr>
                                <th>PACOTE</th>
                                <th>PREÇO</th>
                                <th>AÇÃO</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td class="package-size">📊 2.8GB</td>
                                <td class="package-price">95 MT</td>
                                <td><button class="buy-btn" data-package="Mensal 2.8GB" data-price="95MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">📊 3.8GB</td>
                                <td class="package-price">125 MT</td>
                                <td><button class="buy-btn" data-package="Mensal 3.8GB" data-price="125MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">📊 4.8GB</td>
                                <td class="package-price">145 MT</td>
                                <td><button class="buy-btn" data-package="Mensal 4.8GB" data-price="145MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">📊 5.8GB</td>
                                <td class="package-price">165 MT</td>
                                <td><button class="buy-btn" data-package="Mensal 5.8GB" data-price="165MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">📊 6.8GB</td>
                                <td class="package-price">195 MT</td>
                                <td><button class="buy-btn" data-package="Mensal 6.8GB" data-price="195MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">📊 7.8GB</td>
                                <td class="package-price">215 MT</td>
                                <td><button class="buy-btn" data-package="Mensal 7.8GB" data-price="215MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">📊 10.8GB</td>
                                <td class="package-price">285 MT</td>
                                <td><button class="buy-btn" data-package="Mensal 10.8GB" data-price="285MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">📊 12.8GB</td>
                                <td class="package-price">345 MT</td>
                                <td><button class="buy-btn" data-package="Mensal 12.8GB" data-price="345MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">📊 20.8GB</td>
                                <td class="package-price">565 MT</td>
                                <td><button class="buy-btn" data-package="Mensal 20.8GB" data-price="565MT">Comprar</button></td>
                            </tr>
                        </tbody>
                    </table>
                </div>
                
                <!-- Ilimitado -->
                <div class="tab-content" id="ilimitado-content">
                    <table class="package-table">
                        <thead>
                            <tr>
                                <th>PACOTE</th>
                                <th>PREÇO</th>
                                <th>BENEFÍCIOS</th>
                                <th>AÇÃO</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td class="package-size">🔷️ 11GB</td>
                                <td class="package-price">450 MT</td>
                                <td>Chamadas📞 + SMS ilimitadas + 11GB♾️🛜</td>
                                <td><button class="buy-btn" data-package="Ilimitado 11GB" data-price="450MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">🔷️ 15GB</td>
                                <td class="package-price">550 MT</td>
                                <td>Chamadas📞 + SMS ilimitadas + 15GB♾️🛜</td>
                                <td><button class="buy-btn" data-package="Ilimitado 15GB" data-price="550MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">🔷️ 21GB</td>
                                <td class="package-price">750 MT</td>
                                <td>Chamadas📞 + SMS ilimitadas + 21GB♾️🛜</td>
                                <td><button class="buy-btn" data-package="Ilimitado 21GB" data-price="750MT">Comprar</button></td>
                            </tr>
                            <tr>
                                <td class="package-size">🔷️ 31GB</td>
                                <td class="package-price">1100 MT</td>
                                <td>Chamadas📞 + SMS ilimitadas + 31GB♾️🛜</td>
                                <td><button class="buy-btn" data-package="Ilimitado 31GB" data-price="1100MT">Comprar</button></td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
            
            <!-- Seção de Pagamento -->
            <div class="payment-section">
                <h2 class="section-title">💳 FORMAS DE PAGAMENTO 💸</h2>
                <p class="subtitle">Escolha a forma de pagamento mais conveniente para você:</p>
                
                <div class="payment-options">
                    <div class="payment-card">
                        <h3><i class="fas fa-mobile-alt"></i> M-Pesa</h3>
                        <div class="number">853529033</div>
                        <div class="name">Ercílio Uanela</div>
                    </div>
                    
                    <div class="payment-card">
                        <h3><i class="fas fa-wallet"></i> e-Mola</h3>
                        <div class="number">865627840</div>
                        <div class="name">Alexandre Uanela</div>
                    </div>
                </div>
            </div>
            
            <!-- Call to Action -->
            <div class="cta-box pulse">
                <h2>⭐ OFERTA ESPECIAL! ⭐</h2>
                <p>Adquira <span class="highlight">QUALQUER PACOTE</span> agora e receba <span class="highlight">5% DE BÔNUS</span> em sua próxima compra!</p>
                <p>Garanta já seus megabytes com a melhor internet de Moçambique!</p>
                <a href="https://wa.me/865627840" class="whatsapp-btn" style="font-size: 1.2rem; padding: 0.8rem 2rem;" target="_blank">
                    <i class="fab fa-whatsapp"></i> COMPRAR AGORA PELO WHATSAPP
                </a>
            </div>
        </div>
    </div>
    
    <footer>
        <p>© Desenvolvedor Ercílio🧑‍💻. Todos os direitos reservados.</p>
        <p>Adquira já os teus megas com segurança, confiança e rapidez!🚨🔥</p>
    </footer>
    
    <!-- Modal de Compra -->
    <div class="modal" id="purchaseModal">
        <div class="modal-content">
            <span class="close-modal">&times;</span>
            <h3>FINALIZAR COMPRA</h3>
            
            <div class="selected-package">
                <p><strong>Pacote Selecionado:</strong> <span id="selectedPackage"></span></p>
                <p><strong>Valor:</strong> <span id="selectedPrice"></span></p>
            </div>
            
            <form id="purchaseForm">
                <div class="form-group">
                    <label for="phoneNumber">Número para receber os megabytes:</label>
                    <input type="tel" id="phoneNumber" placeholder="Ex: 841234567" required>
                </div>
                
                <div class="form-group">
                    <label for="paymentMethod">Forma de Pagamento:</label>
                    <select id="paymentMethod" required>
                        <option value="">Selecione uma opção</option>
                        <option value="M-Pesa">M-Pesa</option>
                        <option value="e-Mola">e-Mola</option>
                    </select>
                </div>
                
                <button type="submit" class="modal-btn">
                    <i class="fab fa-whatsapp"></i> CONFIRMAR COMPRA VIA WHATSAPP
                </button>
            </form>
        </div>
    </div>

    <script>
        // Tab functionality
        const tabBtns = document.querySelectorAll('.tab-btn');
        const tabContents = document.querySelectorAll('.tab-content');
        
        tabBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                // Remove active class from all buttons
                tabBtns.forEach(b => b.classList.remove('active'));
                // Add active class to clicked button
                btn.classList.add('active');
                
                // Hide all tab contents
                tabContents.forEach(content => content.classList.remove('active'));
                // Show the corresponding tab content
                const tabId = btn.getAttribute('data-tab') + '-content';
                document.getElementById(tabId).classList.add('active');
            });
        });
        
        // Modal functionality
        const modal = document.getElementById('purchaseModal');
        const closeModal = document.querySelector('.close-modal');
        const buyBtns = document.querySelectorAll('.buy-btn');
        const selectedPackageEl = document.getElementById('selectedPackage');
        const selectedPriceEl = document.getElementById('selectedPrice');
        const purchaseForm = document.getElementById('purchaseForm');
        
        // Open modal when clicking any "Comprar" button
        buyBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                const package = btn.getAttribute('data-package');
                const price = btn.getAttribute('data-price');
                
                selectedPackageEl.textContent = package;
                selectedPriceEl.textContent = price;
                
                modal.style.display = 'flex';
                document.body.style.overflow = 'hidden';
            });
        });
        
        // Close modal when clicking the close button
        closeModal.addEventListener('click', () => {
            modal.style.display = 'none';
            document.body.style.overflow = 'auto';
        });
        
        // Close modal when clicking outside of it
        window.addEventListener('click', (e) => {
            if (e.target === modal) {
                modal.style.display = 'none';
                document.body.style.overflow = 'auto';
            }
        });
        
        // Form submission
        purchaseForm.addEventListener('submit', (e) => {
            e.preventDefault();
            
            const phoneNumber = document.getElementById('phoneNumber').value;
            const paymentMethod = document.getElementById('paymentMethod').value;
            const package = selectedPackageEl.textContent;
            const price = selectedPriceEl.textContent;
            
            // Create WhatsApp message
            const message = `Olá! Gostaria de comprar o pacote *${package}* no valor de *${price}*.%0A%0A` +
                            `Número para envio: *${phoneNumber}*%0A` +
                            `Forma de pagamento: *${paymentMethod}*`;
            
            // Open WhatsApp with pre-filled message
            window.open(`https://wa.me/865627840?text=${message}`, '_blank');
            
            // Close modal
            modal.style.display = 'none';
            document.body.style.overflow = 'auto';
            
            // Reset form
            purchaseForm.reset();
        });
        
        // Auto-scroll to packages section
        window.addEventListener('load', () => {
            setTimeout(() => {
                document.querySelector('.tabs-container').scrollIntoView({
                    behavior: 'smooth'
                });
            }, 500);
        });
    </script>
</body>
</html>
