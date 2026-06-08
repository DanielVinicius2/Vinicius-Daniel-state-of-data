# Vinicius-Daniel-state-of-data

# Quais fatores mais influenciam o salário de um profissional de dados no Brasil em 2024?

**Trabalho Final — Análise Avançada de Dados**  
Centro Universitário Santo Agostinho (UNIFSA) · Engenharia de Software  
Disciplina ministrada pela Prof.ª Ma. Heloisa Guimarães

**Integrantes:** Vinícius · Daniel

---

## Resposta à pergunta central

A análise dos dados do *State of Data Brazil 2024–2025* aponta a **senioridade** como o principal fator associado ao salário de profissionais de dados no Brasil. Profissionais classificados como sênior apresentam remuneração mediana substancialmente superior à de júniores e plenos, com maior dispersão dentro do grupo — o que indica que, no nível sênior, fatores como setor de atuação, cargo específico e empresa passam a fazer diferença relevante.

O **tempo de experiência na área de dados** é o segundo fator mais associado ao salário, medido pelo coeficiente de correlação de Spearman. Quanto mais anos de atuação específica em dados, maior a tendência de remuneração mais alta. A experiência prévia em TI também contribui positivamente, mas com magnitude menor.

A **região geográfica** é o terceiro fator relevante: profissionais no Sudeste e Sul apresentam salários médios superiores, refletindo a concentração de empresas de tecnologia e o maior custo de vida nessas localidades. Diferenças salariais por **gênero** e **raça/etnia** também foram observadas, mas devem ser interpretadas com cautela — elas não controlam por senioridade e cargo, e envolvem grupos com taxas de não-resposta relevantes na pesquisa.

---

## Sobre os dados

- **Fonte:** [State of Data Brazil 2024–2025](https://www.kaggle.com/datasets/datahackers/state-of-data-brazil-20242025) — Data Hackers em parceria com a Bain & Company
- **Período:** 2024–2025
- **Respondentes:** 5.217 profissionais de dados e IA no Brasil
- **Colunas originais:** mais de 400

---

## Decisões de limpeza

**Faixas salariais → ponto médio numérico**  
A coluna de salário original é textual (ex: `"de R$ 4.001/mês a R$ 6.000/mês"`). Cada faixa foi convertida para seu ponto médio numérico (ex: R$ 5.000) para permitir cálculos estatísticos. A faixa mais alta (`"Acima de R$ 30.000/mês"`) foi estimada em R$ 35.000. Essa decisão introduz imprecisão, já que o valor real do respondente pode estar em qualquer ponto da faixa.

**Renomeação de colunas**  
As colunas originais usam prefixos crípticos como `1.b_genero` e `2.h_faixa_salarial`. As 15 colunas relevantes para a análise foram renomeadas para nomes legíveis antes de qualquer processamento.

**Gênero e raça não imputados**  
Os campos `genero` e `raca` possuem valores ausentes que representam escolha do respondente, não erro de coleta. Imputar esses campos distorceria uma informação que é, por si só, analiticamente relevante. Qualquer conclusão sobre desigualdade salarial por gênero ou raça deve considerar que os resultados refletem apenas quem optou por se identificar.

**Padronização de cargos**  
Variações como `"Data Analyst"`, `"analista de dados jr"` e `"analista de dados pleno"` foram mapeadas para uma categoria unificada. Cargos sem correspondência no mapeamento foram mantidos como estão. Valores ausentes receberam a categoria `"Não informado"`.

**Experiência numérica**  
As variáveis de tempo de experiência em dados e em TI também eram faixas textuais e foram convertidas para ponto médio numérico pelo mesmo critério aplicado ao salário.

---

## Estrutura do repositório

```
vinicius-daniel-state-of-data/
├── README.md
├── notebook/
│   └── vinicius-daniel-analise.ipynb
├── relatorio/
│   └── vinicius-daniel-relatorio.pdf
└── dados/
    └── README.md
```

---

## Dashboard

> 🔗 [Link do dashboard no Google Looker Studio](#) ← substituir pelo link real antes de entregar

---

## Referências

- Data Hackers & Bain & Company. *State of Data Brazil 2024–2025*. Disponível em: https://www.kaggle.com/datasets/datahackers/state-of-data-brazil-20242025
- McKinney, W. *Python for Data Analysis*. O'Reilly, 2022.
- Bibliotecas utilizadas: `pandas`, `numpy`, `matplotlib`, `seaborn`
