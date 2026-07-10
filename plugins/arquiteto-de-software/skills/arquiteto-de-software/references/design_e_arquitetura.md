# Referência: Design e arquitetura

Como estruturar o sistema: camadas, fronteiras, serviços e padrões.

## Princípios
- Arquitetura é sobre fronteiras e dependências, não sobre pastas. A
  pergunta central é: o que pode mudar sem quebrar o resto?
- Acoplamento e coesão mandam: coisas que mudam juntas ficam juntas;
  coisas independentes se isolam por uma interface estável.
- Dependências apontam para dentro, do detalhe (framework, banco, UI)
  para a regra de negócio, que não deve conhecer o detalhe.
- Padrão é ferramenta, não meta. Aplique quando o problema que ele
  resolve existe de fato; padrão sem problema é peso morto.

## Método prático
1. Comece pela regra de negócio e pelos casos de uso. A tecnologia é
   consequência, não ponto de partida.
2. Desenhe as fronteiras onde a mudança dói: o que muda por motivo
   diferente vira módulo separado (ex.: pagamento e catálogo).
3. Defina o que atravessa cada fronteira (contrato/interface) e
   mantenha esse contrato estável e explícito.
4. Só extraia um serviço/módulo quando houver razão concreta (equipes
   separadas, escala independente, ciclo de deploy próprio). Antes
   disso, módulo bem separado dentro do monolito basta.
5. Documente a decisão em um ADR curto: contexto, opções, escolha,
   consequências. O futuro do time agradece.

## Monolito vs. serviços
- Comece com monolito modular quase sempre. Ele é mais fácil de
  refatorar, depurar e mover fronteiras enquanto o domínio ainda é
  incerto.
- Microserviços resolvem problema de organização e escala
  independente, e cobram em rede, observabilidade, consistência
  distribuída e operação. Só valem quando esses custos são menores
  que a dor que aliviam.
- Fronteira mal colocada dentro do monolito vira microserviço
  distribuído mal colocado — pior, agora com latência de rede.

## Erros comuns
- Arquitetura orientada a currículo: adotar o padrão da moda sem o
  problema que ele resolve.
- Abstração prematura: criar interface genérica para uma única
  implementação, "por precaução".
- Camadas por camadas: repassar dados por três classes que só
  encaminham, sem regra própria.
- Distribuir cedo demais e herdar todos os problemas de sistema
  distribuído antes de precisar de qualquer benefício.

## Bandeiras vermelhas / limites
- "Vamos de microserviços desde o dia um" em time pequeno e domínio
  ainda instável: quase sempre erro; questione.
- Reescrita total ("big bang rewrite") como resposta a código ruim:
  altíssimo risco; prefira estrangulamento incremental do legado.
- Decisão irreversível (formato de dados público, contrato de API
  externo) sendo tomada às pressas: force uma pausa e um ADR.
