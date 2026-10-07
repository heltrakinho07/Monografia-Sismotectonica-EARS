# Monografia Sismotectónica — Extremo Sul do EARS

Repositório científico associado à monografia sobre a **caracterização da sismicidade do extremo sul do East African Rift System (EARS), no centro de Moçambique**, recorrendo a técnicas de aprendizagem profunda, associação automática de fases, relocalização hipocentral, inversão de fonte sísmica e agrupamento espacial.

## Workflow científico

```text
Dados sísmicos / metadados
        ↓
01. Download e organização dos dados
        ↓
02. Pré-processamento e controlo de qualidade
        ↓
03. EQTransformer
    detecção automática + picks P/S
        ↓
04. PyOcto
    associação de fases + catálogo preliminar
        ↓
05. NLL-SSST-Coherence
    localização / relocalização hipocentral
        ↓
06. Grond
    inversão de formas de onda / parâmetros de fonte
        ↓
07. DBSCAN
    agrupamento espacial da sismicidade
        ↓
08. Análise, visualização e interpretação sismotectónica
```

## Estrutura do repositório

| Pasta | Conteúdo |
|---|---|
| `01_Download_Dados/` | aquisição, organização e inventário dos dados sísmicos |
| `02_Pre_Processamento/` | preparação, filtragem, controlo de qualidade e conversões |
| `03_EQTransformer/` | detecção automática e picking das fases P e S |
| `04_PyOcto/` | associação espaço-temporal de picks e geração de eventos |
| `05_NLL_SSST_Coherence/` | localização e relocalização com NonLinLoc / SSST / coherence |
| `06_Inversao_Grond/` | inversão de formas de onda e parâmetros de fonte com Grond |
| `07_Agrupamentos_DBSCAN/` | agrupamento espacial e análise de clusters sísmicos |
| `08_Analise_Visualizacao/` | mapas, gráficos, estatísticas e interpretação final |
| `Extra/` | resultados seleccionados de cada etapa do workflow |
| `docs/` | metodologia, dados, reprodutibilidade e notas técnicas |

## Dados

Os volumes sísmicos brutos, MiniSEED/SAC, caches, modelos pesados e resultados temporários de grande dimensão **não são versionados** neste repositório.

O repositório mantém principalmente:

- scripts e notebooks;
- configurações e parâmetros;
- metadados e pequenos catálogos;
- resultados finais seleccionados;
- figuras, mapas e tabelas;
- documentação necessária para reproduzir o workflow.

## Resultados

A pasta `Extra/` reúne os produtos derivados considerados relevantes para auditoria científica e para a monografia:

- picks do EQTransformer;
- catálogos e assignments do PyOcto;
- resultados das iterações NLL-SSST/Coherence;
- soluções de inversão Grond;
- clusters DBSCAN;
- mapas, tabelas, estatísticas e figuras finais.

## Reprodutibilidade

Consulte:

- `docs/metodologia.md`
- `docs/dados.md`
- `docs/reprodutibilidade.md`
- o `README.md` específico de cada etapa.

As versões definitivas dos parâmetros de processamento devem ser mantidas junto dos respectivos scripts/configurações.

## Autor

**Hélder Gonçalves Félix Traquinho**  
Universidade Eduardo Mondlane — Moçambique

## Uso científico

Ao reutilizar código, configurações ou resultados deste projecto, consulte `CITATION.cff` e cite os softwares e trabalhos científicos originais utilizados em cada etapa.

## Licença

O código original deste repositório é disponibilizado sob a licença MIT. Dependências externas mantêm as suas próprias licenças.
