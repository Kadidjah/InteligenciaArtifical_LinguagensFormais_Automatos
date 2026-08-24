
writing{variant="document" id="58321" title="Práticas de Linguagem Formal — Linguagem, Alfabeto e Gramática"}

Práticas de Linguagem Formal

Linguagem, Alfabeto e Gramática

Disciplina: Práticas de Linguagem Formal
Conteúdo: Linguagem, alfabetos, palavras e gramáticas
Quantidade: 10 exercícios comentados + 10 exercícios propostos


---

Objetivos

Ao final desta lista, o estudante deverá ser capaz de:

identificar e representar alfabetos;

reconhecer palavras sobre um alfabeto;

determinar o comprimento de uma palavra;

identificar o símbolo vazio ε;

verificar se uma palavra pertence a uma linguagem;

representar linguagens por extensão e por compreensão;

compreender a definição de uma gramática formal;

identificar terminais e não terminais;

realizar derivações simples;

reconhecer palavras geradas por uma gramática.



---

Exercício 1 — Identificando um alfabeto

Considere o conjunto:

\Sigma = \{0,1\}

Questão

O que representa o conjunto ?

Resolução comentada

O símbolo  representa um alfabeto.

Um alfabeto é um conjunto finito e não vazio de símbolos que podem ser utilizados para formar palavras.

Neste caso:

\Sigma = \{0,1\}

Portanto, o alfabeto possui dois símbolos:

0

1


Algumas palavras que podem ser formadas sobre esse alfabeto são:

0,\quad 1,\quad 00,\quad 01,\quad 10,\quad 11,\quad 0101

Logo, o alfabeto é:

\boxed{\Sigma=\{0,1\}}

Exercício para o estudante

Considere:

\Sigma = \{a,b,c\}

1. Quantos símbolos existem no alfabeto?


2. Liste cinco palavras que podem ser formadas sobre esse alfabeto.


3. A palavra abcab utiliza somente símbolos de ?




---

Exercício 2 — Verificando se uma sequência é uma palavra

Considere o alfabeto:

\Sigma = \{a,b\}

Determine quais das sequências abaixo são palavras sobre :

a,\quad ab,\quad aba,\quad abc,\quad bba

Resolução comentada

Uma palavra sobre um alfabeto deve possuir somente símbolos pertencentes ao alfabeto.

Como:

\Sigma=\{a,b\}

temos:

a → pertence ao alfabeto → é palavra

ab → utiliza a e b → é palavra

aba → utiliza a e b → é palavra

abc → contém c, que não pertence a  → não é palavra

bba → utiliza b e a → é palavra


Portanto:

\boxed{a,\ ab,\ aba,\ bba}

são palavras sobre .

Exercício para o estudante

Considere:

\Sigma=\{0,1\}

Classifique as sequências abaixo como palavras ou não palavras sobre :

001,\quad 1010,\quad 120,\quad 111,\quad 00a


---

Exercício 3 — Comprimento de uma palavra

Considere a palavra:

w=101101

Determine o comprimento de .

Resolução comentada

O comprimento de uma palavra é a quantidade de símbolos que ela possui.

A palavra:

101101

possui seis símbolos:

1,\ 0,\ 1,\ 1,\ 0,\ 1

Logo:

|w|=6

Portanto:

\boxed{|101101|=6}

Exercício para o estudante

Determine o comprimento das seguintes palavras:

1. 0101


2. 111111


3. abcabc


4. 10000001


5. aabbab




---

Exercício 4 — A palavra vazia

Considere o alfabeto:

\Sigma=\{a,b\}

Qual é o comprimento da palavra vazia ?

Resolução comentada

A palavra vazia é representada por:

\varepsilon

Ela não possui nenhum símbolo.

Portanto, seu comprimento é:

|\varepsilon|=0

É importante não confundir a palavra vazia com uma palavra que contém algum símbolo.

Assim:

\boxed{|\varepsilon|=0}

Exercício para o estudante

Responda:

1. Quantos símbolos existem em ?


2. Qual é o valor de ?


3. A palavra vazia pode ser considerada uma palavra sobre qualquer alfabeto?




---

Exercício 5 — Linguagem por extensão

Considere:

L=\{a,ab,aba\}

Questão

Determine se as palavras abaixo pertencem a :

a

b

ab

aba

abab


Resolução comentada

A linguagem foi definida explicitamente:

L=\{a,ab,aba\}

Portanto, pertencem à linguagem somente as palavras que aparecem no conjunto.

Assim:

a\in L

b\notin L

ab\in L

aba\in L

abab\notin L

Logo:

Palavra	Pertence a ?

a	Sim
b	Não
ab	Sim
aba	Sim
abab	Não


Exercício para o estudante

Considere:

L=\{0,01,011,111\}

Determine quais palavras pertencem à linguagem:

0,\quad 00,\quad 01,\quad 011,\quad 11,\quad 111,\quad 0111


---

Exercício 6 — Linguagem definida por propriedade

Considere o alfabeto:

\Sigma=\{0,1\}

e a linguagem:

L=\{w\in\Sigma^* \mid w\text{ termina em }1\}

Determine se as palavras abaixo pertencem a :

01,\quad 10,\quad 111,\quad 100,\quad 101

Resolução comentada

A condição para pertencer à linguagem é:

> A palavra deve terminar com o símbolo 1.



Analisando:

01 → termina em 1 → pertence.

10 → termina em 0 → não pertence.

111 → termina em 1 → pertence.

100 → termina em 0 → não pertence.

101 → termina em 1 → pertence.


Portanto:

\boxed{01,\ 111,\ 101\in L}

e:

\boxed{10,\ 100\notin L}

Exercício para o estudante

Considere:

L=\{w\in\{a,b\}^* \mid w\text{ começa com }a\}

Determine quais palavras pertencem a :

a,\quad ab,\quad ba,\quad abb,\quad bba,\quad aaab


---

Exercício 7 — Identificando uma gramática

Considere a gramática:

G=(V,T,P,S)

com:

V=\{S\}

T=\{a,b\}

e as produções:

S\rightarrow aS

S\rightarrow b

Questão

Identifique os conjuntos de símbolos terminais e não terminais.

Resolução comentada

Uma gramática possui, entre outros elementos:

símbolos não terminais;

símbolos terminais;

produções;

símbolo inicial.


Neste exemplo:

V=\{S\}

é o conjunto dos não terminais.

O conjunto:

T=\{a,b\}

é o conjunto dos terminais.

Portanto:

Não terminal: S

Terminais: a e b

Símbolo inicial: S


As produções são:

S\rightarrow aS

e

S\rightarrow b

Exercício para o estudante

Considere a gramática:

G=(V,T,P,S)

com:

V=\{S,A\}

T=\{0,1\}

e:

S\rightarrow 0A

A\rightarrow 1

Identifique:

1. Os não terminais.


2. Os terminais.


3. O símbolo inicial.


4. As produções da gramática.




---

Exercício 8 — Realizando uma derivação

Considere a gramática:

S\rightarrow aS

S\rightarrow b

Questão

Mostre uma derivação para a palavra:

aaab

Resolução comentada

Começamos pelo símbolo inicial:

S

Aplicamos a produção:

S\rightarrow aS

Obtendo:

S\Rightarrow aS

Aplicamos novamente:

aS\Rightarrow aaS

Mais uma vez:

aaS\Rightarrow aaaS

Agora utilizamos:

S\rightarrow b

Então:

aaaS\Rightarrow aaab

A derivação completa é:

\boxed{S\Rightarrow aS\Rightarrow aaS\Rightarrow aaaS\Rightarrow aaab}

Portanto, a gramática consegue gerar a palavra aaab.

Exercício para o estudante

Utilizando a mesma gramática:

S\rightarrow aS

S\rightarrow b

faça uma derivação para:

aaab

Agora tente fazer também uma derivação para:

aaaab


---

Exercício 9 — Descobrindo a linguagem de uma gramática

Considere:

S\rightarrow aS

S\rightarrow b

Questão

Descreva a linguagem gerada pela gramática.

Resolução comentada

A produção:

S\rightarrow aS

permite adicionar quantos a forem necessários.

A produção:

S\rightarrow b

encerra a derivação.

Assim, podemos gerar:

b

ab

aab

aaab

aaaab

e assim por diante.

Portanto, a linguagem é:

L=\{a^nb\mid n\geq0\}

Em palavras: a linguagem contém qualquer quantidade de símbolos a, seguida obrigatoriamente por um b.

Exercício para o estudante

Considere a gramática:

S\rightarrow 0S

S\rightarrow 1

1. Escreva as cinco primeiras palavras geradas.


2. Escreva a linguagem usando uma expressão matemática semelhante a .


3. A palavra 0001 pertence à linguagem?


4. A palavra 0010 pertence à linguagem?




---

Exercício 10 — Analisando uma gramática completa

Considere a gramática:

G=(V,T,P,S)

onde:

V=\{S\}

T=\{0,1\}

e:

P:
\begin{cases}
S\rightarrow 0S\\
S\rightarrow 1S\\
S\rightarrow\varepsilon
\end{cases}

Questão

Que linguagem essa gramática gera?

Resolução comentada

As duas primeiras produções permitem acrescentar 0 ou 1:

S\rightarrow0S

S\rightarrow1S

A terceira produção:

S\rightarrow\varepsilon

permite finalizar a derivação.

Por exemplo:

S\Rightarrow0S\Rightarrow01S\Rightarrow011S\Rightarrow011\varepsilon

Logo:

S\Rightarrow011

Podemos gerar:

\varepsilon,\ 0,\ 1,\ 00,\ 01,\ 10,\ 11,\ 000,\ 001,\ldots

Ou seja, podemos gerar qualquer palavra formada pelos símbolos 0 e 1, inclusive a palavra vazia.

Portanto:

\boxed{L(G)=\{0,1\}^*}

Exercício para o estudante

Considere:

S\rightarrow aS

S\rightarrow bS

S\rightarrow\varepsilon

Responda:

1. Qual é o alfabeto terminal?


2. Qual é o símbolo inicial?


3. A palavra abba pode ser gerada?


4. Faça uma derivação para abba.


5. A palavra vazia pertence à linguagem?


6. Descreva a linguagem gerada pela gramática.




---

Gabarito dos exercícios para o estudante

Exercício 1

1. O alfabeto possui 3 símbolos.


2. Exemplos: a, b, c, ab, abc.


3. Sim, abcab utiliza somente símbolos de .



Exercício 2

001 → palavra

1010 → palavra

120 → não é palavra

111 → palavra

00a → não é palavra


Exercício 3

1. 0101 → 4


2. 111111 → 6


3. abcabc → 6


4. 10000001 → 8


5. aabbab → 6



Exercício 4

1. Nenhum símbolo.


2. .


3. Sim. A palavra vazia pode ser elemento de  para qualquer alfabeto .



Exercício 5

Pertencem:

0,\quad01,\quad011,\quad111

Não pertencem:

00,\quad11,\quad0111

Exercício 6

Pertencem à linguagem:

a,\quad ab,\quad abb,\quad aaab

Não pertencem:

ba,\quad bba

Exercício 7

1. Não terminais:



\{S,A\}

2. Terminais:



\{0,1\}

3. Símbolo inicial:



S

4. Produções:



S\rightarrow0A

A\rightarrow1

Exercício 8

Uma possível derivação é:

S\Rightarrow aS\Rightarrow aaS\Rightarrow aaaS\Rightarrow aaab

Para aaaab:

S\Rightarrow aS\Rightarrow aaS\Rightarrow aaaS\Rightarrow aaaaS\Rightarrow aaaab

Exercício 9

As cinco primeiras palavras são:

1,\quad01,\quad001,\quad0001,\quad00001

A linguagem é:

L=\{0^n1\mid n\geq0\}

0001 pertence à linguagem.

0010 não pertence.

Exercício 10

1. Terminais:



\{a,b\}

2. Símbolo inicial:



S

3. Sim, abba pode ser gerada.


4. Uma derivação:



S\Rightarrow aS\Rightarrow abS\Rightarrow abbS\Rightarrow abbaS\Rightarrow abba

5. Sim, pois:



S\Rightarrow\varepsilon

6. A linguagem é:



L=\{a,b\}^*


---

Resumo dos principais conceitos

Conceito	Significado

Alfabeto 	Conjunto finito de símbolos
Símbolo	Elemento pertencente ao alfabeto
Palavra	Sequência finita de símbolos
	Palavra vazia
	w
	Conjunto de todas as palavras sobre , incluindo 
Linguagem	Conjunto de palavras
Gramática	Sistema formal usado para gerar palavras
Terminal	Símbolo que aparece nas palavras geradas
Não terminal	Símbolo utilizado durante a derivação
Produção	Regra de transformação da gramática
Derivação	Aplicação sucessiva das produções



---

Desafio final

Considere a gramática:

S\rightarrow0S

S\rightarrow1S

S\rightarrow\varepsilon

Tente responder sem consultar o gabarito:

1. Qual é o alfabeto?


2. Qual é o símbolo inicial?


3. Faça uma derivação para 01011.


4. Faça uma derivação para 111.


5. A palavra 010201 pertence à linguagem?


6. Qual é a linguagem gerada pela gramática?



Objetivo: perceber que uma gramática simples pode representar uma linguagem infinita.

writing{variant="document" id="58321" title="Práticas de Linguagem Formal — Linguagem, Alfabeto e Gramática"}
# Práticas de Linguagem Formal
## Linguagem, Alfabeto e Gramática

**Disciplina:** Práticas de Linguagem Formal  
**Conteúdo:** Linguagem, alfabetos, palavras e gramáticas  
**Quantidade:** 10 exercícios comentados + 10 exercícios propostos

---

## Objetivos

Ao final desta lista, o estudante deverá ser capaz de:

- identificar e representar alfabetos;
- reconhecer palavras sobre um alfabeto;
- determinar o comprimento de uma palavra;
- identificar o símbolo vazio `ε`;
- verificar se uma palavra pertence a uma linguagem;
- representar linguagens por extensão e por compreensão;
- compreender a definição de uma gramática formal;
- identificar terminais e não terminais;
- realizar derivações simples;
- reconhecer palavras geradas por uma gramática.

---

# Exercício 1 — Identificando um alfabeto

Considere o conjunto:

\[
\Sigma = \{0,1\}
\]

### Questão

O que representa o conjunto \Sigma?

### Resolução comentada

O símbolo \Sigma representa um **alfabeto**.

Um alfabeto é um conjunto finito e não vazio de símbolos que podem ser utilizados para formar palavras.

Neste caso:

\[
\Sigma = \{0,1\}
\]

Portanto, o alfabeto possui dois símbolos:

- `0`
- `1`

Algumas palavras que podem ser formadas sobre esse alfabeto são:

\[
0,\quad 1,\quad 00,\quad 01,\quad 10,\quad 11,\quad 0101
\]

Logo, o alfabeto é:

\[
\boxed{\Sigma=\{0,1\}}
\]

### Exercício para o estudante

Considere:

\[
\Sigma = \{a,b,c\}
\]

1. Quantos símbolos existem no alfabeto?
2. Liste cinco palavras que podem ser formadas sobre esse alfabeto.
3. A palavra `abcab` utiliza somente símbolos de \Sigma?

---

# Exercício 2 — Verificando se uma sequência é uma palavra

Considere o alfabeto:

\[
\Sigma = \{a,b\}
\]

Determine quais das sequências abaixo são palavras sobre \Sigma:

\[
a,\quad ab,\quad aba,\quad abc,\quad bba
\]

### Resolução comentada

Uma palavra sobre um alfabeto deve possuir **somente símbolos pertencentes ao alfabeto**.

Como:

\[
\Sigma=\{a,b\}
\]

temos:

- `a` → pertence ao alfabeto → **é palavra**
- `ab` → utiliza `a` e `b` → **é palavra**
- `aba` → utiliza `a` e `b` → **é palavra**
- `abc` → contém `c`, que não pertence a \Sigma → **não é palavra**
- `bba` → utiliza `b` e `a` → **é palavra**

Portanto:

\[
\boxed{a,\ ab,\ aba,\ bba}
\]

são palavras sobre \Sigma.

### Exercício para o estudante

Considere:

\[
\Sigma=\{0,1\}
\]

Classifique as sequências abaixo como palavras ou não palavras sobre \Sigma:

\[
001,\quad 1010,\quad 120,\quad 111,\quad 00a
\]

---

# Exercício 3 — Comprimento de uma palavra

Considere a palavra:

\[
w=101101
\]

Determine o comprimento de w.

### Resolução comentada

O comprimento de uma palavra é a quantidade de símbolos que ela possui.

A palavra:

\[
101101
\]

possui seis símbolos:

\[
1,\ 0,\ 1,\ 1,\ 0,\ 1
\]

Logo:

\[
|w|=6
\]

Portanto:

\[
\boxed{|101101|=6}
\]

### Exercício para o estudante

Determine o comprimento das seguintes palavras:

1. `0101`
2. `111111`
3. `abcabc`
4. `10000001`
5. `aabbab`

---

# Exercício 4 — A palavra vazia

Considere o alfabeto:

\[
\Sigma=\{a,b\}
\]

Qual é o comprimento da palavra vazia \varepsilon?

### Resolução comentada

A palavra vazia é representada por:

\[
\varepsilon
\]

Ela não possui nenhum símbolo.

Portanto, seu comprimento é:

\[
|\varepsilon|=0
\]

É importante não confundir a palavra vazia com uma palavra que contém algum símbolo.

Assim:

\[
\boxed{|\varepsilon|=0}
\]

### Exercício para o estudante

Responda:

1. Quantos símbolos existem em \varepsilon?
2. Qual é o valor de |\varepsilon|?
3. A palavra vazia pode ser considerada uma palavra sobre qualquer alfabeto?

---

# Exercício 5 — Linguagem por extensão

Considere:

\[
L=\{a,ab,aba\}
\]

### Questão

Determine se as palavras abaixo pertencem a L:

- `a`
- `b`
- `ab`
- `aba`
- `abab`

### Resolução comentada

A linguagem foi definida explicitamente:

\[
L=\{a,ab,aba\}
\]

Portanto, pertencem à linguagem somente as palavras que aparecem no conjunto.

Assim:

\[
a\in L
\]

\[
b\notin L
\]

\[
ab\in L
\]

\[
aba\in L
\]

\[
abab\notin L
\]

Logo:

| Palavra | Pertence a L? |
|---|---|
| `a` | Sim |
| `b` | Não |
| `ab` | Sim |
| `aba` | Sim |
| `abab` | Não |

### Exercício para o estudante

Considere:

\[
L=\{0,01,011,111\}
\]

Determine quais palavras pertencem à linguagem:

\[
0,\quad 00,\quad 01,\quad 011,\quad 11,\quad 111,\quad 0111
\]

---

# Exercício 6 — Linguagem definida por propriedade

Considere o alfabeto:

\[
\Sigma=\{0,1\}
\]

e a linguagem:

\[
L=\{w\in\Sigma^* \mid w\text{ termina em }1\}
\]

Determine se as palavras abaixo pertencem a L:

\[
01,\quad 10,\quad 111,\quad 100,\quad 101
\]

### Resolução comentada

A condição para pertencer à linguagem é:

> A palavra deve terminar com o símbolo `1`.

Analisando:

- `01` → termina em `1` → pertence.
- `10` → termina em `0` → não pertence.
- `111` → termina em `1` → pertence.
- `100` → termina em `0` → não pertence.
- `101` → termina em `1` → pertence.

Portanto:

\[
\boxed{01,\ 111,\ 101\in L}
\]

e:

\[
\boxed{10,\ 100\notin L}
\]

### Exercício para o estudante

Considere:

\[
L=\{w\in\{a,b\}^* \mid w\text{ começa com }a\}
\]

Determine quais palavras pertencem a L:

\[
a,\quad ab,\quad ba,\quad abb,\quad bba,\quad aaab
\]

---

# Exercício 7 — Identificando uma gramática

Considere a gramática:

\[
G=(V,T,P,S)
\]

com:

\[
V=\{S\}
\]

\[
T=\{a,b\}
\]

e as produções:

\[
S\rightarrow aS
\]

\[
S\rightarrow b
\]

### Questão

Identifique os conjuntos de símbolos terminais e não terminais.

### Resolução comentada

Uma gramática possui, entre outros elementos:

- símbolos não terminais;
- símbolos terminais;
- produções;
- símbolo inicial.

Neste exemplo:

\[
V=\{S\}
\]

é o conjunto dos **não terminais**.

O conjunto:

\[
T=\{a,b\}
\]

é o conjunto dos **terminais**.

Portanto:

- Não terminal: `S`
- Terminais: `a` e `b`
- Símbolo inicial: `S`

As produções são:

\[
S\rightarrow aS
\]

e

\[
S\rightarrow b
\]

### Exercício para o estudante

Considere a gramática:

\[
G=(V,T,P,S)
\]

com:

\[
V=\{S,A\}
\]

\[
T=\{0,1\}
\]

e:

\[
S\rightarrow 0A
\]

\[
A\rightarrow 1
\]

Identifique:

1. Os não terminais.
2. Os terminais.
3. O símbolo inicial.
4. As produções da gramática.

---

# Exercício 8 — Realizando uma derivação

Considere a gramática:

\[
S\rightarrow aS
\]

\[
S\rightarrow b
\]

### Questão

Mostre uma derivação para a palavra:

\[
aaab
\]

### Resolução comentada

Começamos pelo símbolo inicial:

\[
S
\]

Aplicamos a produção:

\[
S\rightarrow aS
\]

Obtendo:

\[
S\Rightarrow aS
\]

Aplicamos novamente:

\[
aS\Rightarrow aaS
\]

Mais uma vez:

\[
aaS\Rightarrow aaaS
\]

Agora utilizamos:

\[
S\rightarrow b
\]

Então:

\[
aaaS\Rightarrow aaab
\]

A derivação completa é:

\[
\boxed{S\Rightarrow aS\Rightarrow aaS\Rightarrow aaaS\Rightarrow aaab}
\]

Portanto, a gramática consegue gerar a palavra `aaab`.

### Exercício para o estudante

Utilizando a mesma gramática:

\[
S\rightarrow aS
\]

\[
S\rightarrow b
\]

faça uma derivação para:

\[
aaab
\]

Agora tente fazer também uma derivação para:

\[
aaaab
\]

---

# Exercício 9 — Descobrindo a linguagem de uma gramática

Considere:

\[
S\rightarrow aS
\]

\[
S\rightarrow b
\]

### Questão

Descreva a linguagem gerada pela gramática.

### Resolução comentada

A produção:

\[
S\rightarrow aS
\]

permite adicionar quantos `a` forem necessários.

A produção:

\[
S\rightarrow b
\]

encerra a derivação.

Assim, podemos gerar:

\[
b
\]

\[
ab
\]

\[
aab
\]

\[
aaab
\]

\[
aaaab
\]

e assim por diante.

Portanto, a linguagem é:

\[
L=\{a^nb\mid n\geq0\}
\]

Em palavras: a linguagem contém **qualquer quantidade de símbolos `a`, seguida obrigatoriamente por um `b`**.

### Exercício para o estudante

Considere a gramática:

\[
S\rightarrow 0S
\]

\[
S\rightarrow 1
\]

1. Escreva as cinco primeiras palavras geradas.
2. Escreva a linguagem usando uma expressão matemática semelhante a a^nb.
3. A palavra `0001` pertence à linguagem?
4. A palavra `0010` pertence à linguagem?

---

# Exercício 10 — Analisando uma gramática completa

Considere a gramática:

\[
G=(V,T,P,S)
\]

onde:

\[
V=\{S\}
\]

\[
T=\{0,1\}
\]

e:

\[
P:
\begin{cases}
S\rightarrow 0S\\
S\rightarrow 1S\\
S\rightarrow\varepsilon
\end{cases}
\]

### Questão

Que linguagem essa gramática gera?

### Resolução comentada

As duas primeiras produções permitem acrescentar `0` ou `1`:

\[
S\rightarrow0S
\]

\[
S\rightarrow1S
\]

A terceira produção:

\[
S\rightarrow\varepsilon
\]

permite finalizar a derivação.

Por exemplo:

\[
S\Rightarrow0S\Rightarrow01S\Rightarrow011S\Rightarrow011\varepsilon
\]

Logo:

\[
S\Rightarrow011
\]

Podemos gerar:

\[
\varepsilon,\ 0,\ 1,\ 00,\ 01,\ 10,\ 11,\ 000,\ 001,\ldots
\]

Ou seja, podemos gerar **qualquer palavra formada pelos símbolos `0` e `1`**, inclusive a palavra vazia.

Portanto:

\[
\boxed{L(G)=\{0,1\}^*}
\]

### Exercício para o estudante

Considere:

\[
S\rightarrow aS
\]

\[
S\rightarrow bS
\]

\[
S\rightarrow\varepsilon
\]

Responda:

1. Qual é o alfabeto terminal?
2. Qual é o símbolo inicial?
3. A palavra `abba` pode ser gerada?
4. Faça uma derivação para `abba`.
5. A palavra vazia pertence à linguagem?
6. Descreva a linguagem gerada pela gramática.

---

# Gabarito dos exercícios para o estudante

## Exercício 1

1. O alfabeto possui 3 símbolos.
2. Exemplos: `a`, `b`, `c`, `ab`, `abc`.
3. Sim, `abcab` utiliza somente símbolos de \Sigma.

## Exercício 2

- `001` → palavra
- `1010` → palavra
- `120` → não é palavra
- `111` → palavra
- `00a` → não é palavra

## Exercício 3

1. `0101` → 4
2. `111111` → 6
3. `abcabc` → 6
4. `10000001` → 8
5. `aabbab` → 6

## Exercício 4

1. Nenhum símbolo.
2. |\varepsilon|=0.
3. Sim. A palavra vazia pode ser elemento de \Sigma^* para qualquer alfabeto \Sigma.

## Exercício 5

Pertencem:

\[
0,\quad01,\quad011,\quad111
\]

Não pertencem:

\[
00,\quad11,\quad0111
\]

## Exercício 6

Pertencem à linguagem:

\[
a,\quad ab,\quad abb,\quad aaab
\]

Não pertencem:

\[
ba,\quad bba
\]

## Exercício 7

1. Não terminais:

\[
\{S,A\}
\]

2. Terminais:

\[
\{0,1\}
\]

3. Símbolo inicial:

\[
S
\]

4. Produções:

\[
S\rightarrow0A
\]

\[
A\rightarrow1
\]

## Exercício 8

Uma possível derivação é:

\[
S\Rightarrow aS\Rightarrow aaS\Rightarrow aaaS\Rightarrow aaab
\]

Para `aaaab`:

\[
S\Rightarrow aS\Rightarrow aaS\Rightarrow aaaS\Rightarrow aaaaS\Rightarrow aaaab
\]

## Exercício 9

As cinco primeiras palavras são:

\[
1,\quad01,\quad001,\quad0001,\quad00001
\]

A linguagem é:

\[
L=\{0^n1\mid n\geq0\}
\]

`0001` pertence à linguagem.

`0010` não pertence.

## Exercício 10

1. Terminais:

\[
\{a,b\}
\]

2. Símbolo inicial:

\[
S
\]

3. Sim, `abba` pode ser gerada.

4. Uma derivação:

\[
S\Rightarrow aS\Rightarrow abS\Rightarrow abbS\Rightarrow abbaS\Rightarrow abba
\]

5. Sim, pois:

\[
S\Rightarrow\varepsilon
\]

6. A linguagem é:

\[
L=\{a,b\}^*
\]

---

# Resumo dos principais conceitos

| Conceito | Significado |
|---|---|
| Alfabeto \Sigma | Conjunto finito de símbolos |
| Símbolo | Elemento pertencente ao alfabeto |
| Palavra | Sequência finita de símbolos |
| \varepsilon | Palavra vazia |
| |w| | Comprimento da palavra w |
| \Sigma^* | Conjunto de todas as palavras sobre \Sigma, incluindo \varepsilon |
| Linguagem | Conjunto de palavras |
| Gramática | Sistema formal usado para gerar palavras |
| Terminal | Símbolo que aparece nas palavras geradas |
| Não terminal | Símbolo utilizado durante a derivação |
| Produção | Regra de transformação da gramática |
| Derivação | Aplicação sucessiva das produções |

---

## Desafio final

Considere a gramática:

\[
S\rightarrow0S
\]

\[
S\rightarrow1S
\]

\[
S\rightarrow\varepsilon
\]

Tente responder sem consultar o gabarito:

1. Qual é o alfabeto?
2. Qual é o símbolo inicial?
3. Faça uma derivação para `01011`.
4. Faça uma derivação para `111`.
5. A palavra `010201` pertence à linguagem?
6. Qual é a linguagem gerada pela gramática?

**Objetivo:** perceber que uma gramática simples pode representar uma linguagem infinita.2. Versão LaTeX para gerar o PDF

writing{variant="document" id="74106" title="Práticas de Linguagem Formal — Versão PDF em LaTeX"}

\documentclass[12pt,a4paper]{article}

\usepackage[utf8]{inputenc}
\usepackage[T1]{fontenc}
\usepackage[brazil]{babel}
\usepackage{amsmath,amssymb}
\usepackage{geometry}
\usepackage{xcolor}
\usepackage{enumitem}
\usepackage{booktabs}
\usepackage{fancyhdr}

\geometry{
    a4paper,
    left=2.5cm,
    right=2.5cm,
    top=2.5cm,
    bottom=2.5cm
}

\pagestyle{fancy}
\fancyhf{}
\rhead{Práticas de Linguagem Formal}
\lhead{Linguagem, Alfabeto e Gramática}
\cfoot{\thepage}

\title{
    \textbf{Práticas de Linguagem Formal}\\
    \large Linguagem, Alfabeto e Gramática
}

\author{}
\date{}

\begin{document}

\maketitle

\section*{Objetivos}

Ao final desta lista, o estudante deverá ser capaz de:

\begin{itemize}
    \item identificar e representar alfabetos;
    \item reconhecer palavras sobre um alfabeto;
    \item determinar o comprimento de uma palavra;
    \item identificar a palavra vazia $\varepsilon$;
    \item verificar se uma palavra pertence a uma linguagem;
    \item representar linguagens por extensão e por compreensão;
    \item compreender a definição de uma gramática formal;
    \item identificar terminais e não terminais;
    \item realizar derivações simples;
    \item reconhecer palavras geradas por uma gramática.
\end{itemize}

\section{Exercício 1 -- Identificando um alfabeto}

Considere:

\[
\Sigma=\{0,1\}
\]

O conjunto $\Sigma$ representa um \textbf{alfabeto}.

Um alfabeto é um conjunto finito e não vazio de símbolos que podem ser utilizados para formar palavras.

Neste caso, o alfabeto possui os símbolos $0$ e $1$.

Exemplos de palavras:

\[
0,\quad 1,\quad 00,\quad 01,\quad 10,\quad 11,\quad 0101
\]

\subsection*{Exercício para o estudante}

Considere:

\[
\Sigma=\{a,b,c\}
\]

\begin{enumerate}
    \item Quantos símbolos existem no alfabeto?
    \item Liste cinco palavras que podem ser formadas.
    \item A palavra $abcab$ utiliza somente símbolos de $\Sigma$?
\end{enumerate}

\section{Exercício 2 -- Verificando uma palavra}

Considere:

\[
\Sigma=\{a,b\}
\]

Classifique:

\[
a,\quad ab,\quad aba,\quad abc,\quad bba
\]

Uma palavra sobre um alfabeto deve conter somente símbolos pertencentes ao alfabeto.

Assim:

\[
a,\ ab,\ aba,\ bba
\]

são palavras sobre $\Sigma$.

A sequência $abc$ não é uma palavra sobre $\Sigma$, pois contém o símbolo $c$.

\subsection*{Exercício para o estudante}

Considere:

\[
\Sigma=\{0,1\}
\]

Classifique:

\[
001,\quad1010,\quad120,\quad111,\quad00a
\]

como palavras ou não palavras sobre $\Sigma$.

\section{Exercício 3 -- Comprimento}

Considere:

\[
w=101101
\]

O comprimento de uma palavra corresponde à quantidade de símbolos que ela possui.

Como $101101$ possui seis símbolos:

\[
|w|=6
\]

Logo:

\[
\boxed{|101101|=6}
\]

\subsection*{Exercício para o estudante}

Determine:

\begin{enumerate}
    \item $|0101|$
    \item $|111111|$
    \item $|abcabc|$
    \item $|10000001|$
    \item $|aabbab|$
\end{enumerate}

\section{Exercício 4 -- Palavra vazia}

A palavra vazia é representada por:

\[
\varepsilon
\]

Ela não possui nenhum símbolo.

Portanto:

\[
\boxed{|\varepsilon|=0}
\]

\subsection*{Exercício para o estudante}

Responda:

\begin{enumerate}
    \item Quantos símbolos existem em $\varepsilon$?
    \item Qual é o valor de $|\varepsilon|$?
    \item A palavra vazia pode ser considerada uma palavra sobre qualquer alfabeto?
\end{enumerate}

\section{Exercício 5 -- Linguagem por extensão}

Considere:

\[
L=\{a,ab,aba\}
\]

As palavras $a$, $ab$ e $aba$ pertencem a $L$.

As palavras $b$ e $abab$ não pertencem a $L$.

\[
a\in L,\qquad ab\in L,\qquad aba\in L
\]

\[
b\notin L,\qquad abab\notin L
\]

\subsection*{Exercício para o estudante}

Considere:

\[
L=\{0,01,011,111\}
\]

Determine quais pertencem a $L$:

\[
0,\quad00,\quad01,\quad011,\quad11,\quad111,\quad0111
\]

\section{Exercício 6 -- Linguagem definida por propriedade}

Considere:

\[
L=\{w\in\{0,1\}^*\mid w\text{ termina em }1\}
\]

Analisando:

\[
01\in L
\]

\[
10\notin L
\]

\[
111\in L
\]

\[
100\notin L
\]

\[
101\in L
\]

Portanto:

\[
\boxed{01,\ 111,\ 101\in L}
\]

\subsection*{Exercício para o estudante}

Considere:

\[
L=\{w\in\{a,b\}^*\mid w\text{ começa com }a\}
\]

Determine quais pertencem a $L$:

\[
a,\quad ab,\quad ba,\quad abb,\quad bba,\quad aaab
\]

\section{Exercício 7 -- Identificando uma gramática}

Considere:

\[
G=(V,T,P,S)
\]

com:

\[
V=\{S\}
\]

\[
T=\{a,b\}
\]

e:

\[
S\rightarrow aS
\]

\[
S\rightarrow b
\]

O conjunto $V$ representa os não terminais.

O conjunto $T$ representa os terminais.

Portanto:

\[
V=\{S\}
\]

é o conjunto de não terminais e:

\[
T=\{a,b\}
\]

é o conjunto de terminais.

\subsection*{Exercício para o estudante}

Considere:

\[
V=\{S,A\},\qquad T=\{0,1\}
\]

e:

\[
S\rightarrow0A
\]

\[
A\rightarrow1
\]

Identifique os não terminais, terminais, símbolo inicial e produções.

\section{Exercício 8 -- Derivação}

Considere:

\[
S\rightarrow aS
\]

\[
S\rightarrow b
\]

Uma derivação para $aaab$ é:

\[
S\Rightarrow aS
\Rightarrow aaS
\Rightarrow aaaS
\Rightarrow aaab
\]

Logo:

\[
\boxed{S\Rightarrow aS\Rightarrow aaS\Rightarrow aaaS\Rightarrow aaab}
\]

\subsection*{Exercício para o estudante}

Utilizando a mesma gramática, faça uma derivação para:

\[
aaaab
\]

\section{Exercício 9 -- Linguagem de uma gramática}

Considere:

\[
S\rightarrow aS
\]

\[
S\rightarrow b
\]

Podemos gerar:

\[
b,\quad ab,\quad aab,\quad aaab,\quad aaaab,\ldots
\]

Portanto:

\[
\boxed{L=\{a^nb\mid n\geq0\}}
\]

\subsection*{Exercício para o estudante}

Considere:

\[
S\rightarrow0S
\]

\[
S\rightarrow1
\]

\begin{enumerate}
    \item Escreva as cinco primeiras palavras.
    \item Represente a linguagem matematicamente.
    \item Verifique se $0001$ pertence à linguagem.
    \item Verifique se $0010$ pertence à linguagem.
\end{enumerate}

\section{Exercício 10 -- Gramática completa}

Considere:

\[
S\rightarrow0S
\]

\[
S\rightarrow1S
\]

\[
S\rightarrow\varepsilon
\]

As produções permitem acrescentar qualquer quantidade de $0$ e $1$.

A produção:

\[
S\rightarrow\varepsilon
\]

permite finalizar a derivação.

Por exemplo:

\[
S\Rightarrow0S
\Rightarrow01S
\Rightarrow011S
\Rightarrow011\varepsilon
\]

Logo:

\[
S\Rightarrow011
\]

A gramática gera qualquer palavra formada por $0$ e $1$, inclusive a palavra vazia.

Portanto:

\[
\boxed{L(G)=\{0,1\}^*}
\]

\subsection*{Exercício para o estudante}

Considere:

\[
S\rightarrow aS
\]

\[
S\rightarrow bS
\]

\[
S\rightarrow\varepsilon
\]

Responda:

\begin{enumerate}
    \item Qual é o alfabeto terminal?
    \item Qual é o símbolo inicial?
    \item A palavra $abba$ pode ser gerada?
    \item Faça uma derivação para $abba$.
    \item A palavra vazia pertence à linguagem?
    \item Descreva a linguagem gerada.
\end{enumerate}

\section*{Desafio final}

Considere:

\[
S\rightarrow0S
\]

\[
S\rightarrow1S
\]

\[
S\rightarrow\varepsilon
\]

Responda:

\begin{enumerate}
    \item Qual é o alfabeto?
    \item Qual é o símbolo inicial?
    \item Faça uma derivação para $01011$.
    \item Faça uma derivação para $111$.
    \item A palavra $010201$ pertence à linguagem?
    \item Qual é a linguagem gerada?
\end{enumerate}

\section*{Resumo}

\begin{center}
\begin{tabular}{ll}
\toprule
\textbf{Conceito} & \textbf{Significado}\\
\midrule
Alfabeto $\Sigma$ & Conjunto finito de símbolos\\
Palavra & Sequência finita de símbolos\\
$\varepsilon$ & Palavra vazia\\
$|w|$ & Comprimento de uma palavra\\
$\Sigma^*$ & Todas as palavras sobre $\Sigma$\\
Linguagem & Conjunto de palavras\\
Gramática & Sistema formal para gerar palavras\\
Terminal & Símbolo utilizado nas palavras\\
Não terminal & Símbolo usado durante derivações\\
Produção & Regra da gramática\\
Derivação & Aplicação sucessiva das produções\\
\bottomrule
\end{tabular}
\end{center}

\end{document}

Para gerar o PDF, salve o segundo conteúdo como praticas-linguagem-formal.tex e compile com LaTeX (por exemplo, pdflatex praticas-linguagem-formal.tex). O primeiro arquivo pode ser salvo diretamente como README.md para o GitHub.

writing{variant="document" id="74106" title="Práticas de Linguagem Formal — Versão PDF em LaTeX"}
```latex
\documentclass[12pt,a4paper]{article}

\usepackage[utf8]{inputenc}
\usepackage[T1]{fontenc}
\usepackage[brazil]{babel}
\usepackage{amsmath,amssymb}
\usepackage{geometry}
\usepackage{xcolor}
\usepackage{enumitem}
\usepackage{booktabs}
\usepackage{fancyhdr}

\geometry{
    a4paper,
    left=2.5cm,
    right=2.5cm,
    top=2.5cm,
    bottom=2.5cm
}

\pagestyle{fancy}
\fancyhf{}
\rhead{Práticas de Linguagem Formal}
\lhead{Linguagem, Alfabeto e Gramática}
\cfoot{\thepage}

\title{
    \textbf{Práticas de Linguagem Formal}\\
    \large Linguagem, Alfabeto e Gramática
}

\author{}
\date{}

\begin{document}

\maketitle

\section*{Objetivos}

Ao final desta lista, o estudante deverá ser capaz de:

\begin{itemize}
    \item identificar e representar alfabetos;
    \item reconhecer palavras sobre um alfabeto;
    \item determinar o comprimento de uma palavra;
    \item identificar a palavra vazia $\varepsilon$;
    \item verificar se uma palavra pertence a uma linguagem;
    \item representar linguagens por extensão e por compreensão;
    \item compreender a definição de uma gramática formal;
    \item identificar terminais e não terminais;
    \item realizar derivações simples;
    \item reconhecer palavras geradas por uma gramática.
\end{itemize}

\section{Exercício 1 -- Identificando um alfabeto}

Considere:

\[
\Sigma=\{0,1\}
\]

O conjunto $\Sigma$ representa um \textbf{alfabeto}.

Um alfabeto é um conjunto finito e não vazio de símbolos que podem ser utilizados para formar palavras.

Neste caso, o alfabeto possui os símbolos $0$ e $1$.

Exemplos de palavras:

\[
0,\quad 1,\quad 00,\quad 01,\quad 10,\quad 11,\quad 0101
\]

\subsection*{Exercício para o estudante}

Considere:

\[
\Sigma=\{a,b,c\}
\]

\begin{enumerate}
    \item Quantos símbolos existem no alfabeto?
    \item Liste cinco palavras que podem ser formadas.
    \item A palavra $abcab$ utiliza somente símbolos de $\Sigma$?
\end{enumerate}

\section{Exercício 2 -- Verificando uma palavra}

Considere:

\[
\Sigma=\{a,b\}
\]

Classifique:

\[
a,\quad ab,\quad aba,\quad abc,\quad bba
\]

Uma palavra sobre um alfabeto deve conter somente símbolos pertencentes ao alfabeto.

Assim:

\[
a,\ ab,\ aba,\ bba
\]

são palavras sobre $\Sigma$.

A sequência $abc$ não é uma palavra sobre $\Sigma$, pois contém o símbolo $c$.

\subsection*{Exercício para o estudante}

Considere:

\[
\Sigma=\{0,1\}
\]

Classifique:

\[
001,\quad1010,\quad120,\quad111,\quad00a
\]

como palavras ou não palavras sobre $\Sigma$.

\section{Exercício 3 -- Comprimento}

Considere:

\[
w=101101
\]

O comprimento de uma palavra corresponde à quantidade de símbolos que ela possui.

Como $101101$ possui seis símbolos:

\[
|w|=6
\]

Logo:

\[
\boxed{|101101|=6}
\]

\subsection*{Exercício para o estudante}

Determine:

\begin{enumerate}
    \item $|0101|$
    \item $|111111|$
    \item $|abcabc|$
    \item $|10000001|$
    \item $|aabbab|$
\end{enumerate}

\section{Exercício 4 -- Palavra vazia}

A palavra vazia é representada por:

\[
\varepsilon
\]

Ela não possui nenhum símbolo.

Portanto:

\[
\boxed{|\varepsilon|=0}
\]

\subsection*{Exercício para o estudante}

Responda:

\begin{enumerate}
    \item Quantos símbolos existem em $\varepsilon$?
    \item Qual é o valor de $|\varepsilon|$?
    \item A palavra vazia pode ser considerada uma palavra sobre qualquer alfabeto?
\end{enumerate}

\section{Exercício 5 -- Linguagem por extensão}

Considere:

\[
L=\{a,ab,aba\}
\]

As palavras $a$, $ab$ e $aba$ pertencem a $L$.

As palavras $b$ e $abab$ não pertencem a $L$.

\[
a\in L,\qquad ab\in L,\qquad aba\in L
\]

\[
b\notin L,\qquad abab\notin L
\]

\subsection*{Exercício para o estudante}

Considere:

\[
L=\{0,01,011,111\}
\]

Determine quais pertencem a $L$:

\[
0,\quad00,\quad01,\quad011,\quad11,\quad111,\quad0111
\]

\section{Exercício 6 -- Linguagem definida por propriedade}

Considere:

\[
L=\{w\in\{0,1\}^*\mid w\text{ termina em }1\}
\]

Analisando:

\[
01\in L
\]

\[
10\notin L
\]

\[
111\in L
\]

\[
100\notin L
\]

\[
101\in L
\]

Portanto:

\[
\boxed{01,\ 111,\ 101\in L}
\]

\subsection*{Exercício para o estudante}

Considere:

\[
L=\{w\in\{a,b\}^*\mid w\text{ começa com }a\}
\]

Determine quais pertencem a $L$:

\[
a,\quad ab,\quad ba,\quad abb,\quad bba,\quad aaab
\]

\section{Exercício 7 -- Identificando uma gramática}

Considere:

\[
G=(V,T,P,S)
\]

com:

\[
V=\{S\}
\]

\[
T=\{a,b\}
\]

e:

\[
S\rightarrow aS
\]

\[
S\rightarrow b
\]

O conjunto $V$ representa os não terminais.

O conjunto $T$ representa os terminais.

Portanto:

\[
V=\{S\}
\]

é o conjunto de não terminais e:

\[
T=\{a,b\}
\]

é o conjunto de terminais.

\subsection*{Exercício para o estudante}

Considere:

\[
V=\{S,A\},\qquad T=\{0,1\}
\]

e:

\[
S\rightarrow0A
\]

\[
A\rightarrow1
\]

Identifique os não terminais, terminais, símbolo inicial e produções.

\section{Exercício 8 -- Derivação}

Considere:

\[
S\rightarrow aS
\]

\[
S\rightarrow b
\]

Uma derivação para $aaab$ é:

\[
S\Rightarrow aS
\Rightarrow aaS
\Rightarrow aaaS
\Rightarrow aaab
\]

Logo:

\[
\boxed{S\Rightarrow aS\Rightarrow aaS\Rightarrow aaaS\Rightarrow aaab}
\]

\subsection*{Exercício para o estudante}

Utilizando a mesma gramática, faça uma derivação para:

\[
aaaab
\]

\section{Exercício 9 -- Linguagem de uma gramática}

Considere:

\[
S\rightarrow aS
\]

\[
S\rightarrow b
\]

Podemos gerar:

\[
b,\quad ab,\quad aab,\quad aaab,\quad aaaab,\ldots
\]

Portanto:

\[
\boxed{L=\{a^nb\mid n\geq0\}}
\]

\subsection*{Exercício para o estudante}

Considere:

\[
S\rightarrow0S
\]

\[
S\rightarrow1
\]

\begin{enumerate}
    \item Escreva as cinco primeiras palavras.
    \item Represente a linguagem matematicamente.
    \item Verifique se $0001$ pertence à linguagem.
    \item Verifique se $0010$ pertence à linguagem.
\end{enumerate}

\section{Exercício 10 -- Gramática completa}

Considere:

\[
S\rightarrow0S
\]

\[
S\rightarrow1S
\]

\[
S\rightarrow\varepsilon
\]

As produções permitem acrescentar qualquer quantidade de $0$ e $1$.

A produção:

\[
S\rightarrow\varepsilon
\]

permite finalizar a derivação.

Por exemplo:

\[
S\Rightarrow0S
\Rightarrow01S
\Rightarrow011S
\Rightarrow011\varepsilon
\]

Logo:

\[
S\Rightarrow011
\]

A gramática gera qualquer palavra formada por $0$ e $1$, inclusive a palavra vazia.

Portanto:

\[
\boxed{L(G)=\{0,1\}^*}
\]

\subsection*{Exercício para o estudante}

Considere:

\[
S\rightarrow aS
\]

\[
S\rightarrow bS
\]

\[
S\rightarrow\varepsilon
\]

Responda:

\begin{enumerate}
    \item Qual é o alfabeto terminal?
    \item Qual é o símbolo inicial?
    \item A palavra $abba$ pode ser gerada?
    \item Faça uma derivação para $abba$.
    \item A palavra vazia pertence à linguagem?
    \item Descreva a linguagem gerada.
\end{enumerate}

\section*{Desafio final}

Considere:

\[
S\rightarrow0S
\]

\[
S\rightarrow1S
\]

\[
S\rightarrow\varepsilon
\]

Responda:

\begin{enumerate}
    \item Qual é o alfabeto?
    \item Qual é o símbolo inicial?
    \item Faça uma derivação para $01011$.
    \item Faça uma derivação para $111$.
    \item A palavra $010201$ pertence à linguagem?
    \item Qual é a linguagem gerada?
\end{enumerate}

\section*{Resumo}

\begin{center}
\begin{tabular}{ll}
\toprule
\textbf{Conceito} & \textbf{Significado}\\
\midrule
Alfabeto $\Sigma$ & Conjunto finito de símbolos\\
Palavra & Sequência finita de símbolos\\
$\varepsilon$ & Palavra vazia\\
$|w|$ & Comprimento de uma palavra\\
$\Sigma^*$ & Todas as palavras sobre $\Sigma$\\
Linguagem & Conjunto de palavras\\
Gramática & Sistema formal para gerar palavras\\
Terminal & Símbolo utilizado nas palavras\\
Não terminal & Símbolo usado durante derivações\\
Produção & Regra da gramática\\
Derivação & Aplicação sucessiva das produções\\
\bottomrule
\end{tabular}
\end{center}

