# Referência: System design em entrevista

Objetivo: conduzir uma sessão de projeto aberto sem se perder. O
formato costuma ficar em torno de 45 min, mas confirme a duração com o
recrutador. Não existe resposta certa, existe caminho defensável: o
entrevistador quer ver se você levanta requisitos, escolhe com critério
e admite o custo. Isto é exercício de entrevista — arquitetura de
sistema real em produção é do Arquiteto de Software.

## Roteiro de 5 blocos (proporções do tempo disponível)
1. Requisitos (~15%). Quem usa e para quê, o que entra no escopo e o
   que fica de fora, ordem de grandeza de usuários e de leitura x
   escrita, latência, consistência forte ou eventual. Escreva na tela o
   combinado e pergunte números em vez de inventar — se o entrevistador
   não der, proponha uma estimativa e diga que é premissa sua.
2. Interface e modelo (~10%). As poucas operações do sistema e as
   entidades principais com seus campos. É aqui que se percebe se
   você entendeu o problema.
3. Desenho de alto nível (~25%). Cliente, entrada da requisição,
   serviço, armazenamento. Caixas e setas simples primeiro; detalhe
   depois. Fale o caminho de uma requisição de ponta a ponta.
4. Aprofundar um ponto (~35%). O entrevistador vai escolher, ou você
   escolhe o mais interessante — o que acontece quando dobra o
   tráfego, como evitar trabalho repetido, o que quebra se um nó cai.
5. Trade-offs e limites (~15%). O que sua escolha custa, o que
   monitorar, o que faria diferente com mais tempo ou mais dados.

## O vocabulário que precisa estar afiado
Banco relacional x não relacional e por que naquele caso; índice; cache
e a hora de invalidar; fila para desacoplar trabalho lento; réplica de
leitura; particionamento por chave; balanceador; idempotência; limite
de requisições; o que acontece com dado duplicado. Saber explicar cada
um em duas frases vale mais que citar dez tecnologias pelo nome.

## Erros comuns
- Começar pelo banco ou pela tecnologia favorita antes de saber o
  que o sistema faz.
- Encher o desenho de componentes que ninguém pediu — cada caixa a
  mais é uma pergunta que você vai ter que responder.
- Citar nome de produto sem dizer o problema que ele resolve ali.
- Afirmar número de escala com falsa precisão. Diga a ordem de
  grandeza e chame de premissa.
- Ficar mudo desenhando. Narre a decisão enquanto desenha.

## Bandeiras vermelhas
- Sair projetando sem perguntar nada. É o erro que cobra mais caro
  nessa etapa: levantar requisito é parte do que está sendo avaliado.
- Defender a própria escolha quando o entrevistador aponta um furo.
  Reconhecer e ajustar é exatamente o que se está avaliando.
- Prometer que o desenho "aguenta qualquer escala".

## Como treinar
Pegue um sistema que você usa, dê 40 minutos no timer e faça o roteiro
inteiro em voz alta, desenhando. Depois releia procurando o que assumiu
sem perguntar. Repetir com 5 sistemas ensina mais que ler 20 artigos.
