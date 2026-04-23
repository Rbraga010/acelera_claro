# Claro Acelera

Proposta comercial — Programa de capacitação de parceiros Claro.

**Elaborado por Rodrigo Braga** · V2.0 · Abril 2026

---

## 📁 Estrutura

```
claro-acelera/
├── index.html           # Home: hero + 2 cards (Documento / Apresentação)
├── doc.html             # Documento completo (14 seções, sidebar + scroll-spy)
├── slides.html          # Apresentação executiva (13 slides, fullscreen, keyboard nav)
├── assets/
│   └── images/          # Imagens geradas no Google Flow / Nano Banana
│       └── README.md    # Lista de imagens + prompts + dimensões
├── vercel.json          # Config de deploy
└── README.md            # Este arquivo
```

---

## 🚀 Rodar local

Abrir `index.html` em qualquer navegador moderno. Não requer build step.

```bash
# macOS
open index.html

# Windows
start index.html

# Linux
xdg-open index.html
```

Também funciona por servidor estático:

```bash
# Node
npx serve .

# Python
python3 -m http.server 8000
```

---

## ⌨️ Atalhos da apresentação (`slides.html`)

| Tecla | Ação |
|---|---|
| `→` / `Espaço` / `Enter` | Próximo slide |
| `←` / `Backspace` | Slide anterior |
| `Home` | Voltar ao primeiro |
| `End` | Pular ao último |
| `F` | Alternar tela cheia |
| `Esc` | Sair da tela cheia |
| Clique na metade esquerda/direita | Prev/next |

---

## 🖼️ Imagens

Os HTMLs rodam **sem nenhuma imagem real** — há placeholders em CSS puro (gradiente + grain) nos pontos onde as fotos entram. Quando Rodrigo gerar as imagens reais no Flow/Nano Banana, basta salvá-las em `assets/images/` com os nomes exatos listados em `assets/images/README.md` e referenciá-las trocando os blocos `<div class="img-placeholder">` / `<div class="s-img">` por `<img src="assets/images/NOME.jpg">`.

8 imagens previstas:
1. `hero-main.jpg` — Capa (index + slide 1)
2. `avatar-parceiro.jpg` — Avatar (doc s4 + slide 4)
3. `ia-gentes-whatsapp.jpg` — Metodologia (doc s7)
4. `embaixador-selo.jpg` — Identidade e Selos (doc s13)
5. `time-loja.jpg` — 5 Dimensões (doc s6)
6. `dashboard-celular.jpg` — Empreendedor Sistêmico
7. `workshop-regional.jpg` — Workshops (doc s9 + slide 9)
8. `rodrigo-braga.jpg` — Rodapé doc + slide 13

Prompts completos em `assets/images/README.md`.

---

## 🌐 Deploy (Vercel)

### Opção 1 — CLI

```bash
npm install -g vercel
cd /caminho/para/claro-acelera
vercel login
vercel --prod
```

### Opção 2 — GitHub + dashboard

```bash
cd /caminho/para/claro-acelera
git init
git add .
git commit -m "Claro Acelera V2.0"
gh repo create claro-acelera --private --source=. --push
```

Então no dashboard do Vercel:
1. Import Project → GitHub → selecionar `claro-acelera`
2. Framework Preset: **Other**
3. Build Command: (deixar vazio)
4. Output Directory: (deixar vazio — raiz)
5. Deploy

Domínio automático: `claro-acelera.vercel.app`.

---

## ✅ Checklist antes de apresentar

- [ ] Abrir `index.html` e conferir hero + cards
- [ ] Abrir `doc.html` e testar scroll-spy + sumário lateral
- [ ] Abrir `slides.html`, testar setas do teclado + F (fullscreen)
- [ ] Gerar as 8 imagens no Flow/Nano Banana e substituir placeholders
- [ ] Testar em Chrome, Firefox, Safari e mobile (375px)
- [ ] Deploy no Vercel (opcional — pode apresentar local também)

---

## 🎨 Decisões de design

- **Paleta Claro Executivo:** vermelho `#ED1C24` + amarelo `#FFCD00` como acentos de energia sobre dark base (`#0B0B0E` / `#141418`) com dourado `#C5A572` como textura editorial premium
- **Tipografia:** Outfit (display/titles) + Inter (body) + Instrument Serif italic (accents editoriais)
- **Sem logo da Claro** (arquivo oficial não disponível ainda — usamos tipografia forte "Claro Acelera" + letra "C" estilizada)
- **Sem menção a "PulsarH.ai"** em nenhum arquivo voltado ao cliente
- **Assinatura única:** Rodrigo Braga

---

## 📐 Vocabulário-chave do programa

| Termo | Uso |
|---|---|
| **Claro Acelera** | Nome da iniciativa |
| **Empreendedor na Era da IA** | Figura central aspiracional |
| **IA.gentes** | Agentes de IA que trabalham na loja |
| **H.gente** | O humano do time |
| **5 Dimensões** | Conector, Hiperprodutivo, Humilde, Sistêmico, Humano |
| **PULSAR** | Metodologia de gestão (P-U-L-S-A-R) |
| **H** | Filtro de Humanização |
| **IA** | Potência de produtividade |
| **Parceiro Embaixador** | Parceiro top do programa |

---

## 👤 Autoria

Elaborado por **Rodrigo Braga**
Consultor e especialista em liderança e IA aplicada ao varejo
21 anos · R$1 bi em operação gerenciada · 4.500 pessoas lideradas
