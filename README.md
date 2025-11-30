# Otimização de Elenco de Futebol Multi-Período

Este repositório contém o trabalho final da disciplina de **Otimização (COS-360/COM-361)**, período 2025/2. O projeto consiste em um modelo de montagem de elenco de futebol focado em realismo e com parâmetros configuráveis para priorizar diferentes objetivos estratégicos.

## 📄 Sobre o Projeto

O problema abordado é classificado como uma variante do **Team Formation Problem (TFP)** combinada com características do **Problema da Mochila Quadrático (QKP)** e de problemas de **Estoque Multi-Período**.

O objetivo é maximizar um *Score Total* que equilibra performance esportiva, saúde financeira e estabilidade do elenco ao longo de janelas de transferência consecutivas.

### Principais Características
* **Modelagem Matemática:** Formulado como um modelo de **Programação Inteira Mista (MILP)**, utilizando técnicas de linearização para os componentes quadráticos de interação ("química") entre jogadores.
* **Dinâmica Temporal:** Projeção determinística de atributos onde o jogador sofre depreciação (envelhecimento) ou valorização (potencial) ao longo do tempo.
* **Restrições Suaves (Soft Constraints):** Utilização de penalidades na função objetivo (como fator de fricção) para simular a inércia realista de um ambiente de gestão, desencorajando rotatividade excessiva sem impor limites rígidos.
* **Perfis Estratégicos:** Configuração de modos de operação distintos (Equilibrado, Conservador e Arriscado) para capturar diferentes filosofias de gestão.

## 📂 Estrutura do Repositório

* `montagem_de_elenco_v5.ipynb`: **Arquivo principal**. Notebook contendo a implementação final do modelo, explicação sucinta e visualização dos resultados.
* `player-data-full.csv`: Dataset base extraído do EA Sports FC 24 (via Kaggle).
* `flamengo_custom_players.csv`: Arquivo complementar com dados calibrados do elenco do Flamengo para contornar limitações de licenciamento da base original.

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python 3.13.3.
* **Modelagem:** Biblioteca PuLP.
* **Solver:** Gurobi Optimizer.

## ⚽ Estudo de Caso

Para validação, foi estabelecido o cenário fictício **"Flamengo na Premier League"** (2026). O desafio proposto ao modelo foi planejar contratações e vendas por 3 janelas, garantindo competitividade imediata na Europa sem comprometer a solvência do clube, utilizando um aporte inicial de €40 milhões.

---
**Autor:** Daniel Rebouças de Sousa Barros
