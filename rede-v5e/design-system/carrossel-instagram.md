# Design system — Carrossel Instagram (V5E)

Padrão visual dos carrosséis gerados a partir do blog. Toda arte é feita no **Nano Banana Pro editando uma foto anexada**: a foto é real e não se altera. O modelo só aplica o degradê e o texto por cima.

## Princípios

1. **A imagem manda.** Use foto limpa e clara, com céu aberto, luz natural e poucos elementos. O texto ocupa só a parte de baixo.
2. **Nunca inventar imagem.** A foto é sempre anexada. O prompt proíbe adicionar, remover ou alterar qualquer elemento da cena.
3. **Sem logos**, selos, ícones, marcas d'água, molduras ou @ na arte.
4. **Uma ideia por página.** Cada página tem um H1 e um corpo curto.

## Formato

| | |
| --- | --- |
| Proporção | 4:5 |
| Tamanho | 1080 × 1350 px |
| Páginas | 3 a **10 no máximo**, nunca mais |
| Margem lateral | 90 px (protege o corte 3:4 do grid do perfil) |
| Margem inferior | 120 px |
| Área de texto | da base até no máximo 45% da altura (y ≥ 740) |

## Paleta

| Papel | Cor | Hex |
| --- | --- | --- |
| Dourado (destaque) | dourado | `#C9A24A` |
| Marrom (degradê, apoio) | marrom café | `#3B2A1E` |
| Marrom profundo (base do degradê) | marrom quase preto | `#1C130C` |
| Palha (detalhe opcional) | palha | `#E9DCB8` |
| Texto | branco | `#FFFFFF` |

- O texto é sempre **branco**.
- As **palavras de destaque** do H1 ficam em **dourado** `#C9A24A`. Use 1 a 3 palavras por página, nunca a frase inteira.
- A palha só aparece em detalhes finos, como o fio acima do H1 e o "arraste" da capa. Nunca vai no texto principal.

## Degradê de contraste

- Fica atrás das letras, de baixo para cima, sempre linear vertical.
- A base usa `#1C130C` com 90% de opacidade, passa por `#3B2A1E` a 60% por volta de 30% da altura e chega a 0% (transparente) em 55–60% da altura.
- A metade de cima da foto fica 100% intacta, sem escurecer.
- Sem blur e sem caixa sólida atrás do texto.

## Tipografia

| Elemento | Fonte | Peso | Tamanho | Entrelinha | Cor |
| --- | --- | --- | --- | --- | --- |
| H1 capa | Playfair Display | Bold | 92–100 px | 1.05 | branco + dourado |
| H1 páginas | Playfair Display | Bold | 72–80 px | 1.1 | branco + dourado |
| Corpo | Montserrat | Regular | 34–38 px | 1.35 | branco |
| Numeração da opção (ex.: "01") | Montserrat | SemiBold | 30 px, espaçamento +8% | — | dourado |
| "Arraste →" (só na capa) | Montserrat | Medium | 26 px, CAIXA ALTA, espaçamento +12% | — | palha |
| Fio decorativo acima do H1 | — | 3 px de espessura, 80 px de largura | — | — | dourado |

- Alinhamento à esquerda em todas as páginas.
- O H1 tem até 7 palavras. O corpo tem até 25 palavras, em no máximo 3 linhas.

## Estrutura do carrossel

1. **Capa.** H1 com o gancho (o título do tema), um subtítulo de 1 linha e "Arraste →".
2. **Contexto.** 1 ou 2 páginas explicando por que o tema importa ou como escolher.
3. **Opções.** Uma opção por página, numerada ("01", "02"...). O H1 traz o nome da opção e o corpo diz para quem ela funciona melhor.
4. **Fechamento** (opcional, se couber nas 10). Resumo ou CTA leve ("Fale com um especialista"), sem logo.

Se o post tiver mais opções do que cabe, escolha as melhores para o público (resorts e viagens internacionais) e corte o resto. O limite de 10 páginas não muda.

## Foto de referência (o que anexar)

- Foto vertical, ou horizontal que aguente o corte 4:5.
- Clara e limpa: dia aberto, cores naturais, sem filtro pesado.
- A parte de baixo deve ser "calma" (mar, areia, piscina, calçada, céu) para receber o texto.
- Sem texto, logo ou marca d'água na foto.
- Pessoas só de costas ou ao longe, sem rosto em destaque.
- Fontes: banco do fornecedor ou resort, Unsplash, Pexels ou acervo próprio.

## Prompt base (Nano Banana Pro)

O prompt é escrito em inglês e o texto da arte fica em português, entre aspas. Troque só o que está entre `{ }`.

```
Edit the attached photo. Keep the photo exactly as it is: do not add, remove, move or alter any object, person, building, sky or color in the scene. Do not generate new scenery. Output 4:5, 1080x1350 px (crop/extend only if needed, without inventing content).

Only add these overlays:
1) A smooth vertical dark gradient from the bottom edge: #1C130C at 90% opacity at the bottom, #3B2A1E at 60% around 30% of the height, fading to fully transparent at about 58% of the height. The top half of the photo stays untouched.
2) Text, left-aligned, 90 px side margins, 120 px bottom margin, all inside the lower 45% of the image:
{BLOCO_DE_TEXTO}

Typography: headline in Playfair Display Bold, body in Montserrat Regular. Text color pure white #FFFFFF; highlighted words in gold #C9A24A. Crisp, correctly spelled Portuguese text with accents exactly as written.
No logos, no icons, no watermarks, no stickers, no borders, no extra text.
```

Bloco de texto da **capa**:

```
- Small gold line (80 px wide, 3 px thick) above the headline.
- Headline (96 px): "{H1}" — words "{DESTAQUE}" in gold #C9A24A, rest white.
- Subtitle (36 px, white): "{CORPO}"
- Bottom line (26 px, uppercase, letter-spacing 12%, color #E9DCB8): "ARRASTE →"
```

Bloco de texto das **páginas de contexto**:

```
- Small gold line (80 px wide, 3 px thick) above the headline.
- Headline (76 px): "{H1}" — words "{DESTAQUE}" in gold #C9A24A, rest white.
- Body (36 px, white, line height 1.35): "{CORPO}"
```

Bloco de texto das **páginas de opção**:

```
- Number label (30 px, Montserrat SemiBold, gold #C9A24A, letter-spacing 8%): "{NN}"
- Headline (76 px): "{H1}" — words "{DESTAQUE}" in gold #C9A24A, rest white.
- Body (36 px, white, line height 1.35): "{CORPO}"
```

## Legenda do Instagram

- 1ª linha: gancho que funcione antes do "mais".
- Depois, 3 a 6 linhas curtas com o valor do conteúdo.
- CTA para o WhatsApp ("Fale com um especialista no WhatsApp"), sem nome de consultor ou loja.
- 8 a 15 hashtags, misturando temas amplos (#viagem) e específicos (#grecia).
- Nunca citar a fonte do blog na arte ou na legenda. Reescreva o conteúdo com nossas palavras.
