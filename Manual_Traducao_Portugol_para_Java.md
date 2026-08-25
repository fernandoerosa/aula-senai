# Manual de Tradução — Portugol Studio → Java
## Unidade 2 — Lógica de Programação e Representação de Algoritmos

Este manual segue a mesma estrutura da Documentação de Portugol Studio, mostrando lado a lado como cada conceito é escrito em Java. O objetivo é o aluno perceber que a **lógica não muda** — só a sintaxe.

> **Nota sobre tipos:** em Java existem os tipos primitivos (`int`, `double`, `boolean`, `char`) e as classes wrapper (`Integer`, `Double`, `Boolean`, `Character`). Para o dia a dia de quem está aprendendo lógica, o uso correto e mais comum é o tipo primitivo. As classes wrapper (`Integer`, `Double` etc.) existem para casos específicos — como guardar números em coleções (`ArrayList`) ou quando o valor pode ser nulo — e serão retomadas quando o curso chegar em Programação de Aplicativos / Coleções. Por isso, abaixo mostramos os dois: o equivalente direto pedido (wrapper) e o equivalente idiomático (primitivo), que é o recomendado para uso comum.

---

## 1. Estrutura básica de um programa

| Portugol | Java |
|---|---|
| `programa { funcao inicio() { ... } }` | `public class NomeDoPrograma { public static void main(String[] args) { ... } }` |

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

| Portugol | Java (wrapper — tradução direta) | Java (primitivo — uso recomendado) |
|---|---|---|
| `inteiro` | `Integer` | `int` |
| `real` | `Double` | `double` |
| `cadeia` | `String` | `String` (não existe primitivo para texto) |
| `caractere` | `Character` | `char` |
| `logico` | `Boolean` | `boolean` |

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

**Java (wrapper):**
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

**Java (primitivo — recomendado):**
```java
int idade;
double altura;
String nome;
boolean aprovado;

idade = 18;
altura = 1.75;
nome = "Maria";
aprovado = true;
```

> Repare: `verdadeiro`/`falso` do Portugol viram `true`/`false` em Java. Toda linha termina com `;` em Java — isso não existe no Portugol.

**Constantes:**

| Portugol | Java |
|---|---|
| `const inteiro IDADE_MINIMA = 18` | `final int IDADE_MINIMA = 18;` |

```java
final int IDADE_MINIMA = 18;
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
> - Cada tipo tem seu próprio método de leitura: `nextLine()` (texto), `nextInt()` (inteiro), `nextDouble()` (real), `nextBoolean()` (lógico).

---

## 4. Operadores

### Aritméticos — são os mesmos símbolos

| Operador | Significado | Portugol | Java |
|---|---|---|---|
| `+` | soma | igual | igual |
| `-` | subtração | igual | igual |
| `*` | multiplicação | igual | igual |
| `/` | divisão | igual | igual |
| `%` | resto da divisão | igual | igual |

### Relacionais — também são os mesmos símbolos

| Operador | Significado |
|---|---|
| `==` | igual a |
| `!=` | diferente de |
| `>` | maior que |
| `<` | menor que |
| `>=` | maior ou igual |
| `<=` | menor ou igual |

> **Atenção com `String`:** em Java, comparar textos com `==` não funciona de forma confiável. Usa-se `nome.equals("Maria")` em vez de `nome == "Maria"`. Isso não existe no Portugol e é um dos erros mais comuns de quem está migrando.

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
int idade = 20;
boolean maiorDeIdade = idade >= 18;
boolean podeEntrar = maiorDeIdade && true;
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
for (int i = 1; i <= 10; i++) {
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
int contador = 0;
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
int contador = 0;
do {
    System.out.print(contador + " ");
    contador++;
} while (contador < 5);
```

> Repare que o `do...while` do Java termina com `;` depois do `while (condição)` — detalhe fácil de esquecer.

---

## 7. Vetores (listas)

| Portugol | Java (array — tradução direta) |
|---|---|
| `inteiro notas[5]` | `int[] notas = new int[5];` |
| `inteiro notas[5] = {8,7,9,6,10}` | `int[] notas = {8, 7, 9, 6, 10};` |

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
int[] notas = new int[5];

notas[0] = 8;
notas[1] = 7;
notas[2] = 9;
notas[3] = 6;
notas[4] = 10;

for (int i = 0; i < 5; i++) {
    System.out.print(notas[i] + " ");
}
```

Declarando já com valores:

```java
int[] notas = {8, 7, 9, 6, 10};
```

> **Sobre a tabela wrapper x primitivo em arrays:** um array de `Integer[]` também existe em Java (`Integer[] notas = new Integer[5];`) e é a tradução literal se quisermos manter "inteiro → Integer" também nos vetores. Mas para arrays de números, `int[]` é sempre a escolha usada na prática — mais simples e mais eficiente. `Integer[]` só é necessário em situações avançadas (ex.: dentro de `ArrayList<Integer>`), fora do escopo desta unidade.

---

## 8. Tabela-cola de tradução rápida

| Portugol | Java |
|---|---|
| `programa { funcao inicio() {...} }` | `public class Nome { public static void main(String[] args) {...} }` |
| `inteiro` | `int` (ou `Integer`) |
| `real` | `double` (ou `Double`) |
| `cadeia` | `String` |
| `caractere` | `char` (ou `Character`) |
| `logico` | `boolean` (ou `Boolean`) |
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
| `tipo vetor[tamanho]` | `tipo[] vetor = new tipo[tamanho];` |
| `&&` `\|\|` `!` | iguais em Java |
| `==` `!=` `>` `<` `>=` `<=` | iguais em Java (exceto comparar `String`, que usa `.equals()`) |
| fim de instrução (nada) | `;` (ponto e vírgula obrigatório) |
| blocos `{ }` | iguais em Java |

---

## 9. Diferenças que costumam confundir quem vem do Portugol

1. **Ponto e vírgula (`;`)** ao final de cada instrução — no Portugol não existe, em Java é obrigatório.
2. **Comparação de texto:** `nome == "Maria"` não funciona como esperado em Java; use `nome.equals("Maria")`.
3. **Concatenação de texto:** Portugol junta valores com vírgula no `escreva`; Java usa o operador `+`.
4. **Java é case-sensitive nos tipos:** `int` (minúsculo) é o tipo primitivo; `Int` não existe — a classe wrapper é `Integer`.
5. **Toda instrução Java mora dentro de uma classe** — não existe código "solto" fora de `public class { ... }` como no `programa { }` do Portugol.
6. **Índice de array:** em ambos começa em `0` — isso não muda.
