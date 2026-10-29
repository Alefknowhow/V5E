# Vídeo 3 — Oferta do Dia (molde)

| | |
| --- | --- |
| Período | Todo dia, conforme a promoção da operadora |
| Função | Orgânico: status do WhatsApp, Stories, lista de transmissão, grupo (lojas que têm) |
| Formato | 9:16, ~10s |
| Arquivo | `{Resort}_{DDMM}_916_VID_OFR_V1` |

Não vai para o anúncio pago: trocar o criativo todo dia reinicia o aprendizado, e a promoção pode mudar no mesmo dia.

## Variáveis

| Campo | Exemplo |
| --- | --- |
| `{RESORT}` | Nome do resort |
| `{DESTINO}` | Punta Cana |
| `{XX}` | 30 |
| `{NOITES}` | 5 |
| `{ORIGEM}` | Florianópolis |
| `{PARCELA}` | 10x de R$ 1.200 |

## Roteiro

| # | Tempo | Tipo | Imagem | Texto na tela |
| --- | --- | --- | --- | --- |
| 1 | 0–0,6s | CARD | — | **OFERTA DO DIA** |
| 2 | 0,6–3s | CENA | Resort do dia, 2 cortes | {RESORT} · {DESTINO} |
| 3 | 3–3,6s | CARD | — | **{XX}% OFF** |
| 4 | 3,6–5,5s | CENA | Piscina ou praia do resort | Pacote aéreo · {NOITES} noites all inclusive |
| 5 | 5,5–7s | CENA | Quarto ou restaurante | Saindo de {ORIGEM} · a partir de {PARCELA} |
| 6 | 7–7,6s | CARD | — | **SÓ HOJE ATÉ 23:59** |
| 7 | 7,6–10s | CARD | — | **Chame no WhatsApp** + logo |

## Narração

> Oferta do dia: {resort}, em {destino}. Pacote com voo e {noites} noites all inclusive, saindo de {origem}, a partir de {parcela}. Só hoje, até as vinte e três e cinquenta e nove. Chama no WhatsApp.

Na ElevenLabs, escreva números por extenso como devem ser falados ("dez vezes de mil e duzentos").

## Rotina diária (~15 min)

1. Operadora solta a promoção → print ou texto da oferta.
2. Preencher as variáveis, puxar os cortes da biblioteca de resorts, gerar narração.
3. Exportar vídeo 9:16 + card estático (prompts do Nano Banana).
4. Publicar: status do WhatsApp e Stories das 3 lojas, lista de transmissão, grupo de quem tiver.
5. Ao vencer ou esgotar: repostar o card com "ESGOTADO" por cima.
