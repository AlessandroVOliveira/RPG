# Memórias de regras — Tormenta20

⚠️ **Personagem arquivado.** O Andor jogado nesta mesa migrou para o sistema clássico do Tormenta RPG — ver [[../classico/README.md]] e `personagens/andor-classico/`. Este material fica aqui só como referência/histórico de `personagens/andor-t20/`.

Resumo das regras de **Tormenta20** (edição atual, "Jogo do Ano" — a mesma em que "os antigos talentos agora se chamam poderes", livro do jogador pág. 12) extraídas diretamente de `manuais-t20/Tormenta 20.pdf` (407 páginas, livro do jogador — regras principais).

⚠️ `manuais-t20/tormenta-rpg---o-mundo-de-arton.pdf` (livro de região, 120 páginas) é de uma **edição anterior** do sistema (usa "CA", "bônus base de ataque", classes antigas) — qualquer regra/talento de lá precisa ser adaptado pro vocabulário do livro do jogador antes de valer. Ver `talentos-nativos-arton.md` para um exemplo de como isso foi feito.

Objetivo: evitar ter que reabrir e reprocessar os PDFs (108MB e 20MB) toda vez que for preciso conferir uma regra, uma tabela ou os poderes de uma classe. Estes arquivos são a fonte de verdade project-local — se algo aqui divergir do livro, o livro manda.

## Arquivos

- **[regras-base.md](regras-base.md)** — fórmulas centrais: perícias, Defesa, PV/PM, ataque/dano, tamanho, deslocamento. É o que `personagens/andor-t20/Ficha T20.html` implementa em JS.
- **[guerreiro.md](guerreiro.md)** — tabela de progressão da classe Guerreiro e lista completa dos 19 Poderes de Guerreiro.
- **[poderes-gerais.md](poderes-gerais.md)** — Poderes de Combate e Poderes de Destino (listas completas com pré-requisitos).
- **[humano-e-origens.md](humano-e-origens.md)** — habilidades de raça Humano e a Tabela 1-18 de Origens (34 origens).
- **[equipamento.md](equipamento.md)** — armas conhecidas, Tabela 3-4 (Armaduras & Escudos), Carga (Força×3/×10) e regra de equipamento inicial/dinheiro de 1º nível.
- **[talentos-nativos-arton.md](talentos-nativos-arton.md)** — Talentos Nativos (habilidades regionais) do livro de Arton, edição antiga — inclui o usado no Andor (Lutar em Formação) já adaptado.

## Como usar em outro PC / outra conversa

Copie a pasta `memorias/t20/` junto com `personagens/andor-t20/` (ficha, json e docs) para o novo ambiente. Não precisa dos PDFs de `manuais-t20/` para consultar este material — só para conferir alguma regra que não esteja documentada aqui ou para tirar dúvidas de outras classes/raças/origens que ainda não foram extraídas.

## O que NÃO está aqui (ainda)

Só foi extraído o que era necessário para a build do Andor Duvane (Guerreiro Humano, origem Soldado): regras gerais, a classe Guerreiro por completo, Poderes de Combate/Destino, raça Humano, todas as Origens (a tabela é geral) e equipamento de combate corpo a corpo/escudo/armadura pesada. Coisas como magias, outras classes (Arcanista, Bardo, Clérigo etc.), outras raças, Poderes de Magia/Concedidos/Tormenta em detalhe, e o livro de Arton (região) **não foram** extraídas em detalhe — se precisar delas, é preciso voltar ao PDF.
