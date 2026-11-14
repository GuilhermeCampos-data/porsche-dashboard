# 🏎️ Porsche Sales Performance Dashboard

Dashboard interativa desenvolvida para o desafio do Bootcamp de Data Analytics com Agentes de IA da DIO. O projeto transforma uma base de 100 vendas da Porsche em uma aplicação web interativa publicada no GitHub Pages.

🔗 **Acesse a Dashboard Online:** https://guilhermecampos-data.github.io/porsche-dashboard/

---

## 🎯 Perguntas de Negócio Escolhidas (e Por Quê)

Para transformar a base de 100 vendas em uma ferramenta de decisão comercial, a dashboard foi construída para responder a 4 perguntas principais:

1. **Qual é o modelo mais vendido?** (`01 / Product Mix`)
   * **Por quê:** Identifica os veículos com maior saída em volume e faturamento, ajudando a direcionar o planejamento de estoque e as estratégias comerciais para os modelos de maior demanda.
2. **Qual é a forma de pagamento mais utilizada?** (`02 / Payment Profile`)
   * **Por quê:** Revela o perfil financeiro dos compradores (financiamento, à vista, leasing, etc.), permitindo alinhar condições comerciais e parcerias bancárias à preferência real dos clientes.
3. **Entre carros 0 km (0 milhas) e seminovos, qual é a diferença de vendas?** (`03 / Vehicle Condition`)
   * **Por quê:** Compara tanto o volume de unidades quanto a receita gerada entre veículos novos e usados, mostrando o peso de cada categoria no faturamento total e no ticket médio.
4. **Qual é a porcentagem de compras canceladas comparado com as vendas confirmadas?** (`04 / Order Status`)
   * **Por quê:** Mede a eficiência operacional do funil de vendas e o impacto das desistências na receita, permitindo investigar gargalos por modelo, estado ou forma de pagamento através dos filtros.

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
