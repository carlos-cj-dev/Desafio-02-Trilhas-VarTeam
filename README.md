# Desafio 02 — Análise Exploratória da Loja de Roupas

## Equipe
- Arthur Sousa Furtado
- Carlos Antônio Dos Santos Mello Junior
- Suene Michelle Miranda dos Santos

---

## 1. A base escolhida

Utilizamos a base `loja_roupas.csv`, que contém 509 registros de vendas de uma loja de roupas no período de 1º de março a 20 de junho de 2025. A base foi escolhida porque traz informações completas sobre categoria, produto, valor, forma de pagamento, horário da venda e localização, permitindo analisar diferentes aspectos do negócio. Não há valores nulos e os dados foram consistentes após verificação.

---

## 2. Perguntas investigadas

| Pergunta | Por que isso importa? |
|----------|----------------------|
| Qual é o faturamento total e o ticket médio das vendas? | Avaliar o desempenho financeiro e o valor médio gasto por cliente. |
| Quais categorias e produtos geram maior faturamento? | Identificar os itens mais importantes para a receita e priorizar estoque. |
| Como o faturamento e a quantidade de vendas evoluem ao longo dos meses? | Detectar tendências sazonais e planejar promoções. |
| Quais horários concentram o maior volume de vendas? | Organizar os horários de funcionários para melhorar o atendimento. |
| Vendas de clientes cadastrados possuem ticket médio maior? | Verificar se vale a pena investir em programas de cadastro de clientes. |

---

## 3. Preparação dos dados

- ✅ **Verificação:** A base possui 509 linhas e 11 colunas, sem valores nulos.
- ✅ **Padronização:** Colunas de texto (categoria, produto, forma de pagamento, etc.) foram convertidas para letras maiúsculas para evitar duplicatas.
- ✅ **Transformação:** Da coluna `data`, extraímos novas colunas: dia, mês, ano e horário, facilitando análises temporais.
- ✅ **Arquivo tratado:** Os dados limpos foram salvos em `data/loja_roupas_tratado_limpo.csv` para uso nas análises.

---

## 4. Respostas e conclusões

### 📌 Pergunta 1 — Faturamento e Ticket Médio
- O faturamento total e o ticket médio foram calculados somando todos os valores de venda e dividindo pelo número total de transações. Esses números são fundamentais para saber o tamanho do negócio e definir metas de crescimento.

### 📌 Pergunta 2 — Categorias e Produtos
- As categorias Camisas e Calças lideraram o faturamento. Entre os produtos, Camisa Polo e Calça Jeans apareceram como os mais vendidos. Essa informação ajuda a loja a manter sempre esses itens bem abastecidos e em destaque.

### 📌 Pergunta 3 — Evolução Mensal
- As vendas mostraram uma tendência de crescimento de março a junho. Cada mês foi analisado separadamente, contando quantas vendas aconteceram e quanto foi faturado. Isso mostra quais períodos precisam de mais atenção.

### 📌 Pergunta 4 — Horários de Maior Movimento
- Os horários com mais vendas foram entre as 14h e 20h. Com essa informação, a loja pode escalonar os funcionários para ter mais pessoas atendendo nesses horários de pico, melhorando a experiência de compra.

### 📌 Pergunta 5 — Teste de Hipótese: Clientes Cadastrados Gastam Mais?

> **Hipótese Nula (H₀):** Não há diferença significativa entre o ticket médio de cadastrados e não cadastrados.
> **Hipótese Alternativa (H₁):** Clientes cadastrados possuem ticket médio maior.
> **Nível de significância:** 5% (α = 0,05)

- Utilizamos o **teste t de Student** para comparar os dois grupos.
- Se o **valor-p < 0,05**, a diferença é estatisticamente significativa — ou seja, não é por acaso.
- **Resultado:** A análise mostra que clientes cadastrados tendem a gastar mais por compra, indicando que vale a pena incentivar o cadastro dos clientes da loja.

---

## 💡 Principais Conclusões

1. As categorias Camisas e Calças são as maiores geradoras de receita da loja.
2. Os horários de maior movimento são no período da tarde e início da noite.
3. As vendas apresentaram crescimento ao longo dos meses analisados.
4. Existe indicação de que clientes cadastrados gastam mais — o que reforça a importância de manter e ampliar o cadastro de clientes.

---

## 🤔 Reflexão

**O que ficou mais fácil em Python do que em planilhas?**
- Carregar e verificar se existem dados faltantes em segundos, sem precisar conferir linha por linha.
- Criar automaticamente colunas com dia, mês e horário a partir de uma única coluna de data.
- Gerar gráficos profissionais para visualizar os resultados de forma clara.
- Fazer um teste de hipótese com um único comando — algo que seria muito complexo de fazer manualmente em uma planilha.

**Como a equipe dividiu o trabalho?**
- Um membro organizou a base de dados e fez a limpeza.
- Outro estruturou as perguntas e as explicações de cada etapa.
- Outro revisou o notebook e escreveu as conclusões no README.

Cada um contribuiu com uma parte, e juntos conseguimos entregar uma análise completa! ✅

---

> 📂 **Arquivos do projeto:**
> - `data/loja_roupas.csv` — Base original
> - `data/loja_roupas_tratado_limpo.csv` — Base tratada
> - `desafio_loja_roupas.ipynb` — Notebook com a análise completa

