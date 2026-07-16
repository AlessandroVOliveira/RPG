# CLAUDE.md — RPG (Tormenta20 / Andor Duvane)

## Estrutura do projeto

```
Ficha T20.html      → ficha de personagem interativa (abrir no navegador, funciona offline)
andor-t20.json       → dados do Andor Duvane, mesmo formato que a ficha lê/exporta/importa
manuais/              → PDFs oficiais (livro do jogador, livro de Arton, fichas em branco/impressas) — gitignorado, muito grande
docs/                 → builds e decisões do Andor em Markdown (atributos, progressão, raça/origem)
anotacoes/            → notas de sessão/aventura em .txt (uso livre do usuário)
memorias/             → regras de T20 já extraídas dos PDFs, organizadas por tema
```

## Fluxo de consulta de regras de Tormenta20

1. **Primeiro, procure em `memorias/*.md`.** É o resumo já extraído e validado — ler esses arquivos é rápido e não gasta tempo reabrindo um PDF de 108MB.
2. **Se não encontrar lá** (regra não coberta ainda, ou parece incompleta/desatualizada), consulte os PDFs em `manuais/`:
   - `Tormenta 20.pdf` — livro do jogador (regras, classes, raças, origens, perícias, poderes, equipamento).
   - `tormenta-rpg---o-mundo-de-arton.pdf` — livro de região/mundo.
3. **Para ler os PDFs, qualquer ferramenta/comando está liberado sem pedir confirmação antes** — `pdftotext`, `python3` (com PyPDF2 ou o que for necessário), `node` para conferir cálculos, etc. São operações locais e somente leitura sobre arquivos do próprio projeto. Isso já está refletido em `.claude/settings.json` (`Bash(pdftotext *)` e `Bash(python3 *)` permitidos).
4. **Depois de achar a informação no PDF, complemente e evolua os `.md` de `memorias/`** correspondentes — não deixe a resposta só na conversa. Adicione a regra nova no arquivo de tema certo (ou crie um novo arquivo de tema se não existir nenhum adequado) e atualize `memorias/README.md` se for um arquivo novo. Cite a página impressa do livro, como já é o padrão nos arquivos existentes.

## Coisas a lembrar

- Extração de texto de PDF com `pdftotext -layout` costuma embaralhar colunas de tabelas (aconteceu com a tabela de armas). Nesses casos, prefira `pdftotext -f <pág> -l <pág> "arquivo.pdf" -` (sem `-layout`, página isolada) e cruze duas extrações antes de cravar um número — ou marque explicitamente como não confirmado em vez de arriscar um valor errado.
- `manuais/` está no `.gitignore` — os PDFs não vão para o repositório. Só `memorias/`, `docs/`, a ficha e o JSON precisam ser versionados para o projeto continuar usável em outra máquina.
- "Despertar" e "Protetor Imortal" são conceitos homebrew do próprio jogador para o Andor, não termos do livro — não procure isso nos PDFs.
- nunca se mencione como co autor dos comits.