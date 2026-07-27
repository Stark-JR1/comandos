# ArqMentor — Cérebro de Comandos

Este repositório é um manual vivo para consulta rápida de comandos, rotinas e checklists usados no dia a dia.

## Índice

- [Git e GitHub](01-GIT/comandos-basicos.md)
- [Python](02-PYTHON/ambiente-e-dependencias.md)
- [Testes e qualidade](02-PYTHON/testes-e-qualidade.md)
- [Discord.py](03-DISCORD/discord-bot.md)
- [FastAPI](04-FASTAPI/fastapi.md)
- [Docker](05-DOCKER/docker.md)
- [SQLite e SQL](06-SQL/sqlite.md)
- [PowerShell e Windows](07-POWERSHELL/windows-powershell.md)
- [Linux](08-LINUX/linux.md)
- [Codex](09-CODEX/codex.md)
- [Playwright](10-PLAYWRIGHT/playwright.md)
- [OCR](11-OCR/ocr.md)
- [Ollama](12-OLLAMA/ollama.md)
- [n8n](13-N8N/n8n.md)
- [Deploy](14-DEPLOY/deploy.md)
- [Checklists](CHECKLISTS/README.md)

## Atalhos principais

### Criar e ativar ambiente Python

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

### Instalar dependências

```powershell
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### Rodar projeto

```powershell
python run.py
```

### Testar

```powershell
python -m pytest -q
python -m ruff check .
python -m mypy bot
```

### Subir para o GitHub

```powershell
git status
git add .
git commit -m "descrição da alteração"
git push origin main
```

## Regra de uso

Antes de executar comandos destrutivos, confira o diretório atual e rode `git status`. Humanos conseguem apagar a pasta errada com uma eficiência impressionante.
