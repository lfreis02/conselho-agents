# Referência: Decisões e trade-offs

Escolher com critério, evitar over-engineering e gerir dívida técnica.

## Princípios
- YAGNI: não construa para o requisito que você imagina que virá.
  Construa para o que existe; o código simples de hoje é mais fácil
  de estender amanhã do que a abstração errada de ontem.
- Toda escolha é troca. A pergunta nunca é "qual é o melhor?", e sim
  "o que ganho, o que pago, e o custo cabe no contexto?".
- Custo total inclui operação e manutenção, não só escrever. A opção
  que economiza uma semana agora e cobra um mês por ano perde.
- Reversibilidade é um eixo de decisão. Decisão barata de desfazer se
  toma rápido e se corrige; decisão cara pede análise.

## Método prático
1. Escreva o problema em uma frase e os requisitos em bullets. Se não
   der, o problema ainda não está entendido — volte ao intake.
2. Liste 2-3 opções reais, incluindo "não fazer nada" e "a mais
   simples possível". A opção simples é a régua contra a qual as
   outras precisam se justificar.
3. Para cada opção: custo de construir, de operar, de reverter, e a
   curva para o time. Prefira o concreto ao "mais elegante".
4. Classifique: porta de mão dupla (reversível) decide-se logo; porta
   de mão única (cara) merece pausa, ADR e talvez um protótipo.
5. Registre a decisão e o gatilho de revisão: "escolhemos X; se
   acontecer Y, reavaliamos". Isso liberta o futuro sem prender.

## Dívida técnica
- Nem toda dívida é ruim: atalho consciente para validar algo rápido
  é estratégia legítima — desde que anotado e com juros à vista.
- Dívida vira problema quando é invisível e quando os juros (atrito
  em cada mudança) já pesam mais que o custo de pagar.
- Pague dívida no caminho do trabalho que já está acontecendo naquela
  área, não em mutirão desligado de entrega. Refatoração oportunista
  supera o "sprint de tech debt" que nunca vem.

## Erros comuns
- Abstrair na primeira ocorrência. Espere o padrão aparecer (a
  terceira vez costuma ser a hora); DRY aplicado cedo acopla o que
  era só parecido.
- Genericidade especulativa: parâmetros e ganchos "para o dia que
  precisar" que só adicionam superfície para bug.
- Framework/serviço a mais para um problema que uma função resolvia.
- Tratar toda decisão como irreversível e paralisar; a maioria é de
  mão dupla.

## Bandeiras vermelhas / limites
- "Já que estamos aqui, vamos deixar preparado para o futuro": sinal
  clássico de over-engineering; peça o requisito concreto que
  justifica.
- Decisão grande sem dono nem registro: vira lenda oral e ninguém
  lembra por que existe. Force um ADR curto.
- Reescrita total motivada por tédio com o código atual, não por
  incapacidade dele de evoluir: quase sempre má troca.
