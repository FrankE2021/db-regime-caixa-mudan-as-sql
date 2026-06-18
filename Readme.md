<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Documentação de Mudanças | Regime de Caixa - Sankhya ERP</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-primary: #ffffff;
            --bg-secondary: #f8fafc;
            --bg-tertiary: #f1f5f9;
            --bg-dark: #0a0f1a;
            --text-primary: #1e293b;
            --text-secondary: #475569;
            --text-light: #94a3b8;
            --text-white: #f8fafc;
            --border-color: #e2e8f0;
            --border-light: #f1f5f9;
            --blue-50: #eff6ff;
            --blue-100: #dbeafe;
            --blue-200: #bfdbfe;
            --blue-300: #93c5fd;
            --blue-400: #60a5fa;
            --blue-500: #3b82f6;
            --blue-600: #2563eb;
            --blue-700: #1d4ed8;
            --blue-800: #1e40af;
            --blue-900: #1e3a8a;
            --accent: #2563eb;
            --green-500: #22c55e;
            --green-100: #dcfce7;
            --green-700: #15803d;
            --red-500: #ef4444;
            --red-100: #fef2f2;
            --red-700: #b91c1c;
            --orange-500: #f59e0b;
            --orange-100: #fff7ed;
            --orange-700: #c2410c;
            --gradient-1: linear-gradient(135deg, #1e3a8a 0%, #2563eb 50%, #3b82f6 100%);
            --gradient-2: linear-gradient(135deg, #0f172a 0%, #1e293b 50%, #1e3a8a 100%);
            --shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
            --shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -2px rgba(0, 0, 0, 0.1);
            --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -4px rgba(0, 0, 0, 0.1);
            --shadow-xl: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 8px 10px -6px rgba(0, 0, 0, 0.1);
            --radius-sm: 0.5rem;
            --radius-md: 0.75rem;
            --radius-lg: 1rem;
            --radius-xl: 1.25rem;
            --radius-2xl: 1.5rem;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            font-size: 16px;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            background-color: var(--bg-secondary);
            color: var(--text-primary);
            line-height: 1.7;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }

        /* ===== HERO ===== */
        .hero {
            padding: 5rem 2rem 4rem;
            background: var(--gradient-2);
            position: relative;
            overflow: hidden;
            text-align: center;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(ellipse at 30% 50%, rgba(59, 130, 246, 0.12) 0%, transparent 60%),
                        radial-gradient(ellipse at 70% 30%, rgba(30, 64, 175, 0.15) 0%, transparent 60%);
            animation: heroGlow 8s ease-in-out infinite alternate;
        }

        @keyframes heroGlow {
            0% { transform: translate(0, 0) scale(1); }
            100% { transform: translate(2%, -2%) scale(1.05); }
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            margin: 0 auto;
        }

        .hero-badge {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            color: var(--blue-200);
            padding: 0.5rem 1.25rem;
            border-radius: 100px;
            font-size: 0.85rem;
            font-weight: 500;
            margin-bottom: 1.5rem;
            backdrop-filter: blur(10px);
        }

        .hero-badge-dot {
            width: 8px;
            height: 8px;
            background: #22c55e;
            border-radius: 50%;
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.4; }
        }

        .hero h1 {
            font-size: clamp(2rem, 5vw, 3.5rem);
            font-weight: 900;
            color: white;
            line-height: 1.15;
            letter-spacing: -0.03em;
            margin-bottom: 1rem;
        }

        .hero h1 span {
            background: linear-gradient(135deg, #60a5fa, #93c5fd, #bfdbfe);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero p {
            font-size: 1.1rem;
            color: var(--text-light);
            font-weight: 400;
            line-height: 1.7;
        }

        .hero-meta {
            display: flex;
            gap: 2rem;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 2rem;
        }

        .hero-meta-item {
            color: var(--text-light);
            font-size: 0.85rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        /* ===== CONTAINER ===== */
        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* ===== SECTIONS ===== */
        .section {
            padding: 4rem 0;
        }

        .section-title {
            font-size: clamp(1.5rem, 3vw, 2.2rem);
            font-weight: 800;
            color: var(--text-primary);
            letter-spacing: -0.02em;
            margin-bottom: 0.75rem;
            line-height: 1.2;
        }

        .section-subtitle {
            font-size: 1rem;
            color: var(--text-secondary);
            margin-bottom: 2rem;
        }

        /* ===== SUMMARY CARDS ===== */
        .summary-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            gap: 1.25rem;
            margin-bottom: 3rem;
        }

        .summary-card {
            background: white;
            border: 1px solid var(--border-color);
            border-radius: var(--radius-xl);
            padding: 1.75rem;
            box-shadow: var(--shadow-sm);
            transition: all 0.3s ease;
        }

        .summary-card:hover {
            box-shadow: var(--shadow-lg);
            transform: translateY(-2px);
        }

        .summary-card-icon {
            width: 44px;
            height: 44px;
            border-radius: var(--radius-md);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.3rem;
            margin-bottom: 1rem;
        }

        .summary-card-icon.red { background: var(--red-100); }
        .summary-card-icon.green { background: var(--green-100); }
        .summary-card-icon.blue { background: var(--blue-50); }
        .summary-card-icon.orange { background: var(--orange-100); }

        .summary-card h3 {
            font-size: 0.85rem;
            font-weight: 700;
            color: var(--text-primary);
            margin-bottom: 0.25rem;
            text-transform: uppercase;
            letter-spacing: 0.04em;
        }

        .summary-card .value {
            font-size: 2rem;
            font-weight: 900;
            letter-spacing: -0.02em;
        }

        .summary-card .value.red { color: var(--red-500); }
        .summary-card .value.green { color: var(--green-500); }
        .summary-card .value.blue { color: var(--accent); }
        .summary-card .value.orange { color: var(--orange-500); }

        /* ===== TABLE ===== */
        .table-wrapper {
            overflow-x: auto;
            border-radius: var(--radius-xl);
            border: 1px solid var(--border-color);
            background: white;
            box-shadow: var(--shadow-md);
            margin-bottom: 2rem;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            font-size: 0.88rem;
        }

        thead {
            background: #0f172a;
        }

        th {
            padding: 1rem 1.25rem;
            text-align: left;
            font-weight: 700;
            color: white;
            font-size: 0.78rem;
            text-transform: uppercase;
            letter-spacing: 0.06em;
            white-space: nowrap;
        }

        td {
            padding: 0.9rem 1.25rem;
            border-bottom: 1px solid var(--border-light);
            color: var(--text-secondary);
            vertical-align: top;
        }

        tr:last-child td {
            border-bottom: none;
        }

        tbody tr {
            transition: background 0.2s ease;
        }

        tbody tr:hover {
            background: var(--blue-50);
        }

        .badge {
            display: inline-block;
            padding: 0.25rem 0.65rem;
            border-radius: 100px;
            font-size: 0.7rem;
            font-weight: 700;
            letter-spacing: 0.03em;
            text-transform: uppercase;
        }

        .badge-red {
            background: var(--red-100);
            color: var(--red-700);
        }

        .badge-green {
            background: var(--green-100);
            color: var(--green-700);
        }

        .badge-blue {
            background: var(--blue-50);
            color: var(--blue-700);
        }

        .badge-orange {
            background: var(--orange-100);
            color: var(--orange-700);
        }

        /* ===== ETAPAS CARDS ===== */
        .etapas-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 1.5rem;
            margin-bottom: 2rem;
        }

        .etapa-card {
            background: white;
            border: 1px solid var(--border-color);
            border-radius: var(--radius-xl);
            padding: 2rem;
            box-shadow: var(--shadow-sm);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .etapa-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
        }

        .etapa-card.etapa-1::before { background: var(--accent); }
        .etapa-card.etapa-2::before { background: var(--green-500); }
        .etapa-card.etapa-3::before { background: var(--orange-500); }

        .etapa-card:hover {
            box-shadow: var(--shadow-lg);
            transform: translateY(-2px);
        }

        .etapa-card-header {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            margin-bottom: 1.25rem;
        }

        .etapa-numero {
            width: 40px;
            height: 40px;
            border-radius: var(--radius-md);
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 900;
            font-size: 1.1rem;
            color: white;
            flex-shrink: 0;
        }

        .etapa-1 .etapa-numero { background: var(--accent); }
        .etapa-2 .etapa-numero { background: var(--green-500); }
        .etapa-3 .etapa-numero { background: var(--orange-500); }

        .etapa-card h3 {
            font-size: 1rem;
            font-weight: 700;
            color: var(--text-primary);
        }

        .etapa-card p {
            font-size: 0.85rem;
            color: var(--text-secondary);
            line-height: 1.6;
            margin-bottom: 0.75rem;
        }

        .etapa-card ul {
            list-style: none;
            font-size: 0.82rem;
            color: var(--text-secondary);
        }

        .etapa-card ul li {
            padding: 0.25rem 0;
            padding-left: 1.25rem;
            position: relative;
        }

        .etapa-card ul li::before {
            content: '▸';
            position: absolute;
            left: 0;
            color: var(--accent);
            font-weight: 700;
        }

        .etapa-2 ul li::before { color: var(--green-500); }
        .etapa-3 ul li::before { color: var(--orange-500); }

        /* ===== CODE BLOCK ===== */
        .code-block {
            background: #0d1117;
            border-radius: var(--radius-lg);
            padding: 1.25rem;
            overflow-x: auto;
            font-family: 'SF Mono', 'Fira Code', 'Fira Mono', 'Roboto Mono', monospace;
            font-size: 0.78rem;
            line-height: 1.7;
            color: #c9d1d9;
            border: 1px solid #21262d;
            margin-bottom: 1.5rem;
        }

        .code-block .kw { color: #ff7b72; }
        .code-block .fn { color: #d2a8ff; }
        .code-block .str { color: #a5d6ff; }
        .code-block .cm { color: #8b949e; font-style: italic; }
        .code-block .tb { color: #ffa657; }
        .code-block .op { color: #79c0ff; }
        .code-block .num { color: #a5d6ff; }

        /* ===== NATUREZAS LIST ===== */
        .natureza-list {
            background: white;
            border: 1px solid var(--border-color);
            border-radius: var(--radius-xl);
            padding: 1.5rem 2rem;
            box-shadow: var(--shadow-sm);
        }

        .natureza-list h4 {
            font-size: 0.9rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: var(--text-primary);
        }

        .natureza-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 0.5rem;
        }

        .natureza-item {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            padding: 0.5rem 0.75rem;
            background: var(--bg-tertiary);
            border-radius: var(--radius-sm);
            font-size: 0.82rem;
        }

        .natureza-codigo {
            font-weight: 700;
            color: var(--accent);
            font-family: 'SF Mono', 'Fira Code', monospace;
            font-size: 0.8rem;
            min-width: 65px;
        }

        .natureza-desc {
            color: var(--text-secondary);
        }

        /* ===== FOOTER ===== */
        .footer {
            background: var(--bg-dark);
            color: var(--text-light);
            padding: 2rem;
            text-align: center;
            border-top: 1px solid #1e293b;
            font-size: 0.82rem;
        }

        .footer strong {
            color: white;
        }

        /* ===== RESPONSIVE ===== */
        @media (max-width: 768px) {
            .hero {
                padding: 4rem 1.5rem 3rem;
            }

            .hero h1 {
                font-size: 1.8rem;
            }

            .section {
                padding: 2.5rem 0;
            }

            .container {
                padding: 0 1.25rem;
            }

            .etapas-grid {
                grid-template-columns: 1fr;
            }

            .summary-grid {
                grid-template-columns: 1fr 1fr;
            }

            th, td {
                padding: 0.65rem 0.75rem;
                font-size: 0.75rem;
            }
        }

        @media (max-width: 480px) {
            .summary-grid {
                grid-template-columns: 1fr;
            }

            .hero-meta {
                flex-direction: column;
                gap: 0.5rem;
            }
        }

        /* ===== PRINT ===== */
        @media print {
            body {
                background: white;
            }

            .hero {
                background: #0f172a !important;
                -webkit-print-color-adjust: exact;
            }

            .etapa-card, .summary-card, .table-wrapper {
                break-inside: avoid;
                box-shadow: none;
            }
        }
    </style>
</head>
<body>

    <!-- HERO -->
    <section class="hero">
        <div class="hero-content">
            <div class="hero-badge">
                <div class="hero-badge-dot"></div>
                Documentação Técnica · Junho 2026
            </div>
            <h1>Documentação de Mudanças<br><span>Regime de Caixa</span></h1>
            <p>Análise comparativa entre a query original e a versão corrigida, detalhando todas as alterações realizadas para atender às três etapas de extração solicitadas.</p>
            <div class="hero-meta">
                <div class="hero-meta-item">📋 Tela: Regime de Caixa</div>
                <div class="hero-meta-item">🗄️ Base: TGFFIN / AD_VINCULAPA / TGFABF</div>
                <div class="hero-meta-item">📅 Versão: 2.0 Corrigida</div>
            </div>
        </div>
    </section>

    <!-- CONTEÚDO -->
    <div class="container">

        <!-- RESUMO -->
        <section class="section">
            <h2 class="section-title">Resumo das Alterações</h2>
            <p class="section-subtitle">Indicadores comparativos entre a versão original e a versão corrigida da query.</p>

            <div class="summary-grid">
                <div class="summary-card">
                    <div class="summary-card-icon red">🔴</div>
                    <h3>Problemas Identificados</h3>
                    <div class="value red">7</div>
                    <p style="font-size:0.85rem;color:var(--text-secondary);margin-top:0.5rem;">Erros de lógica, filtros incorretos e etapas ausentes.</p>
                </div>
                <div class="summary-card">
                    <div class="summary-card-icon green">✅</div>
                    <h3>Problemas Corrigidos</h3>
                    <div class="value green">7</div>
                    <p style="font-size:0.85rem;color:var(--text-secondary);margin-top:0.5rem;">Todos os problemas foram resolvidos na nova versão.</p>
                </div>
                <div class="summary-card">
                    <div class="summary-card-icon blue">📊</div>
                    <h3>Etapas de Extração</h3>
                    <div class="value blue">3</div>
                    <p style="font-size:0.85rem;color:var(--text-secondary);margin-top:0.5rem;">Original: 1 etapa. Corrigida: 3 UNION ALL.</p>
                </div>
                <div class="summary-card">
                    <div class="summary-card-icon orange">🆕</div>
                    <h3>Nova Coluna</h3>
                    <div class="value orange">1</div>
                    <p style="font-size:0.85rem;color:var(--text-secondary);margin-top:0.5rem;">DTBAIXACX (Data Baixa CX) adicionada.</p>
                </div>
            </div>
        </section>

        <!-- COMPARATIVO ESTRUTURA -->
        <section class="section">
            <h2 class="section-title">Comparativo de Estrutura</h2>
            <p class="section-subtitle">Diferenças fundamentais entre a query original e a versão corrigida.</p>

            <div class="table-wrapper">
                <table>
                    <thead>
                        <tr>
                            <th>Aspecto</th>
                            <th>Original</th>
                            <th>Corrigida</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><strong>Tipo de Consulta</strong></td>
                            <td><span class="badge badge-red">1 SELECT</span></td>
                            <td><span class="badge badge-green">3 UNION ALL</span></td>
                        </tr>
                        <tr>
                            <td><strong>Número de Etapas</strong></td>
                            <td><span class="badge badge-red">1 (misturada)</span></td>
                            <td><span class="badge badge-green">3 (separadas)</span></td>
                        </tr>
                        <tr>
                            <td><strong>CTE (WITH)</strong></td>
                            <td><span class="badge badge-red">Sim</span></td>
                            <td><span class="badge badge-green">Removido</span></td>
                        </tr>
                        <tr>
                            <td><strong>JOIN CB</strong></td>
                            <td><span class="badge badge-red">LEFT JOIN</span></td>
                            <td><span class="badge badge-green">INNER JOIN (direto)</span></td>
                        </tr>
                        <tr>
                            <td><strong>JOIN VPA</strong></td>
                            <td><span class="badge badge-red">LEFT JOIN</span></td>
                            <td><span class="badge badge-green">INNER JOIN (2ª e 3ª)</span></td>
                        </tr>
                        <tr>
                            <td><strong>JOIN TGFABF</strong></td>
                            <td><span class="badge badge-red">Não existia</span></td>
                            <td><span class="badge badge-green">INNER JOIN (3ª parte)</span></td>
                        </tr>
                        <tr>
                            <td><strong>Filtro RECDESP</strong></td>
                            <td><span class="badge badge-red">Apenas -1</span></td>
                            <td><span class="badge badge-green">-1 / sem filtro / 1</span></td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

        <!-- ETAPAS -->
        <section class="section">
            <h2 class="section-title">As 3 Etapas de Extração</h2>
            <p class="section-subtitle">Cada etapa possui sua própria lógica de extração, fonte de dados e regra para a Data Baixa CX.</p>

            <div class="etapas-grid">
                <!-- ETAPA 1 -->
                <div class="etapa-card etapa-1">
                    <div class="etapa-card-header">
                        <div class="etapa-numero">1</div>
                        <h3>Despesa Real Baixados</h3>
                    </div>
                    <p><strong>Fonte:</strong> TGFFIN + TGFMBC + TSICTA</p>
                    <p><strong>DTBAIXACX:</strong> FIN.DHBAIXA</p>
                    <ul>
                        <li>Filtro: RECDESP = -1</li>
                        <li>Exclui: Pag. Antecipados (9 natur.)</li>
                        <li>Exclui: Vinculados PA (NOT EXISTS)</li>
                        <li>NUPA e NUNOTAPA = NULL</li>
                    </ul>
                </div>

                <!-- ETAPA 2 -->
                <div class="etapa-card etapa-2">
                    <div class="etapa-card-header">
                        <div class="etapa-numero">2</div>
                        <h3>Vinculações Compensação/PA</h3>
                    </div>
                    <p><strong>Fonte:</strong> TGFFIN + AD_VINCULAPA</p>
                    <p><strong>DTBAIXACX:</strong> VPA.DATABAIXAPA</p>
                    <ul>
                        <li>Filtro: VPA.NUPA IS NOT NULL</li>
                        <li>Preenche NUPA e NUNOTAPA</li>
                        <li>Período: DATABAIXAPA</li>
                    </ul>
                </div>

                <!-- ETAPA 3 -->
                <div class="etapa-card etapa-3">
                    <div class="etapa-card-header">
                        <div class="etapa-numero">3</div>
                        <h3>PA's Pendentes</h3>
                    </div>
                    <p><strong>Fonte:</strong> TGFFIN + AD_VINCULAPA + TGFABF</p>
                    <p><strong>DTBAIXACX:</strong> ABF.DHMOV</p>
                    <ul>
                        <li>Filtro: RECDESP = 1</li>
                        <li>Filtro: DHBAIXA IS NULL</li>
                        <li>Naturezas de PA específicas</li>
                        <li>Data da Antecipação (TGFABF)</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- FILTROS -->
        <section class="section">
            <h2 class="section-title">Comparativo de Filtros WHERE</h2>
            <p class="section-subtitle">Diferenças detalhadas nos filtros aplicados em cada versão.</p>

            <div class="table-wrapper">
                <table>
                    <thead>
                        <tr>
                            <th>Filtro</th>
                            <th>Original</th>
                            <th>Corrigida</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><strong>RECDESP</strong></td>
                            <td><span class="badge badge-red">-1 apenas</span></td>
                            <td><span class="badge badge-green">-1 (1ª) | sem (2ª) | 1 (3ª)</span></td>
                        </tr>
                        <tr>
                            <td><strong>CB.CONTASBAIXA</strong></td>
                            <td><span class="badge badge-orange">OR VPA.NUPA</span></td>
                            <td><span class="badge badge-green">IS NOT NULL (1ª apenas)</span></td>
                        </tr>
                        <tr>
                            <td><strong>NOT EXISTS PA</strong></td>
                            <td><span class="badge badge-red">Excluía tudo</span></td>
                            <td><span class="badge badge-green">Apenas na 1ª parte</span></td>
                        </tr>
                        <tr>
                            <td><strong>DHBAIXA IS NOT NULL</strong></td>
                            <td><span class="badge badge-red">Não verificava</span></td>
                            <td><span class="badge badge-green">Sim (1ª parte)</span></td>
                        </tr>
                        <tr>
                            <td><strong>DHBAIXA IS NULL</strong></td>
                            <td><span class="badge badge-red">Não existia</span></td>
                            <td><span class="badge badge-green">Sim (3ª parte)</span></td>
                        </tr>
                        <tr>
                            <td><strong>CODNAT NOT IN</strong></td>
                            <td><span class="badge badge-red">Não existia</span></td>
                            <td><span class="badge badge-green">9 naturezas excluídas</span></td>
                        </tr>
                        <tr>
                            <td><strong>CODNAT IN</strong></td>
                            <td><span class="badge badge-red">Não existia</span></td>
                            <td><span class="badge badge-green">9 naturezas incluídas (3ª)</span></td>
                        </tr>
                        <tr>
                            <td><strong>ABF.DHMOV</strong></td>
                            <td><span class="badge badge-red">Não existia</span></td>
                            <td><span class="badge badge-green">Filtro 3ª parte</span></td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

        <!-- NATUREZAS -->
        <section class="section">
            <h2 class="section-title">Naturezas Excluídas (Pagamentos Antecipados)</h2>
            <p class="section-subtitle">Códigos de natureza excluídos da 1ª etapa e incluídos exclusivamente na 3ª etapa.</p>

            <div class="natureza-list">
                <h4>🚫 Excluídos da 1ª Parte | ✅ Incluídos na 3ª Parte</h4>
                <div class="natureza-grid">
                    <div class="natureza-item">
                        <span class="natureza-codigo">90200</span>
                        <span class="natureza-desc">PA - PAGAMENTO ANTECIPADO</span>
                    </div>
                    <div class="natureza-item">
                        <span class="natureza-codigo">90201</span>
                        <span class="natureza-desc">PA - PAGAMENTO ANTECIPADO</span>
                    </div>
                    <div class="natureza-item">
                        <span class="natureza-codigo">90202</span>
                        <span class="natureza-desc">PA - PAG. ANTECIPADO EXTERIOR</span>
                    </div>
                    <div class="natureza-item">
                        <span class="natureza-codigo">90203</span>
                        <span class="natureza-desc">PA - PAG. ANTECIPADO PORTO COMEX</span>
                    </div>
                    <div class="natureza-item">
                        <span class="natureza-codigo">90204</span>
                        <span class="natureza-desc">PA - PAG. ANTECIPADO FÁBRICA NOVA</span>
                    </div>
                    <div class="natureza-item">
                        <span class="natureza-codigo">90205</span>
                        <span class="natureza-desc">PA - PAG. ANTECIPADO IMOBILIZADO</span>
                    </div>
                    <div class="natureza-item">
                        <span class="natureza-codigo">90206</span>
                        <span class="natureza-desc">PA - PAG. ANTECIPADO IMOB. EXTERIOR</span>
                    </div>
                    <div class="natureza-item">
                        <span class="natureza-codigo">190200</span>
                        <span class="natureza-desc">PA - PAG. ANTECIPADO - MPVB</span>
                    </div>
                    <div class="natureza-item">
                        <span class="natureza-codigo">290200</span>
                        <span class="natureza-desc">PA - PAG. ANTECIPADO - LP</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- COLUNAS -->
        <section class="section">
            <h2 class="section-title">Comparativo de Colunas</h2>
            <p class="section-subtitle">Alterações nas colunas retornadas pela query.</p>

            <div class="table-wrapper">
                <table>
                    <thead>
                        <tr>
                            <th>Coluna</th>
                            <th>Original</th>
                            <th>Corrigida</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><strong>DTBAIXA</strong></td>
                            <td><span class="badge badge-orange">CASE WHEN (misturado)</span></td>
                            <td><span class="badge badge-green">1ª: DHBAIXA | 2ª: DATABAIXAPA | 3ª: NULL</span></td>
                        </tr>
                        <tr>
                            <td><strong>DTBAIXACX</strong></td>
                            <td><span class="badge badge-red">Não existia</span></td>
                            <td><span class="badge badge-green">NOVA COLUNA</span></td>
                        </tr>
                        <tr>
                            <td><strong>CONTASBAIXA</strong></td>
                            <td><span class="badge badge-orange">Do CTE CB</span></td>
                            <td><span class="badge badge-green">1ª: JOIN | 2ª e 3ª: NULL</span></td>
                        </tr>
                        <tr>
                            <td><strong>NUPA</strong></td>
                            <td><span class="badge badge-orange">Do LEFT JOIN VPA</span></td>
                            <td><span class="badge badge-green">1ª: NULL | 2ª e 3ª: VPA.NUPA</span></td>
                        </tr>
                        <tr>
                            <td><strong>NUNOTAPA</strong></td>
                            <td><span class="badge badge-orange">Do LEFT JOIN VPA</span></td>
                            <td><span class="badge badge-green">1ª: NULL | 2ª e 3ª: VPA.NUNOTAPA</span></td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

        <!-- RESUMO PROBLEMAS -->
        <section class="section">
            <h2 class="section-title">Resumo dos Problemas Corrigidos</h2>
            <p class="section-subtitle">Lista completa de todos os problemas identificados na query original e suas respectivas correções.</p>

            <div class="table-wrapper">
                <table>
                    <thead>
                        <tr>
                            <th>#</th>
                            <th>Problema Original</th>
                            <th>Correção Aplicada</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>Misturava Despesa e PA em um único SELECT</td>
                            <td><span class="badge badge-green">Separado em 3 UNION ALL</span></td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>Não excluía Pagamentos Antecipados</td>
                            <td><span class="badge badge-green">CODNAT NOT IN (9 naturezas)</span></td>
                        </tr>
                        <tr>
                            <td>3</td>
                            <td>LEFT JOIN fraco (incluía NULLs indevidamente)</td>
                            <td><span class="badge badge-green">INNER JOIN preciso por etapa</span></td>
                        </tr>
                        <tr>
                            <td>4</td>
                            <td>Não existia a 3ª parte (PA's Pendentes)</td>
                            <td><span class="badge badge-green">Criada com TGFABF</span></td>
                        </tr>
                        <tr>
                            <td>5</td>
                            <td>Não existia coluna Data Baixa CX</td>
                            <td><span class="badge badge-green">Adicionada DTBAIXACX</span></td>
                        </tr>
                        <tr>
                            <td>6</td>
                            <td>NOT EXISTS excluía erroneamente</td>
                            <td><span class="badge badge-green">Movido apenas para 1ª parte</span></td>
                        </tr>
                        <tr>
                            <td>7</td>
                            <td>CASE WHEN misturava lógicas diferentes</td>
                            <td><span class="badge badge-green">Separado por etapa</span></td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

    </div>

    <!-- FOOTER -->
    <footer class="footer">
        <p><strong>Documentação de Mudanças · Regime de Caixa · Sankhya ERP</strong></p>
        <p>Versão 2.0 Corrigida · Junho 2026</p>
        <p style="margin-top:0.75rem;font-size:0.75rem;color:#64748b;">
            Esta documentação apresenta todas as alterações realizadas na query original da tela Regime de Caixa,
            incluindo a separação em 3 etapas de extração conforme solicitado pelo cliente.
        </p>
    </footer>

</body>
</html>