# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Página estática única (index.html com CSS/JS inline), nginx em Docker, deploy via Coolify na VPS Contabo (deploy manual — clicar Deploy no painel após push). Sem framework; decisão herdada do codebase existente.

## Users

Primário (confirmado 24/08/2026): pessoa com veículo quebrado/acidentado em São Paulo — no celular, na rua, estressada, decidindo em segundos. Secundário: quem agenda transporte (leilão, oficina, transferência de pátio, mudança de veículo) e parceiros comerciais (e-mail para orçamentos e parcerias).

## Product Purpose

Converter a visita em contato imediato: WhatsApp com texto pré-preenchido ou ligação. Não há formulário nem checkout — o site existe para gerar a chamada. Sucesso = conversa iniciada no WhatsApp/telefone (ou chamado triado pelo chat 24h).

## Positioning

Frota própria com mais de 10 veículos cobrindo leves E pesados (plataformas + guincho pesado próprio) — a maioria dos concorrentes locais só faz leves. ~20 anos de operação em SP. **Mais de 120 reboques por dia** (confirmado pelo Gabriel, 24/08/2026) — escala de operadora, não de guincheiro de esquina. Presta serviço para seguradoras e assistências: Loovi, Porto Seguro, HDI Seguros, Bradesco, Itaú e Maxpar (confirmados pelo Gabriel em 24/08/2026; "HDI" corrigido de "HBI", "Maxpar" interpretado de "MAAXPART" — ambos ditados por voz). Transporte documentado: checklist na origem, amarração adequada por tipo de veículo, entrega com assinatura do responsável e foto. Já transportou Ferrari 458 e Ferrari 360 (fotos reais em assets/).

## Operating Context

Atendimento 24h, todos os dias. Canal principal: WhatsApp (11) 95125-1014; segundo WhatsApp (11) 97176-6491; telefones (11) 5043-9790 e (11) 97530-8004; e-mail g7guinchosadm@gmail.com; Instagram @g7_guinchos2. Chat 24h no site: widget JS → POST /api/chat → proxy nginx → webhook n8n (agente em construção; dados pessoais vão num mini-form que não passa pela LLM). Domínio g7guinchos.com ainda aponta pro WordPress antigo; migração pro nosso servidor pendente (domínio vence 09/09/2026).

## Capabilities and Constraints

Confirmado 24/08/2026 (entrevista):
- **Light mode é obrigatório** — decisão do Gabriel; o redesign moderniza dentro do fundo claro.
- **CTAs só WhatsApp/ligar** — sem formulário; textos pré-preenchidos por contexto (leve/pesado/emergência/agendamento).
- **Fotos 100% reais** — nunca stock. ⚠️ frota-pesado.jpg tem porta escrita "Saquete Guincho" — confirmar com o pai se é da frota antes de manter.
- **Conteúdo e seções do v5 preservados** (serviços, segurança, como funciona, frota, quem somos, contatos) — muda a roupa, não a história.
- **Chat 24h preservado** (pode ser reestilizado).
- Emergência (pessoa na rua) é a audiência nº 1 do redesign.
- **Nova seção obrigatória (pedido 24/08): "Para seguradoras e assistências"** — parceiros como Loovi, Porto Seguro, HBI. Sem logos oficiais em mãos: usar nomes em chips de texto até o Gabriel fornecer/autorizar logos.

## Brand Commitments

Logo G7 (G azul + 7 cinza; assets/logo-g7.png e icone-g7.png). Slogan: "Te atender é a nossa missão". Azul da marca (claro #39B5FF — não passa contraste AA sobre branco; azul profundo #0F77B8 usado como acento em fundo claro no v5). Verde = "online/atendendo agora" (pedido explícito do Gabriel). Light mode (ver acima).

## Evidence on Hand

Fotos reais em `assets/`: frota-hero.webp (Cargo plataforma, hero), frota.webp (frota reunida), frota-pesado.jpg (cavalo Volvo — ⚠️ confirmar), e as 7 recuperadas em 24/08: frota-hrv.webp, frota-duplo-evoque.webp (reboque duplo Evoque+Cruze), frota-duplo-fiesta.webp (duplo Fiesta+van), frota-cavalos.webp (2 cavalos mecânicos), frota-cargo-815.webp (plataforma inclinada), frota-ferrari-458.webp, frota-ferrari-360.webp.
Números reais: +20 anos, **+120 reboques/dia**, +10 veículos, 24h/7d, SP e região, RNTRC ativo. Parceiros reais (lista parcial): Loovi, Porto Seguro, HBI.
Logos oficiais em `assets/`: logo-loovi.svg, logo-porto.svg (sites das marcas), logo-hdi.png, logo-bradesco.svg, logo-itau.svg (Wikimedia Commons) — todos baixados 24/08/2026 a pedido do Gabriel.
**Ausências que não podem ser fabricadas:** tempo médio de chegada (não medido), depoimentos/avaliações de clientes (não coletados), preços. ⚠️ "MAAXPART" (ditado por voz) foi interpretado como **Maxpar** (empresa de assistências do Grupo Autoglass, maxpar.com) — chip de texto até o Gabriel confirmar a marca/enviar logo.

## Product Principles

1. Quem chega em emergência decide em segundos: o contato fica a um toque em qualquer ponto da página.
2. Prova real acima de adjetivo — foto da frota e números verdadeiros no lugar de autoelogio.
3. Nenhum claim inventado: sem tempo de chegada, nota ou depoimento que não exista.
4. Documentação (checklist → assinatura + foto) é o diferencial a dramatizar, não nota de rodapé.
5. Mobile-first de verdade: uma mão, sol na tela, pressa.

## Accessibility & Inclusion

Usuário sob estresse, ao ar livre, tela com reflexo: contraste alto, alvos de toque ≥44px, ações principais sem depender de hover, reduced-motion respeitado (já implementado no v5).
