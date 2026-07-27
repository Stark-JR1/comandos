# Python — testes e qualidade

## Pytest

```powershell
python -m pytest -q
python -m pytest -v
python -m pytest tests/test_arquivo.py -q
python -m pytest tests/test_arquivo.py::test_nome -q
```

## Ruff

```powershell
python -m ruff check .
python -m ruff check . --fix
python -m ruff format .
python -m ruff format --check .
```

## MyPy

```powershell
python -m mypy bot
```

## Compilação

```powershell
python -m compileall bot
```

## Verificação antes de commit

```powershell
python -m pytest -q
python -m ruff check .
python -m ruff format --check .
python -m mypy bot
python -m compileall bot
git diff --check
```

## Regra prática

Não declarar projeto concluído apenas porque testes antigos passaram. Funcionalidade nova precisa de teste novo, sobretudo botões, modais, interações Discord e regressões de fluxo.
