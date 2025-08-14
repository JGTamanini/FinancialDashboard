# FinancialDashboard

Um sistema de controle financeiro pessoal que permite registrar, visualizar e analisar entradas e saídas de caixa a partir de um banco de dados SQLite
(posteriormente migrável para um banco em nuvem). O objetivo é oferecer insights rápidos e visuais para ajudar o usuário a organizar suas contas mensais, 
identificar tendências de gastos e planejar futuras compras.

Funcionalidades Principais
    1. Cadastro de entradas e saídas
        - Registro de valores, data, descrição, categoria, e no caso de saídas, método de pagamento.
        - Fontes de receita e categorias personalizáveis.
    2. Métricas e Análises
        - Gráficos mensais de receitas e despesas.
        - Percentual de cada categoria nos gastos.
        - Evolução de saldo ao longo do tempo.
    3. Previsões e Alertas (fase avançada)
        - Estimativa de gastos futuros com base em histórico.
        - Alertas para gastos que ultrapassem metas definidas.
    4. Interface e Experiência do Usuário
        - Interface visual (inicialmente CLI, depois GUI/web).
        - Exportação de relatórios para CSV/XLSX.
        - Temas de cores personalizáveis para gráficos e interface.

Checklist de Desenvolvimento
Fase 1 — Fundamentos e Estrutura
 - Organizar diretórios do projeto (src, data, docs, tests).
 - Criar banco de dados SQLite com tabelas:
    - transacoes (id, data, descricao, categoria, tipo, valor, metodo_pagamento).
    - categorias (id, nome, tipo).
 - Criar script Python para CRUD no banco.
 - Popular banco com dados fictícios para testes.
 - Implementar leitura e escrita em CSV/XLSX.

Fase 2 — Análise e Métricas
 - Criar consultas SQL para:
    - Total mensal de entradas e saídas.
    - Gastos por categoria.
    - Saldo acumulado.
 - Integrar consultas ao Python usando Pandas.
 - Implementar gráficos com Matplotlib/Seaborn.

Fase 3 — Interface do Usuário
 - Criar menu no console para cadastro, listagem e análise.
 - Implementar versão simples em Tkinter (GUI local) ou Streamlit (web).
 - Adicionar opção de exportar relatório completo.
 - Implementar personalização de cores e temas.

Fase 4 — Funcionalidades Avançadas
 - Criar módulo de previsão de gastos com base no histórico.
 - Adicionar sistema de alertas para metas.
 - Implementar backup automático do banco.
 - Migrar para banco em nuvem (Heroku/PostgreSQL ou Firebase).
