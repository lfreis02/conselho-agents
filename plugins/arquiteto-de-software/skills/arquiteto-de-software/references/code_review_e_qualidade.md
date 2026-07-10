# Referência: Code review e qualidade

Revisar código e defender qualidade sem virar polícia de estilo.

## Princípios
- Código é lido muitas vezes mais do que escrito: otimize para quem
  vai ler daqui a seis meses, não para quem digita agora.
- Clareza vence esperteza. Uma linha "inteligente" que exige três
  minutos para entender é dívida disfarçada.
- Revisão é sobre o código, nunca sobre a pessoa. O objetivo é o
  sistema ficar melhor e o autor aprender, não vencer o argumento.
- Nem todo comentário tem o mesmo peso: separe "isto está errado" de
  "eu faria diferente".

## Método prático
1. Entenda a intenção do PR antes de comentar: que problema ele
   resolve, qual o escopo. Revisar sem contexto gera ruído.
2. Vá do maior para o menor: primeiro corretude e design (a mudança
   faz o que promete? a fronteira está certa?), depois legibilidade,
   por último estilo — que idealmente é do linter, não seu.
3. Classifique cada comentário: bloqueador (corrige antes de mergear),
   sugestão (considere), nit (opcional, marque como tal). Isso evita
   travar PR por preferência pessoal.
4. Proponha, não só aponte: em vez de "isto está confuso", mostre a
   forma mais clara. Feedback acionável vale dez críticas vagas.
5. Elogie o que está bom. Revisão só com o negativo desgasta o time e
   esconde o que vale repetir.

## Sinais de qualidade a observar
- Nomes que dizem a intenção; funções que fazem uma coisa.
- Tratamento de erro explícito, não engolido em silêncio.
- Efeitos colaterais e estado compartilhado sob controle.
- Testes que cobrem o comportamento novo e os casos de borda.
- Ausência de duplicação que vá divergir — mas cuidado: nem toda
  repetição é duplicação (ver decisoes_e_tradeoffs.md sobre DRY).

## Erros comuns
- Reescrever o PR nos comentários em vez de deixar o autor conduzir.
- Travar merge por gosto pessoal disfarçado de "boa prática".
- Revisar só a sintaxe e deixar passar o erro de design embaixo.
- PRs gigantes: revisão profunda vira impossível; oriente fatiar.

## Bandeiras vermelhas / limites
- Métrica de qualidade virando meta (cobertura de 100%, zero warnings
  a qualquer custo): gera teste teatral e código torturado. Cobertura
  é sintoma, não objetivo.
- Código de segurança, cripto, autenticação ou pagamento: revisão de
  par não substitui revisão especializada; sinalize (ver limites.md).
- "Refatorar tudo" no meio de um PR de feature: separe em PRs; misturar
  torna a revisão impossível e esconde regressões.
