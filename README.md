# Desafio 02 — Análise exploratória da loja de roupas

[Abrir no Google Colab](https://colab.research.google.com/github/carlos-cj-dev/Desafio-02-Trilhas-VarTeam/blob/main/tratamento_limpeza.ipynb)


Análise exploratória de dados de vendas de uma loja de roupas, desenvolvida como parte do Desafio 02.

## Equipe

- Arthur Sousa Furtado
- Carlos Antônio Dos Santos Mello Junior
- Suene Michelle Miranda dos Santos

## Perguntas

1. Qual é o faturamento total e o ticket médio das vendas?
2. Quais categorias e produtos geram maior faturamento?
3. Como o faturamento e a quantidade de vendas evoluem ao longo dos meses?
4. Quais horários concentram o maior volume de vendas?
5. Vendas de clientes cadastrados possuem ticket médio maior que vendas de clientes não cadastrados? **Teste de hipótese.**

## Principais conclusões

Nesta etapa, foram identificados os seguintes pontos sobre a base:

- A base original possui 509 registros de vendas e 11 colunas.
- O período analisado vai de 1º de março a 20 de junho de 2025.
- Não foram encontrados valores nulos na base.
- A coluna `data` foi convertida para o formato datetime.
- O arquivo tratado possui novas colunas de dia, mês, ano e horário para facilitar as análises temporais.
- As colunas categóricas foram padronizadas em maiúsculas no arquivo tratado.

As conclusões relacionadas ao faturamento, aos produtos, aos horários e ao teste de hipótese serão apresentadas no notebook após a execução das análises e dos gráficos.

## Arquivos

- `tratamento_limpeza.ipynb`: notebook com o carregamento, a limpeza, as transformações e as perguntas da análise.
- `data/loja_roupas.csv`: base original, sem alterações.
- `data/loja_roupas_tratado_limpo.csv`: base depois da padronização e da criação das colunas temporais.
- `README.md`: documentação do projeto.

## Como rodar

### Só para ver

Abra o arquivo `tratamento_limpeza.ipynb` no GitHub ou no Jupyter. O notebook contém as células utilizadas no tratamento da base.

### No computador

Você precisa do Python 3.10 ou mais novo.

1. Baixe ou clone este repositório.
2. Abra o terminal na pasta do projeto.
3. Crie o ambiente virtual:

```bash
python -m venv .venv
```

4. Ative o ambiente virtual.

No Linux ou macOS:

```bash
source .venv/bin/activate
```

No Windows:

```bash
.venv\Scripts\activate
```

5. Instale as bibliotecas necessárias:

```bash
pip install pandas jupyter
```

6. Abra o Jupyter Lab:

```bash
python -m jupyter lab
```

7. Abra `tratamento_limpeza.ipynb` e use **Run → Run All Cells**.

O notebook precisa permanecer na pasta principal do projeto, com a pasta `data/` no mesmo nível. Essa estrutura é necessária porque os dados são carregados pelos caminhos `data/loja_roupas.csv` e `data/loja_roupas_tratado_limpo.csv`.

Ao terminar, o ambiente virtual pode ser desativado com:

```bash
deactivate
```

### No Google Colab

Abra o notebook no Colab e envie o arquivo `tratamento_limpeza.ipynb` junto com a pasta `data/`, mantendo a mesma estrutura de diretórios. Depois, use **Ambiente de execução → Executar tudo**.

## Limitações da base

A base não possui identificador individual do cliente, descontos, estoque, custos ou informações de entrega. Por isso, a análise não permite medir recompra individual, margem de lucro, estoque disponível ou tempo de entrega.
