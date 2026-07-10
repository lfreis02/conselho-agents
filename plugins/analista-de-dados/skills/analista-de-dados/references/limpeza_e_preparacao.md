# Referência: Limpeza e preparação

Objetivo: deixar o dado confiável antes de analisar. Análise sobre dado
sujo produz conclusão errada com cara de certeza — a limpeza é onde o
erro se esconde. Quase toda pergunta passa por aqui primeiro.

## Princípios
- Guarde o dado bruto intocado; limpe numa cópia. Toda transformação
  tem que ser reproduzível, não um conserto manual que ninguém lembra.
- Um dado limpo é "arrumado" (tidy): cada linha é uma observação, cada
  coluna é uma variável, cada célula um valor único. Datas em coluna,
  categorias em texto padronizado, números como número.
- Antes de confiar, conheça: quantas linhas, período coberto, de onde
  veio, quem gerou. Dado sem procedência é hipótese, não fato.

## Checklist prático
1. Duplicatas: identifique a chave que deveria ser única e conte
   repetições antes de remover; entenda por que duplicaram.
2. Faltantes: quanto falta e por quê. Vazio não é zero. Decida com
   critério — remover linha, deixar em branco ou preencher — e diga
   qual escolheu e o efeito no resultado.
3. Tipos e formatos: número guardado como texto não soma; datas em
   formatos misturados (dd/mm x mm/dd) corrompem ordenação; unidades
   diferentes na mesma coluna (kg e g) invalidam a conta.
4. Texto: espaços sobrando, maiúsculas inconsistentes, acentos e
   grafias diferentes ("SP", "S.P.", "São Paulo") viram categorias
   falsamente distintas — padronize.
5. Outliers: valor absurdo pode ser erro de digitação ou caso real.
   Investigue antes de apagar; nunca remova só porque atrapalha.

## Erros comuns
- Tratar célula vazia como zero e afundar a média.
- Remover duplicata sem entender a causa e perder linhas legítimas.
- Preencher faltante com a média sem avisar, fabricando dado.
- Consertar na mão sem registrar o passo — na próxima carga, o erro
  volta e ninguém sabe o que foi feito.

## Bandeiras vermelhas / limites
- Muitos faltantes ou dado de origem duvidosa: diga que a conclusão
  fica frágil e proponha confirmar a fonte antes de seguir.
- Se limpar "resolve" o resultado a favor do que a pessoa queria, pare
  e reveja — pode ser viés escondido, não limpeza.
- Dados pessoais (nome, CPF, e-mail, saúde): minimize, não exponha e
  veja references/limites.md antes de manipular.
