# Projeto — Evasão Escolar

Material de trabalho da disciplina de Tópicos de Big Data, com notebooks de preparação e análise de dados de matrículas e rendimento escolar.

## Conteúdo

```text
Projeto-Evasao-Escolar/
├── README.md
├── .gitignore
├── Notebooks do Colab/                 # 5 notebooks Python (.ipynb)
└── Arquivos criados no Colab/     # 27 CSVs processados
```

## Dados brutos no Google Drive

| Base | Link | Arquivos disponíveis | Volume aproximado |
|---|---|---|---|
| Matriculados | [Abrir pasta](https://drive.google.com/drive/folders/1aKAk9_axBDTvHXkC03sLoGERuMoWAGBy?usp=drive_link) | 11 CSVs com nomes de 2015 a 2025 | 2,28 GB |
| Rendimento | [Abrir pasta](https://drive.google.com/drive/folders/1goc_C9Tek869mQUdFl53uAD16qNjUDsH?usp=drive_link) | 12 planilhas com nomes de 2014 a 2025 | 501,70 MB |

## Notebooks

| Notebook | Finalidade observada no código |
|---|---|
| Notebook para filtrar dados do inep(rendimentos).ipynb | Filtrar planilhas de rendimento por municípios e indicadores do ensino médio. |
| Concatenando dados do rendimento.ipynb | Reunir os CSVs de rendimento em uma tabela. |
| Notebook para filtrar dados do inep(matriculados).ipynb | Filtrar matrículas, concatenar os resultados e trabalhar na junção com rendimentos. |
| Organizando a tabela principal.ipynb | Ler a tabela de junção e preparar a tabela final. |
| Primeiro Pipeline.ipynb | Notebook adicional presente na pasta do Drive; incluído para revisão da dupla. |

O recorte encontrado nos filtros inclui Niterói, São Gonçalo, Maricá e Rio de Janeiro.


## Dados processados

A pasta contém 11 CSVs anuais de matrículas, 11 CSVs anuais de rendimento e cinco arquivos consolidados:

- `matriculados_concatenados.csv`
- `rendimentos_concatenados.csv`
- `matriculados_rendimentos_join.csv`
- `matriculados_rendimentos_join_2025.csv`
- `tabela_final.csv`

## Como usar no Google Colab

1. Abra o notebook desejado no Colab pela opção de upload de um arquivo .ipynb.
2. Para explorar a tabela já preparada, carregue o CSV processado correspondente. O notebook de organização lê `matriculados_rendimentos_join_2025.csv`.
3. Para refazer a preparação, obtenha os dados brutos nos links deste README.
4. Carregue os arquivos na sessão do Colab ou monte seu Drive e ajuste os caminhos de leitura e saída.
5. Confira os nomes dos arquivos e execute as células na ordem, verificando os resultados de cada etapa.
