# Dados

## Princípio geral

Os dados sísmicos brutos não são alojados neste repositório público devido ao volume, proveniência e requisitos de distribuição.

## Devem ser versionados

- inventários de estações de pequena dimensão;
- listas de redes/estações/canais;
- parâmetros de download;
- janelas temporais;
- catálogos derivados;
- tabelas CSV pequenas;
- exemplos mínimos necessários para testar scripts.

## Não devem ser versionados

- grandes volumes MiniSEED/SAC;
- caches de waveforms;
- modelos ou checkpoints de grande dimensão;
- outputs temporários de processamento;
- ficheiros binários reproduzíveis a partir dos dados originais.

Cada pasta de etapa deve explicar claramente os inputs esperados e a forma de os obter.
