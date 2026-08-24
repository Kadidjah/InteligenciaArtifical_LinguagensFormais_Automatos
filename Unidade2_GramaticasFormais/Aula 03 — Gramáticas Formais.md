# Gramáticas Formais

**Disciplina:** Linguagens Formais e Autômatos  
**Duração:** 1h30  
**Tema:** Gramáticas Formais e Hierarquia de Chomsky

---

# 1. Objetivos da aula

Ao final da aula, o estudante deverá ser capaz de:

- Compreender o conceito de gramática formal;
- Identificar os componentes de uma gramática;
- Interpretar e ler regras de produção;
- Realizar derivações passo a passo;
- Diferenciar gramáticas regulares e livres de contexto;
- Compreender a Hierarquia de Chomsky;
- Classificar uma gramática a partir de suas regras;
- Construir exemplos simples de gramáticas regulares e livres de contexto.

---

# 2. Roteiro da aula

| Tempo | Etapa | Atividade |
|---|---|---|
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

$$
\Sigma = \{a,b\}
$$

Uma linguagem pode ser formada por várias palavras:

$$
L = \{a, ab, abb, abbb,\ldots\}
$$

Uma pergunta importante é:

> **Como podemos descrever formalmente quais palavras pertencem a uma linguagem?**

Uma das respostas é utilizar uma **gramática formal**.

---

# 4. O que é uma Gramática Formal?

Uma gramática formal pode ser representada por:

$$
G = (V,T,P,S)
$$

Cada componente possui uma função específica.

| Símbolo | Nome | Função |
|---|---|---|
| $V$ | Variáveis ou não terminais | Símbolos auxiliares utilizados durante a geração |
| $T$ | Terminais | Símbolos que aparecem nas palavras da linguagem |
| $P$ | Produções | Regras utilizadas para gerar as palavras |
| $S$ | Símbolo inicial | Símbolo onde começa a derivação |

Podemos pensar em uma gramática como um conjunto de regras para produzir palavras.

---

# 5. Como ler uma regra de produção?

Considere a regra:

$$
S \rightarrow aS
$$

Lemos:

> **"S produz aS"**

ou:

> **"S pode ser substituído por aS."**

Outra regra:

$$
S \rightarrow b
$$

Lemos:

> **"S produz b."**

O símbolo:

$$
\rightarrow
$$

pode ser interpretado como:

> **"pode ser substituído por"** ou **"produz"**.

---

# 6. Exemplo de derivação passo a passo

Considere a gramática:

$$
G = (\{S\},\{a,b\},P,S)
$$

com as produções:

$$
P:
\begin{cases}
S \rightarrow aS\\
S \rightarrow b
\end{cases}
$$

Vamos gerar uma palavra.

## Passo 1 — Começamos pelo símbolo inicial

$$
S
$$

## Passo 2 — Aplicamos a primeira produção

$$
S \rightarrow aS
$$

Portanto:

$$
S \Rightarrow aS
$$

## Passo 3 — Aplicamos novamente a regra

$$
aS \Rightarrow aaS
$$

## Passo 4 — Encerramos a derivação

Agora utilizamos:

$$
S \rightarrow b
$$

Logo:

$$
aaS \Rightarrow aab
$$

A derivação completa é:

$$
\boxed{
S \Rightarrow aS \Rightarrow aaS \Rightarrow aab
}
$$

A palavra gerada é:

$$
\boxed{aab}
$$

## Como saber que terminou?

A derivação termina quando não existem mais variáveis ou não terminais.

Nesse exemplo:

```text
aab
