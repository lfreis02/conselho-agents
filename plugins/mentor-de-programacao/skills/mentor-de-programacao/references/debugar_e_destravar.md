# Referência: Debugar e destravar (ler erros, achar bugs)

Saber debugar é a habilidade que separa quem depende de tutorial de
quem constrói sozinho. Mensagem de erro não é castigo: é o computador
dizendo, de graça, o que está errado e onde. Ensine a LER, não só a
consertar.

## Princípios
- O erro é seu amigo mais honesto. Iniciante entra em pânico e fecha a
  tela do erro; a informação que resolve está justamente ali.
- Bug quase nunca é mistério: é uma suposição sua que não bate com a
  realidade do código. Debugar é caçar essa suposição.
- Um palpite por vez. Mudar cinco coisas de uma vez e rodar não é
  debugar, é loteria.

## Como ler uma mensagem de erro
1. Ler de baixo para cima: a última linha costuma dizer o TIPO do erro
   e a mensagem; o resto é o caminho até ali.
2. Achar o arquivo e a LINHA que o erro aponta — e olhar essa linha e a
   de cima. O erro real muitas vezes é uma linha antes do que ele
   acusa.
3. Traduzir o tipo do erro em português: "não definido" (usou nome que
   não existe/erro de digitação), "de tipo" (misturou texto com
   número), "de sintaxe" (faltou fechar parêntese/aspas/dois-pontos),
   "índice fora do intervalo" (pediu item que não existe na lista).
4. Colar a mensagem do erro numa busca é técnica legítima e
   profissional — não é trapaça. Ensine a buscar a parte genérica do
   erro, sem os dados pessoais do código.

## Método prático quando o código não faz o esperado (sem erro)
- Reproduzir de forma mínima: qual a menor entrada que mostra o
  problema.
- Imprimir o estado: colocar prints mostrando o valor das variáveis nos
  pontos-chave e comparar com o que você ESPERAVA ali. A diferença
  aponta o bug.
- Ler o código como o computador: linha a linha, na ordem, sem
  "arredondar" para o que você quis dizer.
- Método do patinho de borracha: explicar o código em voz alta, linha
  a linha, para um objeto. Metade dos bugs aparece na própria
  explicação.

## Erros comuns de iniciante
- Fechar o erro sem ler e sair mudando código no chute.
- Editar sem salvar, ou rodar o arquivo errado, e achar que "não
  mudou nada".
- Assumir que o problema está numa parte complexa quando é um erro de
  digitação bobo perto do erro apontado.
- Pedir a resposta antes de ter lido a própria mensagem de erro.

## Limites e como o mentor age
- Quando a pessoa traz um erro: NÃO entregue só o código corrigido.
  Aponte a linha, explique o que o erro diz, sugira a correção e peça
  que ela aplique e rode. O objetivo é que da próxima vez ela leia
  sozinha.
- Se o erro depende de versão de ferramenta ou sistema operacional,
  mande conferir a documentação oficial em vez de chutar de memória.
