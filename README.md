# Projeto Análise Dados iFood Hackday

![hackday](https://github.com/user-attachments/assets/dc0613fa-424d-4449-8ed1-78f71a269578)



# 📦 Análise Logístico de Entregas - iFood

Este projeto tem como foco diagnosticar os principais gargalos operacionais da logística de entregas no iFood, utilizando dados simulados para gerar insights acionáveis que auxiliem na tomada de decisões estratégicas.

---

## 🚨 Problema de Negócio

Apesar de existirem SLAs (Service Level Agreement) bem definidos, o time de operações do iFood enfrenta baixa visibilidade operacional para responder com agilidade a perguntas como:

- Quais restaurantes estão impactando negativamente a logística?
- Existe algum padrão de atraso em horários, dias ou regiões?
- O atraso vem do restaurante, do entregador ou do modelo de entrega?

Essa falta de visibilidade dificulta a identificação das causas dos atrasos e compromete a qualidade do serviço.

---

## 🎯 Objetivo do Projeto


1. 📊 Diagnosticar os principais pontos de falha na operação de entrega  
2. 📐 Criar métricas comparativas de performance entre restaurantes  
3. 💡 Sugerir ações baseadas em dados para reduzir os atrasos e melhorar a logística

---

## 🛠️ Ferramentas Utilizadas

- **Google Sheets** (pré-processamento e análise de dados)
- **Looker Studio** (dashboard interativo com filtros e indicadores)

---

## 🔍 Análises Realizadas

### ✅ Taxa de Atraso

<img width="218" height="134" alt="Captura de Tela 2025-08-06 às 21 18 27" src="https://github.com/user-attachments/assets/992fa9b9-bd99-42fd-945c-7d02cd5f4c39" />


- **Taxa média de atraso:** 9,9%
- **Datas críticas:** 10/04 e 12/04 apresentaram picos de atraso de 11,5%
- **Horários críticos:** picos entre **0h e 2h (30%)** e **7h (15%)**, frente a uma média geral de 9,2%
- **Modalidade:** Entregas via **E-Bike** tiveram 33% de atraso em 10/04
  

---

### ✅ Restaurantes x Entregadores

- Restaurantes são responsáveis por **~39% dos pedidos atrasados**

    <img width="218" height="134" alt="Captura de Tela 2025-08-06 às 21 18 58" src="https://github.com/user-attachments/assets/9cf8f79c-b024-48c1-903e-25b28ed67301" />
  
- Entregadores são responsáveis por **~10% dos atrasos**

    <img width="218" height="134" alt="Captura de Tela 2025-08-06 às 21 19 05" src="https://github.com/user-attachments/assets/07fe188e-ba5d-451f-ab42-7d5ac50f1883" />


Foi verificado também que:
- Existem **42 restaurantes que atrasaram 100% dos seus pedidos**
- **37,8% dos restaurantes** têm taxa de atraso acima da média

---

### ✅ Modelo de Entrega

<img width="246" height="151" alt="Captura de Tela 2025-08-06 às 21 17 26" src="https://github.com/user-attachments/assets/d0de616f-ea7a-4f55-9700-09026971aea1" />


- Não há evidências fortes de que o **modelo de entrega** impacta significativamente nos atrasos

Porém, também foi identificado:
- **Multi Drop**: Pedidos com múltiplas entregas possuem **12,3% de taxa de atraso**
- **Bicicletas**: Pedidos entregues por bicicleta apresentam **14,9% de atraso**

---

### ✅ Scoring Operacional

- No total tem 2.299 lojas registradas no banco de dados
- Foi feito um scoring com base na taxa de atraso de pedidos de cada loja individualmente:
  - **Excelente:** 0% a 20% de taxa de atraso
  - **Bom:** 21% a 40% de taxa de atraso
  - **Regular:** 41% a 60% de taxa de atraso
  - **Ruim:** 61% a 80% de taxa de atraso
  - **Crítico:** Acima de 80% de taxa de atraso
 
    <img width="395" height="227" alt="Captura de Tela 2025-08-06 às 21 20 34" src="https://github.com/user-attachments/assets/4fa3d82c-b599-4b53-9289-c2fc282ec702" />

- Restaurantes com maior representatividade de pedidos, que ultrapassam a média geral de 9.9%

    <img width="411" height="387" alt="Captura de Tela 2025-08-06 às 21 21 08" src="https://github.com/user-attachments/assets/f48b656e-82ed-4d28-bc25-dcf41739ac5d" />



---

## 📌 Principais Insights

- Restaurantes são o maior gargalo na cadeia de entrega, com alto percentual de atrasos
- Horários de pico precisam de reforço logístico e ações preventivas
- Reavaliação dos restaurantes com desempenho crítico é urgente
- Adoção de **KPIs operacionais** como “%Pedidos Atrasados por Restaurante” é essencial

---

## ✨ Possíveis Ações Recomendadas

- Criar score operacional para restaurantes, integrando taxa de atraso e volume de pedidos
- Aplicar punições ou incentivos com base em desempenho
- Implementar monitoramento em tempo real para horários críticos
- Reforçar o time de entregadores em turnos com alta incidência de atraso

---

## 📷 Capturas de Tela

Dashboard criado para o monitoramento geral da base de dados, a fim de saber o que está acontecendo em cada dia. De modo que, ajude o analista observar possíveis anomalias e a partir daí realizar novas análises mais profundas:

<img width="878" height="620" alt="Captura de Tela 2025-08-06 às 21 12 56" src="https://github.com/user-attachments/assets/ac57a19c-0bd1-41ad-b3cc-a167f736d741" />


---

## 🚀 Próximos Passos

- Automatizar alertas com base em metas de SLA
- Cruzar dados de avaliação dos clientes com performance operacional
- Expandir o modelo para outras regiões e segmentos

---

## 📎 Links Úteis

- 🔗 [Dashboard no Looker Studio]([https://link-para-o-looker](https://lookerstudio.google.com/reporting/0e052491-a41f-49cb-8659-f3b146cc9161))
- 📄 [Google Sheets com Base de Dados]([https://link-do-sheets](https://docs.google.com/spreadsheets/d/1E9-XWQbyWeNFkYxrX-moARdzdiCHVBAPmssxMciTWOo/edit?usp=sharing))


