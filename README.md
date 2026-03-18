# Debriefing — Meta Ads × Kiwify

Sistema de análise de performance que cruza dados de campanhas do Meta Ads com vendas da Kiwify via UTMs.

## Como usar

1. Acesse o sistema publicado na Vercel
2. Faça upload das 4 planilhas CSV:
   - **Campanhas** — export de campanhas do Meta Ads
   - **Conjuntos de anúncios** — export de adsets do Meta Ads
   - **Anúncios** — export de anúncios (nível criativo) do Meta Ads
   - **Vendas Kiwify** — export de vendas com UTMs
3. Configure a meta de CPA e o nome do produto front
4. Clique em **Gerar debriefing**

## O que o sistema entrega

- **Visão Geral** — totais consolidados de todas as campanhas + comparativo por segmento
- **Por segmento** — INLEAD, Página, INLEAD-2 com funil de mídia e faturamento
- **Todos os criativos** — ranking completo com filtros interativos
- **CPA ≤ meta** — criativos dentro do CPA alvo com filtros

## Filtros disponíveis (criativos)

- Busca por nome
- Formato (IMG / VID / BNR)
- Status CPA (Excelente / Dentro / Limítrofe / Acima)
- Segmento de origem
- Ordenação por vendas, CPA, ROAS, faturamento ou investimento

## Tecnologias

- HTML/CSS/JS puro — sem backend, sem dependências de servidor
- [PapaParse](https://www.papaparse.com/) — leitura de CSV no browser
- [Chart.js](https://www.chartjs.org/) — gráficos
- Os dados ficam **apenas no navegador do usuário** — nenhuma informação é enviada a servidores externos

## Deploy

Hospedado via [Vercel](https://vercel.com) como site estático.

```
├── index.html     # aplicação completa
├── vercel.json    # configuração de deploy
└── README.md      # este arquivo
```
