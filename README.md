# RPG — Andor Duvane (Tormenta20)

## Estrutura

```
Ficha T20.html      → ficha de personagem interativa (abrir no navegador, funciona offline)
andor-t20.json       → dados do Andor Duvane, mesmo formato que a ficha lê/exporta/importa
manuais/              → PDFs oficiais (livro do jogador, livro de Arton, fichas em branco) + fichas impressas
docs/                 → anotações e builds em Markdown (atributos, progressão, raça/origem do Andor)
anotacoes/            → notas de sessão/aventura em .txt (uso livre)
memorias/             → resumo das regras de T20 extraídas dos PDFs, pra não ter que reabri-los toda hora
```

## Uso rápido

- Jogar/editar a ficha: abra `Ficha T20.html` no navegador.
- Consultar uma build ou decisão já tomada: `docs/`.
- Consultar uma regra (fórmula de perícia, tabela de poderes, equipamento): `memorias/` primeiro, PDF em `manuais/` só se não estiver lá.
- Registrar o que aconteceu numa sessão: um `.txt` novo em `anotacoes/`.

## Portabilidade

`memorias/`, `docs/`, `Ficha T20.html` e `andor-t20.json` são leves e foram pensados para ir num repositório git. Os PDFs de `manuais/` são grandes (o livro do jogador sozinho tem ~108MB) — considere não versioná-los (`.gitignore`) se o repositório remoto tiver limite de tamanho.
