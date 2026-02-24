# 🎮 Video Game Sales Analysis — Exploratory Data Analysis with Python

Análise exploratória de dados históricos de vendas de videogames globais para identificar padrões de sucesso por plataforma, gênero e região, com testes estatísticos de hipóteses.

📓 **[Ver notebook no nbviewer](https://nbviewer.org/github/mauroroc/sprint6/blob/main/projeto.ipynb)**

---

## 📌 Sobre o Projeto

Análise realizada sob o contexto de uma loja fictícia de videogames (**Ice**) que opera globalmente. O objetivo é identificar quais fatores determinam o sucesso comercial de um jogo — plataforma, gênero, região e classificação etária — para subsidiar decisões de planejamento de campanhas publicitárias para 2017, com base em dados históricos até 2016.

---

## 🔍 Etapas da Análise

**Etapa 1 — Carregamento e inspeção dos dados**
- Dataset com 16.715 registros e 11 colunas
- Colunas: `name`, `platform`, `year_of_release`, `genre`, `na_sales`, `eu_sales`, `jp_sales`, `other_sales`, `critic_score`, `user_score`, `rating`

**Etapa 2 — Pré-processamento**
- Padronização de nomes de colunas (snake_case)
- Tratamento de valores ausentes em `year_of_release`, `critic_score`, `user_score` e `rating`
- Criação da coluna `total_sales` com a soma de vendas globais

**Etapa 3 — Análise Exploratória**
- Evolução de lançamentos e vendas por ano
- Identificação do período relevante: foco nos últimos 5 anos (2011–2016)
- Análise de vendas por plataforma → **PS4 e X360** lideram
- Correlação entre scores de críticos/usuários e vendas
- Gêneros mais lucrativos → **Action e Shooter** dominam em volume; **Shooter e Platform** lideram em média por jogo

**Etapa 4 — Análise Regional (NA, EU, JP)**
- Top plataformas por região: América do Norte prefere X360/PS, Europa segue tendência similar, Japão tem perfil próprio com domínio do 3DS
- Perfil de gêneros e classificações ESRB por região
- Japão prefere classificações `E` (Everyone) e `T` (Teen); Ocidente lidera com classificação `M` (Mature)

**Etapa 5 — Testes de Hipóteses**
- **Hipótese 1:** As classificações médias dos usuários de Xbox One e PC são iguais → *Não rejeitada* (p-value: 0.63)
- **Hipótese 2:** As classificações médias de usuários para Action e Sports são diferentes → *Rejeitada* (p-value: 5.2e-24)
- Nível de significância utilizado: **α = 0.05**

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Uso |
|---|---|
| Python 3.x | Linguagem principal |
| Pandas | Manipulação e análise de dados |
| NumPy | Operações numéricas |
| Matplotlib | Visualizações estáticas |
| SciPy (stats) | Testes de hipóteses (t-test) |

---

## 📂 Estrutura do Projeto

```
videogame-sales-eda/
├── projeto.ipynb     # Notebook principal com toda a análise
├── datasets/
│   └── games.csv     # Dataset de vendas de videogames
└── README.md
```

---

## 📊 Principais Conclusões

- O mercado de consoles está em constante renovação: plataformas com mais de 5–7 anos perdem relevância rapidamente
- **PS4** lidera em média de vendas por jogo nos últimos anos analisados
- Jogos do gênero **Shooter** têm a maior média de vendas por título, apesar de o **Action** dominar em volume total
- O perfil de consumo japonês é significativamente diferente do ocidental, exigindo estratégias de marketing distintas
- A classificação ESRB **Mature (M)** está fortemente associada aos jogos mais vendidos na América do Norte e Europa

---

## 👨‍💻 Autor

**Mauro Rocha**  
Desenvolvedor Web em transição para Data Science e Automação  
[GitHub](https://github.com/mauroroc)

---

## 📝 Licença

Este projeto está sob a licença MIT.
