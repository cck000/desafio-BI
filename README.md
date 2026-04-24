# 📈 Predição de Captação Líquida em Fundos de Ações (Top-Decile)

Este repositório contém o pipeline completo de ponta a ponta (ETL, Engenharia de Features, Modelagem e Validação) para prever a captação líquida futura de fundos de investimento da classe "Ações". O estudo utiliza dados públicos da Comissão de Valores Mobiliários (CVM), já adaptados à instrução RCVM 175.

O objetivo do modelo é identificar fundos com alta probabilidade de figurar no decil superior (Top-Decile) de captação líquida nos próximos 21 dias úteis. Esta inteligência permite direcionar esforços comerciais e focar a distribuição B2B nos produtos com maior tração de mercado.

---

## 📂 Estrutura do Repositório

O projeto foi intencionalmente consolidado em um único Jupyter Notebook para facilitar a reprodutibilidade e a leitura do fluxo lógico.

├── desafio.ipynb           # Notebook central com o pipeline Fim-a-Fim
├── requirements.txt        # Dependências do projeto
├── dossie.pdf              # Documento detalhado com análises e justificativas
└── README.md               # Este arquivo


## ⚙️ Pré-requisitos e Instalação

Para garantir a execução correta, recomenda-se o uso do Python 3.13+.

1. Clone este repositório
2. Crie e ative um ambiente virtual:
    python -m venv venv
        No Windows:
            venv\Scripts\activate
        No Linux/Mac:
            source venv/bin/activate

3. Instale as dependências essenciais:
    pip install -r requirements.txt

## 🚀 Como Executar o Pipeline (Fim-a-Fim)

1. Inicie o ambiente do Jupyter:
    jupyter notebook
2. Abra o arquivo `desafio.ipynb`
3. No menu superior, clique em Kernel > Restart & Run All (ou execute as células sequencialmente).

## 📊Principais Resultados

* Métrica Principal (PR-AUC): 0.3405 (Superando de forma robusta a linha de base aleatória de ~0.09).

* Métrica Secundária (ROC-AUC): 0.7834.

* Insights de Negócio: A análise de Feature Importance revelou que o tamanho estrutural (LOG_PL) e a aversão do investidor à oscilação recente (VOL_63D) são determinantes mais fortes para a atração de novo capital do que retornos de curtíssimo prazo.

Para um aprofundamento nas justificativas estatísticas, limitações da amostra e próximos passos, consulte *dossie.pdf*