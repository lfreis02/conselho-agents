# Referência: Planilhas e SQL

Objetivo: escolher a ferramenta certa e a fórmula/query mais simples
que responde à pergunta, sempre de forma que a pessoa consiga refazer.

## Princípios
- Planilha para dados até dezenas de milhares de linhas, exploração
  rápida e visual. SQL quando o dado mora num banco, é grande, ou a
  mesma pergunta se repete e precisa ser confiável.
- A fórmula/query mais legível vence a mais esperta: quem mantém o
  arquivo é uma pessoa, não a máquina.
- Separe dado bruto de cálculo: uma aba/tabela crua intocada, outra
  para as contas. Nunca calcule por cima do original.

## Planilhas — o que resolve a maioria
- Busca entre tabelas: PROCV/VLOOKUP resolve o caso simples;
  ÍNDICE+CORRESP (INDEX+MATCH) ou PROCX/XLOOKUP são mais robustos e não
  quebram ao inserir coluna.
- Somar/contar com condição: SOMASE(S)/SUMIF(S), CONT.SE(S)/COUNTIF(S).
- Resumir e cruzar: tabela dinâmica (pivot) — a ferramenta mais
  subutilizada; troca dezenas de fórmulas por um resumo arrastável.
- Limpeza: ARRUMAR/TRIM, MAIÚSCULA/MINÚSCULA, SEERRO/IFERROR para não
  poluir a planilha com #N/D.

## SQL — do básico ao intermediário
1. SELECT colunas FROM tabela WHERE condição — sempre comece filtrando.
2. GROUP BY + agregação (COUNT, SUM, AVG) responde "quanto por
   categoria"; combine com HAVING para filtrar o resultado agregado.
3. ORDER BY ... LIMIT para ver topo/fundo sem trazer tudo.
4. JOIN para cruzar tabelas: entenda a chave que liga as duas antes de
   escrever; INNER perde linhas sem par, LEFT preserva a tabela da
   esquerda.
Escreva a query em passos e teste com LIMIT antes de rodar no todo.

## Erros comuns
- PROCV com o valor à direita da chave (não funciona) — use XLOOKUP ou
  ÍNDICE+CORRESP.
- Intervalo sem travar ($) ao arrastar a fórmula.
- COUNT/AVG ignorando NULL sem a pessoa perceber e mudando o resultado.
- JOIN que duplica linhas porque a chave não é única — confira a
  contagem antes e depois.
- Rodar UPDATE/DELETE sem WHERE ou sem backup.

## Limites
- Não escreva query destrutiva (UPDATE/DELETE/DROP) em base real sem a
  pessoa ter backup e entender o efeito; prefira SELECT para validar.
- Dialetos variam (Excel x Sheets; MySQL x PostgreSQL x BigQuery):
  funções e sintaxe mudam. Na dúvida de sintaxe específica, diga para
  conferir na documentação da ferramenta dela.
