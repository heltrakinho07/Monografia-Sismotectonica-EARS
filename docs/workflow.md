# Workflow

```mermaid
flowchart TD
    A[Download de dados] --> B[Pré-processamento]
    B --> C[EQTransformer]
    C --> D[PyOcto]
    D --> E[NLL-SSST-Coherence]
    E --> F[Grond]
    E --> G[DBSCAN]
    F --> H[Análise e visualização]
    G --> H
```

## Interfaces entre etapas

- **Download → Pré-processamento:** waveforms + StationXML/inventários.
- **Pré-processamento → EQTransformer:** dados organizados e metadados compatíveis.
- **EQTransformer → PyOcto:** picks P/S com tempo, estação e probabilidade.
- **PyOcto → NLL-SSST:** eventos associados + picks por evento.
- **NLL-SSST → Grond:** eventos relocalizados e selecção de waveforms.
- **NLL-SSST → DBSCAN:** catálogo hipocentral refinado.
- **Grond + DBSCAN → interpretação:** parâmetros de fonte, clusters e contexto sismotectónico.
