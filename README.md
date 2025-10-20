# 📊 Sistema de Gestão de Liderança (Leadership Management System)

Este é um sistema de gestão de liderança em **página única (Single-Page Application - SPA)**, desenvolvido puramente com **HTML, CSS e JavaScript Vanilla**. Ele utiliza o `localStorage` do navegador para armazenar todos os dados de forma persistente, permitindo a avaliação, o acompanhamento e o registro de ocorrências de líderes em um período específico.

## 🚀 Funcionalidades Principais

O sistema é dividido em abas principais, cada uma com um propósito de gestão:

### 📋 1. Ocorrências (Registro Diário)
* **Registro Rápido:** Permite registrar ocorrências (positivas e negativas) para líderes específicos em uma data definida.
* **Tipos de Ocorrência:** Suporta diversos tipos de indicadores com pesos e limites configuráveis (ex: Reclamação Pós Venda, Etiqueta Cancelada, Assertividade da Equipe, Faltas, Advertências, Notas de Limpeza, Relacionamento com Supervisor, etc.).
* **Acompanhamento:** Visualização imediata das ocorrências registradas no dia.

### 📈 2. Resultado (Avaliação Individual)
* **Pontuação Final:** Calcula a performance do líder em uma escala de 0 a 100 pontos, subtraindo penalidades das ocorrências registradas.
* **Filtros de Período:** Permite selecionar o resultado por mês ou por ano.
* **Detalhamento:** Apresenta um *feedback* detalhado de todas as perdas de pontos e um resumo das ocorrências que geraram penalidade no período.

### 🥇 3. Comparativo (Ranking)
* **Gráfico de Barras:** Visualização gráfica da pontuação de todos os líderes em um determinado período (mês ou anual).
* **Classificação:** Classifica os líderes em categorias (Excelente, Bom, Regular, Ruim, Crítico) e os exibe em um *grid* de cartões.
* **Tabela Detalhada:** Apresenta um ranking com os principais indicadores de cada líder (pontuação, classificação, total de ocorrências).
* **Exportação:** Funcionalidade para exportar o relatório (incluindo o gráfico e a tabela) como **PDF (Imagem de Alta Resolução)** e a tabela como **Excel/CSV**.

### 📚 4. Histórico e Manutenção
* **Busca Avançada:** Filtra todas as ocorrências por Líder, Período (Mês/Ano ou Todo o Período), e Tipo de Ocorrência.
* **Backup e Restauração:** Permite fazer *backup* de todos os dados do sistema em um arquivo JSON local e restaurá-lo, garantindo a segurança das informações.
* **Limpeza Total:** Opção de limpar todos os dados armazenados no navegador (com confirmação de segurança).

### 👥 Gestão de Líderes (Modal)
* Permite cadastrar, editar e remover líderes da base de dados.
* Ao editar ou remover, o sistema garante a integridade dos dados, atualizando ou excluindo as ocorrências históricas relacionadas ao líder.

## ⚙️ Tecnologias Utilizadas

Este projeto é uma aplicação *front-end* pura, sem dependências de servidor.

| Tecnologia | Finalidade |
| :--- | :--- |
| **HTML5 & CSS3** | Estrutura e Estilização (Utiliza um sistema de *design* similar ao Material Design). |
| **JavaScript Vanilla** | Toda a lógica de gestão, persistência de dados e manipulação do DOM. |
| **LocalStorage** | Persistência e armazenamento de todos os dados (Líderes, Ocorrências, Configurações). |
| **Chart.js** | Geração dos gráficos comparativos. |
| **jsPDF & jsPDF-autotable** | Criação e exportação de relatórios em formato PDF (Tabela). |
| **html2canvas** | Criação de imagem (*screenshot*) do conteúdo para exportação PDF de alta resolução. |
| **Font Awesome** | Ícones utilizados na interface do usuário. |
| **Google Fonts (Roboto)** | Tipografia da aplicação. |

## 📦 Como Executar

Como esta é uma aplicação em página única baseada em *local storage*, não é necessário um servidor.

1.  **Clone ou baixe** este repositório.
2.  Abra o arquivo `index.html` diretamente no seu navegador (Chrome, Firefox, Edge, etc.).
3.  O sistema estará pronto para uso. Os dados serão salvos automaticamente no seu navegador.

## ⚠️ Observação sobre Dados

Todos os dados (líderes, ocorrências e configurações de pontuação) são armazenados localmente no seu navegador utilizando o `localStorage`.
* Se você limpar o cache/dados do seu navegador, os dados serão perdidos.
* É altamente recomendável utilizar a função **Fazer Backup (JSON)** na aba **Histórico** regularmente para salvar seus dados externamente.