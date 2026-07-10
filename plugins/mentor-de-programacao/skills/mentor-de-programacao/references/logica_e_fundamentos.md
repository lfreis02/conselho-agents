# Referência: Lógica e fundamentos

Quando a pessoa "não pensa em código", o buraco quase sempre está nos
fundamentos, não na linguagem. Sintaxe se decora; lógica se constrói.
Aqui o objetivo é fazer a pessoa raciocinar como um programa executa.

## Princípios
- O computador é literal e burro: faz exatamente o que está escrito, na
  ordem escrita. A maioria dos bugs de iniciante é "eu quis dizer X mas
  escrevi Y".
- Programar é decompor: quebrar um problema grande em passos pequenos e
  claros o suficiente para virar instrução.
- Entender > memorizar. Se a pessoa sabe o QUE cada construção faz, a
  sintaxe exata ela consulta.

## Os fundamentos que sustentam tudo
Confira se a pessoa domina, em ordem:
1. Variável: uma caixa com nome que guarda um valor que pode mudar.
2. Tipos: número, texto, verdadeiro/falso, lista — e por que somar
   texto com número dá erro ou coisa estranha.
3. Condição (if/else): o programa escolhe um caminho conforme algo for
   verdadeiro ou falso.
4. Repetição (loop): fazer algo várias vezes sem copiar e colar; onde
   começa, onde para, o que muda a cada volta.
5. Função: um bloco com nome que recebe entradas e devolve uma saída —
   a ferramenta contra repetição e a base de organizar código.
6. Coleções (lista/dicionário) e como percorrê-las.

## Método prático para ensinar lógica
- Faça a pessoa descrever o passo a passo em português ANTES de
  codar — a famosa "receita de bolo". Se ela não explica em palavras,
  não vai codar.
- Simulação na mão: percorra o loop volta a volta anotando o valor de
  cada variável. Ver o estado mudar destrava mais que qualquer
  explicação abstrata.
- Problemas minúsculos e reais: par ou ímpar, maior de uma lista,
  contar vogais. Pequeno o bastante para terminar, real o bastante para
  valer.
- Sempre peça para prever a saída antes de rodar; depois rode e compare
  com a previsão. A diferença é onde está o aprendizado.

## Erros comuns
- Copiar solução de loop/condição sem conseguir refazer do zero — sinal
  de que o fundamento não fixou. Volte um passo.
- Confundir atribuição (=) com comparação (==) na maioria das
  linguagens.
- Achar que decorar sintaxe é aprender a programar; é o contrário —
  sintaxe é a parte que a documentação resolve.
- Pular direto para frameworks sem saber função e loop; vira mágica que
  quebra e a pessoa não sabe onde.

## Limites e encaminhamento
- Se a pessoa domina esses fundamentos e ainda se sente parada, o
  gargalo é falta de projeto próprio, não de teoria ->
  references/projetos_e_pratica.md.
- Não empurre estruturas de dados/algoritmos avançados cedo demais:
  isso serve a entrevista técnica e otimização, não a quem ainda está
  fixando loop.
