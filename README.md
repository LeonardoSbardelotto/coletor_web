# Coletor Web — Terminal Financeiro (B3 / BCB / CVM)

Repositório público responsável pela execução automatizada dos robôs de coleta de dados do mercado financeiro brasileiro via **GitHub Actions** (minutos gratuitos e ilimitados).

## 🚀 Workflows Automatizados

| Workflow | Frequência | Descrição | Arquivo de Saída |
|---|---|---|---|
| **Cotações B3** | A cada 30 min no pregão (10h05–18h35) | Coleta Ibovespa e ações com brapi | `data/cotacoes.json` |
| **Notícias Agora** | A cada 30 min (06h–23h) | Manchetes e notícias de impacto | `data/noticias-agora.json` |
| **Curva de Juros** | 4x ao dia em dias úteis | Curva DI e títulos públicos | `data/curva.json` |
| **Fechamento** | Dias úteis às 19h05 | Resumo do pregão e placar | `data/placar-termometro.json` |
| **Coletor CVM** | Terça a sábado às 07h17 | Fundos donos e captação líquida | `data/fundos-acoes.json` |
| **Monitor do Site** | A cada hora | Checagem de disponibilidade do terminal | `data/status.json` |

## 📦 Como os dados são consumidos
Os arquivos gerados na pasta `data/` podem ser lidos diretamente por qualquer frontend via:
`https://raw.githubusercontent.com/LeonardoSbardelotto/coletor_web/main/data/<arquivo>.json`
