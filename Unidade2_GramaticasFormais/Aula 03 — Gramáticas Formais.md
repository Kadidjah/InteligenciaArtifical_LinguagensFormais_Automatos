# Gramáticas Formais

**Disciplina:** Linguagens Formais e Autômatos  
**Duração:** 1h30  
**Tema:** Gramáticas Formais e Hierarquia de Chomsky

---

## 1. Objetivos da aula

Ao final da aula, o estudante deverá ser capaz de:

- Compreender o conceito de **gramática formal**;
- Identificar os componentes de uma gramática;
- Interpretar e **ler regras de produção**;
- Realizar derivações passo a passo;
- Diferenciar gramáticas **regulares** e **livres de contexto**;
- Compreender a **Hierarquia de Chomsky**;
- Classificar uma gramática a partir de suas regras;
- Construir exemplos simples de gramáticas regulares e livres de contexto.

---

## 2. Roteiro da aula

| Tempo | Etapa | Atividade |
|---:|---|---|
| 0–10 min | Introdução | Retomada de alfabetos, palavras e linguagens |
| 10–25 min | Conceito | O que é uma gramática formal? |
| 25–40 min | Produções | Como ler e aplicar uma regra |
| 40–55 min | Gramática Regular | Exemplo completo passo a passo |
| 55–70 min | Gramática Livre de Contexto | Exemplo completo passo a passo |
| 70–80 min | Chomsky | Hierarquia e classificação |
| 80–87 min | Exercícios | Atividade individual ou em dupla |
| 87–90 min | Fechamento | Correção e síntese |

---

# 3. Retomando: alfabetos, palavras e linguagens

Antes de estudar gramáticas, vamos relembrar alguns conceitos.

Considere o alfabeto:

\[
\Sigma = \{a,b\}
\]

Uma linguagem pode ser formada por várias palavras:

\[
L = \{a, ab, abb, abbb,\ldots\}
\]

Uma pergunta importante é:

> **Como podemos descrever formalmente quais palavras pertencem a uma linguagem?**

Uma das respostas é utilizar uma **gramática formal**.

---

# 4. O que é uma Gramática Formal?

Uma gramática formal pode ser representada por:

\[
G = (V,T,P,S)
\]

Cada componente possui uma função específica.

| Símbolo | Nome | Função |
|---|---|---|
| \(V\) | Variáveis ou não terminais | Símbolos auxiliares utilizados durante a geração |
| \(T\) | Terminais | Símbolos que aparecem nas palavras da linguagem |
| \(P\) | Produções | Regras utilizadas para gerar as palavras |
| \(S\) | Símbolo inicial | Símbolo onde começa a derivação |

Podemos pensar em uma gramática como um **conjunto de regras para produzir palavras**.

---

# 5. Como ler uma regra de produção?

Considere a regra:

\[
S \rightarrow aS
\]

Lemos:

> **"S produz aS"**

ou:

> **"S pode ser substituído por aS."**

Outra regra:

\[
S \rightarrow b
\]

Lemos:

> **"S produz b."**

O símbolo:

\[
\rightarrow
\]

pode ser interpretado como:

> **"pode ser substituído por"** ou **"produz"**.

---

# 6. Exemplo de derivação passo a passo

Considere a gramática:

\[
G = (\{S\},\{a,b\},P,S)
\]

com as produções:

\[
P:
\begin{cases}
S \rightarrow aS\\
S \rightarrow b
\end{cases}
\]

Vamos gerar uma palavra.

## Passo 1 — Começamos pelo símbolo inicial

\[
S
\]

## Passo 2 — Aplicamos a primeira produção

\[
S \rightarrow aS
\]

Portanto:

\[
S \Rightarrow aS
\]

## Passo 3 — Aplicamos novamente a regra

\[
aS \Rightarrow aaS
\]

## Passo 4 — Encerramos a derivação

Agora utilizamos:

\[
S \rightarrow b
\]

Logo:

\[
aaS \Rightarrow aab
\]

A derivação completa é:

\[
\boxed{
S \Rightarrow aS \Rightarrow aaS \Rightarrow aab
}
\]

A palavra gerada é:

\[
\boxed{aab}
\]

### Como saber que terminou?

A derivação termina quando **não existem mais variáveis ou não terminais**.

Nesse exemplo:

\[
aab
\]

possui somente símbolos terminais.

---

# 7. Gramáticas Regulares

As **gramáticas regulares** possuem regras bastante restritas.

Considere:

\[
G:
\begin{cases}
S \rightarrow aS\\
S \rightarrow b
\end{cases}
\]

Podemos gerar:

\[
b
\]

ou:

\[
S \Rightarrow aS \Rightarrow ab
\]

ou:

\[
S \Rightarrow aS \Rightarrow aaS \Rightarrow aab
\]

ou:

\[
S \Rightarrow aS \Rightarrow aaS \Rightarrow aaaS \Rightarrow aaab
\]

Assim, podemos obter palavras como:

```text
b
ab
aab
aaab
aaaab
...
```

---

## 7.1. Observe o padrão

As palavras possuem a estrutura:

```text
b
ab
aab
aaab
aaaab
...
```

A gramática determina exatamente quais palavras podem ser produzidas.

Por exemplo, palavras como:

```text
ba
abb
aabb
```

não podem ser geradas por essa gramática.

---

# 8. Exercício — Gramática Regular

Considere:

\[
G:
\begin{cases}
S \rightarrow 0S\\
S \rightarrow 1
\end{cases}
\]

### Questão 1

Gere a palavra:

```text
0001
```

### Resolução

Começamos com:

\[
S
\]

Aplicamos:

\[
S \Rightarrow 0S
\]

Depois:

\[
0S \Rightarrow 00S
\]

Depois:

\[
00S \Rightarrow 000S
\]

Finalmente:

\[
000S \Rightarrow 0001
\]

Portanto:

\[
\boxed{
S \Rightarrow 0S
\Rightarrow 00S
\Rightarrow 000S
\Rightarrow 0001
}
\]

### Questão 2

Gere outras três palavras utilizando a mesma gramática.

---

# 9. Gramáticas Livres de Contexto

Agora vamos considerar uma gramática com regras mais flexíveis.

Considere:

\[
G:
\begin{cases}
S \rightarrow aSb\\
S \rightarrow \varepsilon
\end{cases}
\]

O símbolo:

\[
\varepsilon
\]

representa a **palavra vazia**.

A regra:

\[
S \rightarrow aSb
\]

pode ser lida como:

> **"S pode ser substituído por a, seguido de S, seguido de b."**

---

# 10. Gerando `aabb` passo a passo

Queremos gerar:

```text
aabb
```

Começamos:

\[
S
\]

Aplicamos:

\[
S \rightarrow aSb
\]

Resultado:

\[
S \Rightarrow aSb
\]

Aplicamos novamente:

\[
aSb \Rightarrow aaSbb
\]

Agora usamos:

\[
S \rightarrow \varepsilon
\]

Então:

\[
aaSbb \Rightarrow aa\varepsilon bb
\]

Como:

\[
\varepsilon
\]

não possui símbolos, temos:

\[
aa\varepsilon bb = aabb
\]

Portanto:

\[
\boxed{
S \Rightarrow aSb
\Rightarrow aaSbb
\Rightarrow aa\varepsilon bb
\Rightarrow aabb
}
\]

---

# 11. Gerando `aaabbb`

Agora queremos gerar:

```text
aaabbb
```

Precisamos aplicar a regra:

\[
S \rightarrow aSb
\]

três vezes.

### Derivação

\[
S
\]

\[
\Rightarrow aSb
\]

\[
\Rightarrow aaSbb
\]

\[
\Rightarrow aaaSbbb
\]

Agora utilizamos:

\[
S \rightarrow \varepsilon
\]

Então:

\[
aaaSbbb
\Rightarrow aaa\varepsilon bbb
\]

Resultado:

\[
\boxed{aaabbb}
\]

### O que podemos observar?

A gramática consegue produzir:

```text
ab
aabb
aaabbb
aaaabbbb
...
```

Existe uma correspondência entre a quantidade de `a` e de `b`.

---

# 12. Comparando as gramáticas

## Gramática Regular

\[
S \rightarrow aS
\]

\[
S \rightarrow b
\]

Exemplos:

```text
b
ab
aab
aaab
...
```

## Gramática Livre de Contexto

\[
S \rightarrow aSb
\]

\[
S \rightarrow \varepsilon
\]

Exemplos:

```text
ε
ab
aabb
aaabbb
aaaabbbb
...
```

### Pergunta para reflexão

> Qual das duas gramáticas consegue gerar uma quantidade correspondente de `a` e `b`?

A segunda:

\[
S \rightarrow aSb
\]

Ela permite construir uma estrutura em que cada aplicação adiciona um `a` no início e um `b` no final.

---

# 13. Hierarquia de Chomsky

As gramáticas formais podem ser classificadas de acordo com a **Hierarquia de Chomsky**.

| Tipo | Nome | Característica geral |
|---|---|---|
| Tipo 0 | Irrestrita | Sem restrições gerais |
| Tipo 1 | Sensível ao contexto | As produções dependem do contexto |
| Tipo 2 | Livre de contexto | O lado esquerdo possui um único não terminal |
| Tipo 3 | Regular | Possui regras bastante restritas |

A hierarquia pode ser representada por:

\[
\boxed{\text{Tipo 3}}
\subset
\boxed{\text{Tipo 2}}
\subset
\boxed{\text{Tipo 1}}
\subset
\boxed{\text{Tipo 0}}
\]

Isso significa que:

> **Toda linguagem regular é livre de contexto, mas nem toda linguagem livre de contexto é regular.**

---

# 14. Relação com os modelos computacionais

A hierarquia também está relacionada aos modelos de computação:

| Gramática | Linguagem | Modelo associado |
|---|---|---|
| Tipo 3 | Regular | Autômato Finito |
| Tipo 2 | Livre de Contexto | Autômato de Pilha |
| Tipo 1 | Sensível ao Contexto | Autômato Limitado Linearmente |
| Tipo 0 | Irrestrita | Máquina de Turing |

Essa relação será importante nas próximas aulas sobre **Autômatos Finitos, Expressões Regulares, Autômatos de Pilha e Máquinas de Turing**.

---

# 15. Como classificar uma gramática?

Ao receber uma gramática, siga estes passos:

### Passo 1 — Identifique os componentes

Procure:

- terminais;
- não terminais;
- símbolo inicial;
- produções.

### Passo 2 — Observe as produções

Analise a estrutura das regras.

### Passo 3 — Procure restrições

Pergunte:

- O lado esquerdo possui apenas um não terminal?
- As produções possuem estrutura regular?
- Existe dependência de contexto?
- As regras são irrestritas?

### Passo 4 — Classifique

Determine o tipo da gramática de acordo com a hierarquia.

---

# 16. Exercícios

## Exercício 1 — Derivação

Considere:

\[
G_1:
\begin{cases}
S \rightarrow aS\\
S \rightarrow b
\end{cases}
\]

### a)

Gere:

```text
aaab
```

### b)

Gere outras duas palavras.

### c)

Explique:

> Como você sabe que a derivação terminou?

---

## Exercício 2 — Gramática Livre de Contexto

Considere:

\[
G_2:
\begin{cases}
S \rightarrow aSb\\
S \rightarrow \varepsilon
\end{cases}
\]

### a)

Gere:

```text
aabb
```

### b)

Gere:

```text
aaabbb
```

### c)

É possível gerar:

```text
aabbb
```

Justifique.

---

# 17. Exercício 3 — Classificação

Classifique cada gramática como **Regular** ou **Livre de Contexto**.

### Gramática A

\[
S \rightarrow aS
\]

\[
S \rightarrow b
\]

**Classificação:** ____________________

**Justificativa:**  
______________________________________

---

### Gramática B

\[
S \rightarrow aSb
\]

\[
S \rightarrow \varepsilon
\]

**Classificação:** ____________________

**Justificativa:**  
______________________________________

---

### Gramática C

\[
S \rightarrow aA
\]

\[
A \rightarrow b
\]

**Classificação:** ____________________

**Justificativa:**  
______________________________________

---

# 18. Desafio

Considere:

\[
G:
\begin{cases}
S \rightarrow aS\\
S \rightarrow bS\\
S \rightarrow \varepsilon
\end{cases}
\]

### Desafio 1

Gere:

```text
aab
```

### Desafio 2

Gere:

```text
abba
```

### Desafio 3

A gramática consegue gerar:

```text
ababab
```

Justifique.

### Desafio 4

Descreva, com suas palavras, qual é o padrão das palavras geradas.

---

# 19. Resumo da aula

Nesta aula aprendemos que:

- Uma **gramática formal** é formada por variáveis, terminais, produções e um símbolo inicial;
- As **produções** são utilizadas para gerar palavras;
- Uma **derivação** começa no símbolo inicial;
- Uma derivação termina quando não existem mais variáveis;
- Gramáticas **regulares** possuem regras bastante restritas;
- Gramáticas **livres de contexto** permitem estruturas mais complexas;
- A **Hierarquia de Chomsky** classifica as gramáticas em Tipos 0, 1, 2 e 3;
- Gramáticas regulares estão associadas aos **autômatos finitos**;
- Gramáticas livres de contexto estão associadas aos **autômatos de pilha**.

---

# 20. Para lembrar

> **Gramática = regras para gerar palavras.**

> **Derivação = aplicação passo a passo das regras.**

> **Terminal = aparece na palavra final.**

> **Não terminal = utilizado durante a derivação.**

> **Gramática Regular → Tipo 3**

> **Gramática Livre de Contexto → Tipo 2**

---

## Referências

- MENEZES, P. F. B. *Linguagens Formais e Autômatos*. 4. ed. Sagra Luzzatto.
- SOUSA, C. E. B. et al. *Linguagens Formais e Autômatos*. SAGAH, 2021.
- HOPCROFT, J. E.; ULLMAN, J. D.; MOTWANI, R. *Introdução à Teoria de Autômatos, Linguagens e Computação*.

---

## Próxima aula

### Autômatos Finitos

Na próxima aula serão introduzidos:

- Autômatos Finitos Determinísticos (AFD);
- Autômatos Finitos Não Determinísticos (AFN);
- estados;
- transições;
- estado inicial;
- estados finais;
- reconhecimento de linguagens.