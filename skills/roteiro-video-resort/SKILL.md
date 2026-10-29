---
name: roteiro-video-resort
description: Cria roteiros de vídeo 9:16 (Reels/Stories, anúncio Meta ou orgânico) para a Viagens 5 Estrelas no padrão V5E — cortes de material de resort, cards de cor sólida, motion, legenda e narração. Use ao pedir roteiro, copy ou narração de vídeo de resort all inclusive, campanha sazonal ou oferta do dia.
---

# Roteiro de vídeo de resort — padrão V5E

## Quem é o público

Cliente que **já conhece e já viaja para resort all inclusive**, principalmente famílias e grupos. Ele quer:

- a **melhor tarifa** (condição de pagamento, desconto, data);
- **acertar na escolha** do resort para o perfil dele;
- **atendimento de especialista**.

Nunca explique o que é all inclusive ("comida inclusa", "sem conta no fim do dia"). Fale de tarifa, condição, escassez e atendimento.

## O produto

Sempre **pacote aéreo: voo + hospedagem em resort all inclusive**. Deixe isso explícito em texto ou narração. Se a oferta for só hospedagem, diga "sem aéreo".

## Material e edição

O vídeo é montado só com **cortes do material fornecido pelos resorts** (resort, praia, piscina, quarto, restaurante, drone). Não há gravação própria.

- `[CENA]`: corte do material, 0,7 a 2,5s, com legenda.
- `[CARD]`: fundo de cor sólida com 1 a 3 palavras gigantes, 0,4 a 0,8s. Alterne cena e card para dar ritmo.
- Motion: entrada de impacto (escala 120% → 100%) ou palavra a palavra, sempre com efeito sonoro (whoosh, impacto, pop, tic-tac).
- Trilha tropical house ~120 BPM, cortes na batida. A música abaixa quando a narração entra.
- Ferramentas: ElevenLabs (narração pt-BR + efeitos) e Claude Code com Remotion (vídeo em código, textos como variáveis).

## Safe zone (Reels Meta, 1080×1920)

- Topo: **270 px** livres. Base: **672 px** livres. Laterais: **65 px**.
- Todo texto, preço, legenda e logo entre **y=270 e y=1248**.
- Legenda na faixa y≈1050–1200. Texto de card centralizado entre y≈600 e y≈1000; a cor do card pode ir até a borda.
- Stories sozinho permite base de 384 px, mas o padrão V5E usa sempre a regra do Reels.

## Copy

- Ganchos que funcionam: "Black Friday", "Esquenta Black Friday", "Oferta do dia", "Últimas unidades", "Seu resort all inclusive".
- Mensagens-base: "melhor condição/tarifa do ano", "pacotes completos com voo e hospedagem", "atendimento personalizado com especialistas", "reserve as férias da sua família", "unidades limitadas".
- **Escassez só real:** quartos, prazos e descontos vêm da operadora. Nunca invente número.
- CTA sempre para o WhatsApp ("Chame no WhatsApp", "Faça sua cotação"). Não dependa de grupo VIP: uma das lojas não tem.
- Anúncio compartilhado pelas 3 lojas: nada de nome de consultor ou loja específica.

## Narração (ElevenLabs)

- 2 a 3 palavras por segundo; vídeo de 15s comporta ~35 palavras.
- Números e horas por extenso, como devem ser falados ("dez vezes de mil e duzentos", "vinte e três e cinquenta e nove").
- Teste 2 ou 3 vozes; o resultado do anúncio decide.
- Toda peça tem versão **com e sem narração**. Sem narração: cards +0,2s, trilha mais alta, impacto sonoro em todo card.

## Formato de entrega

Cada roteiro é um `.md` com:

1. Tabela de metadados: período, função, formato/duração, versões, nome de arquivo.
2. Tabela do roteiro: `# | Tempo | Tipo | Imagem | Texto na tela`.
3. Narração.
4. Texto do anúncio, título e mensagem pré-preenchida (se for anúncio).
5. Variações (remarketing, sem narração).

Nome de arquivo: `[DESTINO]_[PERÍODO]_[FORMATO]_[TIPO]_[VERSÃO]` (ex.: `BlackFriday_BF26_916_VID_V1`).

## Exemplos

- `campanhas/black-friday-2026/videos/01-pre-black.md`
- `campanhas/black-friday-2026/videos/02-black-friday.md`
- `campanhas/black-friday-2026/videos/03-oferta-do-dia.md`
