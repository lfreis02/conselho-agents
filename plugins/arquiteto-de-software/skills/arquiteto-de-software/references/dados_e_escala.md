# Referência: Dados e escala

Modelagem de dados, performance e escalabilidade sem chute nem susto.

## Princípios
- O modelo de dados sobrevive ao código. Trocar de framework é uma
  tarde; migrar um esquema mal desenhado com dados em produção é um
  projeto. Invista onde é caro reverter.
- Escale o gargalo real, não o imaginado. Otimização sem medição é
  superstição. Meça, encontre o ponto quente, então atue.
- Consistência, disponibilidade e latência se compram uma à custa da
  outra em sistema distribuído. Escolha conscientemente o que o
  produto precisa, não o que soa robusto.
- A maioria dos sistemas não é grande. Resolver problema de escala do
  Google num produto com mil usuários é custo puro.

## Método prático
1. Modele o domínio primeiro: entidades, relações, invariantes (o que
   nunca pode ficar inconsistente). O tipo de banco vem depois.
2. Relacional é o padrão sensato: transações, integridade e consultas
   flexíveis cobrem a maioria dos casos. Só saia dele com motivo
   nomeado (padrão de acesso específico, escala comprovada).
3. Antes de otimizar, meça: identifique a consulta/rota lenta com
   dados reais, olhe o plano de execução, cheque índices. O gargalo
   costuma ser um N+1 ou um índice faltando, não a linguagem.
4. Suba a escala na ordem barata: índice e consulta melhor -> cache
   no ponto certo -> réplica de leitura -> só então particionar. Cada
   degrau adiciona complexidade; não pule para o topo.
5. Toda mudança de esquema em produção é migração versionada,
   reversível e aplicada em passos (expandir, migrar, contrair).

## Cache, com cuidado
- Cache resolve leitura repetida e cara; introduz o problema de
  invalidação, que é dos mais difíceis. Defina a política de
  expiração antes de adicionar.
- Cache para esconder consulta mal feita é curativo: conserte a
  consulta primeiro.

## Erros comuns
- Escolher NoSQL "porque escala" sem conhecer o padrão de acesso, e
  descobrir tarde que precisava de junções e transações.
- Índice demais (escrita lenta) ou de menos (leitura lenta); ambos se
  resolvem medindo.
- Otimizar micro (trocar laço) enquanto o N+1 no banco domina o tempo.
- Guardar dado desnormalizado sem plano de como mantê-lo coerente.

## Bandeiras vermelhas / limites
- "Precisamos aguentar milhões" sem número de tráfego atual nem
  projeção fundamentada: questione a premissa antes de arquitetar.
- Decisão de particionar (sharding) tomada cedo: é das mais caras de
  reverter; exija dados de carga que a justifiquem.
- Sistema com requisito forte de consistência (financeiro, estoque)
  indo para arquitetura eventualmente consistente sem que o time
  entenda as implicações: pare e explicite o trade-off.
- Não afirmo que "tecnologia X aguenta Y requisições" — isso depende
  de esquema, hardware e carga; mede-se no seu ambiente.
