# Base de Dados

Este projeto utiliza a base de dados **State of Data Brazil 2024–2025**, disponibilizada pela comunidade Data Hackers em parceria com a Bain & Company.

## Download da Base

A base pode ser obtida gratuitamente no Kaggle:

https://www.kaggle.com/datasets/datahackers/state-of-data-brazil-20242025

## Arquivos Necessários

Após realizar o download, extraia os arquivos e coloque o arquivo CSV na raiz do projeto ou ajuste o caminho utilizado no notebook.

Estrutura esperada:

```
projeto/
├── notebook/
│   └── vinicius-daniel-analise.ipynb
├── dados/
│   └── README.md
└── State_of_data_2024.csv
```

## Como Reproduzir a Análise

1. Clone o repositório:

```bash
git clone <link-do-repositorio>
```

2. Instale as bibliotecas necessárias:

```bash
pip install pandas numpy matplotlib seaborn
```

3. Baixe a base de dados no Kaggle.

4. Posicione o arquivo CSV conforme indicado na estrutura do projeto.

5. Execute o notebook:

```bash
jupyter notebook
```

ou

```bash
jupyter lab
```

6. Abra o arquivo:

```text
vinicius-daniel-analise.ipynb
```

7. Execute as células em sequência para reproduzir:
   - Limpeza e tratamento dos dados;
   - Conversão das faixas salariais para valores numéricos;
   - Conversão das variáveis de experiência para formato numérico;
   - Análises estatísticas univariadas e bivariadas;
   - Geração dos gráficos e visualizações utilizadas no relatório e dashboard.

## Observação

O arquivo CSV não foi incluído neste repositório por questões de organização e para seguir as orientações da disciplina. Todos os dados utilizados podem ser obtidos diretamente pela fonte oficial indicada acima.

## Fonte

Data Hackers & Bain & Company. State of Data Brazil 2024–2025.
