# 🏎️ Porsche Sales Performance Dashboard

Dashboard interativa desenvolvida para o desafio do Bootcamp de Data Analytics com Agentes de IA da DIO. O projeto transforma uma base de 100 vendas da Porsche em uma aplicação web interativa publicada no GitHub Pages.

🔗 **Acesse a Dashboard Online:** https://github.io

---

## 🎯 Perguntas de Negócio Respondidas

1. **Proporção Operacional (Vendas Reais):** Qual a relação entre veículos entregues (`Delivered`) frente aos pendentes, em trânsito ou cancelados?
2. **Gargalos Geográficos:** Quais estados (`UF`) apresentam a maior taxa de cancelamento e qual o volume financeiro por região?
3. **Perfil do Estoque (Novos vs. Seminovos):** Como as vendas se dividem entre veículos zero km (`0` milhas) e seminovos (`> 0` milhas)?
4. **Mix de Produtos:** Qual o ranking dos modelos Porsche mais vendidos em volume?
5. **Comportamento Financeiro:** Quais são as formas de pagamento mais utilizadas pelos clientes até as menos utilizadas?
6. **Faturamento por Período e Validação de Datas:** Qual o valor total de vendas concretizadas dentro das datas válidas identificadas versus registros com data inválida (`INVALID`)?

---

## 🧹 Tratamento e Segurança dos Dados

Antes de gerar a dashboard, a planilha original (`.xlsx`) passou pelas seguintes etapas:
* **Seleção de Colunas Sanitizadas:** Foram mantidas apenas as 9 colunas limpas (`SaleDateSanitized`, `PorscheModelSanitized`, `ModelYearSanitized`, `SalesPriceSanitized`, `VehicleMileageSanitized`, `PayMethodSanitized`, `CitySanitized`, `StateSanitized` e `DeliveryStatusSanitized`).
* **Privacidade:** As colunas `customer_name` e `salesperson` foram removidas para não expor dados pessoais no código HTML público.
* **Padronização Numérica:** Valores monetários (`SalesPriceSanitized`), anos e quilometragem foram formatados como números puros.
* **Tratamento de Datas Inválidas:** Registros marcados como `INVALID` na coluna de data foram mantidos nos indicadores gerais e ganharam um filtro próprio na interface.

---

## 🤖 Processo de Criação com IA

* **Ferramenta:** Assistente de IA com geração de código em arquivo único (`HTML5` + `Tailwind CSS` + `Chart.js`).
* **Prompt e Refinamentos:** O prompt solicitou uma interface inspirada na identidade visual oficial da Porsche (modo escuro elegante, detalhes em vermelho `#d5001c` e tipografia limpa), com 7 filtros dinâmicos, 4 indicadores de topo (KPIs) e 6 blocos analíticos. Nos testes, foram ajustados a formatação monetária em Dólar (`USD`), a ordenação dos rankings e o painel de insights automáticos.
