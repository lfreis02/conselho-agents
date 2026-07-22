# Referência: Métricas e iteração

Métrica existe para responder pergunta, não para decorar apresentação.
Produto melhora por ciclo — decidir o que testar, construir pequeno,
observar, concluir e repetir. Número sem pergunta antes vira desculpa
para acreditar no que já se queria acreditar.

## Princípios
- Pergunta primeiro, métrica depois. "O que eu preciso saber para
  decidir?" define o que medir.
- Poucas métricas, bem entendidas. Uma que representa valor entregue
  ao usuário, mais duas ou três de apoio.
- Contagem que só cresce (cadastros acumulados, total de downloads)
  faz sentir bem e não informa nada. Prefira comportamento por
  período e por grupo de entrada.
- Número mostra o quê; conversa mostra o porquê. Andar só com um dos
  dois é andar de olho fechado.
- Meta é referência de aprendizado, não promessa. Se não sabe o
  patamar, o primeiro ciclo serve para medir a linha de base.

## Método prático
1. Escreva a métrica de valor do seu produto — a ação que significa
   que o usuário resolveu o problema (não abriu o app, resolveu).
2. Monte o caminho até essa ação em etapas e conte quantas pessoas
   passam de uma para a outra. A maior queda entre etapas é o alvo
   do próximo ciclo.
3. Estabeleça a linha de base com o seu próprio dado, antes de mudar
   qualquer coisa. Sem antes, não existe depois.
4. Acompanhe por grupo de entrada — quem chegou nesta semana, na
   seguinte — em vez de média geral, que esconde melhora e piora.
5. Antes de construir, escreva a previsão: o que espera ver, em quanto
   tempo, e o que faria você abandonar a ideia. Guarde a frase.
6. Depois do ciclo, compare com a previsão e escreva a conclusão em
   uma linha: confirmou, não confirmou, ou não deu para saber. "Não
   deu para saber" é honesto e comum — geralmente falta volume ou o
   recorte misturou duas mudanças.
7. Decida entre insistir, ajustar ou mudar de rumo com base no
   acumulado de ciclos, não num resultado isolado. Defina desde o
   começo quanto tempo e dinheiro você topa gastar nessa aposta.

## Erros comuns
- Mudar três coisas de uma vez e não saber qual funcionou.
- Comemorar pico de acesso vindo de divulgação pontual como se fosse
  produto melhor.
- Olhar média geral e não ver que os antigos usam e os novos somem.
- Comparar seu número com "benchmark do setor" achado na internet
  sem saber como foi calculado nem sobre qual produto.
- Perseguir métrica que sobe sem que ninguém resolva mais problema —
  tempo de tela, notificação, clique induzido.
- Construir sem definir o que seria evidência de fracasso.

## Bandeiras vermelhas / limites
- Nunca cravar taxa de conversão, retenção ou engajamento "normal".
  Não existe número universal; existe o seu, medido.
- Métrica que melhora à custa do usuário (engano, fricção para
  cancelar, notificação abusiva) é problema ético, não vitória.
- Consulta em banco, SQL, modelagem e análise estatística são do
  Analista de Dados. Instrumentação e infraestrutura de coleta, do
  Arquiteto de Software.
- Coleta de comportamento envolve dado pessoal — consentimento e
  finalidade vão para o Guia LGPD.
