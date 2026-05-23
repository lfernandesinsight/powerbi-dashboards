# 📊 Power BI Dashboards

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=F2C811&height=120&section=header&text=Power%20BI%20Dashboards&fontSize=36&fontColor=1A3C5E&fontAlignY=55&desc=DAX%20%7C%20Linguagem%20M%20%7C%20ETL%20%7C%20Transformando%20dados%20em%20decisões&descAlignY=80&descSize=14&descColor=1A3C5E" alt="Power BI Dashboards" />
</div>

---

## 📌 Sobre este repositório

Coleção de dashboards e relatórios desenvolvidos em **Power BI**, com foco em análises gerenciais, KPIs estratégicos e visualizações orientadas a negócio. Cada projeto inclui documentação, modelo de dados e principais métricas DAX utilizadas.

---

## 📁 Estrutura do Repositório

```
📁 powerbi-dashboards/
│
├── 📁 financeiro/
│   ├── dashboard_financeiro.pbix
│   └── README.md
│
├── 📁 vendas/
│   ├── dashboard_vendas.pbix
│   └── README.md
│
├── 📁 rh/
│   ├── dashboard_rh.pbix
│   └── README.md
│
├── 📁 templates/
│   ├── template_corporativo.pbix
│   └── README.md
│
├── .gitignore
└── README.md
```

---

## 🚀 Projetos

| Dashboard | Descrição | Status |
|---|---|---|
| 💰 [Financeiro](#) | Análise de receitas, despesas e fluxo de caixa | 🚧 Em breve |
| 📈 [Vendas](#) | Performance de vendas por região, produto e período | 🚧 Em breve |
| 👥 [RH](#) | Headcount, turnover e indicadores de pessoas | 🚧 Em breve |
| 🎨 [Templates](#) | Temas e layouts corporativos reutilizáveis | 🚧 Em breve |

---

## 🛠️ Tecnologias Utilizadas

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)

---

## 💡 Padrões e Boas Práticas

### Nomenclatura de Medidas DAX
```
// Prefixos utilizados
[M] Métrica Base       → ex: [M] Total Vendas
[%] Percentual         → ex: [%] Margem Bruta
[Δ] Variação           → ex: [Δ] Crescimento MoM
[YTD] Acumulado no ano → ex: [YTD] Receita
[LY] Ano anterior      → ex: [LY] Total Vendas
```

### Exemplo de Medida DAX
```dax
-- Variação percentual vs. ano anterior
Crescimento YoY % =
VAR VendasAtual = [M] Total Vendas]
VAR VendasAnterior = CALCULATE([M] Total Vendas], SAMEPERIODLASTYEAR('Calendário'[Data]))
RETURN
    DIVIDE(VendasAtual - VendasAnterior, VendasAnterior, 0)
```

### Modelo de Dados (Star Schema)
```
        fVendas (Fato)
           │
    ┌──────┼──────┐
    │      │      │
dCliente dData dProduto  (Dimensões)
```

---

## 📋 Como usar os arquivos .pbix

1. Faça o download do arquivo `.pbix` desejado
2. Abra no **Power BI Desktop** (gratuito — [baixar aqui](https://powerbi.microsoft.com/downloads/))
3. Atualize a fonte de dados conforme seu ambiente
4. Explore e adapte conforme necessário

---

## 📬 Contato

<div align="left">
  <a href="mailto:lfernandes.insight@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
  <a href="https://www.linkedin.com/in/lfernandesinsight" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  <a href="https://github.com/lfernandesinsight" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
  </a>
</div>

---

<div align="center">
  <sub>Desenvolvido por <a href="https://github.com/lfernandesinsight">Leandro Fernandes</a></sub>
</div>
