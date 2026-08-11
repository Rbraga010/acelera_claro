# Rentabiliza.ai — Site · Changelog & Handoff para auditoria (copy + UI)
**Data:** 2026-08-11 · **Domínio:** https://rentabilizaai.gestaopulsarh.com.br

---

## ⚠️ LEIA PRIMEIRO — estado do versionamento
As alterações abaixo estão **NO AR na Vercel**, mas **NÃO estão commitadas no GitHub** (o deploy foi folder-deploy direto, sem token de push). O último commit do repo `Rbraga010/acelera_claro` (branch `main`) é:
- **`7783ea9`** — "Add proposta.html" · 22/07/2026 → **este commit é ANTERIOR a tudo que fizemos.**

Ou seja: o dev **não deve** partir do github (está desatualizado). Ele deve partir de **(a)** o ZIP da fonte atual que acompanha este doc, ou **(b)** o site vivo no domínio acima. Quando houver token de push, dá pra subir tudo e gerar o commit oficial.

---

## Stack & design system (pro auditor)
- HTML estático + Vercel. `vercel.json` tem `cleanUrls: true` (URLs sem `.html`).
- Tokens em `assets/brand/rentabiliza-tokens.css`.
- **Fontes:** Fraunces (display/títulos), Inter (corpo), JetBrains Mono (labels/números).
- **Cores:** Noite `#0D1117` · Papel `#F4F1E8` · Âmbar `#F4B93E` (protagonista) · Mint `#3DDC97` (só KPI positivo) · Coral `#FF6B47` (só humanização).

## Páginas do site
| Arquivo | O que é | Status |
|---|---|---|
| `index.html` | Capa/home institucional | **principal** |
| `proposta.html` | LP de proposta comercial (genérica) | ativa |
| `slides.html` | Apresentação executiva (base genérica) | ativa |
| `slides-claro/tim/motorola/levanci.html` | Versões por cliente da executiva | novas |
| `slides-varejo.html` | Apresentação parceiros comerciais | ativa |
| `entregaveis.html` | Apresentação de entregáveis | **nova** |
| `doc.html` | Business case | ativa |
| `escopo.html` | Modelo de negócio | ativa |
| `manifesto.html` | Manifesto da marca | ativa |
| `simulador.html` | Simulador de cenários | órfã (avaliar) |
| `escopo-doc.html` | Duplicata órfã de escopo.html | **LIXO — remover** |

---

## O que foi feito nesta rodada

### `index.html` (capa/home)
1. **Hero reescrita.** Headline: "Transformamos quem representa a sua empresa em quem *impulsiona o seu crescimento*." + sub + 3 bullets (Desenvolvemos / Transformamos / Criamos) + 2 CTAs (Fale com a gente / Conhecer o movimento).
2. **Fix do vídeo da hero.** Removido o atributo `media="(min-width:769px)"` do `<source>` (esse atributo quebrava o autoplay em Chrome/Safari). Desktop-only agora é só via CSS.
3. **Padronização de fontes** — escala reduzida ~20% (nos tokens + hardcoded).
4. **Removidos** os cards de apresentação da home.
5. **Adicionadas 9 sessões institucionais** (na ordem): Quem somos · No que acreditamos · O que entregamos · Como funciona · Nossos valores · Nossos números · Pra quem é · Painel Colaboradores · Vamos conversar. (TradeUp foi removido de toda a copy institucional.)
6. **Botão "🔒 Painel Colaboradores"** (fixo no topo + sessão própria) → modal com **senha `Pulsar@2026`** → menu:
   - Proposta comercial
   - Accordion "Apresentações Comerciais": **Claro** (ativa) · TIM / Motorola DIMO / Levanci Cowork (marcadas "em construção")
   - Apresentação de Entregáveis · Apresentação Parceiros · Business Case · Modelo de Negócio · Manifesto
   - ⚠️ Segurança: a senha é client-side (porta com trinco, não cofre). Pra material sensível, migrar pra login real.

### `proposta.html`
- Removidas **todas as 41 menções a "Claro"** + 2 logos → generalizado para "sua marca / da marca". A LP virou institucional (serve qualquer indústria).

### `slides.html` → versões por cliente
- Base genérica (slot "Preparado para « Marca Parceira »"). Geradas **4 versões** com o nome na capa: `slides-claro`, `slides-tim`, `slides-motorola`, `slides-levanci`. (Sem logos reais de TIM/Motorola/Levanci — só nome.)

### `entregaveis.html` (NOVA — a mais trabalhada)
Apresentação de entregáveis, na identidade do site:
- **Hero** → **01 · O conceito** (4 cards padronizados: Não somos curso · Instalamos 3 coisas · Um arsenal que escala · Feito com a sua marca) → **02 · A jornada** (Start / Master / Pro / Ultra, cada um em card de 3 colunas: *o que entregamos · na loja · sua marca ganha*) → **03 · O retorno** (risco reverso + ROI honesto).

---

## Pendências / o que o auditor deve olhar
- **Sincronizar github** (falta token) — prioridade se for versionar.
- **Deletar** `escopo-doc.html` (lixo).
- **Decidir** `simulador.html` (órfão).
- Revisar **responsividade mobile** (tabelas do entregaveis viram cards empilhados — validar em telas pequenas).
- Coerência de **copy** entre páginas antigas (doc, escopo, manifesto, slides ainda em tom telecom-Claro/antigo) e a capa+entregaveis (já no posicionamento novo institucional). **Recomendação: alinhar todas ao novo posicionamento.**
- Frase "sua camada" remanescente no card conceito 04 do entregaveis (só copy, não bug).

## Como pegar o estado atual
1. **Site vivo:** https://rentabilizaai.gestaopulsarh.com.br (e as páginas `/proposta`, `/entregaveis`, `/slides-claro` etc — sem `.html` por causa do cleanUrls).
2. **Fonte atual:** ZIP anexo (ou push pro github quando houver token).
