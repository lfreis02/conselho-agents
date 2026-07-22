# Referência: Escopo e MVP

MVP não é "produto pela metade". É o menor recorte que responde a uma
pergunta específica com usuário real. A pergunta vem primeiro; o
recorte é consequência dela. Escopo que cresce sem critério é a forma
mais comum de nunca lançar.

## Princípios
- Um MVP tem uma dúvida. Se a pessoa não consegue dizer qual, o que
  ela quer é lançar o produto inteiro com nome de MVP.
- O produto precisa fazer bem uma coisa que resolva o problema de
  ponta a ponta para uma pessoa, não dez coisas pela metade para
  todas.
- Software é o teste mais caro. Antes dele existem conversa,
  protótipo clicável, página explicando a oferta, atendimento feito
  na mão nos bastidores.
- Cortar escopo é decisão de produto, não fracasso; o que fica de
  fora precisa ser dito em voz alta, com motivo. Mas qualidade do
  que entra não se corta — fluxo confuso ou que perde dado do
  usuário não ensina nada, só afasta.

## Método prático
1. Escreva a frase do experimento — "se [usuário] conseguir [tarefa]
   com o produto, aprendemos que [suposição] se sustenta".
2. Mapeie o caminho mínimo do usuário até o valor: os passos entre
   chegar e resolver o problema uma vez. Tudo que não está nesse
   caminho é candidato natural ao corte.
3. Liste o escopo em três colunas — entra agora, fica para depois,
   não faremos. A terceira coluna é a mais importante e a mais
   evitada.
4. Aceite substituto manual onde couber. Cadastro por formulário
   simples, envio feito por uma pessoa, relatório montado à mão. Se o
   valor só existe com automação, aí a automação entra no recorte.
5. Escreva o que precisa ser construído em linguagem de resultado
   para o usuário, não de tela: quem faz, o que precisa conseguir
   fazer, o que caracteriza pronto, o que acontece quando dá errado
   (campo vazio, sem conexão, dado inválido).
6. Combine com quem constrói, antes de começar, o prazo e o que fazer
   quando o trabalho estourar — cortar escopo, adiar data ou reduzir
   o recorte. Decidir isso na véspera é decidir com pressa.
7. Defina a data de olhar o resultado no mesmo dia em que define o
   escopo.

## Erros comuns
- Adicionar "só mais uma coisinha" até descobrir, meses depois, que
  ninguém quis a primeira.
- Confundir MVP com protótipo bonito, sem usuário na frente.
- Copiar funcionalidade de concorrente sem saber o que ela resolve lá.
- Lançar para todo mundo de uma vez e não observar ninguém de perto.
- Esquecer o caso de erro e o estado vazio — é neles que se desiste.

## Bandeiras vermelhas / limites
- Recorte que só cabe no prazo se todo mundo trabalhar de madrugada
  não é recorte — é dívida com pessoa. Corte de novo.
- Como construir, que tecnologia usar, banco de dados e arquitetura
  são do Arquiteto de Software.
- Produto que trata dado sensível, dinheiro ou saúde tem exigência
  legal que não se corta em nome do MVP; encaminhar para Guia LGPD,
  contador ou advogado conforme o caso.
