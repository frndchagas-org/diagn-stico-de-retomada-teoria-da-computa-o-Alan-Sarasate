[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/zHqjFsRx)
# Diagnóstico de retomada - Teoria da Computação

Esta atividade serve para mapear o que você já domina sobre linguagens formais, autômatos, gramáticas e computabilidade.

Responda individualmente. Use suas palavras. Se usar IA depois da primeira tentativa, registre o uso na seção 7.

## 1. Mapa do que eu lembro

Marque cada tópico como: lembro bem, lembro parcialmente, não lembro, nunca vi ou não tenho certeza.

- alfabeto: lembro bem
- cadeia: lembro bem
- linguagem: lembro bem
- gramática: lembro bem
- autômato finito: lembro bem
- linguagem regular: lembro parcialmente
- linguagem livre de contexto: lembro parcialmente
- linguagem sensível ao contexto: não lembro
- linguagem irrestrita: não lembro
- hierarquia de Chomsky: não lembro
- computabilidade: lembro bem
- máquina de Turing: lembro parcialmente

## 2. Definições com exemplo

Explique, com suas palavras e com um exemplo simples, usando o alfabeto `Sigma = {a, b}`.

1. O que é um alfabeto?
R: é um conjunto de simbolos não vazio que determina o vocabulário que pode ser usado
2. O que é uma cadeia?
R: é uma sqquência finita de simbolos escolhidos com base no alfabeto
3. O que é uma linguagem?
R: é um conjunto de cadeias que é aceito por um autômato específico
4. O que é uma gramática?
R: o conjunto de regras que dá origem a uma linguagem (conjunto de cadeias).

## 3. Linguagens

Considere as linguagens:

```text
L1 = { w em {0,1}* | w termina com 01 }
L2 = { a^n b^n | n >= 0 }
L3 = { a^n b^n c^n | n >= 0 }
```

Para cada linguagem:

1. escreva três palavras que pertencem à linguagem;
R: L1 = {0001, 10001, 111101), L2 = {ab, aabb, aaabbb}, L3 = {abc, aabbcc, aaabbbccc}
2. escreva duas palavras que não pertencem;
R: l1 = {111, 110}, L2 = {aab, abbb}, L3 = {abbc, abcccc}
3. diga, se souber, em qual classe ela provavelmente se encaixa;
R: Não lembro exatamente o que isso significa.
4. explique o motivo em linguagem simples.
R: Não consegui responder a 3.

Não há problema em dizer "não sei". Nesse caso, escreva o que te deixou em dúvida.

## 4. Autômato finito

Considere o autômato abaixo, sobre o alfabeto `{0,1}`:

```text
Estados: q0, q1, q2
Estado inicial: q0
Estado final: q2

Transições:
q0 --0--> q1
q0 --1--> q0
q1 --0--> q1
q1 --1--> q2
q2 --0--> q1
q2 --1--> q0
```

Responda:

1. Qual linguagem esse autômato parece reconhecer?
R: Cadeias de números binários
2. Execute manualmente as cadeias abaixo e diga se aceita ou rejeita:
   - `01` aceita, pois: q0 -> q1 -> q2, terminando em q2, que é estado final.
   - `101` rejeitada, pois: q0 -> q0 -> q1, terminando em q1, que não é estado final.
   - `100` rejeitado, q0 -> q0 -> q0, terminando em q0, que não é estado final
   - `1101` aceita, pois: q0 -> q0 -> q1 -> q2
   - `111` rejeitado, pois: q0 -> q0 -> q0 -> q0
3. Monte uma tabela curta mostrando o caminho dos estados para pelo menos duas cadeias.
1101         |   0001
q0 -> q0: 1  |   q0 -> q1: 0
q0 -> q0: 1  |   q1 -> q1: 0
q0 -> q1: 0  |   q1 -> q1: 0
q1 -> q2: 1  |   q1 -> q2: 1

## 5. Gramática

Considere a gramática:

```text
S -> aS
S -> b
```

Responda:

1. Gere cinco cadeias produzidas por essa gramática.
R: ab, aab, aaab, aaaab, aaaaab
2. Descreva a linguagem em palavras.
R: É um conjuntos de cadeias que tem uma quantidade qualquer (finita) de a e sempre termina em b.
3. Essa gramática parece regular, livre de contexto ou outra classe? Justifique de forma simples.
R: Não lembro como classificar linguagens.

## 6. Ponto de dificuldade

Escolha um tópico da lista inicial e escreva:

1. o que você entende dele;
R: Classes de linguagens
2. onde você se confunde;
R: Não sei exatamente como classificar as lingaugens, Me confundo entre elas e alguns tipos eu realmente não sei/lembro.
3. que tipo de explicação ajudaria: desenho, exemplo, exercício guiado, analogia, prova passo a passo ou lista curta.
R: exemplos, lista curta

## 7. Uso de IA, se houver

Se você usou IA depois da primeira tentativa, registre:
R: Não usei IA, tudo que eu escrevi foram de coisas que eu lembrava e/ou tinha anotado.

```text
Pergunta feita:
Resumo da resposta:
Como eu verifiquei:
O que eu alterei na minha resposta:
O que ainda não entendi:
```

## Submissão no Moodle

Depois de finalizar, copie no Moodle:

```text
Repositório:
Commit final:
Autoavaliação: nível atual, maior dificuldade e tópico que precisa ser retomado.
```
