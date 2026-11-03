---
name: carrossel-blog
description: Transforma um post de blog de viagem em carrossel de Instagram no padrão V5E, com texto (H1 + corpo) por página, prompts do Nano Banana Pro, sugestão de foto para anexar e legenda pronta. Use na rotina diária do blog ou quando pedirem um carrossel a partir de um post.
---

# Carrossel a partir do blog — padrão V5E

Antes de escrever, leia o design system: `rede-v5e/design-system/carrossel-instagram.md`.

## 1. Fonte

Blog: `https://www.cvc.com.br/dicas-de-viagem/` (WordPress).

- Lista dos posts mais novos: `GET /dicas-de-viagem/wp-json/wp/v2/posts?per_page=15&_fields=id,date,link,title`
- Conteúdo de um post: `GET /dicas-de-viagem/wp-json/wp/v2/posts?include={id}&_fields=content`

O site bloqueia acesso direto pela nuvem. Leia pelo navegador embutido (browser pane) do computador vinculado: abra a home do blog e rode os `fetch` acima com a ferramenta de JavaScript da página.

## 2. Escolha do tópico

1. Ordene pelos **mais novos** (campo `date`).
2. Ignore os IDs que já estão em `rede-v5e/carrosseis/historico.md`.
3. Pegue o mais novo que se encaixa no público, nesta ordem de prioridade:
   - resorts (all inclusive, hotéis-resort, parques com hospedagem);
   - viagens internacionais (destinos, roteiros, quando ir);
   - educação de viagem (bagagem, regras de voo, documentos, normas, dicas de aeroporto).
4. Se nenhum post novo se encaixar, use o mais novo que ainda faça sentido para quem viaja a lazer. Só pule posts puramente institucionais (promoção da própria loja, cupom, evento).

## 3. Roteiro do carrossel

Tem no **máximo 10 páginas**.

- **Capa:** o tema como gancho, em forma de pergunta ou promessa.
- **Contexto:** 1 a 2 páginas (por que importa, como escolher, o erro mais comum).
- **Opções:** **uma por página**, numeradas, com o nome da opção e para quem funciona melhor.
- **Fechamento** opcional, só se couber.

Se houver opções demais, priorize as mais ligadas a resort ou internacional. O conteúdo é reescrito com nossas palavras, sem citar a fonte. Não invente fatos: tudo vem do post.

Para cada página, entregue:

- **H1** (até 7 palavras) e as **palavras em dourado** (1 a 3);
- **Corpo** (até 25 palavras);
- **Foto para anexar:** descrição objetiva do que procurar (cena, enquadramento, luz, parte de baixo calma para o texto);
- **Prompt Nano Banana Pro** completo, montado a partir do prompt base do design system, pronto para colar.

## 4. Legenda

Siga a regra de legenda do design system: gancho, valor, CTA para WhatsApp e hashtags.

## 5. Entrega

1. Salve em `rede-v5e/carrosseis/AAAA-MM-DD_slug-curto.md`, usando o modelo do primeiro arquivo da pasta.
2. Adicione uma linha em `rede-v5e/carrosseis/historico.md` com data, ID do post, título e arquivo.
3. Faça commit e push na `main` com a mensagem `carrossel: {título curto}`.
