# 05 — NLL-SSST-Coherence

## Objectivo
Refinar a localização dos eventos e avaliar a consistência das soluções.

## Estrutura prevista
- `scripts/`
- `configs/`
- `velocity_models/`
- `station_files/`
- `examples/`

## Sequência NLL-SSST
```text
NLLoc Iter0
→ LocSum Iter0
→ Loc2ssst Iter1
→ NLLoc Iter1
→ LocSum Iter1
→ Loc2ssst Iter2
→ NLLoc Iter2
```

A componente de coherence deve ser identificada separadamente quando aplicada, evitando misturar os resultados puramente NLL-SSST com os resultados de waveform coherence.

Resultados seleccionados: `Extra/03_NLL_SSST_Coherence/`.
