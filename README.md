<!DOCTYPE html>
<html lang="pt-BR" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Currículo Interativo - Daniele Cardoso Sales</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700;800&display=swap" rel="stylesheet">
    <!-- Chosen Palette: Warm Professional (bg-stone-50, text-stone-800, accent-amber-600) -->
    <!-- Application Structure Plan: A SPA (Single Page Application) com uma abordagem de "Jornada Profissional Interativa". A estrutura é desenhada para guiar o recrutador através de uma narrativa de crescimento, começando com um impacto imediato (o KPI de crescimento de 916%), seguido por uma visão geral das competências, uma linha do tempo interativa da carreira, um foco aprofundado no projeto de maior destaque, e finalizando com informações de contato. Esta estrutura foi escolhida por ser mais envolvente e memorável do que um CV estático, permitindo a exploração não-linear da experiência e focando nos resultados para maximizar o impacto. -->
    <!-- Visualization & Content Choices: 
        - Resumo (KPIs): Informar/Impactar -> Cartões de destaque com números grandes (916% de crescimento) usando HTML/Tailwind para capturar atenção imediata.
        - Competências: Organizar/Informar -> Cartões de habilidades com ícones (Unicode) para uma visualização rápida das áreas de domínio. Interação de hover sutil.
        - Trajetória Profissional: Mostrar Mudança/Explorar -> Linha do tempo vertical interativa (HTML/CSS/JS). Clicar em cada cargo revela detalhes, mantendo a interface limpa e focada.
        - Projeto Destaque ("Reputation Media"): Comparar/"Wow" Factor -> Gráfico de barras (Chart.js) para visualizar o crescimento massivo de receita. Isso transforma um número em uma história visual poderosa.
        - Contato: Agir -> Seção clara com links diretos para LinkedIn e e-mail.
        - Justificativa: A combinação de KPIs de alto impacto, visualização de habilidades, uma linha do tempo explorável e um gráfico de destaque cria uma experiência rica que comunica valor de forma muito mais eficaz do que apenas texto.
        - Library/Method: Chart.js para o gráfico. HTML/Tailwind/JS para o resto. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .chart-container {
            position: relative;
            height: 350px;
            width: 100%;
            max-width: 700px;
            margin: auto;
        }
        .timeline-item:before {
            content: '';
            position: absolute;
            left: 11px;
            top: 0;
            bottom: 0;
            width: 2px;
            background-color: #d6d3d1; /* stone-300 */
        }
        .timeline-item:last-child:before {
            display: none;
        }
        .timeline-dot {
            position: absolute;
            left: 0;
            top: 4px;
            height: 24px;
            width: 24px;
            border-radius: 50%;
            border: 4px solid #f5f5f4; /* stone-100 */
            background-color: #ca8a04; /* amber-600 */
            z-index: 10;
        }
    </style>
</head>
<body class="bg-stone-100 text-stone-800">

    <header id="header" class="bg-stone-100/80 backdrop-blur-md sticky top-0 z-50 shadow-sm">
        <nav class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                <div class="flex-shrink-0">
                    <h1 class="text-xl font-bold text-amber-600">Daniele C. Sales</h1>
                </div>
                <div class="hidden md:block">
                    <div class="ml-10 flex items-baseline space-x-4">
                        <a href="#summary" class="text-stone-600 hover:text-amber-600 px-3 py-2 rounded-md text-sm font-medium">Resumo</a>
                        <a href="#skills" class="text-stone-600 hover:text-amber-600 px-3 py-2 rounded-md text-sm font-medium">Competências</a>
                        <a href="#career" class="text-stone-600 hover:text-amber-600 px-3 py-2 rounded-md text-sm font-medium">Carreira</a>
                        <a href="#spotlight" class="text-stone-600 hover:text-amber-600 px-3 py-2 rounded-md text-sm font-medium">Projeto Destaque</a>
                        <a href="#contact" class="bg-amber-500 hover:bg-amber-600 text-white px-3 py-2 rounded-md text-sm font-medium">Contato</a>
                    </div>
                </div>
            </div>
        </nav>
    </header>

    <main class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-8">
        
        <section id="hero" class="text-center py-16">
            <h1 class="text-4xl md:text-5xl font-extrabold tracking-tight">
                <span class="block">Daniele Cardoso Sales</span>
                <span class="block text-amber-600 text-2xl md:text-3xl mt-2">Líder em Monetização Digital para Publishers</span>
            </h1>
            <p class="mt-4 max-w-2xl mx-auto text-lg text-stone-600">
                Especialista em AdTech e Publicidade Programática, transformando dados e tecnologia em crescimento de receita e inovação para publishers.
            </p>
        </section>

        <section id="summary" class="py-12">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold">Resumo Profissional</h2>
                <p class="mt-2 text-stone-600">Uma carreira de 15 anos focada em resultados e crescimento estratégico.</p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 text-center">
                <div class="bg-white p-8 rounded-lg shadow-md hover:shadow-xl transition-shadow duration-300">
                    <div class="text-5xl font-extrabold text-amber-600">+916%</div>
                    <h3 class="mt-3 text-xl font-bold">Crescimento de Receita</h3>
                    <p class="mt-2 text-stone-600">Aumento na receita anual de Ads liderando o projeto "Reputation Media" no Reclame Aqui.</p>
                </div>
                <div class="bg-white p-8 rounded-lg shadow-md hover:shadow-xl transition-shadow duration-300">
                    <div class="text-5xl font-extrabold text-amber-600">15</div>
                    <h3 class="mt-3 text-xl font-bold">Anos de Experiência</h3>
                    <p class="mt-2 text-stone-600">Sólida expertise na gestão estratégica de ecossistemas publicitários e monetização digital.</p>
                </div>
                <div class="bg-white p-8 rounded-lg shadow-md hover:shadow-xl transition-shadow duration-300">
                    <div class="text-5xl font-extrabold text-amber-600">🚀</div>
                    <h3 class="mt-3 text-xl font-bold">Inovação e Liderança</h3>
                    <p class="mt-2 text-stone-600">Criação de novos produtos e fluxos de receita, da ideação à implementação em múltiplos publishers.</p>
                </div>
            </div>
        </section>

        <section id="skills" class="py-12 bg-stone-200 rounded-lg">
             <div class="text-center mb-12">
                <h2 class="text-3xl font-bold">Principais Competências</h2>
                <p class="mt-2 text-stone-600">As ferramentas e estratégias que utilizo para gerar crescimento.</p>
            </div>
            <div class="grid grid-cols-2 md:grid-cols-4 gap-6 text-center">
                <div class="bg-white p-6 rounded-lg shadow-sm">
                    <span class="text-4xl">⚙️</span>
                    <h3 class="mt-4 font-bold">AdTech & Ad Servers</h3>
                    <p class="text-sm text-stone-600">Google Ad Manager, Prebid.js</p>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-sm">
                    <span class="text-4xl">📊</span>
                    <h3 class="mt-4 font-bold">Mídia Programática</h3>
                    <p class="text-sm text-stone-600">Open Auction, Deals, DMPs, DSPs</p>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-sm">
                    <span class="text-4xl">📈</span>
                    <h3 class="mt-4 font-bold">Análise e BI</h3>
                    <p class="text-sm text-stone-600">Google Analytics, BI Tools</p>
                </div>
                 <div class="bg-white p-6 rounded-lg shadow-sm">
                    <span class="text-4xl">🎯</span>
                    <h3 class="mt-4 font-bold">Gestão de Dados</h3>
                    <p class="text-sm text-stone-600">First-Party Data, Segmentação</p>
                </div>
            </div>
        </section>
        
        <section id="career" class="py-16">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold">Trajetória Profissional</h2>
                <p class="mt-2 text-stone-600">Navegue pela minha carreira. Clique em cada cargo para ver detalhes e conquistas.</p>
            </div>
            <div id="timeline-container" class="relative pl-8">
            </div>
        </section>

        <section id="spotlight" class="py-12">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-amber-600">Projeto Destaque: Reputation Media</h2>
                <p class="mt-2 text-stone-600 max-w-3xl mx-auto">Como a criação de um novo conceito de mídia no Reclame Aqui gerou um crescimento de receita sem precedentes e fortaleceu o posicionamento da marca no mercado.</p>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-lg">
                 <div class="chart-container">
                    <canvas id="growthChart"></canvas>
                </div>
            </div>
        </section>

        <section id="contact" class="py-16 text-center bg-stone-800 text-white rounded-lg">
            <h2 class="text-3xl font-bold">Vamos Conversar?</h2>
            <p class="mt-4 text-lg text-stone-300 max-w-xl mx-auto">Estou em busca de novos desafios e adoraria discutir como minha experiência em crescimento e monetização pode beneficiar sua empresa.</p>
            <div class="mt-8 flex justify-center items-center gap-6">
                <a href="mailto:dcardososales@gmail.com" class="bg-amber-500 hover:bg-amber-600 text-white font-bold py-3 px-6 rounded-lg transition-transform duration-300 hover:scale-105">
                    Enviar E-mail
                </a>
                <a href="https://www.linkedin.com/in/danielecsales" target="_blank" class="border-2 border-amber-500 text-amber-500 hover:bg-amber-500 hover:text-white font-bold py-3 px-6 rounded-lg transition-all duration-300">
                    Ver LinkedIn
                </a>
            </div>
        </section>
    </main>
    
    <footer class="text-center py-4 text-sm text-stone-500">
        <p>&copy; 2024 Daniele Cardoso Sales. Currículo Interativo desenvolvido com IA.</p>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const timelineContainer = document.getElementById('timeline-container');
            
            const careerData = [
                {
                    company: 'Reclame Aqui',
                    period: 'Abr/2022 - Jul/2025',
                    title: 'Especialista Sênior AdTech, AdOps e Programmatic Sell Side',
                    details: [
                        'Liderança na gestão estratégica e técnica de ecossistemas publicitários, incluindo implementação e otimização de Ad Servers (Google Ad Manager), soluções de header bidding e estratégias de segmentação de dados first-party.',
                        '<strong>Liderança na concepção e desenvolvimento do conceito e formato "Reputation Media", resultando em um crescimento de 916% na receita anual de Ads e gerando novas fontes de receita e inovação no mercado.</strong>',
                        'Definição e acompanhamento de OKRs, priorização de backlog e atuação direta com equipes de Desenvolvimento, Produto e Gerência de Projetos, garantindo a entrega de soluções de monetização de alta performance.',
                        'Expertise em otimização de campanhas programáticas e desenvolvimento de novos produtos publicitários, alinhando resultados de alta performance às necessidades comerciais e à experiência do usuário.'
                    ]
                },
                {
                    company: 'Canal Rural',
                    period: 'Jul/2021 - Mar/2022',
                    title: 'Especialista em Mídia Programática',
                    details: [
                        'Liderança na implementação técnica de Ad Servers (Google Ad Manager), Prebid.js e DMPs.',
                        'Gestão de campanhas publicitárias em diversas modalidades (diretas, programáticas e open auction), com foco em otimização de resultados.',
                        'Definição e otimização de floors de leilão, produtos de mídia e formatos (display, vídeo e nativo), <strong>contribuindo para um aumento significativo da receita.</strong>',
                        'Colaboração ativa na criação do Mídia Kit e na definição de tabelas de preços, suportando a área comercial.'
                    ]
                },
                {
                    company: 'CNN Brasil',
                    period: 'Mar/2020 - Jul/2021',
                    title: 'Analista de Operações Comerciais Sênior',
                    details: [
                         'Responsável pela implementação inicial do AdServer (Google Ad Manager), estabelecendo a infraestrutura de monetização <strong>e garantindo a escalabilidade para o crescimento da receita.</strong>',
                         'Supervisão de campanhas diretas e programáticas, garantindo alta performance e entrega de resultados.',
                         'Desenvolvimento de relacionamentos estratégicos com parceiros tecnológicos e implementação de melhorias contínuas no inventário e campanhas.'
                    ]
                },
                {
                    company: 'Editora Abril',
                    period: 'Set/2017 - Fev/2020',
                    title: 'AdOps - Digital Marketing',
                    details: [
                        'Otimização de campanhas programáticas em diversos formatos (display, vídeo, mobile e nativos).',
                        'Validação e configuração de tags, retargeting e segmentação de dados (first-party e third-party).',
                        'Criação de relatórios detalhados e apresentação de insights para clientes, <strong>otimizando a receita em Ad Exchange.</strong>'
                    ]
                },
                {
                    company: 'UOL - Universo Online',
                    period: 'Nov/2011 - Abr/2017',
                    title: 'Account Manager',
                    details: [
                         'Gestão de campanhas e inventários de publicidade digital, com foco na <strong>otimização de KPIs como CTR, CPA, ROI e viewability, garantindo resultados expressivos em termos de performance e receita.</strong>',
                         'Atuação no planejamento estratégico de campanhas de performance e awareness, garantindo resultados expressivos.',
                         'Colaboração com equipes comerciais para propostas, upselling e soluções de mídia personalizadas.'
                    ]
                }
            ];

            careerData.forEach(job => {
                const item = document.createElement('div');
                item.className = 'timeline-item relative pb-8';

                item.innerHTML = `
                    <div class="timeline-dot"></div>
                    <div class="ml-10">
                        <button class="w-full text-left focus:outline-none">
                            <div class="flex justify-between items-center">
                                <h3 class="text-lg font-bold text-stone-900">${job.title}</h3>
                                <span class="text-sm font-medium text-amber-600">${job.period}</span>
                            </div>
                            <p class="text-md text-stone-600">${job.company}</p>
                        </button>
                        <div class="details-content overflow-hidden max-h-0 transition-all duration-500 ease-in-out mt-2">
                            <ul class="list-disc pl-5 space-y-2 text-stone-700">
                                ${job.details.map(d => `<li>${d}</li>`).join('')}
                            </ul>
                        </div>
                    </div>
                `;
                timelineContainer.appendChild(item);
            });

            timelineContainer.addEventListener('click', (e) => {
                const button = e.target.closest('button');
                if (button) {
                    const content = button.nextElementSibling;
                    if (content.style.maxHeight && content.style.maxHeight !== '0px') {
                        content.style.maxHeight = '0px';
                    } else {
                        content.style.maxHeight = content.scrollHeight + 'px';
                    }
                }
            });

            const ctx = document.getElementById('growthChart').getContext('2d');
            new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: ['Receita Inicial', 'Receita Pós "Reputation Media"'],
                    datasets: [{
                        label: 'Crescimento de Receita de Ads',
                        data: [100, 1016], // Representing 100% base and 916% growth on top
                        backgroundColor: [
                            'rgba(214, 211, 209, 0.6)', // stone-300
                            'rgba(202, 138, 4, 0.6)'    // amber-600
                        ],
                        borderColor: [
                            'rgba(168, 162, 158, 1)',
                            'rgba(180, 83, 9, 1)'
                        ],
                        borderWidth: 1
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    scales: {
                        y: {
                            beginAtZero: true,
                            ticks: {
                                callback: function(value) {
                                    return value + '%';
                                }
                            }
                        }
                    },
                    plugins: {
                        legend: {
                            display: false
                        },
                        tooltip: {
                             callbacks: {
                                label: function(context) {
                                    if (context.dataIndex === 0) return ' Base de Receita: 100%';
                                    return ' Crescimento de +916%';
                                }
                            }
                        }
                    }
                }
            });
        });
    </script>
</body>
</html>
