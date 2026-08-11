# Aula 02: Sumário, objetivos, conteúdo, exemplos, exercícios e revisão para prova.

# 📚 Aula 1 — Linguagens Formais e Gramáticas

> Introdução aos principais conceitos de **Linguagens Formais, Alfabetos, Cadeias, Linguagens e Gramáticas**.

---

## 📑 Sumário

* [🎯 Objetivos da Aula](#-objetivos-da-aula)
* [1. Operadores Lógicos](#1-operadores-lógicos)
* [2. Palavra Vazia — ε](#2-palavra-vazia--)
* [3. Prefixos e Sufixos](#3-prefixos-e-sufixos)
* [4. Alfabeto — Σ](#4-alfabeto--)
* [5. Σ* — Todas as Cadeias Possíveis](#5---todas-as-cadeias-possíveis)
* [6. Linguagem Formal — L](#6-linguagem-formal--l)
* [7. Gramática Formal](#7-gramática-formal)
* [8. Regras de Produção](#8-regras-de-produção)
* [9. Como Ler →](#9-como-ler-)
* [10. Derivação de Palavras](#10-derivação-de-palavras)
* [11. Linguagem Gerada](#11-linguagem-gerada)
* [12. Atividades Práticas](#12-atividades-práticas)
* [13. Resumo para Prova](#13-resumo-para-prova)
* [14. Mapa Mental](#14-mapa-mental)

---

# 🎯 Objetivos da Aula

Ao final desta aula, devemos ser capazes de:

* Entender o conceito de **alfabeto**;
* Identificar **cadeias/palavras**;
* Compreender a **palavra vazia `ε`**;
* Identificar **prefixos e sufixos**;
* Entender o conceito de **linguagem formal**;
* Interpretar a notação **`L ⊆ Σ*`**;
* Compreender o funcionamento de uma **gramática formal**;
* Interpretar **regras de produção**;
* Gerar palavras a partir de uma gramática.

---

# 1. Operadores Lógicos

Os principais operadores estudados são:

| Símbolo | Nome       | Leitura               |
| :-----: | ---------- | --------------------- |
|   `¬`   | Negação    | não                   |
|   `∧`   | E          | e                     |
|   `∨`   | OU         | ou                    |
|   `→`   | Implicação | implica / se... então |

### Exemplo

Considere:

```text
p = "Está chovendo."
q = "Eu levo um guarda-chuva."
```

### Negação — `¬`

```text
¬p
```

Lê-se:

> Não está chovendo.

---

### E — `∧`

```text
p ∧ q
```

Lê-se:

> Está chovendo **e** eu levo um guarda-chuva.

---

### OU — `∨`

```text
p ∨ q
```

Lê-se:

> Está chovendo **ou** eu levo um guarda-chuva.

---

### Implicação — `→`

```text
p → q
```

Lê-se:

> Se está chovendo, então eu levo um guarda-chuva.

> **⚠️ Atenção:** o símbolo `→` possui significados diferentes dependendo do contexto. Em lógica, significa **implicação**. Em gramáticas, normalmente significa **produção/geração**.

---

# 2. Palavra Vazia — `ε`

A palavra vazia é representada por:

```text
ε
```

Lê-se:

> **Épsilon**

Ela representa uma cadeia que **não possui nenhum símbolo**.

Seu tamanho é:

```text
|ε| = 0
```

Ou seja:

> O comprimento da cadeia vazia é zero.

### Exemplo

A cadeia:

```text
abc
```

possui 3 símbolos:

```text
|abc| = 3
```

Já:

```text
ε
```

possui 0 símbolos:

```text
|ε| = 0
```

### ⚠️ Importante

`ε` **não é um espaço em branco**.

`ε` significa:

> **Não existe nenhum símbolo na cadeia.**

---

# 3. Prefixos e Sufixos

Considere a palavra:

```text
ab
```

## Prefixos

Um prefixo é uma parte da palavra que começa **no início**.

Podemos obter:

```text
ε
a
ab
```

Portanto:

```text
Prefixos(ab) = {ε, a, ab}
```

### 🧠 Dica

> **Prefixo → começa no começo.**

---

## Sufixos

Um sufixo é uma parte da palavra que termina **no final**.

Podemos obter:

```text
ε
b
ab
```

Portanto:

```text
Sufixos(ab) = {ε, b, ab}
```

### 🧠 Dica

> **Sufixo → termina no final.**

---

## Resumo

| Palavra | Prefixos       | Sufixos        |
| ------- | -------------- | -------------- |
| `ab`    | `ε`, `a`, `ab` | `ε`, `b`, `ab` |

O `ε` é considerado tanto **prefixo** quanto **sufixo**.

---

# 4. Alfabeto — `Σ`

Um **alfabeto** é um conjunto finito de símbolos.

Ele é representado por:

```text
Σ
```

Lê-se:

> **Sigma**

### Exemplo

```text
Σ = {a, b}
```

Nosso alfabeto possui dois símbolos:

```text
a
b
```

A partir deles podemos criar palavras:

```text
a
b
aa
ab
ba
bb
aaa
aab
aba
...
```

---

# 5. `Σ*` — Todas as Cadeias Possíveis

A notação:

```text
Σ*
```

representa o conjunto de **todas as cadeias finitas que podem ser formadas utilizando os símbolos de `Σ`**, incluindo `ε`.

Se:

```text
Σ = {a, b}
```

então:

```text
Σ* = {ε, a, b, aa, ab, ba, bb, aaa, ...}
```

## Existe um limite?

**Não existe limite máximo para o tamanho das palavras.**

Podemos formar:

```text
ε
a
aa
aaa
aaaa
aaaaa
...
```

A quantidade de palavras cresce conforme o tamanho aumenta.

Para um alfabeto com 2 símbolos:

```text
Quantidade de cadeias de tamanho n = 2ⁿ
```

| Tamanho | Quantidade |
| :-----: | :--------: |
|    0    |      1     |
|    1    |      2     |
|    2    |      4     |
|    3    |      8     |
|    4    |     16     |
|    5    |     32     |
|   ...   |     ...    |

### 📌 Conclusão

> `Σ*` é infinito, mas cada cadeia individual possui tamanho finito.

---

# 6. Linguagem Formal — `L`

Uma **linguagem formal** é um conjunto de palavras construídas a partir de um alfabeto.

Sua definição é:

```text
L ⊆ Σ*
```

Lê-se:

> **L é um subconjunto de Sigma estrela.**

### Entendendo cada elemento

```text
Σ
```

É o alfabeto.

```text
Σ*
```

É o conjunto de todas as palavras possíveis.

```text
L
```

É um conjunto de palavras escolhidas de `Σ*`.

---

## Exemplo

Considere:

```text
Σ = {a, b}
```

Podemos definir:

```text
L = {a, ab, abb, abbb}
```

Como todas essas palavras podem ser formadas usando `a` e `b`:

```text
L ⊆ Σ*
```

---

## Linguagem finita

```text
L = {ε, a, ab}
```

Possui uma quantidade limitada de palavras.

---

## Linguagem infinita

```text
L = {a, aa, aaa, aaaa, ...}
```

Possui infinitas palavras.

---

# 7. Gramática Formal

Uma gramática formal fornece **regras para gerar palavras**.

Considere:

```text
G = ({S}, {a}, {S → aS | ε}, S)
```

Uma gramática normalmente pode ser representada como:

```text
G = (N, Σ, P, S)
```

Onde:

| Elemento | Significado     |
| -------- | --------------- |
| `N`      | Não terminais   |
| `Σ`      | Terminais       |
| `P`      | Produções       |
| `S`      | Símbolo inicial |

No nosso exemplo:

```text
G = ({S}, {a}, {S → aS | ε}, S)
```

Temos:

### Não terminal

```text
{S}
```

### Terminal

```text
{a}
```

### Produções

```text
S → aS | ε
```

### Símbolo inicial

```text
S
```

---

# 8. Regras de Produção

A regra:

```text
S → aS | ε
```

possui duas possibilidades:

```text
S → aS
```

**OU**

```text
S → ε
```

O símbolo:

```text
|
```

significa:

> **OU**

Portanto:

> `S` pode produzir `aS` ou `ε`.

---

# 9. Como Ler `→`

O símbolo:

```text
→
```

pode ser lido de maneiras diferentes.

## Em gramáticas

Pode significar:

* produz;
* gera;
* deriva em.

Exemplo:

```text
S → aS
```

Lê-se:

> **S produz aS.**

---

## Em lógica

Pode significar:

* implica;
* se... então.

Exemplo:

```text
p → q
```

Lê-se:

> **Se p, então q.**

ou:

> **p implica q.**

---

# 10. Derivação de Palavras

Considere:

```text
G = ({S}, {a}, {S → aS | ε}, S)
```

Começamos sempre pelo símbolo inicial:

```text
S
```

---

## Gerando `ε`

Escolhemos:

```text
S → ε
```

Resultado:

```text
ε
```

---

## Gerando `a`

Primeiro:

```text
S → aS
```

Depois:

```text
S → ε
```

Logo:

```text
S → aS → aε → a
```

Resultado:

```text
a
```

---

## Gerando `aa`

Aplicamos `S → aS` duas vezes:

```text
S → aS
  → aaS
  → aaε
  → aa
```

Resultado:

```text
aa
```

---

## Gerando `aaa`

Aplicamos `S → aS` três vezes:

```text
S → aS
  → aaS
  → aaaS
  → aaaε
  → aaa
```

Resultado:

```text
aaa
```

---

# 11. Linguagem Gerada

A gramática:

```text
G = ({S}, {a}, {S → aS | ε}, S)
```

gera:

```text
ε
a
aa
aaa
aaaa
aaaaa
...
```

Logo:

```text
L(G) = {ε, a, aa, aaa, aaaa, ...}
```

Também podemos representar como:

```text
L(G) = {aⁿ | n ≥ 0}
```

Isso significa:

> A linguagem contém qualquer quantidade de `a`, incluindo **zero `a`**.

O caso de zero `a` é:

```text
ε
```

---

# 12. Atividades Práticas

## 📝 Atividade 1 — Prefixos e Sufixos

Considere a palavra:

```text
ab
```

### Pergunta

Liste os prefixos e sufixos.

### Gabarito

**Prefixos:**

```text
{ε, a, ab}
```

**Sufixos:**

```text
{ε, b, ab}
```

---

## 📝 Atividade 2 — Gramática

Considere:

```text
G = ({S}, {a}, {S → aS | ε}, S)
```

### Pergunta

Liste 3 palavras geradas.

### Gabarito

Uma resposta possível:

```text
ε
a
aa
```

Outras possibilidades:

```text
aaa
aaaa
aaaaa
...
```

---

# 13. Resumo para Prova

### 🔹 Alfabeto

```text
Σ = conjunto de símbolos
```

Exemplo:

```text
Σ = {a, b}
```

---

### 🔹 Cadeia

Uma sequência de símbolos pertencentes ao alfabeto.

Exemplo:

```text
ab
```

---

### 🔹 Palavra vazia

```text
ε
```

Possui zero símbolos:

```text
|ε| = 0
```

---

### 🔹 `Σ*`

Todas as cadeias finitas possíveis sobre `Σ`, incluindo `ε`.

```text
Σ* = {ε, a, b, aa, ab, ba, bb, ...}
```

---

### 🔹 Linguagem

Um conjunto de cadeias:

```text
L ⊆ Σ*
```

---

### 🔹 Prefixo

Começa no início da palavra.

Para `ab`:

```text
{ε, a, ab}
```

---

### 🔹 Sufixo

Termina no final da palavra.

Para `ab`:

```text
{ε, b, ab}
```

---

### 🔹 Gramática

Define regras para gerar palavras.

Exemplo:

```text
S → aS | ε
```

---

### 🔹 `→`

Em gramáticas:

> **produz / gera**

Em lógica:

> **implica / se... então**

---

### 🔹 `|`

Nas regras de produção:

> **OU**

Exemplo:

```text
S → aS | ε
```

Significa:

> S produz `aS` **ou** `ε`.

---

# 14. 🧠 Mapa Mental

```text
                    LINGUAGENS FORMAIS
                           │
          ┌────────────────┼────────────────┐
          │                │                │
          ▼                ▼                ▼
      ALFABETO           CADEIA          LINGUAGEM
          │                │                │
          │                │                └── L ⊆ Σ*
          │                │
          │                └── ε = cadeia vazia
          │
          └── Σ
               │
               └── Σ* = todas as cadeias
                           │
                           ▼
                       GRAMÁTICA
                           │
                           ▼
                    Regras de produção
                           │
                           ▼
                      S → aS | ε
                           │
                           ▼
                ε, a, aa, aaa, ...
```

---

# 📌 Checklist da Aula 1

Antes de avançar para a próxima aula, verifique se você consegue explicar:

* [ ] O que é um **alfabeto `Σ`**;
* [ ] O que é uma **cadeia**;
* [ ] O que significa **`ε`**;
* [ ] Por que **`|ε| = 0`**;
* [ ] O que é um **prefixo**;
* [ ] O que é um **sufixo**;
* [ ] O que significa **`Σ*`**;
* [ ] Se `Σ*` possui limite de tamanho;
* [ ] O que é uma **linguagem formal `L`**;
* [ ] O que significa **`L ⊆ Σ*`**;
* [ ] O que é uma **gramática formal**;
* [ ] O que são **terminais e não terminais**;
* [ ] O que é uma **regra de produção**;
* [ ] Como ler **`S → aS | ε`**;
* [ ] Como gerar palavras usando uma gramática.

---

## 🚀 Conceito-chave

> **Um alfabeto fornece os símbolos.
> As cadeias são formadas com esses símbolos.
> `Σ*` reúne todas as cadeias possíveis.
> Uma linguagem seleciona algumas dessas cadeias.
> Uma gramática define regras para gerar as cadeias da linguagem.**

---

### 📚 Aula 1 concluída

**Próximo passo:** praticar a identificação de alfabetos, cadeias, prefixos, sufixos e a derivação de palavras por meio de gramáticas formais.

