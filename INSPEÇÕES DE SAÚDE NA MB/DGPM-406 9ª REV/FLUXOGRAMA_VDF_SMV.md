---
title: "Fluxograma — IS fim VDF/Término de Incapacidade no SMV (DGPM-406, item 11.8)"
tipo: "Fluxograma BPMN"
documento: "DGPM-406"
revisao: "9ª Revisão (2023)"
capitulo_relacionado: 11
item_relacionado: "11.8"
tags:
  - dgpm-406
  - fluxograma
  - bpmn
  - vdf
  - smv
  - medicina-pericial-mb
competencia_mpi_jrs:
  - MPI
  - JRS
competencia_nota: "O fluxo é conduzido pela JRS; o MPI atua na IS fim Deixar o SMV quando o militar é revertido ao serviço ativo após período de agregação."
fonte: "FLUXOGRAMA_VDF_SMV.bpmn"
---

# Fluxograma — IS fim VDF/Término de Incapacidade no Serviço Militar Voluntário (SMV)

Fluxograma BPMN representando o processo de Verificação de Deficiência Funcional (VDF) e Término de Incapacidade/Restrições durante a prestação do SMV, conforme o item **11.8** do [[ch11-servico-temporario|Capítulo 11]] da DGPM-406.

![[FLUXOGRAMA_VDF_SMV.bpmn]]

## Raias (participantes)

- **OM de Vinculação — Encarregado de Pessoal**: identifica a condição de saúde, apresenta o militar (APS) à JRS para VDF, Término de Restrições/Incapacidade ou Deixar o SMV, e determina o encostamento quando cabível.
- **Junta Regular de Saúde (Hospital Naval de Recife)**: realiza as IS fim VDF, Término de Restrições e Término de Incapacidade, decide sobre prorrogações e exara o laudo de incapacidade definitiva para o SAM, quando aplicável.
- **Serviço de Recrutamento Distrital — Com/3ºDN**: providencia o licenciamento por conveniência do serviço e conduz o fluxo de militares encostados.

## Lógica de decisão (síntese)

1. **Laudo da JRS**: Apto (com ou sem restrições) ou LTS.
2. **Apto com restrições** → verifica se atingiu 36 meses de restrições. Se sim, apresentação para IS fim Deixar o SMV; se não, IS fim Término de Restrições, com possibilidade de prorrogação (retorna à verificação dos 36 meses) ou alta ("Fim - Curado").
3. **LTS** → verifica se atingiu 90 dias. Se não, reapresentação para Término de Incapacidade, com possível prorrogação da LTS (retorna à mesma verificação). Se sim, segue para verificação de **nexo causal (AO/ISO)**.
4. **Sem nexo causal** → licenciamento por conveniência do serviço pelo Com/3ºDN, **sem necessidade de IS fim Deixar o SMV**; nesses casos o militar pode ainda ser encostado para tratamento de saúde (fluxo de encostados, conforme NORDINAV Natal nº 90-03/2026), até esgotamento dos recursos de tratamento ou estabilização.
5. **Com nexo causal** → o militar entra em fase de **agregação** (mantém o vínculo militar, com remuneração, mas sem serviço) para IS fim Término de Incapacidade, reapresentada quantas vezes necessário enquanto houver expectativa de recuperação.
   - **Recuperado** → IS fim Deixar o SMV (realizada por MPI) → reversão ao serviço ativo e licenciamento do SMV pelo SDP.
   - **Não recuperado, mas prazo máximo de agregação ainda não esgotado** → nova IS Término de Incapacidade (reavaliação).
   - **Esgotado o prazo máximo de agregação com incapacidade persistente, ou identificada invalidez** → laudo de **incapacidade definitiva para o SAM, no padrão do Capítulo 6 da DGPM-406**. Se houver invalidez, o militar é reformado; caso contrário, segue para IS fim Deixar o SMV.

> [!important] Aplicação excepcional do Capítulo 6
> O laudo "nos moldes do Capítulo 6" só é exarado nesta hipótese **excepcional**: incapacidade definitiva (ou invalidez) de militar temporário do SMV, com nexo causal comprovado (AO/ISO) com o serviço, após esgotado o prazo máximo de agregação. Fora dessa hipótese, o Capítulo 6 é dirigido, em regra, a militares de carreira — conforme já esclarecido para o fluxo equivalente do SMI.

## Ver também

- [[ch11-servico-temporario#11.8. VERIFICAÇÃO DE DEFICIÊNCIA FUNCIONAL (VDF), TÉRMINO DE INCAPACIDADE/RESTRIÇÕES PARA MILITARES PRESTANDO SMV|Capítulo 11 — item 11.8 (VDF/Término de Incapacidade no SMV)]]
- [[ch06-vdf-termino|Capítulo 6 — VDF, Término de Incapacidade e Restrições]] — capítulo destinado, em regra, a militares de carreira; aplica-se ao militar do SMV apenas **excepcionalmente**, quando a incapacidade definitiva (ou invalidez) tiver nexo causal comprovado com o serviço, após esgotado o prazo máximo de agregação.
- [[FLUXOGRAMA_VDF_SMI|Fluxograma — IS fim VDF no SMI (item 11.3)]] — fluxo equivalente para militares do Serviço Militar Inicial.
