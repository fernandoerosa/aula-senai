# Manual de Tradução — Portugol Studio → Java
## Unidade 2 — Lógica de Programação e Representação de Algoritmos
---

## 1. Estrutura básica de um programa

**Portugol:**
```
programa
{
    funcao inicio()
    {
        // suas instruções aqui
    }
}
```

**Java:**
```java
public class MeuPrograma {
    public static void main(String[] args) {
        // suas instruções aqui
    }
}
```

> Em Java, o nome da classe (`MeuPrograma`) precisa ser igual ao nome do arquivo (`MeuPrograma.java`). O `main` é sempre o ponto de entrada do programa — equivalente à `funcao inicio()`.

---

## 2. Variáveis e tipos de dados

| Portugol | Java |
|---|---|
| `inteiro` | `Integer` |
| `real` | `Double` |
| `cadeia` | `String` |
| `caractere` | `Character` |
| `logico` | `Boolean` |

**Portugol:**
```
inteiro idade
real altura
cadeia nome
logico aprovado

idade = 18
altura = 1.75
nome = "Maria"
aprovado = verdadeiro
```

**Java:**
```java
Integer idade;
Double altura;
String nome;
Boolean aprovado;

idade = 18;
altura = 1.75;
nome = "Maria";
aprovado = true;
```

> Repare: `verdadeiro`/`falso` do Portugol viram `true`/`false` em Java. Toda linha termina com `;` em Java — isso não existe no Portugol.

**Constantes:**

| Portugol | Java |
|---|---|
| `const inteiro IDADE_MINIMA = 18` | `final Integer IDADE_MINIMA = 18;` |

```java
final Integer IDADE_MINIMA = 18;
```

---

## 3. Entrada e saída

| Portugol | Java |
|---|---|
| `escreva(...)` | `System.out.print(...)` ou `System.out.println(...)` |
| `leia(variavel)` | `Scanner` (precisa importar) |

**Portugol:**
```
cadeia nome
escreva("Digite seu nome: ")
leia(nome)
escreva("Olá, ", nome, "!")
```

**Java:**
```java
import java.util.Scanner;

public class Saudacao {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String nome;

        System.out.print("Digite seu nome: ");
        nome = scanner.nextLine();
        System.out.println("Olá, " + nome + "!");
    }
}
```

> **Diferenças importantes:**
> - `escreva` vira `System.out.print` (não pula linha) ou `System.out.println` (pula linha ao final).
> - Java não junta valores com vírgula dentro do `print` como o Portugol — usa-se o operador `+` para concatenar texto.
> - `leia` precisa de um objeto `Scanner`, criado uma vez no início do programa com `new Scanner(System.in)`.
> - Cada tipo tem seu próprio método de leitura, que devolve automaticamente o wrapper correspondente: `nextLine()` → `String`, `nextInt()` → `Integer`, `nextDouble()` → `Double`, `nextBoolean()` → `Boolean`.

---

## 4. Operadores

### Aritméticos — mesmos símbolos do Portugol

| Operador | Significado |
|---|---|
| `+` | soma |
| `-` | subtração |
| `*` | multiplicação |
| `/` | divisão |
| `%` | resto da divisão |

> Ao operar dois `Integer` ou dois `Double` com `+`, `-`, `*`, `/`, `%`, o Java converte automaticamente para fazer a conta e devolve o wrapper — na prática, funciona como se fossem números comuns.

### Relacionais — mesmos símbolos

| Operador | Significado |
|---|---|
| `==` | igual a |
| `!=` | diferente de |
| `>` | maior que |
| `<` | menor que |
| `>=` | maior ou igual |
| `<=` | menor ou igual |

> **Atenção com `String`:** comparar textos com `==` não funciona de forma confiável em Java. Usa-se `nome.equals("Maria")` em vez de `nome == "Maria"`. Isso não existe no Portugol e é um dos erros mais comuns de quem está migrando.
>
> **Atenção com `Integer`, `Double` e `Boolean`:** por serem classes (não tipos primitivos), comparar com `==` também pode dar resultado inesperado em certos casos. O mais seguro, assim como com `String`, é usar `.equals()` — por exemplo `idade.equals(18)`. Nas listas de exercícios desta unidade os operadores relacionais (`>`, `<`, `>=`, `<=`, `==`) funcionam normalmente para os casos trabalhados; o detalhe do `.equals()` fica registrado aqui para quando o assunto for aprofundado.

### Lógicos — mesmos símbolos

| Operador | Significado |
|---|---|
| `&&` | E |
| \|\| | OU |
| `!` | NÃO |

**Portugol:**
```
inteiro idade = 20
logico maiorDeIdade = idade >= 18
logico podeEntrar = maiorDeIdade && verdadeiro
```

**Java:**
```java
Integer idade = 20;
Boolean maiorDeIdade = idade >= 18;
Boolean podeEntrar = maiorDeIdade && true;
```

---

## 5. Estrutura condicional

| Portugol | Java |
|---|---|
| `se (condicao) { ... }` | `if (condicao) { ... }` |
| `senaose (condicao) { ... }` | `else if (condicao) { ... }` |
| `senao { ... }` | `else { ... }` |

**Portugol:**
```
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
```

**Java:**
```java
if (nota >= 7) {
    System.out.println("Aprovado");
} else if (nota >= 5) {
    System.out.println("Recuperação");
} else {
    System.out.println("Reprovado");
}
```

---

## 6. Estruturas de repetição

| Portugol | Java |
|---|---|
| `para (...)` | `for (...)` |
| `enquanto (...)` | `while (...)` |
| `faca { ... } enquanto (...)` | `do { ... } while (...);` |

**`para` → `for`**

Portugol:
```
para (inteiro i = 1; i <= 10; i++)
{
    escreva(i, " ")
}
```

Java:
```java
for (Integer i = 1; i <= 10; i++) {
    System.out.print(i + " ");
}
```

**`enquanto` → `while`**

Portugol:
```
inteiro contador = 0
enquanto (contador < 5)
{
    escreva(contador, " ")
    contador++
}
```

Java:
```java
Integer contador = 0;
while (contador < 5) {
    System.out.print(contador + " ");
    contador++;
}
```

**`faca...enquanto` → `do...while`**

Portugol:
```
inteiro contador = 0
faca
{
    escreva(contador, " ")
    contador++
}
enquanto (contador < 5)
```

Java:
```java
Integer contador = 0;
do {
    System.out.print(contador + " ");
    contador++;
} while (contador < 5);
```

> Repare que o `do...while` do Java termina com `;` depois do `while (condição)` — detalhe fácil de esquecer.

---

## 7. Vetores (listas)

| Portugol | Java |
|---|---|
| `inteiro notas[5]` | `Integer[] notas = new Integer[5];` |
| `inteiro notas[5] = {8,7,9,6,10}` | `Integer[] notas = {8, 7, 9, 6, 10};` |

**Portugol:**
```
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
```

**Java:**
```java
Integer[] notas = new Integer[5];

notas[0] = 8;
notas[1] = 7;
notas[2] = 9;
notas[3] = 6;
notas[4] = 10;

for (Integer i = 0; i < 5; i++) {
    System.out.print(notas[i] + " ");
}
```

Declarando já com valores:

```java
Integer[] notas = {8, 7, 9, 6, 10};
```

---

## 8. Tabela-cola de tradução rápida

| Portugol | Java |
|---|---|
| `programa { funcao inicio() {...} }` | `public class Nome { public static void main(String[] args) {...} }` |
| `inteiro` | `Integer` |
| `real` | `Double` |
| `cadeia` | `String` |
| `caractere` | `Character` |
| `logico` | `Boolean` |
| `verdadeiro` / `falso` | `true` / `false` |
| `const` | `final` |
| `escreva(...)` | `System.out.print(...)` / `System.out.println(...)` |
| `leia(x)` | `scanner.nextInt()` / `.nextDouble()` / `.nextLine()` / `.nextBoolean()` |
| `se` | `if` |
| `senaose` | `else if` |
| `senao` | `else` |
| `para` | `for` |
| `enquanto` | `while` |
| `faca...enquanto` | `do...while` |
| `tipo vetor[tamanho]` | `Tipo[] vetor = new Tipo[tamanho];` |
| `&&` `\|\|` `!` | iguais em Java |
| `==` `!=` `>` `<` `>=` `<=` | iguais em Java (exceto comparar `String`/wrappers com `==`, ver seção 4) |
| fim de instrução (nada) | `;` (ponto e vírgula obrigatório) |
| blocos `{ }` | iguais em Java |

---

## 9. Diferenças que costumam confundir quem vem do Portugol

1. **Ponto e vírgula (`;`)** ao final de cada instrução — no Portugol não existe, em Java é obrigatório.
2. **Comparação de texto e de wrappers:** `nome == "Maria"` não funciona como esperado em Java; use `nome.equals("Maria")`. O mesmo cuidado vale, em teoria, para `Integer`, `Double` e `Boolean` — aqui usamos `==` nos exemplos porque funciona para os casos simples da unidade, mas `.equals()` é o caminho mais seguro.
3. **Concatenação de texto:** Portugol junta valores com vírgula no `escreva`; Java usa o operador `+`.
4. **Toda instrução Java mora dentro de uma classe** — não existe código "solto" fora de `public class { ... }` como no `programa { }` do Portugol.
5. **Índice de array:** em ambos começa em `0` — isso não muda.
6. **Nomes das classes wrapper começam com letra maiúscula** (`Integer`, `Double`, `Boolean`, `Character`) — diferente de `inteiro`, `real`, `logico`, `caractere`, que são minúsculos no Portugol.
