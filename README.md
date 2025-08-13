<!DOCTYPE html>
<html lang="pt-BR" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mercado S.E.R - Apresentação</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&family=Arial:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        /* Estilo para a barra de rolagem */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #f1f1f1;
        }
        ::-webkit-scrollbar-thumb {
            background: #888;
            border-radius: 10px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #555;
        }
        /* Estilos para o Carrossel */
        .carousel-container {
            position: relative;
            overflow: hidden;
        }
        .carousel-track {
            display: flex;
            transition: transform 0.5s ease-in-out;
        }
        .carousel-slide {
            min-width: 100%;
            box-sizing: border-box;
        }
        /* Estilo para o texto em degradê */
        .gradient-text {
            background: -webkit-linear-gradient(45deg, #4f46e5, #c026d3);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-family: 'Arial', sans-serif;
        }
        /* Estilos para o Menu Rápido (FAB) */
        #quick-nav-modal {
            transition: opacity 0.3s ease-in-out;
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-800">
    <!-- Tela de Boas-Vindas (Splash Screen) -->
    <section id="splash" class="h-screen flex flex-col justify-center items-center bg-white">
        <h1 class="text-6xl md:text-8xl font-bold gradient-text text-center">
            Bem-vindo ao Mercado
        </h1>
        <button id="start-btn" class="mt-10 bg-indigo-600 text-white font-bold py-4 px-10 rounded-lg shadow-lg hover:bg-indigo-700 transition duration-300 transform hover:scale-105">
            Começar
        </button>
    </section>
    <!-- Conteúdo Principal do Site (Inicialmente Oculto) -->
    <div id="main-content" class="hidden">
        <!-- Cabeçalho e Navegação -->
        <header class="bg-white/80 backdrop-blur-lg shadow-md sticky top-0 z-40">
            <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
                <a href="#splash" class="flex items-center space-x-2">
                    <!-- Logo SVG -->
                    <svg width="40" height="40" viewBox="0 0 200 200" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <circle cx="100" cy="100" r="95" fill="url(#logo-gradient)"/>
                        <defs>
                            <linearGradient id="logo-gradient" x1="0" y1="0" x2="200" y2="200" gradientUnits="userSpaceOnUse">
                            <stop stop-color="#6366F1"/>
                            <stop offset="1" stop-color="#A855F7"/>
                            </linearGradient>
                        </defs>
                        <text x="50%" y="50%" dominant-baseline="middle" text-anchor="middle" font-family="Arial, sans-serif" font-size="80" font-weight="bold" fill="white">
                            SER
                        </text>
                    </svg>
                    <span class="text-2xl font-bold text-gray-900">Mercado S.E.R</span>
                </a>
                <div class="hidden md:flex space-x-6">
                    <a href="#empreendedores" class="text-gray-600 hover:text-indigo-600 transition duration-300">Os Empreendedores</a>
                    <a href="#projeto" class="text-gray-600 hover:text-indigo-600 transition duration-300">O Projeto</a>
                </div>
                <!-- Menu Mobile -->
                <div class="md:hidden">
                    <button id="menu-btn" class="text-gray-600 hover:text-indigo-600 focus:outline-none">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path></svg>
                    </button>
                </div>
            </nav>
            <!-- Links do Menu Mobile -->
            <div id="menu" class="hidden md:hidden">
                <a href="#empreendedores" class="block py-2 px-6 text-sm text-gray-600 hover:bg-indigo-50">Os Empreendedores</a>
                <a href="#projeto" class="block py-2 px-6 text-sm text-gray-600 hover:bg-indigo-50">O Projeto</a>
            </div>
        </header>
        <main>
            <!-- Seção dos Empreendedores -->
            <section id="empreendedores" class="py-20 bg-gray-50">
                <div class="container mx-auto px-6">
                    <div class="text-center mb-16">
                        <h2 class="text-3xl md:text-4xl font-bold text-gray-900">Nossos Fundadores</h2>
                        <p class="text-md text-gray-600 mt-2">As mentes por trás da inovação.</p>
                    </div>
                    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
                        <!-- Card Sabrinna Louise -->
                        <div class="bg-white rounded-xl shadow-lg p-8 text-center transform hover:-translate-y-2 transition duration-500">
                            <img class="w-32 h-32 rounded-full mx-auto mb-4 border-4 border-indigo-200" src="https://i.postimg.cc/1zHxtvHV/Sabrinna.jpg" alt="Foto de Sabrinna Louise">
                            <h3 class="text-2xl font-bold text-gray-900">Sabrinna Louise</h3>
                            <p class="text-indigo-500 font-medium mt-1">Especialista em Segurança em Nuvem</p>
                            <p class="text-gray-600 mt-4 text-sm">
                                Sabrinna projeta e implementa a arquitetura de segurança, protegendo nossos dados e infraestrutura na nuvem contra ameaças, garantindo conformidade e a integridade dos ativos digitais.
                            </p>
                        </div>
                        <!-- Card Emanuelle Christinie -->
                        <div class="bg-white rounded-xl shadow-lg p-8 text-center transform hover:-translate-y-2 transition duration-500">
                            <img class="w-32 h-32 rounded-full mx-auto mb-4 border-4 border-indigo-200" src="https://i.postimg.cc/LX6cZjCC/Emanuele.jpg" alt="Foto de Emanuelle Christinie">
                            <h3 class="text-2xl font-bold text-gray-900">Emanuelle Christinie</h3>
                            <p class="text-indigo-500 font-medium mt-1">Especialista em I.A</p>
                            <p class="text-gray-600 mt-4 text-sm">
                               Especialista em Inteligência Artificial, Emanuelle desenvolve algoritmos de machine learning e modelos preditivos para extrair insights e automatizar decisões complexas no sistema.
                            </p>
                        </div>
                        <!-- Card Renan Félix -->
                        <div class="bg-white rounded-xl shadow-lg p-8 text-center transform hover:-translate-y-2 transition duration-500">
                            <img class="w-32 h-32 rounded-full mx-auto mb-4 border-4 border-indigo-200" src="https://i.postimg.cc/507Z5jDx/Renan-felix.jpg" alt="Foto de Renan Félix">
                            <h3 class="text-2xl font-bold text-gray-900">Renan Félix</h3>
                            <p class="text-indigo-500 font-medium mt-1">Especialista em Criação de Robôs</p>
                            <p class="text-gray-600 mt-4 text-sm">
                                Focado na automação de processos (RPA), Renan cria robôs de software que executam tarefas repetitivas, otimizando a eficiência operacional e integrando diferentes sistemas de forma automática.
                            </p>
                        </div>
                    </div>
                </div>
            </section>
            <!-- Seção do Projeto Atualizada -->
            <section id="projeto" class="py-20 bg-white">
                <div class="container mx-auto px-6">
                    <div class="text-center mb-16">
                        <h2 class="text-3xl md:text-4xl font-bold text-gray-900">Nossa Arquitetura Tecnológica</h2>
                        <p class="text-md text-gray-600 mt-2">Entenda as camadas que impulsionam o nosso Mercado S.E.R.</p>
                    </div>
                    <!-- Etapa 1: A Base de Tudo -->
                    <div id="etapa1" class="pt-16 -mt-16">
                        <div class="flex flex-col md:flex-row items-center mb-20">
                            <div class="md:w-1/2 p-4 text-center md:text-left">
                                <span class="text-indigo-600 font-semibold">ETAPA 1</span>
                                <h3 class="text-2xl font-bold text-gray-900 my-2">A Base de Tudo: PostgreSQL</h3>
                                <p class="text-gray-600">
                                    Escolhemos o <strong>PostgreSQL</strong> como nosso sistema de gerenciamento de banco de dados. Ele é conhecido por sua <strong>confiabilidade, robustez e performance</strong>. No nosso projeto, ele é o cofre seguro onde todos os dados importantes são armazenados, organizados e mantidos com integridade.
                                </p>
                            </div>
                            <div class="md:w-1/2 p-4">
                                <img src="https://i.postimg.cc/ZR8LZQFX/Elefante-Tecnol-gico-com-Postgre-SQL.png" alt="Diagrama do Banco de Dados PostgreSQL" class="rounded-lg shadow-lg w-full">
                            </div>
                        </div>
                    </div>
                    <!-- Etapa 2: A Inteligência da Operação -->
                    <div id="etapa2" class="pt-16 -mt-16">
                        <div class="flex flex-col md:flex-row-reverse items-center mb-20">
                            <div class="md:w-1/2 p-4 text-center md:text-left">
                                 <span class="text-indigo-600 font-semibold">ETAPA 2</span>
                                <h3 class="text-2xl font-bold text-gray-900 my-2">A Inteligência da Operação: Python</h3>
                                <p class="text-gray-600">
                                    <strong>Python</strong> é a linguagem que serve como o cérebro do nosso sistema. Com sua sintaxe simples e o poder de bibliotecas como <code>psycopg2</code> para conexão e <code>pandas</code> para análise, criamos aplicações que se comunicam com o banco de dados. O Python é responsável por <strong>inserir, consultar e processar os dados</strong> de forma inteligente.
                                </p>
                            </div>
                            <div class="md:w-1/2 p-4">
                                <img src="https://i.postimg.cc/Kj24hGZh/PYYYYYTHOOOOOOON.jpgDDS" alt="Exemplo de código Python" class="rounded-lg shadow-lg w-full">
                            </div>
                        </div>
                    </div>
                    <!-- Etapa 3: Estrutura das Tabelas -->
                    <div id="etapa3" class="pt-16 -mt-16 mb-20">
                        <div class="text-center mb-10">
                            <span class="text-indigo-600 font-semibold">ETAPA 3</span>
                            <h3 class="text-2xl font-bold text-gray-900 my-2">Organizando a Informação: As Tabelas</h3>
                            <p class="text-gray-600 max-w-2xl mx-auto">
                                Os dados são organizados em tabelas relacionais para garantir consistência e facilitar as consultas.
                            </p>
                        </div>
                        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                            <div class="bg-gray-100 p-6 rounded-lg shadow-inner">
                                <h4 class="font-bold text-lg text-indigo-800">Clientes</h4>
                                <ul class="mt-2 text-gray-700 list-disc list-inside">
                                    <li><code>id_cliente</code> (PK)</li>
                                    <li><code>nome</code></li>
                                    <li><code>email</code></li>
                                    <li><code>preco</code></li>
                                    <li><code>CPF</code></li>
                                    <li><code>id_categoria</code></li>
                                </ul>
                            </div>
                            <div class="bg-gray-100 p-6 rounded-lg shadow-inner">
                                <h4 class="font-bold text-lg text-indigo-800">ItensVenda</h4>
                                <ul class="mt-2 text-gray-700 list-disc list-inside">
                                    <li><code>id_item</code> (PK)</li>
                                    <li><code>nome_item</code></li>
                                    <li><code>preco</code></li>
                                    <li><code>quantidade</code></li>
                                    <li><code>venda_id</code></li>
                                    <li><code>estoque</code></li>
                                </ul>
                            </div>
                            <div class="bg-gray-100 p-6 rounded-lg shadow-inner">
                                <h4 class="font-bold text-lg text-indigo-800">Vendas</h4>
                                <ul class="mt-2 text-gray-700 list-disc list-inside">
                                    <li><code>id_venda</code> (PK)</li>
                                    <li><code>id_cliente</code> (FK)</li>
                                    <li><code>id_produto</code> (FK)</li>
                                    <li><code>data_venda</code></li>
                                </ul>
                            </div>
                             <div class="bg-gray-100 p-6 rounded-lg shadow-inner">
                                <h4 class="font-bold text-lg text-indigo-800">Pedidos</h4>
                                <ul class="mt-2 text-gray-700 list-disc list-inside">
                                    <li><code>id_pedido</code> (PK)</li>
                                    <li><code>cliente_id</code></li>
                                    <li><code>data_pedido</code></li>
                                    <li><code>valor_total</code></li>
                                    <li><code>status</code></li>
                                </ul>
                            </div>
                             <div class="bg-gray-100 p-6 rounded-lg shadow-inner">
                                <h4 class="font-bold text-lg text-indigo-800">categorias</h4>
                                <ul class="mt-2 text-gray-700 list-disc list-inside">
                                    <li><code>id_categoria</code> (PK)</li>
                                    <li><code>nome</code></li>
                                </ul>
                            </div>
                             <div class="bg-gray-100 p-6 rounded-lg shadow-inner">
                                <h4 class="font-bold text-lg text-indigo-800">Produtos</h4>
                                <ul class="mt-2 text-gray-700 list-disc list-inside">
                                    <li><code>id_Produto</code> (PK)</li>
                                    <li><code>id_categoria</code></li>
                                    <li><code>preco</code></li>
                                    <li><code>quantidade</code></li>
                                </ul>
                            </div>
                        </div>
                    </div>
                    <!-- Etapa 4: Carrossel Visual -->
                    <div id="etapa4" class="pt-16 -mt-16 text-center mb-20">
                        <span class="text-indigo-600 font-semibold">ETAPA 4</span>
                        <h3 class="text-2xl font-bold text-gray-900 my-2">Galeria Visual do Projeto</h3>
                        <div id="carousel" class="max-w-3xl mx-auto mt-8 bg-white rounded-lg shadow-xl carousel-container">
                            <div class="carousel-track">
                                <div class="carousel-slide p-8">
                                    <h4 class="font-bold text-xl mb-4">Diagrama de Entidade e Relacionamento</h4>
                                    <img src="https://i.postimg.cc/mZmNNJV2/Chat-GPT-Image-11-08-2025-21-12-58.png" class="rounded-md w-full" alt="Diagrama de Entidade e Relacionamento">
                                </div>
                                <div class="carousel-slide p-8">
                                    <h4 class="font-bold text-xl mb-4">Código: Conexão Python</h4>
                                    <img src="https://i.postimg.cc/VsSYGcg7/Captura-de-tela-2025-08-11-185409.png" class="rounded-md w-full" alt="Snippet de código Python">
                                </div>
                                <div class="carousel-slide p-8">
                                    <h4 class="font-bold text-xl mb-4">Consulta SQL</h4>
                                    <img src="https://i.postimg.cc/mgPJRbcq/python-pra-sql.webp" class="rounded-md w-full" alt="Snippet de código SQL">
                                </div>
                            </div>
                            <button id="prevBtn" class="absolute top-1/2 left-4 transform -translate-y-1/2 bg-white/50 hover:bg-white p-2 rounded-full shadow-md transition">
                                &#10094;
                            </button>
                            <button id="nextBtn" class="absolute top-1/2 right-4 transform -translate-y-1/2 bg-white/50 hover:bg-white p-2 rounded-full shadow-md transition">
                                &#10095;
                            </button>
                        </div>
                    </div>
                    <!-- Etapa 5: Funções em Python -->
                    <div id="etapa5" class="pt-16 -mt-16">
                        <div class="text-center mb-10">
                            <span class="text-indigo-600 font-semibold">ETAPA 5</span>
                            <h3 class="text-2xl font-bold text-gray-900 my-2">Principais Funções em Ação</h3>
                            <p class="text-gray-600 max-w-2xl mx-auto">
                                Veja com que perguntas o Python executa tarefas essenciais para o funcionamento do nosso sistema.
                            </p>
                        </div>
                        <div class="space-y-16">
                            <!-- Função 1 -->
                            <div class="flex flex-col md:flex-row items-center gap-8">
                                <img src="https://i.postimg.cc/h47NH4d5/Captura-de-tela-2025-08-11-195533.png" class="md:w-1/2 rounded-lg shadow-lg w-full">
                                <div class="md:w-1/2 text-left">
                                    <h4 class="text-xl font-bold text-gray-800 mb-2">Perguntas</h4>
                                    <p class="text-gray-600">Esta função é responsável por trazer informações, status, quantidade de produtos ou até quem comprou tal produto em que categoria, por exemplo. </p>
                                </div>
                            </div>
                            </div>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
        </main>
        <!-- Rodapé -->
        <footer class="bg-gray-800 text-white py-8">
