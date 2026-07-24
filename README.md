# 🦜 Assistente de Análise de Dados com IA

Assistente interativo construído com **Streamlit** e **Langchain** que permite explorar, analisar e visualizar dados de arquivos CSV usando linguagem natural, com respostas geradas por um agente de IA (via Groq).

## 🌐 Acesse o app online

🔗 [Clique aqui para acessar o app](https://datamind-grzyb.streamlit.app/)

## ✨ Funcionalidades

- **📁 Upload de arquivos CSV**: carregue seus dados diretamente na interface.
- **📄 Relatório de informações gerais**: dimensão do DataFrame, nomes e tipos das colunas, contagem de dados nulos e duplicados, além de sugestões de tratamentos e análises adicionais.
- **📄 Relatório de estatísticas descritivas**: média, mediana, desvio padrão, mínimo, máximo, identificação de possíveis outliers.
- **🔎 Perguntas sobre os dados**: faça perguntas em português como *"Qual é a média da coluna X?"* ou *"Quantos registros existem para cada categoria da coluna Y?"*.
- **📊 Geração automática de gráficos**: crie visualizações a partir de perguntas em linguagem natural, como *"Crie um gráfico da média de tempo de entrega por clima."*.
- **📥 Download de relatórios** gerados em formato Markdown.

## 🛠️ Tecnologias utilizadas

- [Streamlit](https://streamlit.io/) — interface web interativa
- [Langchain](https://www.langchain.com/) — orquestração do agente (ReAct)
- [langchain-groq](https://pypi.org/project/langchain-groq/) — integração com a API da Groq
- [Pandas](https://pandas.pydata.org/) — manipulação e análise de dados
- Modelo de linguagem: `llama-3.3-70b-versatile` (via Groq)

## 📂 Estrutura do projeto

```
.
├── app.py              # Aplicação principal (interface Streamlit e orquestração do agente)
├── ferramentas.py      # Definição das ferramentas (tools) usadas pelo agente
├── requirements.txt    # Dependências do projeto
└── README.md
```

## ✅ Pré-requisitos

- Python 3.9+
- Uma chave de API da [Groq](https://console.groq.com/)

## 🚀 Instalação

1. Clone o repositório:

```bash
git clone <url-do-repositorio>
cd <nome-da-pasta>
```

2. Crie e ative um ambiente virtual (opcional, mas recomendado):

```bash
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
```

3. Instale as dependências a partir do `requirements.txt`:

```bash
pip install -r requirements.txt
```

4. Configure a variável de ambiente com sua chave da Groq no arquivo `.env` (já presente no projeto, mas não versionado por segurança):

```env
GROQ_API_KEY=sua-chave-aqui
```

## ▶️ Como executar

```bash
streamlit run app.py
```

O aplicativo abrirá automaticamente no navegador (geralmente em `http://localhost:8501`).

## 📖 Como usar

1. Faça upload de um arquivo CSV na tela inicial.
2. Visualize as primeiras linhas do DataFrame carregado.
3. Utilize os botões de **ações rápidas** para gerar relatórios automáticos (informações gerais ou estatísticas descritivas).
4. Faça perguntas livres sobre os dados na seção **"Perguntas sobre os dados"**.
5. Gere gráficos automaticamente descrevendo o que deseja visualizar na seção **"Criar gráfico com base em uma pergunta"**.
6. Baixe os relatórios gerados em formato `.md` usando os botões de download.
