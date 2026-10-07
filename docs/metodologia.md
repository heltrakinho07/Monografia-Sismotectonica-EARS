# Metodologia

Este documento descreve a sequência operacional do workflow da monografia.

## 1. Aquisição de dados
Download de formas de onda e metadados de estações para a área e período de estudo.

## 2. Pré-processamento
Verificação de integridade, organização temporal, harmonização de metadados e preparação dos dados para detecção automática.

## 3. EQTransformer
Detecção automática de sinais sísmicos e identificação das chegadas das fases P e S. Os parâmetros exactos utilizados em cada execução devem ser registados em `03_EQTransformer/configs/`.

## 4. PyOcto
Associação espaço-temporal dos picks em hipóteses de eventos sísmicos. O output principal é constituído pelo catálogo preliminar de eventos e pela relação evento–pick.

## 5. NLL-SSST-Coherence
Refinamento da localização hipocentral utilizando NonLinLoc e correcções SSST. Quando aplicável, a etapa de coherence deve ser documentada separadamente para distinguir claramente a componente NLL-SSST da análise por coerência de formas de onda.

Fluxo recomendado:
```text
NLLoc Iter0
→ LocSum Iter0
→ Loc2ssst Iter1
→ NLLoc Iter1
→ LocSum Iter1
→ Loc2ssst Iter2
→ NLLoc Iter2
→ avaliação final
```

## 6. Inversão com Grond
Inversão de formas de onda para eventos seleccionados, com registo explícito das configurações, modelos de Terra, janelas, filtros e funções objectivo.

## 7. DBSCAN
Agrupamento não supervisionado dos hipocentros relocalizados, com documentação de `eps`, `min_samples`, sistema de coordenadas e variáveis usadas.

## 8. Análise final
Integração de estatísticas, mapas, padrões espaciais, profundidades, clusters, mecanismos/fontes e enquadramento tectónico.
