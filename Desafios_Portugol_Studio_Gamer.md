# Desafios Práticos — Portugol Studio (Edição Gamer)
## Unidade 2 — Lógica de Programação e Representação de Algoritmos

Resolva primeiro no papel (fluxograma ou pseudocódigo) e só depois abra o Portugol Studio. Consulte a Documentação sempre que precisar.

---

## Nível 1 — Variáveis, entrada/saída e operadores aritméticos

**Desafio 1.1 — Loja do Fortnite**
Peça o preço de um item da loja (V-Bucks) e a quantidade que o jogador quer comprar. Calcule o total gasto.
*Conceitos: variáveis `real`, `leia`, `escreva`, operador `*`*

**Desafio 1.2 — K/D médio**
Peça o número de kills em 3 partidas e calcule a média de abates por partida.
*Conceitos: variáveis `real`, operadores `+` e `/`*

**Desafio 1.3 — Dano crítico**
Peça o dano base de uma arma e calcule o dano com crítico: `danoCritico = danoBase * 2.5`.
*Conceitos: variáveis `real`, expressão aritmética*

**Desafio 1.4 — Troco de skin**
Peça o preço de uma skin do Fortnite/Roblox e o valor pago em V-Bucks/Robux. Calcule o troco.
*Conceitos: variáveis `real`, subtração*

---

## Nível 2 — Condicionais

**Desafio 2.1 — Level up no Minecraft**
Peça a quantidade de XP do jogador. Se for ≥ 100, mostre "Você subiu de nível!"; senão, mostre quanto falta.
*Conceitos: `se/senao`, operadores relacionais*

**Desafio 2.2 — Rank do jogador**
Peça a pontuação (elo) e classifique: "Bronze" (< 1000), "Prata" (1000–1999), "Ouro" (2000–2999), "Diamante" (≥ 3000).
*Conceitos: `se/senaose/senao`*

**Desafio 2.3 — Vida ou Game Over**
Peça a vida atual do personagem (0 a 100). Se chegar a 0, mostre "GAME OVER"; se estiver abaixo de 20, mostre "CUIDADO, vida baixa!"; senão, "Você está bem".
*Conceitos: `se/senaose/senao`*

**Desafio 2.4 — Combo de Fortnite (build fight)**
Peça se o jogador tem material de madeira, tijolo e metal (verdadeiro/falso cada). Se tiver os três, mostre "Pode construir qualquer coisa!"; se tiver pelo menos um, "Consegue se defender"; senão, "Você tá cru, corre!".
*Conceitos: `se/senaose/senao`, operadores lógicos `&&` e `||`*

---

## Nível 3 — Laços de repetição

**Desafio 3.1 — Contagem regressiva do lobby**
Mostre a contagem regressiva de 10 até 0 antes da partida começar.
*Conceitos: `para`*

**Desafio 3.2 — Farm de recursos no Minecraft**
Peça quantos blocos de madeira o jogador quer minerar e simule, mostrando "Bloco X minerado!" para cada um, de 1 até o total.
*Conceitos: `para`*

**Desafio 3.3 — Sobrevivendo à zona (Fortnite)**
A cada "rodada" (enquanto a vida for maior que 0), a zona tira 5 de vida. Mostre a vida a cada rodada até o jogador "morrer".
*Conceitos: `enquanto`, acumulador*

**Desafio 3.4 — Contador de headshots**
Peça quantos tiros o jogador deu em uma partida e, para cada um, pergunte se foi headshot (verdadeiro/falso). Conte quantos headshots aconteceram no total.
*Conceitos: `para`, `se`, acumulador*

---

## Nível 4 — Vetores (listas)

**Desafio 4.1 — Inventário do Minecraft**
Crie um vetor de 9 posições (hotbar). Peça ao jogador para digitar o nome de 9 itens e guarde cada um. Depois, mostre o inventário completo.
*Conceitos: vetor, `para`, `leia`*

**Desafio 4.2 — Melhor jogador da squad**
Crie um vetor com o K/D de 4 jogadores do squad. Descubra e mostre quem teve o maior K/D (posição do vetor).
*Conceitos: vetor, `para`, `se`*

**Desafio 4.3 — Média de pontuação do Roblox**
Preencha um vetor com as pontuações de 6 partidas de um jogo do Roblox e calcule a média.
*Conceitos: vetor, `para`, acumulador*

**Desafio 4.4 — Classificando o loot**
Preencha um vetor de 12 posições com raridades de itens (0 = comum, 1 = raro, 2 = épico, 3 = lendário). Conte quantos itens existem de cada raridade.
*Conceitos: vetor, `para`, `se/senaose/senao`*

---

## Nível 5 — Desafios integradores

**Desafio 5.1 — Placar final da partida (Fortnite/Free Fire)**
Peça quantos jogadores participaram da squad (n). Crie um vetor de tamanho n para guardar os kills de cada um. Peça os kills em um laço. Ao final, mostre: total de kills da squad, quem teve mais kills (MVP), e quantos jogadores tiveram zero kills.
*Conceitos: variáveis, vetor dinâmico, `para`, `se`, acumulador*

**Desafio 5.2 — Loja de skins com troco em gemas**
Peça um valor de compra (inteiro, em gemas) e calcule quantos "pacotes" de 100, 50 e 10 gemas serão usados para pagar, usando a menor quantidade de pacotes possível.
*Conceitos: variáveis, `/` e `%`, condicionais*

**Desafio 5.3 — Verificador de senha da conta Steam**
Peça uma senha numérica de 4 dígitos guardada em vetor. Verifique se todos os dígitos são iguais (senha fraca tipo "1111"), se está em sequência (tipo "1234", também fraca), ou se é "senha segura".
*Conceitos: vetor, `se/senaose/senao`, laço*

**Desafio 5.4 — Caça ao Creeper (adivinhação)**
O jogo "esconde" um número de 1 a 50 (posição do Creeper numa fileira de blocos). O jogador tenta adivinhar e recebe dicas de "mais longe"/"mais perto" até acertar. Conte e mostre quantas tentativas foram necessárias.
*Conceitos: `faca...enquanto`, `se/senaose`, acumulador de tentativas*

---

## Orientações para o Professor

- **Ordem:** siga os níveis em sequência; 2 a 3 desafios por nível já validam o aprendizado.
- **Antes do computador:** exigir rascunho de fluxograma ou pseudocódigo a partir do Nível 3.
- **Modo passo a passo do Portugol Studio:** use nos Níveis 3 e 4 para os alunos verem as variáveis mudando a cada iteração — equivalente digital do teste de mesa.
- **Nível 5** funciona bem como avaliação prática de fechamento da Unidade 2.
