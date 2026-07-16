# CLAUDE.md — RPG (Andor Duvane)

## Estrutura do projeto

```
personagens/
  andor-classico/    → Andor ATIVO (Tormenta RPG, edição clássica pré-T20 — a que o mestre usa agora)
  andor-t20/          → Andor ARQUIVADO (Tormenta20 — não joga mais nesta edição, mantido de referência)
manuais-classico/     → PDFs oficiais da edição clássica (módulo básico, manuais de classe, bestiários etc.) — gitignorado, muito grande
manuais-t20/           → PDFs oficiais de T20 (livro do jogador, livro de Arton, fichas em branco/impressas) — gitignorado, muito grande
anotacoes/             → notas de sessão/aventura em .txt (uso livre do usuário, compartilhado entre as duas versões)
memorias/
  classico/            → regras da edição clássica já extraídas dos PDFs, organizadas por tema (é onde extrair regras novas a partir de agora)
  t20/                  → regras de T20 já extraídas dos PDFs (arquivado junto com andor-t20)
Imagens/                → arte de referência visual do Andor, compartilhada entre as duas versões, evolui conforme a aventura avança
```

Cada pasta em `personagens/` tem seu próprio README explicando o que contém. `personagens/andor-classico/` é onde o trabalho novo acontece; `personagens/andor-t20/` está congelado.

## Fluxo de consulta de regras

O sistema em uso agora é a **edição clássica do Tormenta RPG** (personagem em `personagens/andor-classico/`). Salvo indicação contrária do usuário, qualquer pergunta de regra é sobre esta edição.

1. **Primeiro, procure em `memorias/classico/*.md`.** É o resumo já extraído e validado — ler esses arquivos é rápido e não gasta tempo reabrindo um PDF grande.
2. **Se não encontrar lá** (regra não coberta ainda, ou parece incompleta/desatualizada), consulte os PDFs em `manuais-classico/` — ver `memorias/classico/README.md` para o índice de qual livro cobre qual assunto (módulo básico, manual das raças, manual do combate/arcano/devoto/malandro, compilado de talentos, guia de armas/armaduras/escudos, bestiários etc.).
3. **Para ler os PDFs, qualquer ferramenta/comando está liberado sem pedir confirmação antes** — `pdftotext`, `python3` (com PyPDF2 ou o que for necessário), `node` para conferir cálculos, etc. São operações locais e somente leitura sobre arquivos do próprio projeto. Isso já está refletido em `.claude/settings.json` (`Bash(pdftotext *)` e `Bash(python3 *)` permitidos).
4. **Depois de achar a informação no PDF, complemente e evolua os `.md` de `memorias/classico/`** correspondentes — não deixe a resposta só na conversa. Adicione a regra nova no arquivo de tema certo (ou crie um novo arquivo de tema se não existir nenhum adequado) e atualize `memorias/classico/README.md` se for um arquivo novo. Cite a página impressa do livro, como já é o padrão nos arquivos de `memorias/t20/`.

Só consulte `memorias/t20/` ou `manuais-t20/` se o usuário perguntar especificamente pela versão antiga/arquivada do personagem.

## Coisas a lembrar

- Extração de texto de PDF com `pdftotext -layout` costuma embaralhar colunas de tabelas (aconteceu com a tabela de armas de T20). Nesses casos, prefira `pdftotext -f <pág> -l <pág> "arquivo.pdf" -` (sem `-layout`, página isolada) e cruze duas extrações antes de cravar um número — ou marque explicitamente como não confirmado em vez de arriscar um valor errado.
- `manuais-classico/` e `manuais-t20/` estão no `.gitignore` — os PDFs não vão para o repositório. Só `memorias/`, `personagens/` (fichas, JSONs, docs) precisam ser versionados para o projeto continuar usável em outra máquina.
- Os atributos base do Andor são fixos nas duas versões (rolados nos dados, ordenados): **17, 15, 13, 12, 12, 11**. O que muda entre `andor-t20` e `andor-classico` é raça, classe, perícias, talentos/poderes e equipamento — não os valores rolados.
- "Despertar" e "Protetor Imortal" são conceitos homebrew do próprio jogador para o Andor, não termos de nenhum livro — não procure isso nos PDFs.
- Imagens novas em `Imagens/` costumam chegar como PNG grande (várias MB, gerado por IA). Antes de commitar, comprimir para JPEG qualidade ~88 (cai pra ~10% do tamanho, sem perda visível) e apagar o PNG original — não versionar o PNG bruto.
- nunca se mencione como co autor dos comits.
