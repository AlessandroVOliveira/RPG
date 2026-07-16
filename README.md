# RPG — Andor Duvane

Um personagem, duas edições do sistema: o mestre trocou de Tormenta20 para a edição clássica do Tormenta RPG, então o projeto guarda as duas versões separadas.

## Estrutura

```
personagens/
  andor-classico/    → Andor ATIVO — ficha, JSON e docs da build atual (Tormenta RPG clássico)
  andor-t20/          → Andor ARQUIVADO — versão anterior (Tormenta20), congelada
manuais-classico/     → PDFs oficiais da edição clássica (gitignorado, muito grande)
manuais-t20/           → PDFs oficiais de T20 (gitignorado, muito grande)
memorias/
  classico/            → regras da edição clássica extraídas dos PDFs, por tema
  t20/                  → regras de T20 extraídas dos PDFs, por tema (arquivado)
anotacoes/             → notas de sessão/aventura em .txt (compartilhado entre as duas versões)
Imagens/                → arte de referência visual do Andor (compartilhada)
```

## Uso rápido

- Jogar/editar a ficha ativa: ver `personagens/andor-classico/` (build em andamento).
- Consultar a versão antiga: `personagens/andor-t20/Ficha T20.html`.
- Consultar uma build ou decisão já tomada: `docs/` dentro da pasta de cada personagem.
- Consultar uma regra: `memorias/classico/` primeiro (ou `memorias/t20/` para a versão arquivada), PDF em `manuais-classico/`/`manuais-t20/` só se não estiver lá.
- Registrar o que aconteceu numa sessão: um `.txt` novo em `anotacoes/`.

## Portabilidade

`memorias/`, `personagens/` (fichas, JSONs, docs) e `anotacoes/` são leves e versionados no git. Os PDFs de `manuais-classico/` e `manuais-t20/` são grandes e ficam fora do repositório (`.gitignore`) — não são necessários para jogar, só para extrair regras ainda não documentadas em `memorias/`.
