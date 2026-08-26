# Desafios Avançados — Portugol Studio (Edição Gamer)
## Unidade 2 — Lógica de Programação e Representação de Algoritmos

Continuação da lista anterior, com problemas mais complexos. Usam apenas o que já foi visto: variáveis, operadores, condicionais, laços e listas — mas combinando mais elementos por exercício.

---

## Nível 1 — Variáveis, entrada/saída e operadores (combinados)

**Desafio 1.1 — Loadout completo**
Peça o preço de 3 itens diferentes da loja (arma, skin, emote) e a quantidade de V-Bucks que o jogador tem. Calcule o total gasto e quanto sobra de V-Bucks. Se sobrar menos de 100, mostre "Saldo baixo".
*Conceitos: variáveis `real`, operadores aritméticos, `se`*

**Desafio 1.2 — Taxa de acerto (accuracy)**
Peça o número de tiros disparados e o número de tiros que acertaram. Calcule a porcentagem de acerto: `(acertos / disparos) * 100`.
*Conceitos: variáveis `real`, divisão, multiplicação*

**Desafio 1.3 — Dano total com efeito de fogo**
Peça o dano base de uma arma e se ela tem efeito de fogo (verdadeiro/falso). Se tiver, o dano total é `danoBase + (danoBase * 0.3)` (30% de dano extra por queimadura); senão, é só o dano base.
*Conceitos: variáveis, `se/senao`, expressão aritmética composta*

---

## Nível 2 — Condicionais (combinados)

**Desafio 2.1 — Loja de skins com desconto por rank**
Peça o preço da skin e o rank do jogador ("Bronze", "Prata", "Ouro", "Diamante"). Aplique desconto: Diamante 20%, Ouro 10%, Prata 5%, Bronze sem desconto. Mostre o preço final.
*Conceitos: `se/senaose/senao`, comparação de `cadeia`, operações aritméticas*

**Desafio 2.2 — Verificação de squad completa**
Peça quantos jogadores estão na squad (0 a 4) e se cada posição está com jogador humano ou bot (4 valores lógicos). Mostre "Squad completa com humanos" se os 4 forem humanos, "Squad com bots" se houver pelo menos 1 bot, ou "Squad incompleta" se tiver menos de 4 jogadores.
*Conceitos: `se/senaose/senao`, operadores lógicos combinados*

**Desafio 2.3 — Sistema de dano com armadura**
Peça a vida atual, a armadura atual (0 a 100) e o dano recebido. Se houver armadura, ela absorve 70% do dano (e o restante vai pra vida); se a armadura acabar no meio do cálculo, o resto do dano vai direto pra vida. Mostre a vida e a armadura restantes. Se a vida chegar a 0 ou menos, mostre "ELIMINADO".
*Conceitos: `se/senaose/senao`, múltiplas variáveis relacionadas, operadores aritméticos e relacionais*

---

## Nível 3 — Laços (combinados)

**Desafio 3.1 — Farm com chance de drop raro**
Simule a mineração de 20 blocos (laço `para`). Para cada bloco, peça ao usuário se caiu um item raro (verdadeiro/falso). Conte quantos itens raros caíram no total e em quais números de bloco (mostre a lista de números).
*Conceitos: `para`, `se`, acumulador, exibição condicional*

**Desafio 3.2 — Sobrevivência com cura**
Um jogador começa com 100 de vida. A cada rodada (`enquanto` a vida for maior que 0 e o número de rodadas for menor que 20), a zona tira 8 de vida, mas a cada rodada par o jogador recupera 3 de vida (bônus de regeneração). Mostre a vida a cada rodada e o motivo de parada no final ("Morreu na zona" ou "Sobreviveu 20 rodadas").
*Conceitos: `enquanto`, `se`, operador `%`, contador de rodadas*

**Desafio 3.3 — Ranking de combo em sequência**
Peça ao jogador para digitar uma sequência de 15 números representando pontos de combo (cada golpe conectado). Conte a **maior sequência consecutiva de combos acima de 50 pontos** (ou seja, quantos golpes seguidos, sem interrupção, tiveram pontuação > 50).
*Conceitos: `para`, `se`, duas variáveis acumuladoras (sequência atual e maior sequência), lógica de reinício de contador*

---

## Nível 4 — Listas (combinados)

**Desafio 4.1 — Inventário com peso máximo**
Crie uma lista de 10 posições para guardar o peso de cada item do inventário. Peça o peso de cada item e vá somando. Se a soma ultrapassar 50kg em algum momento, pare de aceitar itens e avise "Inventário cheio, item não coletado" para os itens restantes — mas continue mostrando quantos itens ainda faltavam ser digitados.
*Conceitos: lista, `para`, `se`, acumulador com limite*

**Desafio 4.2 — Comparando dois squads**
Crie duas listas de 4 posições com os kills de dois squads diferentes (Squad A e Squad B). Calcule a soma de kills de cada squad e informe qual squad venceu (ou empatou).
*Conceitos: duas listas, `para`, acumuladores separados, `se/senaose/senao`*

**Desafio 4.3 — Detector de item duplicado no inventário**
Preencha uma lista de 8 posições com IDs de itens (números inteiros) coletados pelo jogador. Verifique se algum ID aparece mais de uma vez (item duplicado) e mostre quais posições têm duplicata.
*Conceitos: lista, dois laços `para` aninhados, `se`*

**Desafio 4.4 — Sequência de loot por raridade com bônus**
Preencha uma lista de 10 posições com a raridade dos itens (0 = comum, 1 = raro, 2 = épico, 3 = lendário). Calcule uma pontuação total do loot, em que cada raridade vale pontos diferentes (comum = 1, raro = 5, épico = 15, lendário = 50). Se o jogador tiver pelo menos 2 lendários, aplique um bônus de +100 pontos na pontuação final.
*Conceitos: lista, `para`, `se/senaose`, acumulador, condição sobre contagem*

---

## Nível 5 — Desafios integradores avançados

**Desafio 5.1 — Campeonato entre squads**
Peça quantas squads vão competir (n, entre 2 e 6). Crie uma lista de tamanho n para guardar o total de pontos de cada squad (soma de kills + posição de colocação). Peça os dados de cada squad em um laço. Ao final, mostre: squad campeã, squad em último lugar, e a diferença de pontos entre o 1º e o 2º colocado. Se a diferença for menor que 5 pontos, mostre "Campeonato apertado!".
*Conceitos: lista de tamanho definido pelo usuário, `para`, acumulador, comparação para achar maior/segundo maior, `se`*

**Desafio 5.2 — Loja com sistema de cupom**
Peça o valor total da compra (em gemas) e um código de cupom (número inteiro simulando o cupom). Se o cupom for 100, aplique 10% de desconto; se for 200, aplique 20%; qualquer outro valor, sem desconto. Depois do desconto, calcule o troco em pacotes de 100, 50 e 10 gemas, como no desafio anterior, mas agora sobre o valor já com desconto.
*Conceitos: `se/senaose/senao`, operadores aritméticos, `/` e `%`, encadeamento de cálculos*

**Desafio 5.3 — Verificador de senha avançado (Steam)**
Peça uma senha de 6 dígitos guardada em uma lista. Verifique e classifique como:
- "Muito fraca": todos os dígitos iguais OU sequência crescente/decrescente completa
- "Fraca": tem pelo menos 3 dígitos repetidos entre si (não necessariamente seguidos)
- "Forte": nenhum dos casos acima

*Conceitos: lista, laços aninhados, múltiplas variáveis lógicas, `se/senaose/senao`*

**Desafio 5.4 — Caça ao Creeper com número de tentativas limitado**
Sorteie (fixe no código) um número entre 1 e 100. O jogador tem no máximo 7 tentativas. A cada tentativa errada, mostre "mais perto"/"mais longe" e quantas tentativas restam. Se acertar, mostre em quantas tentativas conseguiu. Se esgotar as 7 tentativas sem acertar, mostre "O Creeper fugiu! Era o bloco X" (revelando o número).
*Conceitos: `para` ou `enquanto` com contador limitado, `se/senaose`, controle de parada por acerto ou por limite*

**Desafio 5.5 — Painel de estatísticas da temporada**
Crie uma lista de 10 posições com os kills de 10 partidas de um jogador. Calcule: total de kills, média por partida, maior e menor pontuação, quantas partidas tiveram kills acima da média, e classifique a temporada como "Lendária" (média ≥ 15), "Boa" (média ≥ 8) ou "Regular" (média < 8).
*Conceitos: lista, `para`, acumuladores múltiplos, segunda passagem na lista comparando com a média, `se/senaose/senao`*

---
