# Mini-Documentação — Portugol Studio
## Unidade 2 — Lógica de Programação e Representação de Algoritmos

---

## 1. Estrutura básica de um programa

```
programa
{
    funcao inicio()
    {
        // suas instruções aqui
    }
}
```

## 2. Variáveis e tipos de dados

| Tipo | Guarda | Exemplo |
|---|---|---|
| `inteiro` | números sem casa decimal | `10`, `-3`, `0` |
| `real` | números com casa decimal | `3.5`, `-0.2` |
| `cadeia` | texto (string) | `"Fernando"` |
| `caractere` | um único caractere | `'A'` |
| `logico` | verdadeiro ou falso | `verdadeiro`, `falso` |

```
programa
{
    funcao inicio()
    {
        inteiro idade
        real altura
        cadeia nome
        logico aprovado

        idade = 18
        altura = 1.75
        nome = "Maria"
        aprovado = verdadeiro
    }
}
```

**Constantes** (valor que não muda):

```
const inteiro IDADE_MINIMA = 18
```

## 3. Entrada e saída

- `escreva(...)` — imprime na tela
- `leia(variavel)` — lê um valor digitado e guarda na variável

```
programa
{
    funcao inicio()
    {
        cadeia nome
        escreva("Digite seu nome: ")
        leia(nome)
        escreva("Olá, ", nome, "!")
    }
}
```

## 4. Operadores

**Aritméticos**

| Operador | Significado |
|---|---|
| `+` | soma |
| `-` | subtração |
| `*` | multiplicação |
| `/` | divisão |
| `%` | resto da divisão (módulo) |

**Relacionais**

| Operador | Significado |
|---|---|
| `==` | igual a |
| `!=` | diferente de |
| `>` | maior que |
| `<` | menor que |
| `>=` | maior ou igual |
| `<=` | menor ou igual |

**Lógicos**

| Operador | Significado |
|---|---|
| `&&` | E (ambas verdadeiras) |
| \|\| | OU (pelo menos uma verdadeira) |
| `!` | NÃO (inverte) |

```
inteiro idade = 20
logico maiorDeIdade = idade >= 18
logico podeEntrar = maiorDeIdade && verdadeiro
```

## 5. Estrutura condicional

```
se (condicao)
{
    // executa se verdadeiro
}
senaose (outraCondicao)
{
    // executa se a anterior for falsa e essa verdadeira
}
senao
{
    // executa se nenhuma condição anterior for verdadeira
}
```

```
programa
{
    funcao inicio()
    {
        inteiro nota
        escreva("Digite a nota: ")
        leia(nota)

        se (nota >= 7)
        {
            escreva("Aprovado")
        }
        senaose (nota >= 5)
        {
            escreva("Recuperação")
        }
        senao
        {
            escreva("Reprovado")
        }
    }
}
```

## 6. Estruturas de repetição

**`para`** — quando já se sabe quantas vezes repetir:

```
para (inteiro i = 1; i <= 10; i++)
{
    escreva(i, " ")
}
```

**`enquanto`** — repete enquanto a condição for verdadeira (testa antes):

```
inteiro contador = 0
enquanto (contador < 5)
{
    escreva(contador, " ")
    contador++
}
```

**`faca...enquanto`** — executa pelo menos uma vez, testa depois:

```
inteiro contador = 0
faca
{
    escreva(contador, " ")
    contador++
}
enquanto (contador < 5)
```

## 7. Vetores (listas)

```
programa
{
    funcao inicio()
    {
        inteiro notas[5]

        notas[0] = 8
        notas[1] = 7
        notas[2] = 9
        notas[3] = 6
        notas[4] = 10

        para (inteiro i = 0; i < 5; i++)
        {
            escreva(notas[i], " ")
        }
    }
}
```

Também dá para declarar já com valores:

```
inteiro notas[5] = {8, 7, 9, 6, 10}
```

## 8. Referência rápida (cola)

| Preciso de... | Uso |
|---|---|
| guardar um número inteiro | `inteiro x` |
| guardar um número quebrado | `real x` |
| guardar texto | `cadeia x` |
| guardar verdadeiro/falso | `logico x` |
| pedir algo ao usuário | `leia(x)` |
| mostrar algo na tela | `escreva(x)` |
| tomar uma decisão | `se / senaose / senao` |
| repetir número certo de vezes | `para` |
| repetir enquanto for verdade | `enquanto` |
| guardar vários valores juntos | `tipo nomeDoVetor[tamanho]` |
