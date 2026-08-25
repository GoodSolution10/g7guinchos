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
  chip: "11px"
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

O mundo é o "G7 v5 light": chão claro azulado (#F5F7FA), superfícies brancas, tinta quase-preta azulada, e duas vozes de cor com papéis fixos — o azul da marca fala de confiança e operação (navegação, links, acentos, agendamento) e o verde fala de ação e presença ("estamos online, chama agora": WhatsApp, dot pulsante, checkmarks). A primeira dobra encarna o North Star: um trilho escuro de emergência sobre foto real da frota, com ação verde, ao lado de um trilho claro e quieto de agendamento — fechados por uma faixa-marquise branca de logos de parceiros. O resto da página volta ao chão claro e mantém o azul como única voz de acento.

A personalidade é de operadora, não de guincheiro de esquina: números tabulares grandes, caps condensadas, prova fotográfica real em toda seção, zero decoração gratuita. A densidade é generosa (seções de 92px, corpo 17px/1.65) porque o leitor primário está estressado, no sol, no celular.

**Key Characteristics:**
- Light mode obrigatório; a única superfície escura é o véu fotográfico do trilho de emergência.
- Verde = ação/presença; azul = marca/estrutura; nunca invertidos.
- Fotografia 100% real da frota — nenhuma imagem stock, nenhum ícone ilustrativo grande.
- Ícones sempre em stroke SVG inline (sprite `<symbol>`), 16–28px, traço 2–2.8.
- Hover levanta (-2px botões, -4px cards) e nada mais; reduced-motion desliga toda animação, inclusive o marquee.

## Colors

Paleta de duas vozes sobre neutros azulados frios: azul profundo estrutural, verde de ação, e uma escala de tinta única (#0E1B26) diluída em alfas para texto e linhas.

### Primary
- **Brand Deep** (#0F77B8): o acento estrutural do site — links, ícones de contato, botão "Agendar", scrollbar, sublinhado do menu, números da faixa de estatísticas, filete da citação. É o azul que passa contraste AA sobre branco.
- **Brand Sky** (#39B5FF): o azul claro do logo. Só aparece sobre fundo escuro (destaque "sai agora" e selo "24 horas" no hero) porque não passa AA sobre branco.
- **Brand Pressed** (#0C639A): estado hover/pressed de qualquer superfície azul sólida.
- **Brand Tints** (rgba(15,119,184,.08) e .16): lavagens de azul para fundos de ícone, chips do chat, hover da faixa de stats e o gradiente da seção Segurança.

### Secondary
- **WhatsApp Green** (#25D366, hover #1EB456, texto #04170C): exclusivo de CTAs de WhatsApp — botão principal, FAB, metade da dock mobile. Texto sobre ele é verde-quase-preto, nunca branco.
- **Online Green** (#1DA84E): o verde institucional de "atendendo agora" — dot pulsante e todos os checkmarks de lista.

### Neutral
- **Cloud Ground** (#F5F7FA): fundo da página e de cartões sobre superfície branca (inversão deliberada: cartão claro sobre seção branca).
- **Paper Surface** (#FFFFFF): navbar, cards, faixa de stats, marquee de parceiros, rail de agendamento, footer.
- **Mist Surface** (#EDF1F6): fundos de placeholder de foto, cabeçalho/rodapé do chat, bolhas do bot.
- **Asphalt Ink** (#0E1B26): títulos e texto forte; base de todas as sombras e linhas via alfa.
- **Ink Muted / Ink Quiet** (rgba .74 / .68): corpo de texto e legendas.
- **Hairlines** (rgba(14,27,38,.10) e .20): todas as bordas; a forte só em bordas interativas (botão outline, inputs, chips B2B).

### Named Rules
**The Two Voices Rule.** Verde é ação e presença (WhatsApp, online, confirmação); azul é marca e estrutura (navegação, agendamento, informação). Um CTA verde promete conversa imediata; um CTA azul promete processo. Nunca usar verde decorativamente nem azul num botão de WhatsApp.

**The One Ink Rule.** Não existem cinzas soltos: todo texto, linha e sombra deriva de #0E1B26 puro ou em alfa. Neutro novo = alfa novo da mesma tinta.

**The Dark Veil Rule.** Superfície escura só existe como foto real sob véu (brightness(.48) contrast(1.15) saturate(.65) + gradiente rgba(8,14,19,…)). Não há dark mode nem painéis escuros chapados.

## Typography

**Display Font:** Barlow Condensed (600/700/800, com system-ui sans fallback)
**Body Font:** Barlow (400/500/600/700, com system-ui sans fallback)

**Character:** Condensada, alta e em caixa alta para tudo que titula — voz de caminhão, direta; o corpo Barlow normal é aberto e legível para quem lê no sol. O par é uma família só em duas larguras: coeso, sem ornamento.

### Hierarchy
- **Display** (800, clamp(2.4rem, 4.6vw, 3.7rem), 1.02): só o h1 do trilho de emergência, branco sobre o véu, máx. 14ch.
- **Headline** (800, clamp(2rem, 4.4vw, 3.1rem), 1.02): títulos de seção (`.title`), sempre com um trecho em `<em>` azul (#0F77B8) sem itálico. O h2 do trilho de agendamento é a versão contida (clamp(1.6rem, 2.6vw, 2.05rem)) — deliberadamente menor que o h1 vizinho.
- **Title** (800, 1.22–1.5rem, 1.02): títulos de card e de item.
- **Body** (400, 17px desktop / 16px mobile, 1.65): parágrafos; leads a 1.08rem com máx. 62ch.
- **Label** (700 condensada, ~1rem, caixa alta, tracking .1–.17em): wordmark (.17em), chips B2B (.1em), nomes no marquee (.12em), chat-fab (.06em) — a exceção de tracking positivo num sistema de títulos com tracking negativo.
- **Números** (800 condensada, 2.6rem, `font-variant-numeric: tabular-nums`): faixa de estatísticas em azul; o telefone do hero a clamp(2rem…2.9rem) em branco.

### Named Rules
**The Condensed Caps Rule.** Todo h1/h2/h3 é Barlow Condensed 800, uppercase, letter-spacing -0.02em, line-height 1.02. Título fora dessa fôrma não é deste mundo.

**The Blue Em Rule.** O destaque de um título é `<em>` com cor #0F77B8 (ou #39B5FF sobre escuro) e `font-style: normal` — cor no lugar de itálico, um trecho por título.

## Layout

Container único de 1180px (`--wrap`) com gutter de 22px (18px abaixo de 400px). Seções respiram 92px vertical (66px mobile) e alternam fundo: página clara → seção branca com hairlines top/bottom → página clara. Grids fixos no desktop (4 colunas de serviços, 3 etapas, split 1.08fr/.92fr no hero com o marquee de parceiros em `grid-column: 1/-1` fechando a dobra, ~1fr/1fr em about e B2B) que colapsam para 1 coluna em 980px; serviços passam por 2 colunas em 1100px. No colapso, o hero reordena por urgência: emergência (order 1) → marquee (order 2) → agendamento (order 3). A faixa de estatísticas usa grid com gap de 1px sobre a cor da hairline — divisórias sem bordas.

Mobile-first de conversão: abaixo de 820px o menu da navbar some e entra a dock fixa de duas ações (Ligar / WhatsApp, 62px de altura mínima); o FAB de WhatsApp some (a dock o substitui) e o chat-fab sobe. `env(safe-area-inset-*)` em tudo que é fixo. Alvos de toque ≥44px em todo elemento interativo (min-height 44–52px é sistemático).

## Elevation & Depth

Híbrido raso: hairlines fazem a estrutura, sombras fazem o convite. Todo card tem borda de 1px E sombra — a sombra nunca substitui a borda. CTAs sólidos carregam sombra colorida da própria cor (glow suave, não offset duro). Profundidade extra vem de hover: o elemento sobe (-2px/-4px) e troca shadow-1 por shadow-2.

### Shadow Vocabulary
- **Rest** (`--shadow-1: 0 1px 2px rgba(14,27,38,.05), 0 4px 14px -8px rgba(14,27,38,.10)`): cards e caixas em repouso.
- **Raised** (`--shadow-2: 0 4px 10px rgba(14,27,38,.06), 0 22px 40px -22px rgba(14,27,38,.28)`): rails do hero, foto de about, e estado hover de cards.
- **CTA glow verde** (`0 10px 24px -12px rgba(37,211,102,.55)`; FAB: `0 12px 30px rgba(37,211,102,.4)`): sob botões WhatsApp.
- **CTA glow azul** (`0 10px 24px -12px rgba(15,119,184,.5)`; chat-fab: `0 12px 30px rgba(15,119,184,.38)`): sob botões azuis sólidos.
- **Pulse ring** (`0 0 0 4px rgba(29,168,78,.18)` animado 2.4s): exclusivo do dot "online".

### Named Rules
**The Border-And-Shadow Rule.** Superfície elevada = borda hairline de 1px + sombra da escala; nunca só uma das duas.

**The Colored Glow Rule.** Sombra colorida pertence exclusivamente a CTAs sólidos e carrega a cor do próprio botão em glow difuso com spread negativo — nunca sombra dura deslocada, nunca em cards.

## Shapes

Cantos suaves em escala fechada: 10px em botões e chips B2B, 11px em caixas de ícone e inputs do chat, 14px (`--r`) em cards, caixas e no marquee, 18px nos dois rails do hero e no painel do chat, 999px em pills (selo "24 horas", chat-fab, chips do chat) e círculo pleno em FAB, dots e ícones de etapa. Quanto maior a superfície, maior o raio. Bordas sempre 1px hairline (1.5px só no botão outline claro). Fotos vivem em molduras com aspect-ratio fixo (16/10 cards, 4/3 galeria e about, 16/5 no rail de agendamento) com `object-fit: cover`; hover dá zoom de 1.05 em .35s. As bolhas do chat achatam o canto do lado do remetente (15px → 5px). Assinatura de forma: a citação com filete esquerdo de 3px azul em Barlow Condensed caps (`.quote`).

## Components

### Buttons
- **Shape:** cantos suaves (10px), min-height 52px, padding 14px 26px, peso 700, ícone SVG de 19–21px à esquerda (gap 10px).
- **WhatsApp (primário):** verde #25D366 com texto #04170C e glow verde; hover #1EB456.
- **Brand (secundário):** azul #0F77B8 com texto branco e glow azul; hover #0C639A.
- **Outline claro (`.btn-line`):** transparente, texto ink, borda 1.5px hairline forte; hover ganha fundo branco e borda ink. Só sobre superfície clara.
- **Ghost escuro (`.btn-ghost`):** o outline do véu — rgba(255,255,255,.10) com borda rgba(255,255,255,.45) e blur(4px), texto branco; hover clareia (.20, borda #fff). Só sobre o Dark Veil.
- **Hover / Focus:** todos sobem 2px; foco visível = outline 3px azul com offset 3px (global para links e botões).

### Chips (B2B / parceiros)
- **Style:** pastilha branca 52px, borda hairline forte, 10px de raio; conteúdo é logo SVG/PNG real (~24–30px de altura) ou nome em Barlow Condensed 700 caps tracking .1em.
- **State:** hover pinta borda e texto de azul; sem estado selecionado (são prova, não filtro).

### Cards / Containers
- **Corner Style:** 14px.
- **Background:** branco sobre página clara; invertido (fundo #F5F7FA) quando o card senta em seção branca (`.cbox`, `.b2b-card`).
- **Shadow Strategy:** rest → raised no hover, com lift de -4px e borda esquentando para rgba(15,119,184,.4).
- **Border:** 1px hairline, sempre.
- **Internal Padding:** 20px (texto de card de serviço) a 28–32px (caixas maiores).
- **Card de serviço:** foto 16/10 no topo (zoom no hover), título condensado, uma linha de corpo, e link "Solicitar →" azul 700 cuja seta desliza 4px no hover do card.

### Inputs / Fields (chat)
- **Style:** fundo branco, borda 1px hairline forte, raio 10–11px, min-height 46px.
- **Focus:** borda vira azul #0F77B8, sem glow.

### Navigation
- **Navbar:** sticky, branco a 88% com blur(14px), hairline embaixo, 74px. Logo + wordmark condensada tracking .17em; links Barlow 600 com sublinhado azul de 2px que cresce da esquerda no hover; botão WhatsApp verde à direita. Sem link de telefone na navbar (decisão do usuário): o número gigante vive no hero e a dock mobile dá o "Ligar".
- **Mobile:** menu some; a dock fixa de 2 células (Ligar branco / WhatsApp verde, divididas por hairline de 1px via gap) assume o rodapé da tela.

### Split Hero — "Dois Caminhos" (signature)
Dois rails de 18px lado a lado (1.08fr/.92fr; empilha a 980px na ordem emergência → marquee → agendamento). O rail de emergência (min-height 470px, padding 30px 34px): foto real da frota sob o Dark Veil (object-position ajustada por foto), conteúdo ancorado embaixo, h1 branco com destaque #39B5FF e selo-pill "24 horas" elevado como expoente (fundo #39B5FF, texto #04121D), telefone gigante condensado clicável, CTA verde + ghost escuro. O rail de agendamento: superfície branca quieta, h2 ink contido, checklist verde, foto 16/5, CTA azul + outline claro. A hierarquia de cor E de luz codifica a urgência.

### Partner Marquee (signature)
Faixa branca de largura total dentro do split (`grid-column: 1/-1`): raio 14px, borda hairline, shadow-1, padding 13px 0. Loop infinito CSS-only — dois `.mq-grp` idênticos (o segundo `aria-hidden`) em track `width: max-content` animado `translateX(-50%)` em 30s linear; hover pausa, reduced-motion desliga. Máscaras de fade de 60px nas bordas via ::before/::after em gradiente da superfície. Conteúdo: logos reais a 26px de altura (22px mobile, gap 56px→36px) e nomes sem logo em Barlow Condensed 700 caps tracking .12em.

### Stat Band (signature)
Faixa branca entre hairlines, 4 células divididas por gap de 1px na cor da linha; número 800 condensado 2.6rem azul tabular + rótulo pequeno em muted; hover lava a célula de brand-tint.

## Do's and Don'ts

### Do:
- **Do** manter todo contato a um toque em qualquer ponto: navbar com WhatsApp, FAB/dock, `tel:` e `wa` links por seção — CTAs verdes para "agora", azuis para "processo".
- **Do** usar só fotos reais da frota, sempre dentro de moldura com aspect-ratio fixo, borda hairline e `object-fit: cover`.
- **Do** aplicar o padrão de hover completo: lift (-2px/-4px) + upgrade de sombra + transição .18–.22s, com tudo desligado em `prefers-reduced-motion` (inclusive o marquee).
- **Do** escrever números de prova em Barlow Condensed 800 azul com `tabular-nums`.
- **Do** manter min-height ≥44px em qualquer alvo de toque e o focus ring azul de 3px.

### Don't:
- **Don't** criar dark mode ou painéis escuros chapados — escuro só existe como véu sobre foto real (Dark Veil Rule).
- **Don't** usar #39B5FF sobre fundo claro (não passa AA); sobre branco o azul é sempre #0F77B8.
- **Don't** colocar texto branco sobre o verde WhatsApp — o texto é #04170C.
- **Don't** usar ícones preenchidos, icon fonts ou ilustrações — só o sprite SVG stroke inline (exceção única: o glifo oficial do WhatsApp, filled).
- **Don't** inventar claims visuais de prova (tempo de chegada, estrelas, depoimentos): a página só dramatiza números e fotos que existem.
- **Don't** usar sombra dura deslocada nem sombra colorida fora de CTA sólido.
- **Don't** usar `.btn-line` sobre o véu escuro nem `.btn-ghost` sobre superfície clara — cada outline pertence ao seu fundo.
