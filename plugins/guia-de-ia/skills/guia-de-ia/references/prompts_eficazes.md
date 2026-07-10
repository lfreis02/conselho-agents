# Referência: Prompts eficazes

Objetivo: transformar um pedido vago num prompt que produz a resposta
certa de primeira. Resposta genérica quase sempre vem de prompt
genérico — o modelo é bom, faltou direção.

## Princípios
- A IA não adivinha contexto. Ela responde ao que você deu, não ao
  que você tinha na cabeça. Contexto explícito é o maior ganho.
- Especificidade vence tamanho. "E-mail curto e formal recusando o
  convite, agradecendo, tom cordial" bate "escreva um e-mail".
- Formato de saída pedido é formato de saída entregue: tabela, lista,
  número de opções, tom, tamanho. Peça.
- Exemplo do que você quer (ou do que não quer) alinha melhor que
  qualquer adjetivo.
- Iteração é o método normal. O primeiro resultado é rascunho;
  refinar em cima dele é mais rápido que reescrever o prompt do zero.

## Método prático (estrutura CPTFE)
1. Contexto: quem você é, para quem é, qual a situação.
2. Papel: "aja como revisor de currículos", quando ajuda a calibrar.
3. Tarefa: o verbo claro — resuma, reescreva, compare, gere, corrija.
4. Formato: tamanho, estrutura, tom, idioma, quantas opções.
5. Exemplo: cole um modelo do resultado desejado, se tiver.
Depois: peça revisões pontuais ("mais curto", "menos formal",
"troque o segundo parágrafo"), não recomece.

## Truques que rendem
- Peça o raciocínio quando o resultado importa ("explique passo a
  passo antes de responder").
- Peça alternativas ("me dê 3 versões com tons diferentes").
- Dê os dados brutos e deixe a IA formatar, em vez de descrevê-los.
- Peça que a IA faça perguntas se faltar informação, antes de
  responder.

## Erros comuns
- Pedido de uma linha esperando resposta sob medida.
- Empilhar cinco tarefas num prompt só; quebre em passos.
- Não dizer o público nem o tom e reclamar que ficou "sem cara".
- Aceitar o primeiro resultado sem pedir ajuste.
- Assumir que a IA lembra de conversas antigas ou de arquivos que
  você não colou nesta conversa.

## Bandeiras vermelhas
- Prompt pedindo para a IA "garantir que está 100% correto" sobre
  fatos: ela não garante. O prompt não substitui a verificação
  humana (ver verificar_e_confiar.md).
