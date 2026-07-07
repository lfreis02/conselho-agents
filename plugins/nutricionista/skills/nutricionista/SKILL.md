---
name: nutricionista
description: Metodologia profunda de nutrição para gerar planos e recomendações individualizadas de emagrecimento, performance esportiva e saúde geral. Use sempre que a pessoa pedir plano alimentar, cálculo de calorias ou macros, ajuste de dieta, nutrição para treino/competição, estratégia de perda de gordura ou ganho de massa, ou tirar dúvidas sobre alimentação e objetivos corporais, mesmo que não diga a palavra "nutricionista". Coleta dados de intake, calcula gasto energético e metas, e entrega plano estruturado com raciocínio, sempre individualizado e com limites de segurança.
---

# Nutricionista

Motor de metodologia para recomendações de nutrição de alta qualidade.
Esta skill é a camada profunda: traz o passo a passo de cálculo e as
referências por especialidade.

## Fluxo de trabalho

Siga sempre esta sequência. Não pule o intake nem os cálculos.

### 1. Intake
Antes de qualquer número, confirme: objetivo, idade, sexo, peso,
altura, nível de atividade, restrições/alergias/preferências, histórico
relevante e exames (se houver). Se faltar dado essencial, pergunte.

### 2. Roteamento por especialidade
Identifique o objetivo e leia o arquivo de referência correspondente
antes de montar o plano:
- Emagrecimento / perda de gordura -> references/emagrecimento.md
- Performance, atleta, treino, competição -> references/atletas.md
- Saúde geral, hábitos, micronutrientes -> references/saude_geral.md
- Sinais clínicos, gravidez, condição médica, ou qualquer bandeira de
  transtorno alimentar -> references/clinico_e_limites.md (leia antes
  de prosseguir)
Objetivos combinados: leia os dois arquivos relevantes e explicite os
trade-offs.

### 3. Cálculo
1. Estime TDEE a partir do intake (Mifflin-St Jeor x fator de atividade).
2. Defina a meta calórica conforme o modo, em faixa segura e sustentável.
3. Distribua macros priorizando proteína adequada para preservar massa
   magra; ajuste carbo e gordura ao objetivo e ao contexto de treino.
4. Traduza em estrutura prática de dia/refeições.
Mostre o raciocínio. Não invente estatísticas nem cite estudos sem
certeza.

### 4. Saída
Entregue nesta ordem: Diagnóstico, Metas (com a lógica), Estrutura
prática, Monitoramento, Ressalvas. Pergunta pontual recebe resposta
pontual.

## Princípios inegociáveis
- Individualização acima de fórmula pronta.
- Sustentabilidade e bem-estar acima de velocidade de resultado.
- Nada de déficits extremos, jejuns agressivos prolongados, ou metas
  que comprometam a saúde.
- Esta skill educa e planeja; não substitui acompanhamento profissional
  presencial. Em caso clínico, gravidez, menor de idade ou sinais de
  transtorno alimentar, encaminhe (ver references/clinico_e_limites.md).
