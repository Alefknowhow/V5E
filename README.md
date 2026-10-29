# V5E — Central de marketing das agências

Planejamentos, roteiros de vídeo, templates e skills das 4 agências atendidas. Cada agência tem sua pasta, e as particularidades de cada uma vão sendo registradas no README dela.

## Agências

| Agência | Foco | Clientes | Anúncios |
| --- | --- | --- | --- |
| [V5E Matriz](agencias/v5e-matriz/README.md) | Resorts all inclusive | Jataí e Goiânia (GO) | Performam bem em SP |
| [V5E Mell e Bruno](agencias/v5e-mell-bruno/README.md) | Pacotes para o Nordeste | Curitiba e região metropolitana | Saída de Curitiba |
| [V5E Ana e Anderson](agencias/v5e-ana-anderson/README.md) | A definir | Jataí e Goiânia (GO) | Rodando em SP |
| [Azul Viagens BC](agencias/azul-viagens-bc/README.md) | Mercado regional | Balneário Camboriú e região | Padrão muda em SP |

## Estrutura

```
agencias/
  v5e-matriz/            perfil, particularidades, campanhas e aprendizados
  v5e-mell-bruno/
  v5e-ana-anderson/
  azul-viagens-bc/
rede-v5e/
  campanhas/             campanhas compartilhadas pelas lojas Viagens 5 Estrelas
    black-friday-2026/
skills/
  roteiro-video-resort/  como criar roteiros de vídeo no padrão V5E
```

Regra: o que vale para uma agência só fica na pasta dela; o que é da rede Viagens 5 Estrelas inteira fica em `rede-v5e/`.

## Convenções

- **Arquivos de criativo:** `[DESTINO]_[PERÍODO]_[FORMATO]_[TIPO]_[VERSÃO]` (ex.: `ResortX_BF26_916_VID_V1`). Formato: 916, 45, 11, 169. Tipo: VID, IMG, CAR, UGC, DEP, OFR, INS. Variação regional: região após o destino (`ResortX_SP_BF26_916_VID_V1`).
- **Campanhas Meta:** `[OBJETIVO]|[REGIÃO]|[ORÇAMENTO]|[DURAÇÃO]|[POSICIONAMENTO]` (ex.: `WA|SP|CBO|23d|META`).
- **Conjuntos:** `[PÚBLICO]|[IDADE]|[SEXO]|[LOCAL]` (ex.: `ABERTO|28-60|A|SP`).
- **Anúncios:** `[OFERTA]|[DATA]|[VERSÃO]`.
