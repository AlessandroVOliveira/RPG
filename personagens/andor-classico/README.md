# Andor Duvane — Tormenta RPG clássico (ativo)

Andor Duvane para a edição clássica do Tormenta RPG (a que o mestre vai usar na mesa a partir de agora), substituindo a versão T20 arquivada em `personagens/andor-t20/`.

**Build 1º nível fechada** — Humano Guerreiro, mesmo conceito "Protetor Imortal" da versão T20. Ver `docs/Andor Duvane — Guerreiro Humano (Tormenta RPG clássico).md` para a decisão completa (atributos, raça, classe, equipamento, talentos) e `andor-classico.json` para os dados estruturados.

## O que se mantém

Atributos base, rolados nos dados, ordenados: **17, 15, 13, 12, 12, 11** — idênticos à versão T20, com a mesma alocação (+2 racial em Força e Constituição).

## Resumo da build

- **Raça:** Humano (+2 For/+2 Con, 2 talentos extras, 2 perícias treinadas extras)
- **Classe:** Guerreiro (BBA cheio, PV 20+Con, Técnica de Luta a cada 2 níveis)
- **Equipamento inicial:** Espada Longa + Escudo pesado + Brunea (armadura média) — armadura pesada completa fica pra quando puder pagar (1.500 TO)
- **CA 1º nível:** 17 · **PV:** 23 · **Ataque:** +6 (1d8+4, 19-20/x2)
- **Talentos 1º nível:** Foco em Arma (Espada Longa), Esquiva, Ataque com Escudo Aprimorado, Duro de Matar
- **Roadmap de talentos completo, 1º ao 20º nível**, em `docs/` — inclui picareta de Escudo Fraterno (6º), Especialização em Armadura (9º), toda a cadeia de arma (Foco→Especialização→Aprimorados→Mestre em Arma) e os 3 talentos de Destino (Fortitude Maior/Vontade de Ferro/Reflexos Rápidos, todos cumulativos e confirmados em prosa)
- Avaliada e descartada a variante **Estilo Colosso** (Manual do Combate) — ver `docs/` e `memorias/classico/talentos.md` para o porquê

## Pendências conhecidas

- Talento Nativo "Lutar em Formação" (do livro de Arton, mesma edição clássica — pode valer sem adaptação, só falta reextrair o texto)
- Se existe um sistema de "origem/antecedente" mecânico nesta edição (Cap. 6, ainda não lido)
- Classe de prestígio Soldado Veterano (Manual do Combate) combina com o histórico de ex-soldado mas não foi avaliada em detalhe — opção futura de multiclasse

## Conteúdo

- `andor-classico.json` — dados estruturados do personagem (atributos, CA, talentos, equipamento)
- `docs/` — decisão de build completa, com fontes e páginas citadas
- Ficha jogável (HTML) — ainda não existe; por enquanto jogar direto do JSON/docs
