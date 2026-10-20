# Atividade sobre agentes inteligentes

Aula 19/10/2026 | Professora Kadidja Valéria | Inteligência artificial

**Disciplina:** Inteligência Artificial, Linguagens Formais e Autômatos

**Estudante:** Pedro Freire de Farias | **Turma:** Engenharia de Software

Realize os exercícios 2.3, 2.4 e 2.5 do Capítulo 2 sobre agentes inteligentes. Analise a racionalidade, descreva ambientes de tarefa por meio do modelo PEAS e explique os conceitos com suas próprias palavras. Utilize o capítulo disponibilizado e justifique suas respostas.

**Modalidade sugerida:** individual com consulta. **Tempo estimado:** 2h30. **Prazo:** conforme orientação da professora.

## Preparação
Leia os tópicos sobre racionalidade, ambientes e estrutura dos agentes, especialmente a Seção 2.3.2.

## Exercício 2.3
Para cada afirmação, indique V ou F, justifique e forneça exemplo ou contraexemplo. Explicite as hipóteses utilizadas.

### a. Um agente que detecta apenas informações parciais sobre o estado não pode ser perfeitamente racional.

- Julgamento: **F**
- Justificativa: A racionalidade não exige observação completa; exige escolher a melhor ação possível com base nas percepções, no conhecimento e na medida de desempenho. Hipótese: o agente usa adequadamente as informações limitadas que possui.
- Exemplo ou contraexemplo: Um robô aspirador pode agir racionalmente limpando a área detectada e explorando áreas desconhecidas, mesmo sem ver a casa inteira.

### b. Existem ambientes de tarefa nos quais nenhum agente reativo puro pode comportar-se racionalmente.

- Julgamento: **V**
- Justificativa: Um agente reativo puro decide apenas pela percepção atual e não mantém estado interno sobre o passado. Em ambientes nos quais duas situações visualmente iguais exigem ações diferentes por causa do histórico, essa estratégia é insuficiente. Hipótese: a percepção atual não revela o histórico necessário.
- Exemplo ou contraexemplo: Um robô em um labirinto precisa lembrar quais caminhos já explorou; sem memória, pode ficar andando em círculos.

### c. Existe um ambiente de tarefa em que todo agente é racional.

- Julgamento: **V**
- Justificativa: Pode existir um ambiente em que todas as ações disponíveis tenham exatamente o mesmo desempenho; nesse caso, qualquer escolha é racional. Hipótese: a medida de desempenho considera todas as ações equivalentes.
- Exemplo ou contraexemplo: Três botões que concedem a mesma recompensa e não alteram o resultado final.

### d. A entrada para o programa de agente é a mesma que a entrada para a função de agente.

- Julgamento: **F**
- Justificativa: A função de agente é uma descrição abstrata que associa o histórico completo de percepções a uma ação. O programa de agente é sua implementação em uma arquitetura e normalmente recebe apenas a percepção atual, guardando o histórico relevante em estado interno.
- Exemplo ou contraexemplo: O programa recebe a leitura atual de um sensor e consulta a memória antes de agir, enquanto a função considera toda a sequência de leituras.

### e. Toda função de agente é implementável por uma combinação de programa/máquina.

- Julgamento: **F**
- Justificativa: Nem toda função matematicamente possível pode ser implementada por um programa/máquina: há funções não computáveis e limitações de recursos, como memória finita. Hipótese: considera-se a computação convencional.
- Exemplo ou contraexemplo: Não existe algoritmo geral que resolva corretamente o problema da parada para qualquer programa.

### f. Suponha que um agente selecione sua ação uniformemente ao acaso do conjunto de ações possíveis. Existe um ambiente de tarefa determinista em que esse agente é racional.

- Julgamento: **V**
- Justificativa: Um ambiente pode ser determinista e, ainda assim, tornar todas as ações igualmente boas. Se a escolha aleatória não altera a medida de desempenho, o agente continua racional. Hipótese: todas as ações possíveis têm o mesmo valor de desempenho.
- Exemplo ou contraexemplo: Uma sala em que qualquer botão pressionado concede a mesma recompensa.

### g. É possível para um dado agente ser perfeitamente racional em dois ambientes de tarefa distintos.

- Julgamento: **V**
- Justificativa: Um agente pode ser racional em ambientes distintos se suas ações forem adequadas às percepções e aos objetivos de cada um.
- Exemplo ou contraexemplo: Um robô que desvia de obstáculos pode atuar racionalmente em um escritório e em um depósito, desde que seus sensores e regras sejam apropriados aos dois.

### h. Todo agente é racional em um ambiente não observável.

- Julgamento: **F**
- Justificativa: A falta de observações não torna automaticamente todos os agentes racionais. A racionalidade continua dependendo da ação escolhida e da medida de desempenho. Só se todas as ações fossem equivalentes qualquer escolha seria racional.
- Exemplo ou contraexemplo: Em um ambiente sem percepções em que apenas pressionar o botão A dá recompensa, um agente que sempre escolhe B é irracional.

### i. Um agente jogador de pôquer perfeitamente racional nunca perde.

- Julgamento: **F**
- Justificativa: Racionalidade não garante vitória, especialmente em jogos com aleatoriedade e informação incompleta. Um jogador pode tomar a decisão com maior valor esperado e ainda perder por causa das cartas distribuídas ou da estratégia do adversário.
- Exemplo ou contraexemplo: Apostar corretamente com uma mão forte e perder para uma combinação superior do adversário.

## Exercício 2.4
Para cada caso, delimite o agente, preencha o PEAS e justifique todas as classificações. Considere Titã como cenário hipotético do exercício.

### Caso 1 — Jogar futebol.

- Agente analisado: Um jogador de ataque (não a equipe inteira).
- Objetivo e hipóteses: Contribuir para a vitória do time; o agente é um único jogador.
- P — Medida de desempenho: Gols, passes úteis e vitória do time.
- E — Ambiente: Campo, bola, gols, companheiros, adversários e árbitro.
- A — Atuadores: Pernas e pés para correr, chutar e passar; corpo para disputar a bola; voz para se comunicar.
- S — Sensores: Visão e audição.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade | Parcialmente observável | O jogador não vê o campo inteiro ao mesmo tempo nem conhece as intenções dos outros. |
| Número de agentes | Multiagente (cooperação e competição) | Coopera com os companheiros e compete contra os adversários. |
| Previsibilidade | Estocástico | Há incerteza nas ações dos outros jogadores e na execução dos lances. |
| Dependência entre decisões | Sequencial | Cada jogada afeta as jogadas seguintes. |
| Mudança durante a decisão | Dinâmico | Jogadores e bola continuam se movendo enquanto o jogador decide. |
| Natureza dos elementos | Combinação | Elementos discretos (gols, faltas) e contínuos (posição, velocidade e tempo). |
| Conhecimento do funcionamento | Conhecido | O jogador conhece as regras do futebol e o efeito das próprias ações; a incerteza sobre os adversários já está na observabilidade e na previsibilidade. |

### Caso 2 — Explorar os oceanos subterrâneos de Titã.

- Agente analisado: Robô submarino autônomo.
- Objetivo e hipóteses: Explorar e coletar dados em um oceano hipotético sob o gelo; como a comunicação com a Terra é atrasada, o robô precisa decidir sozinho.
- P — Medida de desempenho: Área explorada, qualidade dos dados, energia preservada e conclusão segura da missão.
- E — Ambiente: Oceano escuro, gelado, sob alta pressão e pouco conhecido.
- A — Atuadores: Propulsores, braço de coleta e sistema de comunicação.
- S — Sensores: Sonar, câmera com iluminação e sensores de temperatura, pressão e composição química.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade | Parcialmente observável | No escuro, os sensores só revelam a região próxima ao robô. |
| Número de agentes | Agente único | No modelo simplificado, só o robô age no ambiente; a equipe na Terra é apenas suporte externo. |
| Previsibilidade | Estocástico | Correntes, falhas e condições desconhecidas tornam o resultado das ações incerto. |
| Dependência entre decisões | Sequencial | A rota escolhida e a energia gasta afetam as decisões futuras. |
| Mudança durante a decisão | Dinâmico | Correntes e condições do oceano podem variar enquanto o robô decide. |
| Natureza dos elementos | Combinação | Estados discretos da missão e grandezas contínuas (posição, profundidade, energia). |
| Conhecimento do funcionamento | Desconhecido | Ninguém conhece completamente como esse oceano funciona; o robô precisa aprender durante a exploração. |

### Caso 3 — Comprar livros usados de IA na Internet.

- Agente analisado: Programa que compra o livro solicitado por um usuário.
- Objetivo e hipóteses: Comprar o título correto, priorizando preço total, estado do livro e prazo de entrega.
- P — Medida de desempenho: Livro correto, em bom estado, com menor custo total razoável e entrega no prazo.
- E — Ambiente: Lojas e sites, anúncios, vendedores, outros compradores e sistemas de pagamento.
- A — Atuadores: Pesquisar, filtrar, comparar, adicionar ao carrinho e confirmar a compra após autorização do usuário.
- S — Sensores: Páginas, preços, fotos, descrições, avaliações e confirmações digitais.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade | Parcialmente observável | Fotos e descrições não garantem o estado real do livro. |
| Número de agentes | Multiagente | Vendedores e outros compradores têm interesses próprios e podem comprar o livro antes. |
| Previsibilidade | Estocástico | Anúncios e estoque podem mudar sem aviso. |
| Dependência entre decisões | Sequencial | As etapas se encadeiam: pesquisa, escolha, pagamento e acompanhamento. |
| Mudança durante a decisão | Dinâmico | Ofertas podem desaparecer enquanto o programa compara preços. |
| Natureza dos elementos | Combinação | Escolhas discretas (anúncios, botões) e valores numéricos como preço e prazo. |
| Conhecimento do funcionamento | Conhecido | O programa conhece as regras dos sites e o efeito de suas ações; não saber o estado real do livro é uma questão de observabilidade. |

### Caso 4 — Jogar uma partida de tênis.

- Agente analisado: Um jogador contra outra pessoa.
- Objetivo e hipóteses: Vencer a partida seguindo as regras do tênis.
- P — Medida de desempenho: Pontos, games, sets e vitória.
- E — Ambiente: Quadra, rede, bola, adversário e árbitro.
- A — Atuadores: Braços e raquete para sacar e rebater; pernas para se posicionar.
- S — Sensores: Visão da bola e do adversário, audição e percepção do próprio corpo.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade | Parcialmente observável | As intenções e a próxima jogada do adversário não são conhecidas. |
| Número de agentes | Multiagente competitivo | Há um adversário tentando vencer. |
| Previsibilidade | Estocástico | A execução dos golpes e as condições externas tornam o resultado incerto. |
| Dependência entre decisões | Sequencial | Cada golpe provoca uma resposta do adversário. |
| Mudança durante a decisão | Dinâmico | A bola está em movimento enquanto o jogador decide. |
| Natureza dos elementos | Combinação | Pontuação discreta e movimento contínuo. |
| Conhecimento do funcionamento | Conhecido | O jogador conhece as regras do tênis e o efeito dos próprios golpes. |

### Caso 5 — Praticar tênis contra uma parede.

- Agente analisado: Um jogador treinando sozinho.
- Objetivo e hipóteses: Treinar rebatidas; a parede não é um agente porque não escolhe ações.
- P — Medida de desempenho: Sequência de rebatidas sem erro e precisão.
- E — Ambiente: Área de treino, parede e bola.
- A — Atuadores: Braços, raquete e pernas.
- S — Sensores: Visão da bola, audição e percepção do próprio corpo.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade | Parcialmente observável | O jogador não percebe perfeitamente todas as variáveis do golpe, como efeito e força exata. |
| Número de agentes | Agente único | A parede não decide nada; só o jogador age. |
| Previsibilidade | Estocástico | Pequenas variações na força e no ângulo de cada batida mudam a trajetória da bola, então o retorno não é exatamente previsível. |
| Dependência entre decisões | Sequencial | Cada rebatida define a trajetória da próxima. |
| Mudança durante a decisão | Dinâmico | A bola se move enquanto o jogador decide. |
| Natureza dos elementos | Combinação | Contagem discreta de rebatidas e grandezas contínuas (posição, velocidade). |
| Conhecimento do funcionamento | Conhecido | O jogador conhece como a bola se comporta ao bater na parede e o efeito dos próprios golpes. |

### Caso 6 — Realizar um salto de altura.

- Agente analisado: Atleta de salto em altura.
- Objetivo e hipóteses: Superar o sarrafo na maior altura possível, sem cometer falta e com segurança.
- P — Medida de desempenho: Altura válida, sucesso da tentativa e segurança.
- E — Ambiente: Pista, sarrafo, colchão e condições ambientais.
- A — Atuadores: Pernas para correr e impulsionar; corpo para ajustar a passagem sobre o sarrafo.
- S — Sensores: Visão, equilíbrio e percepção do próprio corpo.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade | Parcialmente observável | Nem todas as variáveis do movimento e do ambiente (como o vento) são percebidas perfeitamente. |
| Número de agentes | Agente único | Ninguém interfere durante a execução do salto. |
| Previsibilidade | Estocástico | Variações na execução e nas condições físicas mudam o resultado. |
| Dependência entre decisões | Sequencial | Corrida, impulsão e passagem são etapas encadeadas. |
| Mudança durante a decisão | Estático | Sarrafo, colchão e pista não mudam enquanto o atleta decide; quem se move é o próprio atleta. |
| Natureza dos elementos | Combinação | Resultado discreto (válido ou inválido) e grandezas contínuas (altura, velocidade e ângulo). |
| Conhecimento do funcionamento | Conhecido | O atleta conhece as regras da prova e a técnica do salto. |

### Caso 7 — Participar de um leilão de um item, realizando lances.

- Agente analisado: Participante que dá lances por um item.
- Objetivo e hipóteses: Ganhar o item sem ultrapassar seu limite financeiro.
- P — Medida de desempenho: Ganhar o item pagando até o limite e evitando preço excessivo.
- E — Ambiente: Plataforma ou casa de leilão, item, leiloeiro e concorrentes.
- A — Atuadores: Levantar a placa, falar o lance ou clicar para ofertar.
- S — Sensores: Lances divulgados, preço atual, tempo restante e informações do item.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade | Parcialmente observável | Os limites e as intenções dos concorrentes são desconhecidos. |
| Número de agentes | Multiagente competitivo | Os concorrentes disputam o mesmo item. |
| Previsibilidade | Estocástico | Os lances futuros dos concorrentes são incertos. |
| Dependência entre decisões | Sequencial | Cada lance altera as decisões seguintes. |
| Mudança durante a decisão | Dinâmico | Preço e tempo mudam enquanto o participante decide. |
| Natureza dos elementos | Combinação | Lances discretos em valores monetários e tempo contínuo. |
| Conhecimento do funcionamento | Conhecido | O participante conhece as regras do leilão; as estratégias dos concorrentes entram em observabilidade e previsibilidade. |

### Opções para classificação
- **Observabilidade:** Completamente observável, parcialmente observável ou não observável.
- **Número de agentes:** Agente único ou multiagente; indique cooperação ou competição quando pertinente.
- **Previsibilidade:** Determinístico ou estocástico; considere a influência estratégica de outros agentes.
- **Dependência entre decisões:** Episódico ou sequencial.
- **Mudança durante a decisão:** Estático, dinâmico ou semidinâmico.
- **Natureza dos elementos:** Discretos, contínuos ou combinação; considere estados, tempo, percepções e ações.
- **Conhecimento do funcionamento:** Conhecido ou desconhecido para o agente.

### Comparação final
1. O que muda entre jogar tênis contra outra pessoa e praticar contra uma parede?
2. Por que comprar livros usados pode exigir decisões com informações incompletas?
3. Como outros agentes influenciam futebol e leilões?

Respostas:

1. No tênis contra uma pessoa, o ambiente é multiagente competitivo: o adversário adapta suas decisões para vencer. Contra uma parede, há um único agente que decide, e a devolução depende só das propriedades físicas da bola e da parede. Os dois continuam sequenciais e dinâmicos.
2. Na compra de livros usados, fotos e descrições não mostram perfeitamente defeitos, autenticidade ou se o vendedor vai cumprir o combinado; por isso, o programa decide com evidências incompletas e precisa avaliar riscos.
3. No futebol, companheiros e adversários mudam posições e oportunidades a todo momento; no leilão, os lances dos concorrentes alteram o preço e a chance de vencer. Nos dois casos, o agente precisa considerar as estratégias dos outros.

## Exercício 2.5
Defina cada termo com suas palavras em duas a quatro linhas e apresente um exemplo.

### Agente

- Definição: Entidade que percebe o ambiente por meio de sensores e age sobre ele por meio de atuadores. Pode ser uma pessoa, um robô ou um programa.
- Exemplo: Um robô aspirador percebe obstáculos e movimenta as rodas para desviar.

### Função de agente

- Definição: Descrição abstrata que associa cada histórico de percepções a uma ação. Define o comportamento esperado sem dizer como ele será programado.
- Exemplo: Se o robô já passou duas vezes pelo mesmo corredor e encontra um obstáculo à frente, a função determina virar para um lado ainda não explorado.

### Programa de agente

- Definição: Implementação executável da função de agente em uma arquitetura. Processa as entradas e produz comandos, podendo manter informações internas.
- Exemplo: Um programa em Python lê a distância do sensor e comanda o desvio do robô.

### Racionalidade

- Definição: Escolher a ação que melhor atende à medida de desempenho, considerando as percepções, o conhecimento e os resultados esperados. Ser racional não significa sempre vencer.
- Exemplo: Um jogador de pôquer desiste quando as probabilidades tornam a aposta desvantajosa.

### Autonomia

- Definição: Capacidade de tomar decisões a partir das próprias percepções e experiências, sem depender inteiramente de instruções externas. A aprendizagem pode aumentar a autonomia.
- Exemplo: Um robô altera sozinho a rota ao detectar um obstáculo inesperado.

### Agente reativo

- Definição: Escolhe ações a partir da percepção atual, geralmente por regras condição–ação, sem manter um modelo interno do histórico.
- Exemplo: Um termostato liga o aquecimento quando a temperatura cai abaixo do limite.

### Agente baseado em modelo

- Definição: Mantém um estado interno que representa aspectos do ambiente e ajuda a interpretar o que não está sendo observado no momento. Usa percepções atuais e informações anteriores.
- Exemplo: Um aspirador registra quais áreas já limpou para escolher onde ir depois.

### Agente baseado em objetivos

- Definição: Escolhe ações considerando um estado ou resultado que deseja alcançar. Pode comparar sequências de ações para chegar ao objetivo.
- Exemplo: Um robô calcula uma rota até a estação de recarga.

### Agente baseado em utilidade

- Definição: Avalia o quanto diferentes resultados são desejáveis por meio de uma medida de utilidade e procura maximizar a utilidade esperada.
- Exemplo: Um programa compara preço, conservação, reputação do vendedor e prazo para escolher um livro usado.

### Agente com aprendizagem

- Definição: Melhora ou adapta seu comportamento a partir da experiência e dos resultados obtidos, podendo agir melhor em situações novas.
- Exemplo: Um sistema de recomendação ajusta sugestões de livros conforme as escolhas e avaliações do usuário.

## Síntese com autômatos
Escolha um caso do item 2.4. Apresente três estados internos, três percepções, três ações e duas regras no formato estado atual + percepção → próximo estado e ação. Explique como estados internos representam informação passada e cite uma limitação da simplificação.

Resposta:

**Caso escolhido:** robô submarino explorando Titã (Caso 2).

| Estados internos | Percepções | Ações |
|---|---|---|
| E1 — Explorando | P1 — Região desconhecida detectada | A1 — Explorar |
| E2 — Coletando | P2 — Sinal ou amostra relevante | A2 — Coletar |
| E3 — Retornando | P3 — Energia baixa | A3 — Retornar |

**Regras:**

- E1 (Explorando) + P2 (amostra relevante) → E2 (Coletando) e A2 (Coletar)
- E2 (Coletando) + P3 (energia baixa) → E3 (Retornando) e A3 (Retornar)

**Como o estado interno representa informação passada:** o estado resume o que aconteceu nas etapas anteriores, como a decisão de investigar um ponto ou a necessidade de interromper a coleta. Assim, o robô não precisa guardar todo o histórico de percepções, só o estado atual.

**Limitação:** três estados não representam toda a complexidade real, como posição, profundidade, incerteza dos sensores, obstáculos e níveis contínuos de energia.

## Entrega e avaliação
Confira: identificação; nove análises no item 2.3; sete casos completos no item 2.4; dez conceitos no item 2.5; síntese; referências.
Nome sugerido: `NomeSobrenome_Atividade_AgentesInteligentes`. Prazo e envio conforme orientação da professora.

| Critério | Atividade avaliativa (1,0 ponto) A2 |
|---|---:|
| Item 2.3 — correção e argumentação | 30% |
| Item 2.4 — PEAS e classificação justificada | 40% |
| Item 2.5 — precisão conceitual e exemplos | 20% |
| Síntese, organização e referências | 10% |

## Referências
Material-base: Capítulo 2 — Agentes inteligentes, disponibilizado para a aula de 19/10/2026.

Referências adicionais: RUSSELL, Stuart J.; NORVIG, Peter. *Inteligência Artificial: uma abordagem moderna*. 3. ed. Rio de Janeiro: Elsevier, 2013. Cap. 2.
