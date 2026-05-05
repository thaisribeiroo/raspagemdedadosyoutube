# 📺 Blanck The Series — Análise de Dados com Python

Análise completa de uma playlist do YouTube utilizando a **YouTube Data API v3**, com coleta de dados, processamento de comentários, análise de sentimento e visualizações interativas.

---

## 📌 Sobre o Projeto

Este projeto coleta e analisa dados da série **Blanck The Series** disponível no YouTube. O objetivo é extrair insights sobre o desempenho dos episódios, o comportamento do público e os padrões de engajamento a partir dos comentários e métricas dos vídeos.

---

## 🔧 Tecnologias Utilizadas

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge&logo=python&logoColor=white)

**Bibliotecas principais:**
- `requests` — consumo da YouTube Data API v3
- `pandas` — manipulação e análise dos dados
- `matplotlib` + `seaborn` — visualizações gráficas
- `langdetect` — detecção de idioma dos comentários
- `networkx` — geração de grafos de co-ocorrência de termos

---

## 📂 Estrutura do Projeto

```
Blanck_the_series/
├── Blanck_the_series_.ipynb   ← Notebook principal com toda a análise
└── youtube_dados.csv          ← Dataset gerado pela coleta via API
```

---

## 🔍 Etapas da Análise

### 1. 📡 Coleta de Dados via API
- Extração de todos os vídeos da playlist via `playlistItems`
- Coleta de métricas por vídeo: título, views, likes, duração, quantidade de comentários
- Download de até 1.000 comentários por vídeo com paginação automática
- Filtro de comentários em **português** com `langdetect`
- Exportação para `youtube_dados.csv`

### 2. 📊 Análise Exploratória
- Total de views ao longo do tempo (gráfico de linhas)
- Views, Likes e Comentários por episódio (gráfico de barras agrupado)
- Top 5 episódios por engajamento (score combinado de Likes + Comentários)
- Top 5 vídeos com mais comentários

### 3. 💬 Análise de Sentimento
- Classificação dos comentários em **Positivo**, **Negativo** e **Neutro**
- Geração de grafos de co-ocorrência de termos por sentimento
- Visualização com `networkx` e `spring_layout`

---

## 📈 Exemplos de Visualizações

| Análise | Descrição |
|---|---|
| 📉 Views ao longo do tempo | Evolução das visualizações por data de publicação |
| 🏆 Top 5 por engajamento | Episódios com maior score (Likes + Comentários × 5) |
| 💬 Top 5 por comentários | Episódios que mais geraram discussão |
| 🌐 Grafo de co-ocorrência | Relação entre termos nos comentários por sentimento |

---

## ▶️ Como Executar

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/blanck-the-series-analysis.git
```

2. Instale as dependências:
```bash
pip install requests pandas matplotlib seaborn langdetect networkx
```

3. Adicione sua chave da YouTube Data API no notebook:
```python
API_KEY = "sua_chave_aqui"
```

4. Execute o notebook `Blanck_the_series_.ipynb` célula por célula.

> ⚠️ **Atenção:** Não compartilhe sua API Key publicamente. Considere usar variáveis de ambiente.

---

## 📬 Contato

- 💼 [LinkedIn](#) ← *adicione seu link aqui*
- 📧 *seu@email.com*

---

> *Projeto desenvolvido para estudo e prática de análise de dados com Python e APIs públicas.* 🚀
