---
name: G7 Guinchos
description: Guincho 24h em São Paulo — site de conversão imediata em light mode, azul de marca e verde de ação.
colors:
  cloud-ground: "#F5F7FA"
  paper-surface: "#FFFFFF"
  mist-surface: "#EDF1F6"
  asphalt-ink: "#0E1B26"
  ink-muted: "rgba(14,27,38,.74)"
  ink-quiet: "rgba(14,27,38,.68)"
  hairline: "rgba(14,27,38,.10)"
  hairline-strong: "rgba(14,27,38,.20)"
  brand-deep: "#0F77B8"
  brand-sky: "#39B5FF"
  brand-tint: "rgba(15,119,184,.08)"
  brand-tint-2: "rgba(15,119,184,.16)"
  brand-pressed: "#0C639A"
  sky-ink: "#04121D"
  media-night: "#0B1116"
  online-green: "#1DA84E"
  whatsapp-green: "#25D366"
  whatsapp-pressed: "#1EB456"
  whatsapp-ink: "#04170C"
typography:
  display:
    fontFamily: "Barlow Condensed, system-ui, sans-serif"
    fontSize: "clamp(2.4rem, 4.6vw, 3.7rem)"
    fontWeight: 800
    lineHeight: 1.02
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "Barlow Condensed, system-ui, sans-serif"
    fontSize: "clamp(2rem, 4.4vw, 3.1rem)"
    fontWeight: 800
    lineHeight: 1.02
    letterSpacing: "-0.02em"
  title:
    fontFamily: "Barlow Condensed, system-ui, sans-serif"
    fontSize: "1.4rem"
    fontWeight: 800
    lineHeight: 1.02
    letterSpacing: "-0.02em"
  body:
    fontFamily: "Barlow, system-ui, -apple-system, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.65
  label:
    fontFamily: "Barlow Condensed, system-ui, sans-serif"
    fontSize: "1.02rem"
    fontWeight: 700
    letterSpacing: "0.1em"
rounded:
  soft: "10px"
  icon-box: "11px"
  duo: "12px"
  card: "14px"
  rail: "18px"
  pill: "999px"
spacing:
  gutter: "22px"
  card-gap: "18px"
  section: "92px"
  section-mobile: "66px"
components:
  button-wa:
    backgroundColor: "{colors.whatsapp-green}"
    textColor: "{colors.whatsapp-ink}"
    rounded: "{rounded.soft}"
    padding: "14px 26px"
    height: "52px"
  button-wa-hover:
    backgroundColor: "{colors.whatsapp-pressed}"
  button-brand:
    backgroundColor: "{colors.brand-deep}"
    textColor: "#FFFFFF"
    rounded: "{rounded.soft}"
    padding: "14px 26px"
    height: "52px"
  button-brand-hover:
    backgroundColor: "{colors.brand-pressed}"
  button-line:
    backgroundColor: "transparent"
    textColor: "{colors.asphalt-ink}"
    rounded: "{rounded.soft}"
    padding: "14px 26px"
    height: "52px"
  button-ghost:
    backgroundColor: "rgba(255,255,255,.10)"
    textColor: "#FFFFFF"
    rounded: "{rounded.soft}"
    padding: "14px 26px"
    height: "52px"
  button-ghost-hover:
    backgroundColor: "rgba(255,255,255,.20)"
  card:
    backgroundColor: "{colors.paper-surface}"
    rounded: "{rounded.card}"
  duo-item:
    backgroundColor: "{colors.cloud-ground}"
    textColor: "{colors.asphalt-ink}"
    rounded: "{rounded.duo}"
    padding: "20px 18px"
  chip-b2b:
    backgroundColor: "{colors.paper-surface}"
    textColor: "{colors.asphalt-ink}"
    typography: "{typography.label}"
    rounded: "{rounded.soft}"
    padding: "10px 20px"
    height: "52px"
---

# Design System: G7 Guinchos

## Overview

**Creative North Star: "Dois Caminhos"**

O mundo é o "G7 v5 light": chão claro azulado (#F5F7FA), superfícies brancas, tinta quase-preta azulada, e duas vozes de cor com papéis fixos — o azul da marca fala de confiança e operação (navegação, links, acentos, agendamento) e o verde fala de ação e presença ("estamos online, chama agora": WhatsApp e checkmarks). A primeira dobra encarna o North Star: um trilho escuro de emergência sobre **vídeo real da frota** sob véu, com telefone gigante e ação verde, ao lado de um trilho claro e quieto de agendamento com dois atalhos-card — fechados por uma faixa-marquise branca de logos de parceiros. O resto da página volta ao chão claro e mantém o azul como única voz de acento.

A personalidade é de operadora, não de guincheiro de esquina: números tabulares grandes, caps condensadas, prova fotográfica real em toda seção, zero decoração gratuita. A densidade é generosa (seções de 92px, corpo 17px/1.65) porque o leitor primário está estressado, no sol, no celular.

**Key Characteristics:**
- Light mode obrigatório; a única superfície escura é o véu de mídia do trilho de emergência (vídeo com fallback #0B1116).
- Verde = ação/presença; azul = marca/estrutura; nunca invertidos.
- Fotografia e vídeo 100% reais da frota — nenhuma imagem stock, nenhum ícone ilustrativo grande.
- Ícones sempre em stroke SVG inline (sprite `<symbol>`), 14–28px, traço 2–2.8.
- Hover levanta (-2px botões, -3px/-4px cards) e nada mais; reduced-motion desliga toda animação — marquee, carrossel de slides e o autoplay do vídeo.

## Colors

Paleta de duas vozes sobre neutros azulados frios: azul profundo estrutural, verde de ação, e uma escala de tinta única (#0E1B26) diluída em alfas para texto e linhas.

### Primary
- **Brand Deep** (#0F77B8): o acento estrutural do site — links, sublinhado do menu, círculos de ícone (duo e etapas de segurança), botão de parceria, scrollbar, números da faixa de estatísticas, filete da citação. É o azul que passa contraste AA sobre branco.
- **Brand Sky** (#39B5FF): o azul claro do logo. Só aparece sobre o véu escuro — destaque `<em>` dos slides do hero, hover do telefone gigante e fundo do selo-pill "24 horas".
- **Sky Ink** (#04121D): a tinta quase-preta usada como texto sobre Brand Sky (selo "24 horas") — nunca branco sobre o azul claro.
- **Brand Pressed** (#0C639A): estado hover/pressed de qualquer superfície azul sólida.
- **Brand Tints** (rgba(15,119,184,.08) e .16): lavagens de azul para fundos de ícone de contato, hover da faixa de stats, conectores das etapas e o gradiente da seção Segurança.

### Secondary
- **WhatsApp Green** (#25D366, hover #1EB456, texto #04170C): exclusivo de CTAs de WhatsApp — botão da navbar, CTA do hero, FAB, metade da dock mobile. Texto sobre ele é verde-quase-preto, nunca branco.
- **Online Green** (#1DA84E): o verde institucional de confirmação — todos os checkmarks de lista (círculo rgba(29,168,78,.13) no rail de agendamento). O dot pulsante com anel rgba(29,168,78,.18) segue definido no CSS como peça reservada de "online".

### Neutral
- **Cloud Ground** (#F5F7FA): fundo da página e de cartões sobre superfície branca (inversão deliberada: cartão claro sobre seção branca — `.duo-item`, `.cbox`, `.b2b-card`).
- **Paper Surface** (#FFFFFF): navbar, cards, faixa de stats, marquee de parceiros, rail de agendamento, footer.
- **Mist Surface** (#EDF1F6): fundos de placeholder de foto e trilha da scrollbar.
- **Media Night** (#0B1116): o backdrop do painel de vídeo do hero — a cor que aparece enquanto o vídeo carrega, atrás do filtro brightness(.48) contrast(1.15) saturate(.65). Nunca usada como superfície de UI fora da moldura de mídia.
- **Asphalt Ink** (#0E1B26): títulos e texto forte; base de todas as sombras e linhas via alfa; fundo dos badges numerados das etapas.
- **Ink Muted / Ink Quiet** (rgba .74 / .68): corpo de texto e legendas.
- **Hairlines** (rgba(14,27,38,.10) e .20): todas as bordas; a forte só em bordas interativas (botão outline, chips B2B).

### Named Rules
**The Two Voices Rule.** Verde é ação e presença (WhatsApp, online, confirmação); azul é marca e estrutura (navegação, agendamento, informação). Um CTA verde promete conversa imediata; um CTA azul promete processo. Nunca usar verde decorativamente nem azul num botão de WhatsApp.

**The One Ink Rule.** Não existem cinzas soltos: todo texto, linha e sombra deriva de #0E1B26 puro ou em alfa. Neutro novo = alfa novo da mesma tinta.

**The Dark Veil Rule.** Superfície escura só existe como mídia real sob véu: vídeo/foto com filter brightness(.48) contrast(1.15) saturate(.65), backdrop #0B1116 e gradiente rgba(8,14,19,.5→.24→.78). Não há dark mode nem painéis escuros chapados.

## Typography

**Display Font:** Barlow Condensed (600/700/800, com system-ui sans fallback)
**Body Font:** Barlow (400/500/600/700, com system-ui sans fallback)

**Character:** Condensada, alta e em caixa alta para tudo que titula — voz de caminhão, direta; o corpo Barlow normal é aberto e legível para quem lê no sol. O par é uma família só em duas larguras: coeso, sem ornamento.

### Hierarchy
- **Display** (800, clamp(2.4rem, 4.6vw, 3.7rem), 1.02): o h1 e os slides `.hx` do trilho de emergência, branco sobre o véu com text-shadow 0 2px 30px rgba(0,0,0,.55), máx. 14ch.
- **Headline** (800, clamp(2rem, 4.4vw, 3.1rem), 1.02): títulos de seção (`.title`), sempre com um trecho em `<em>` azul (#0F77B8) sem itálico. O h2 do trilho de agendamento é a versão contida (clamp(1.6rem, 2.6vw, 2.05rem)) — deliberadamente menor que o h1 vizinho.
- **Title** (800, 1.22–1.5rem, 1.02): títulos de card e de item (1.4rem card de serviço, 1.22rem duo e caixas de contato, 1.5rem b2b-card).
- **Body** (400, 17px desktop / 16px mobile, 1.65): parágrafos; leads a 1.08rem com máx. 62ch; corpo de card e legendas na faixa .88–.98rem (checklists .97–.98rem, small .88rem, footer .92rem, rótulos de stat .94rem).
- **Label** (700 condensada, .8–1.08rem, caixa alta, tracking positivo): wordmark (.17em, 1.04rem), rótulo do marquee (.14em, .8rem), nomes no marquee (.12em, 1.08rem), chips B2B (.1em, 1.02rem) — a exceção de tracking positivo num sistema de títulos com tracking negativo. O badge numerado das etapas usa a mesma condensada 800 a .8rem.
- **Números** (800 condensada, `font-variant-numeric: tabular-nums`): faixa de estatísticas a 2.6rem em azul (2.1rem abaixo de 400px); o telefone do hero a clamp(2rem, 3.4vw, 2.9rem) em branco, hover #39B5FF.

### Named Rules
**The Condensed Caps Rule.** Todo h1/h2/h3 é Barlow Condensed 800, uppercase, letter-spacing -0.02em, line-height 1.02. Título fora dessa fôrma não é deste mundo.

**The Blue Em Rule.** O destaque de um título é `<em>` com cor #0F77B8 (ou #39B5FF sobre escuro) e `font-style: normal` — cor no lugar de itálico, um trecho por título.

## Layout

Container único de 1180px (`--wrap`) com gutter de 22px (18px abaixo de 400px). Seções respiram 92px vertical (66px mobile) e alternam fundo: página clara → seção branca com hairlines top/bottom → página clara. Grids fixos no desktop (4 colunas de serviços, 3 etapas conectadas por traços de 40px, split 1.08fr/.92fr no hero com o marquee de parceiros em `grid-column: 1/-1` fechando a dobra, ~1fr/1fr em about, B2B e no duo de atalhos) que colapsam para 1 coluna em 980px; serviços passam por 2 colunas em 1100px. No colapso, o hero reordena por urgência: emergência (order 1) → marquee (order 2) → agendamento (order 3), e os conectores das etapas viram verticais. A faixa de estatísticas usa grid com gap de 1px sobre a cor da hairline — divisórias sem bordas.

Mobile-first de conversão: abaixo de 820px o menu e o botão WhatsApp da navbar somem e entra a dock fixa de duas ações (Ligar / WhatsApp, 62px de altura mínima); o FAB de WhatsApp some (a dock o substitui). `env(safe-area-inset-*)` em tudo que é fixo. Alvos de toque ≥44px em todo elemento interativo (min-height 44–52px é sistemático). Sem link de telefone na navbar (decisão do usuário, 24/08): o número gigante vive no hero.

## Elevation & Depth

Híbrido raso: hairlines fazem a estrutura, sombras fazem o convite. Todo card tem borda de 1px E sombra — a sombra nunca substitui a borda. CTAs sólidos carregam sombra colorida da própria cor (glow suave, não offset duro). Profundidade extra vem de hover: o elemento sobe (-2px/-3px/-4px) e troca shadow-1 por shadow-2. Sobre o véu, o texto ganha profundidade por text-shadow difuso (0 2px 30px rgba(0,0,0,.55)) — nunca por outline ou sombra dura.

### Shadow Vocabulary
- **Rest** (`--shadow-1: 0 1px 2px rgba(14,27,38,.05), 0 4px 14px -8px rgba(14,27,38,.10)`): cards e caixas em repouso, marquee.
- **Raised** (`--shadow-2: 0 4px 10px rgba(14,27,38,.06), 0 22px 40px -22px rgba(14,27,38,.28)`): rails do hero, foto de about, e estado hover de cards e duo-items.
- **CTA glow verde** (`0 10px 24px -12px rgba(37,211,102,.55)`; FAB: `0 12px 30px rgba(37,211,102,.4)`): sob botões WhatsApp.
- **CTA glow azul** (`0 10px 24px -12px rgba(15,119,184,.5)`; círculos de ícone: `0 8px 18px -8px rgba(15,119,184,.6)`): sob botões e círculos azuis sólidos.
- **Text veil** (`text-shadow: 0 2px 30px rgba(0,0,0,.55)`): exclusivo dos títulos brancos sobre o vídeo do hero.
- **Pulse ring** (`0 0 0 4px rgba(29,168,78,.18)` animado 2.4s): reservado ao dot "online" (definido no CSS).

### Named Rules
**The Border-And-Shadow Rule.** Superfície elevada = borda hairline de 1px + sombra da escala; nunca só uma das duas.

**The Colored Glow Rule.** Sombra colorida pertence exclusivamente a CTAs sólidos e círculos de ícone azuis, e carrega a cor da própria superfície em glow difuso com spread negativo — nunca sombra dura deslocada, nunca em cards.

## Shapes

Cantos suaves em escala fechada: 10px em botões e chips B2B, 11px em caixas de ícone de contato, 12px nos duo-items do rail de agendamento, 14px (`--r`) em cards, caixas e no marquee, 18px nos dois rails do hero, 999px no selo-pill "24 horas" e círculo pleno em FAB, dots, círculos de ícone (46–56px) e checkmarks (26px). Quanto maior a superfície, maior o raio. Bordas sempre 1px hairline (1.5px só no botão outline claro). Fotos vivem em molduras com aspect-ratio fixo (16/10 cards, 4/3 galeria e about) com `object-fit: cover`; hover dá zoom de 1.05 em .35s; recorte transparente usa `contain` sobre degradê claro (`.cut`). Assinatura de forma: a citação com filete esquerdo de 3px azul em Barlow Condensed caps (`.quote`) e o selo "24 horas" como expoente elevado do h1 (pill #39B5FF, texto #04121D, font-size .34em, translateY(-.25em)).

## Components

### Buttons
- **Shape:** cantos suaves (10px), min-height 52px, padding 14px 26px, peso 700 a 1.02rem, ícone SVG de 19–21px à esquerda (gap 10px).
- **WhatsApp (primário):** verde #25D366 com texto #04170C e glow verde; hover #1EB456.
- **Brand (secundário):** azul #0F77B8 com texto branco e glow azul; hover #0C639A.
- **Outline claro (`.btn-line`):** transparente, texto ink, borda 1.5px hairline forte; hover ganha fundo branco e borda ink. Só sobre superfície clara.
- **Ghost escuro (`.btn-ghost`):** o outline do véu — rgba(255,255,255,.10) com borda rgba(255,255,255,.45) e blur(4px), texto branco; hover clareia (.20, borda #fff). Só sobre o Dark Veil.
- **Hover / Focus:** todos sobem 2px; foco visível = outline 3px azul com offset 3px (global para links e botões).

### Chips (B2B / parceiros)
- **Style:** pastilha branca 52px, borda hairline forte, 10px de raio; conteúdo é logo SVG/PNG real (24px de altura, 32px para marcas quadradas `.sq`) ou nome em Barlow Condensed 700 caps tracking .1em.
- **State:** hover pinta borda e texto de azul; sem estado selecionado (são prova, não filtro).

### Cards / Containers
- **Corner Style:** 14px (12px nos duo-items).
- **Background:** branco sobre página clara; invertido (fundo #F5F7FA) quando o card senta em seção branca (`.cbox`, `.b2b-card`) ou no rail branco (`.duo-item`).
- **Shadow Strategy:** rest → raised no hover, com lift de -3px/-4px e borda esquentando para rgba(15,119,184,.4–.45).
- **Border:** 1px hairline, sempre.
- **Internal Padding:** 20px (texto de card de serviço, duo-item 20px 18px) a 28–32px (caixas maiores).
- **Card de serviço:** foto 16/10 no topo (zoom no hover), título condensado, uma linha de corpo, e link "Solicitar →" azul 700 cuja seta desliza 4px no hover do card.
- **Duo-item (atalho):** card 12px sobre fundo claro com círculo azul de 46px (ícone stroke branco, glow azul), título condensado 800 caps 1.22rem tracking .02em e uma linha `small` .88rem; o card inteiro é um link WhatsApp.

### Navigation
- **Navbar:** sticky, branco a 88% com blur(14px), hairline embaixo, 74px. Logo + wordmark condensada tracking .17em; links Barlow 600 com sublinhado azul de 2px que cresce da esquerda no hover; botão WhatsApp verde à direita (some no mobile). Sem link de telefone na navbar.
- **Mobile:** menu some; a dock fixa de 2 células (Ligar branco / WhatsApp verde, divididas por hairline de 1px via gap) assume o rodapé da tela.

### Split Hero — "Dois Caminhos" (signature)
Dois rails de 18px lado a lado (1.08fr/.92fr; empilha a 980px na ordem emergência → marquee → agendamento). O rail de emergência (min-height 470px, padding 30px 34px): vídeo real da frota fixo ao fundo (autoplay muted loop, object-position 50% 60%, pausado em reduced-motion) sobre backdrop #0B1116, sob o Dark Veil; por cima, carrossel CSS-only de 3 mensagens em fade (grid empilhado `1/1`, keyframe de 18s com delays de 6s/12s; reduced-motion mostra só a primeira). Conteúdo ancorado embaixo: título branco com text-shadow difuso, destaque #39B5FF e selo-pill "24 horas" elevado como expoente (fundo #39B5FF, texto #04121D), telefone gigante condensado clicável (clamp até 2.9rem) fixo sob os slides, CTA verde + ghost escuro. O rail de agendamento: superfície branca quieta, h2 ink contido, checklist verde (círculos 26px), e o duo de atalhos-card no rodapé. A hierarquia de cor E de luz codifica a urgência.

### Partner Marquee (signature)
Faixa branca de largura total dentro do split (`grid-column: 1/-1`): raio 14px, borda hairline, shadow-1, padding 13px 0, rótulo "Quem confia na G7" em caps condensadas .8rem tracking .14em. Loop infinito CSS-only — dois `.mq-grp` idênticos (o segundo `aria-hidden`) em track `width: max-content` animado `translateX(-50%)` em 30s linear; hover pausa, reduced-motion desliga. Máscaras de fade de 60px nas bordas via ::before/::after em gradiente da superfície. Conteúdo: logos reais a 26px de altura (38px marcas quadradas; 22/32px mobile, gap 56px→30px).

### Stat Band (signature)
Faixa branca entre hairlines, 4 células (2×2 a 980px) divididas por gap de 1px na cor da linha; número 800 condensado 2.6rem azul tabular (2.1rem abaixo de 400px) + rótulo .94rem em muted; hover lava a célula de brand-tint.

### Safe Steps (signature)
Três etapas conectadas (checklist → transporte → entrega): círculo azul de 56px com ícone stroke branco e glow azul, badge numerado `::after` via CSS counter (círculo ink 24px, condensada 800 .8rem), traço conector de 2px brand-tint-2 entre etapas (horizontal no desktop, vertical no colapso).

## Do's and Don'ts

### Do:
- **Do** manter todo contato a um toque em qualquer ponto: navbar com WhatsApp, FAB/dock, `tel:` e `wa` links por seção — CTAs verdes para "agora", azuis para "processo".
- **Do** usar só fotos e vídeo reais da frota, sempre dentro de moldura com aspect-ratio fixo ou véu, borda hairline e `object-fit: cover` (contain só para recortes transparentes sobre degradê).
- **Do** aplicar o padrão de hover completo: lift (-2px/-3px/-4px) + upgrade de sombra + transição .18–.22s, com tudo desligado em `prefers-reduced-motion` (inclusive marquee, carrossel de slides e autoplay do vídeo).
- **Do** escrever números de prova em Barlow Condensed 800 azul com `tabular-nums`.
- **Do** manter min-height ≥44px em qualquer alvo de toque e o focus ring azul de 3px.

### Don't:
- **Don't** criar dark mode ou painéis escuros chapados — escuro só existe como véu sobre mídia real (Dark Veil Rule); #0B1116 é backdrop de vídeo, não superfície de UI.
- **Don't** usar #39B5FF sobre fundo claro (não passa AA); sobre branco o azul é sempre #0F77B8.
- **Don't** colocar texto branco sobre o verde WhatsApp (texto #04170C) nem sobre o azul-céu (texto #04121D).
- **Don't** usar ícones preenchidos, icon fonts ou ilustrações — só o sprite SVG stroke inline (exceção única: o glifo oficial do WhatsApp, filled).
- **Don't** inventar claims visuais de prova (tempo de chegada, estrelas, depoimentos): a página só dramatiza números e fotos que existem.
- **Don't** usar sombra dura deslocada nem sombra colorida fora de CTA sólido ou círculo de ícone azul.
- **Don't** usar `.btn-line` sobre o véu escuro nem `.btn-ghost` sobre superfície clara — cada outline pertence ao seu fundo.
