---
title: "Fluxograma — IS fim VDF no SMI (DGPM-406, item 11.3)"
tipo: "Fluxograma BPMN"
documento: "DGPM-406"
revisao: "9ª Revisão (2023)"
capitulo_relacionado: 11
item_relacionado: "11.3"
tags:
  - dgpm-406
  - fluxograma
  - bpmn
  - vdf
  - smi
  - medicina-pericial-mb
competencia_mpi_jrs:
  - MPI
  - JRS
competencia_nota: "O fluxo é desencadeado pela OM de vinculação e conduzido pela JRS; o MPI atua no início (perícia menor) e na finalização de casos de 'Deixar o SMI'."
fonte: "FLUXOGRAMA_VDF_SMI.bpmn"
---

# Fluxograma — IS fim VDF no Serviço Militar Inicial (SMI)

Fluxograma BPMN representando o processo de Verificação de Deficiência Funcional (VDF) durante a prestação do SMI, conforme o item **11.3** do [[ch11-servico-temporario|Capítulo 11]] da DGPM-406.

![[FLUXOGRAMA_VDF_SMI.bpmn]]

## Raias (participantes)

- **OM de Vinculação — Encarregado de Pessoal**: identifica a restrição de saúde, apresenta o militar à JRS (APS) e recebe os laudos para as providências administrativas cabíveis.
- **Junta Regular de Saúde (Hospital Naval / RECIGFE)**: realiza a IS fim VDF, decide entre manter LTS, reapresentar para nova VDF, ou exarar o laudo de incapacidade definitiva.
- **Serviço de Recrutamento Distrital do SDP (Com/3ºDN)**: interrompe o Serviço Militar quando não há nexo causal e o laudo é de Incapaz C, ou nos casos de Incapaz C vindos do gateway inicial.

## Lógica de decisão (síntese)

1. **Afastamento excede a perícia menor?** Não → mantido em dispensa por perícia menor (fim). Sim → apresentação para IS fim VDF.
2. **Laudo da JRS**: Apto A (retorno ao serviço) | Incapaz B-1 (< 1 ano) | Incapaz B-2 (> 1 ano) | Incapaz C (definitiva).
3. **Incapaz B-1** → verifica tempo de afastamento (< 90 dias: reapresentação à JRS; ≥ 90 dias: segue para verificação de nexo causal).
4. **Nexo causal (AO/ISO)?** Sim → mantém VDF/LTS até termo do tratamento ou prazo da Administração Naval, podendo evoluir para laudo de incapacidade definitiva para o SAM "nos moldes do Capítulo 6 da DGPM-406" — aplicação **excepcional** do Capítulo 6 a militar temporário, cabível apenas quando há nexo causal comprovado (AO/ISO) da incapacidade definitiva com o serviço. Não (ou Incapaz C) → interrupção do Serviço Militar pelo SDP, sem esse enquadramento.
5. Recuperado após LTS → apresentação para IS fim **Deixar o SMI** (MPI) → fim do Serviço Militar.

## Ver também

- [[ch11-servico-temporario#11.3. VERIFICAÇÃO DE DEFICIÊNCIAS FUNCIONAIS (VDF) DURANTE A PRESTAÇÃO DE SMI|Capítulo 11 — item 11.3 (VDF durante a prestação de SMI)]]
- [[ch06-vdf-termino|Capítulo 6 — VDF, Término de Incapacidade e Restrições]] — capítulo destinado, em regra, a militares de carreira; aplica-se ao militar do SMI apenas **excepcionalmente**, quando a incapacidade definitiva tiver nexo causal comprovado com o serviço, hipótese em que o laudo de incapacidade para o SAM segue os critérios deste capítulo.
- [[FLUXOGRAMA_VDF_SMV|Fluxograma — IS fim VDF/Término de Incapacidade no SMV (item 11.8)]] — fluxo equivalente para militares do Serviço Militar Voluntário.
