# Projetos atuais — operação diária

## Discord Planner RC/PC

```powershell
cd "C:\Users\paulo.junior\OneDrive\ROBOS\discord_planner_FINAL\discord_planner"
.venv\Scripts\Activate.ps1
python scripts\healthcheck.py
python scripts\init_db.py
python run.py
```

Verificação completa:

```powershell
python -m pytest -q
python -m ruff check .
python -m mypy bot
python -m compileall bot
git diff --check
```

## SilentFlow / FastAPI

```powershell
.venv\Scripts\Activate.ps1
uvicorn app.main:app --reload
```

## Robô NF, boleto e PC

Antes de executar:

- conferir pasta de entrada;
- criar backup;
- rodar dry-run;
- revisar pendências;
- confirmar se PDFs com texto são lidos sem OCR;
- aplicar OCR apenas nos escaneados.

## Robô DAE

```powershell
.venv\Scripts\Activate.ps1
python scripts\healthcheck.py
python run.py
```

Validar:

- planilha correta;
- pasta do ano e mês;
- navegador Playwright instalado;
- dados de valor, vencimento e próxima leitura;
- envio de e-mail.

## Regra geral

Cada projeto deve possuir:

```text
README.md
.env.example
.gitignore
requirements.txt
scripts/healthcheck.py
tests/
logs/
data/
backups/
```
