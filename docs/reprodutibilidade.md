# Reprodutibilidade

## Ambiente Python

Opção 1:

```bash
conda env create -f environment.yml
conda activate monografia-sismotectonica-ears
```

Opção 2:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Dependências externas

Algumas etapas requerem software externo que pode não ser instalado apenas pelo `requirements.txt`:

- NonLinLoc / NLLoc;
- LocSum;
- Loc2ssst;
- componentes de coherence, quando utilizados;
- Grond/Pyrocko e respectivos Green's Function stores.

As versões efectivamente usadas na monografia devem ser registadas antes da publicação final.

## Registo de execução

Para cada execução relevante, guardar:

1. versão do código/commit;
2. período processado;
3. parâmetros;
4. inputs;
5. outputs principais;
6. estatísticas de controlo de qualidade;
7. data da execução.

## Dados grandes

Os dados brutos devem ser guardados externamente. O repositório deve conter scripts e metadados suficientes para reconstruir o processamento.
