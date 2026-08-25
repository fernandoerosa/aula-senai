# Gabarito — Desafios Portugol Studio (Edição Gamer)
## Unidade 2 — Lógica de Programação e Representação de Algoritmos

---

## Nível 1

### 1.1 — Loja do Fortnite
```
programa
{
    funcao inicio()
    {
        real preco, quantidade, total
        escreva("Preço do item (V-Bucks): ")
        leia(preco)
        escreva("Quantidade: ")
        leia(quantidade)

        total = preco * quantidade
        escreva("Total gasto: ", total, " V-Bucks")
    }
}
```

### 1.2 — K/D médio
```
programa
{
    funcao inicio()
    {
        real kills1, kills2, kills3, media
        escreva("Kills partida 1: ")
        leia(kills1)
        escreva("Kills partida 2: ")
        leia(kills2)
        escreva("Kills partida 3: ")
        leia(kills3)

        media = (kills1 + kills2 + kills3) / 3
        escreva("Média de kills: ", media)
    }
}
```

### 1.3 — Dano crítico
```
programa
{
    funcao inicio()
    {
        real danoBase, danoCritico
        escreva("Dano base da arma: ")
        leia(danoBase)

        danoCritico = danoBase * 2.5
        escreva("Dano crítico: ", danoCritico)
    }
}
```

### 1.4 — Troco de skin
```
programa
{
    funcao inicio()
    {
        real preco, pago, troco
        escreva("Preço da skin: ")
        leia(preco)
        escreva("Valor pago: ")
        leia(pago)

        troco = pago - preco
        escreva("Troco: ", troco)
    }
}
```

---

## Nível 2

### 2.1 — Level up no Minecraft
```
programa
{
    funcao inicio()
    {
        inteiro xp
        escreva("XP atual: ")
        leia(xp)

        se (xp >= 100)
        {
            escreva("Você subiu de nível!")
        }
        senao
        {
            escreva("Faltam ", 100 - xp, " XP para o próximo nível")
        }
    }
}
```

### 2.2 — Rank do jogador
```
programa
{
    funcao inicio()
    {
        inteiro elo
        escreva("Sua pontuação (elo): ")
        leia(elo)

        se (elo < 1000)
        {
            escreva("Rank: Bronze")
        }
        senaose (elo < 2000)
        {
            escreva("Rank: Prata")
        }
        senaose (elo < 3000)
        {
            escreva("Rank: Ouro")
        }
        senao
        {
            escreva("Rank: Diamante")
        }
    }
}
```

### 2.3 — Vida ou Game Over
```
programa
{
    funcao inicio()
    {
        inteiro vida
        escreva("Vida atual (0-100): ")
        leia(vida)

        se (vida == 0)
        {
            escreva("GAME OVER")
        }
        senaose (vida < 20)
        {
            escreva("CUIDADO, vida baixa!")
        }
        senao
        {
            escreva("Você está bem")
        }
    }
}
```

### 2.4 — Combo de Fortnite (build fight)
```
programa
{
    funcao inicio()
    {
        logico madeira, tijolo, metal
        escreva("Tem madeira? (verdadeiro/falso): ")
        leia(madeira)
        escreva("Tem tijolo? (verdadeiro/falso): ")
        leia(tijolo)
        escreva("Tem metal? (verdadeiro/falso): ")
        leia(metal)

        se (madeira && tijolo && metal)
        {
            escreva("Pode construir qualquer coisa!")
        }
        senaose (madeira || tijolo || metal)
        {
            escreva("Consegue se defender")
        }
        senao
        {
            escreva("Você tá cru, corre!")
        }
    }
}
```

---

## Nível 3

### 3.1 — Contagem regressiva do lobby
```
programa
{
    funcao inicio()
    {
        para (inteiro i = 10; i >= 0; i--)
        {
            escreva(i, " ")
        }
    }
}
```

### 3.2 — Farm de recursos no Minecraft
```
programa
{
    funcao inicio()
    {
        inteiro total
        escreva("Quantos blocos minerar? ")
        leia(total)

        para (inteiro i = 1; i <= total; i++)
        {
            escreva("Bloco ", i, " minerado!\n")
        }
    }
}
```

### 3.3 — Sobrevivendo à zona (Fortnite)
```
programa
{
    funcao inicio()
    {
        inteiro vida = 100

        enquanto (vida > 0)
        {
            escreva("Vida: ", vida, "\n")
            vida = vida - 5
        }
        escreva("Você morreu na zona!")
    }
}
```

### 3.4 — Contador de headshots
```
programa
{
    funcao inicio()
    {
        inteiro totalTiros, contadorHeadshots = 0
        logico foiHeadshot

        escreva("Quantos tiros você deu? ")
        leia(totalTiros)

        para (inteiro i = 1; i <= totalTiros; i++)
        {
            escreva("Tiro ", i, " foi headshot? (verdadeiro/falso): ")
            leia(foiHeadshot)

            se (foiHeadshot)
            {
                contadorHeadshots++
            }
        }
        escreva("Total de headshots: ", contadorHeadshots)
    }
}
```

---

## Nível 4

### 4.1 — Inventário do Minecraft
```
programa
{
    funcao inicio()
    {
        cadeia hotbar[9]

        para (inteiro i = 0; i < 9; i++)
        {
            escreva("Item da posição ", i, ": ")
            leia(hotbar[i])
        }

        escreva("\nSeu inventário:\n")
        para (inteiro i = 0; i < 9; i++)
        {
            escreva(i, " - ", hotbar[i], "\n")
        }
    }
}
```

### 4.2 — Melhor jogador da squad
```
programa
{
    funcao inicio()
    {
        real kd[4]
        inteiro maiorIndice = 0

        para (inteiro i = 0; i < 4; i++)
        {
            escreva("K/D do jogador ", i + 1, ": ")
            leia(kd[i])
        }

        para (inteiro i = 1; i < 4; i++)
        {
            se (kd[i] > kd[maiorIndice])
            {
                maiorIndice = i
            }
        }

        escreva("Melhor jogador: jogador ", maiorIndice + 1, " com K/D ", kd[maiorIndice])
    }
}
```

### 4.3 — Média de pontuação do Roblox
```
programa
{
    funcao inicio()
    {
        inteiro pontuacoes[6]
        real soma = 0, media

        para (inteiro i = 0; i < 6; i++)
        {
            escreva("Pontuação da partida ", i + 1, ": ")
            leia(pontuacoes[i])
            soma = soma + pontuacoes[i]
        }

        media = soma / 6
        escreva("Média de pontuação: ", media)
    }
}
```

### 4.4 — Classificando o loot
```
programa
{
    funcao inicio()
    {
        inteiro loot[12]
        inteiro comuns = 0, raros = 0, epicos = 0, lendarios = 0

        para (inteiro i = 0; i < 12; i++)
        {
            escreva("Raridade do item ", i + 1, " (0-3): ")
            leia(loot[i])

            se (loot[i] == 0)
            {
                comuns++
            }
            senaose (loot[i] == 1)
            {
                raros++
            }
            senaose (loot[i] == 2)
            {
                epicos++
            }
            senao
            {
                lendarios++
            }
        }

        escreva("Comuns: ", comuns, "\n")
        escreva("Raros: ", raros, "\n")
        escreva("Épicos: ", epicos, "\n")
        escreva("Lendários: ", lendarios, "\n")
    }
}
```

---

## Nível 5

### 5.1 — Placar final da partida (Fortnite/Free Fire)
```
programa
{
    funcao inicio()
    {
        inteiro n
        escreva("Quantos jogadores na squad? ")
        leia(n)

        inteiro kills[n]
        inteiro totalKills = 0, mvpIndice = 0, zerados = 0

        para (inteiro i = 0; i < n; i++)
        {
            escreva("Kills do jogador ", i + 1, ": ")
            leia(kills[i])
            totalKills = totalKills + kills[i]

            se (kills[i] == 0)
            {
                zerados++
            }
        }

        para (inteiro i = 1; i < n; i++)
        {
            se (kills[i] > kills[mvpIndice])
            {
                mvpIndice = i
            }
        }

        escreva("Total de kills da squad: ", totalKills, "\n")
        escreva("MVP: jogador ", mvpIndice + 1, " com ", kills[mvpIndice], " kills\n")
        escreva("Jogadores com zero kills: ", zerados, "\n")
    }
}
```

### 5.2 — Loja de skins com troco em gemas
```
programa
{
    funcao inicio()
    {
        inteiro valor, pacotes100, pacotes50, pacotes10

        escreva("Valor da compra (em gemas): ")
        leia(valor)

        pacotes100 = valor / 100
        valor = valor % 100

        pacotes50 = valor / 50
        valor = valor % 50

        pacotes10 = valor / 10
        valor = valor % 10

        escreva("Pacotes de 100: ", pacotes100, "\n")
        escreva("Pacotes de 50: ", pacotes50, "\n")
        escreva("Pacotes de 10: ", pacotes10, "\n")

        se (valor > 0)
        {
            escreva("Restante não pago (menor que 10 gemas): ", valor, "\n")
        }
    }
}
```

### 5.3 — Verificador de senha da conta Steam
```
programa
{
    funcao inicio()
    {
        inteiro senha[4]
        logico todosIguais = verdadeiro
        logico sequencial = verdadeiro

        para (inteiro i = 0; i < 4; i++)
        {
            escreva("Dígito ", i + 1, ": ")
            leia(senha[i])
        }

        para (inteiro i = 1; i < 4; i++)
        {
            se (senha[i] != senha[0])
            {
                todosIguais = falso
            }
            se (senha[i] != senha[i - 1] + 1)
            {
                sequencial = falso
            }
        }

        se (todosIguais)
        {
            escreva("Senha fraca: todos os dígitos iguais")
        }
        senaose (sequencial)
        {
            escreva("Senha fraca: sequência crescente")
        }
        senao
        {
            escreva("Senha segura")
        }
    }
}
```

### 5.4 — Caça ao Creeper (adivinhação)
```
programa
{
    funcao inicio()
    {
        inteiro numeroSecreto = 27   // posição fixa do Creeper, pode variar
        inteiro tentativa, tentativas = 0

        faca
        {
            escreva("Em qual bloco (1-50) está o Creeper? ")
            leia(tentativa)
            tentativas++

            se (tentativa > numeroSecreto)
            {
                escreva("Mais perto! Tente um bloco menor.\n")
            }
            senaose (tentativa < numeroSecreto)
            {
                escreva("Mais longe! Tente um bloco maior.\n")
            }
        }
        enquanto (tentativa != numeroSecreto)

        escreva("Você achou o Creeper em ", tentativas, " tentativas!")
    }
}
```

---

## Observações para correção

- Nomes de variáveis podem variar entre os alunos — o que importa é a lógica e a estrutura corretas.
- No Desafio 5.1, o Portugol Studio permite vetor com tamanho definido por variável (`inteiro kills[n]`); caso a versão usada em sala não suporte, aceitar solução com tamanho fixo (ex.: 4 ou 5) como alternativa válida.
- No Desafio 5.4, o valor de `numeroSecreto` é fixo no código para fins didáticos — pode ser combinado antes com a turma ou trocado a cada execução manualmente pelo professor.
