# Prompt do Agente — Radar de Conteúdo

## Perfis monitorados

### Instagram
- rodrigobacellar_
- purplemetrics
- aerikalinhares
- ilanaberenholc
- shecorp.co
- personalbrandinggroup
- arthur.bender
- danielapersonalbranding
- bitstobrands
- galileunogueira
- marthaleonardis
- amandaholzer
- thatajunqueira_

### Sites
- https://www.brandingmag.com/

### LinkedIn
- linkedin.com/in/marcosmalagris
- linkedin.com/in/pcampos
- linkedin.com/in/thiagolatorre

## Notion — Configuração

Token: ntn_K15293387547clcrxmKwTNPSPapwvSEMrArdyVnG4jz67j
Database ID: 33605b27db8281569c01c3487707201b

## Propriedades do banco (nomes EXATOS)

| Campo | Nome da propriedade | Tipo | Opções válidas |
|-------|-------------------|------|----------------|
| Título | Título | title | — |
| Canal | Canal/Fonte | select | Instagram, LinkedIn, Newsletter, YouTube, Site/Blog, TikTok |
| Resumo | Resumo do Insight | rich_text | — |
| URL | URL da Fonte | url | — |
| Editoria | Editoria | select | Presença Estrutural, Ser Antes de Parecer, Liderança Visível, Vida que Sustenta Presença, Branding Corporativo sem Ilusão, Geral / Tendência |
| Aproveitamento | Aproveitamento | select | 🔥 Usar agora, 📌 Referência futura, ✅ Já usado, 🗑️ Descartar |
| Data | Data da Varredura | date | YYYY-MM-DD |

## Exemplo de curl

curl -s -X POST https://api.notion.com/v1/pages \
  -H "Authorization: Bearer ntn_K15293387547clcrxmKwTNPSPapwvSEMrArdyVnG4jz67j" \
  -H "Content-Type: application/json" \
  -H "Notion-Version: 2022-06-28" \
  -d '{"parent":{"database_id":"33605b27db8281569c01c3487707201b"},"properties":{"Título":{"title":[{"text":{"content":"TITULO AQUI"}}]},"Canal/Fonte":{"select":{"name":"Instagram"}},"Resumo do Insight":{"rich_text":[{"text":{"content":"RESUMO AQUI"}}]},"URL da Fonte":{"url":"https://url-aqui.com"},"Editoria":{"select":{"name":"Geral / Tendência"}},"Aproveitamento":{"select":{"name":"🔥 Usar agora"}},"Data da Varredura":{"date":{"start":"2026-04-13"}}}}'
