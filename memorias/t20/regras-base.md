# Regras base — Tormenta20

Fonte: `manuais-t20/Tormenta 20.pdf`. Página impressa do livro entre parênteses (não é o número de página do PDF).

## Modificador de Atributo

`Modificador = floor((Valor - 10) / 2)`

## Perícias (pág. 114)

```
Modificador de Perícia          = ½ Nível (arred. p/ baixo) + Mod. do Atributo-chave
Modificador de Perícia Treinada = ½ Nível (arred. p/ baixo) + Mod. do Atributo-chave + 2*
```
`*` o bônus de treino sobe para **+4 a partir do 7º nível** e **+6 a partir do 15º nível**.

Penalidade de armadura (quando aplicável): soma a penalidade da armadura **+** a penalidade do escudo (ambas já negativas) direto no teste.

### Tabela 2-1: Perícias (completa, 29 perícias)

| Perícia | Atributo | Só treinada? | Penalidade de armadura? |
|---|---|---|---|
| Acrobacia | Des | Não | **Sim** |
| Adestramento | Car | **Sim** | Não |
| Atletismo | For | Não | Não* |
| Atuação | Car | Não | Não |
| Cavalgar | Des | Não | Não |
| Conhecimento | Int | **Sim** | Não |
| Cura | Sab | Não | Não |
| Diplomacia | Car | Não | Não |
| Enganação | Car | Não | Não |
| Fortitude | Con | Não | Não |
| Furtividade | Des | Não | **Sim** |
| Guerra | Int | **Sim** | Não |
| Iniciativa | Des | Não | Não |
| Intimidação | Car | Não | Não |
| Intuição | Sab | Não | Não |
| Investigação | Int | Não | Não |
| Jogatina | Car | **Sim** | Não |
| Ladinagem | Des | **Sim** | **Sim** |
| Luta | For | Não | Não |
| Misticismo | Int | **Sim** | Não |
| Nobreza | Int | **Sim** | Não |
| Ofício | Int | **Sim** | Não |
| Percepção | Sab | Não | Não |
| Pilotagem | Des | **Sim** | Não |
| Pontaria | Des | Não | Não |
| Reflexos | Des | Não | Não |
| Religião | Sab | **Sim** | Não |
| Sobrevivência | Sab | Não | Não |
| Vontade | Sab | Não | Não |

`*` Atletismo não tem a flag geral de penalidade de armadura na tabela, mas o texto da própria perícia diz que a natação especificamente sofre a penalidade de armadura.

Você recebe perícias treinadas da classe + uma quantidade extra igual ao seu bônus de Inteligência (essas extras não precisam ser da lista da classe).

## Defesa (pág. 106)

```
Defesa = 10 + Mod. de Destreza + bônus de armadura + bônus de escudo
```
- **Armadura pesada:** o personagem **não aplica o bônus de Destreza** na Defesa (zera esse termo, não limita — zera mesmo) e tem o deslocamento reduzido em **3m**.
- Dá pra usar armadura + escudo ao mesmo tempo (bônus acumulam), mas não dois escudos.

## Pontos de Vida / Pontos de Mana (pág. 106)

- PV: definidos pela classe (ex.: Guerreiro = 20 + mod. Con no 1º nível, +5 + mod. Con por nível seguinte).
- PM: definidos pela classe (ex.: Guerreiro = 3 por nível).
- Recuperação por descanso (8h de sono): Ruim = metade do nível · Normal = nível · Confortável = 2x nível · Luxuosa = 3x nível.

## Tamanho (pág. 106, Tabela 1-20)

| Categoria | Modificador Furtividade/Manobras |
|---|---|
| Minúsculo | +5 / −5 |
| Pequeno | +2 / −2 |
| Médio | 0 |
| Grande | −2 / +2 |
| Enorme | −5 / +5 |
| Colossal | −10 / +10 |

Deslocamento padrão: **9m** (antes de qualquer penalidade).

## Teste de Ataque e Dano (pág. 216)

- Ataque corpo a corpo → teste de **Luta**. Ataque à distância → teste de **Pontaria**. CD = Defesa do alvo.
- `Dano corpo a corpo/arremesso = Dano da Arma + Mod. de Força`
- `Dano de arma de disparo = Dano da Arma` (sem Força)
- Crítico: acerto com d20 = 20 natural → multiplica os **dados** de dano (não bônus fixos nem dados extras tipo Ataque Furtivo). Algumas armas ampliam a margem de ameaça (19 ou 18) e/ou o multiplicador (x3, x4) — ver `equipamento.md`.

## Implementado em código

Todas essas fórmulas estão implementadas em `Ficha T20.html` (raiz do projeto), função `recalc()` e `periciaTotal()`. Se uma regra aqui mudar (errata, nova edição), atualize os dois lugares.
