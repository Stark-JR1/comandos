# Python — ambiente e dependências

## Criar e ativar ambiente

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

## Instalar dependências

```powershell
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## Atualizar requirements

```powershell
pip freeze > requirements.txt
```

## Diagnóstico

```powershell
python --version
pip --version
pip list
where python
where pip
```

## Pacotes

```powershell
pip install nome_pacote
pip install --upgrade nome_pacote
pip uninstall nome_pacote
pip cache purge
```

## Sair do ambiente

```powershell
deactivate
```

## Recriar ambiente quebrado

```powershell
deactivate
Remove-Item -Recurse -Force .venv
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```
