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

Os notebooks e CSVs foram copiados do Drive em 26/09/2026, preservando seu conteúdo. Foram removidos apenas espaços finais dos nomes dos notebooks e acrescentada a extensão .ipynb. Os dados brutos continuam no Drive.

## Dados brutos no Google Drive

| Base | Link | Arquivos disponíveis | Volume aproximado |
|---|---|---|---|
| Matriculados | [Abrir pasta](https://drive.google.com/drive/folders/1prSA8hEU-jupnIzTE9B0RYhndZM289Zc) | 11 CSVs com nomes de 2015 a 2025 | 2,28 GB |
| Rendimento | [Abrir pasta](https://drive.google.com/drive/folders/1uf0GGLYDYYM-3A_JbUjIe7snKIglZB8-) | 12 planilhas com nomes de 2014 a 2025 | 501,70 MB |

Os anos acima foram identificados pelos nomes dos arquivos; a correspondência com o período de referência dentro de cada base precisa ser validada pela equipe.

O acesso depende das permissões do Drive. Se necessário, solicite acesso ao responsável pela pasta. Ter o link no README não torna os arquivos públicos.

Os arquivos brutos ficam fora desta pasta para manter o projeto leve. Para reproduzir a preparação dos dados, baixe somente as bases necessárias nos links acima.

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

Os nomes `Rendimento2021ano (1).csv` e `Rendimento2022ano (1).csv` foram preservados como estavam no Drive.

## Como usar no Google Colab

1. Abra o notebook desejado no Colab pela opção de upload de um arquivo .ipynb.
2. Para explorar a tabela já preparada, carregue o CSV processado correspondente. O notebook de organização lê `matriculados_rendimentos_join_2025.csv`.
3. Para refazer a preparação, obtenha os dados brutos nos links deste README.
4. Carregue os arquivos na sessão do Colab ou monte seu Drive e ajuste os caminhos de leitura e saída.
5. Confira os nomes dos arquivos e execute as células na ordem, verificando os resultados de cada etapa.

O código utiliza pandas; o notebook de organização também importa NumPy, seaborn e Matplotlib. A leitura de XLSX pode exigir openpyxl, e a leitura de ODS pode exigir odfpy.

### Ajustes necessários para reprodução

Os notebooks são cópias do trabalho original e não foram executados nesta organização. Eles ainda dependem de caminhos específicos, como `/content/sample_data/matriculados`, `/content/sample_data/rendimentos` e `/content/drive/MyDrive`.

Também foram observadas diferenças entre os nomes usados no código e os arquivos do Drive:

- O notebook de rendimento procura `TX_REND_ESCOLAS_2015.xlsx`, mas o arquivo disponível está em formato `.ods`. É necessário adaptar a leitura ao formato real ou converter uma cópia.
- Para 2018, confira as letras maiúsculas e minúsculas no nome da planilha.
- O arquivo de matrículas de 2020 está com extensão `.CSV`, enquanto o código monta o nome com `.csv`.
- A saída de junção no notebook de matrículas usa `matriculados_rendimentos_join2025.csv`; o notebook de organização lê `matriculados_rendimentos_join_2025.csv`. Padronize o caminho usado entre essas etapas.

Essas diferenças foram documentadas, sem modificar os notebooks ou os dados.

## Fontes e revisão

[Pasta original do projeto no Drive](https://drive.google.com/drive/folders/17xdkOXq5XFrFuckvo4ZMQ93CqxQ9xuPu)

A equipe deve confirmar os períodos das bases e complementar as referências oficiais de origem e a metodologia conforme o desenvolvimento do trabalho.
