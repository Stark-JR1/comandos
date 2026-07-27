# ArqMentor — Cérebro de Comandos

Manual operacional vivo para os projetos atuais: bots Discord, FastAPI, automações Playwright, OCR, SQLite, Docker, IA local e GitHub.

## Índice principal

- [Git e GitHub](01-GIT/comandos-basicos.md)
- [Python: ambiente e dependências](02-PYTHON/ambiente-e-dependencias.md)
- [Python: testes e qualidade](02-PYTHON/testes-e-qualidade.md)
- [Discord.py](03-DISCORD/discord-bot.md)
- [FastAPI](04-FASTAPI/fastapi.md)
- [Docker](05-DOCKER/docker.md)
- [SQLite e SQLAlchemy](06-SQL/sqlite-sqlalchemy.md)
- [Windows e PowerShell](07-POWERSHELL/windows-powershell.md)
- [Playwright e OCR](08-PLAYWRIGHT-OCR/automacoes.md)
- [Ollama e IA local](09-IA-LOCAL/ollama.md)
- [Codex: prompts e fluxo](10-CODEX/prompts-e-fluxo.md)
- [Checklists operacionais](CHECKLISTS/README.md)
- [Operação dos projetos atuais](PROJETOS-ATUAIS/operacao-diaria.md)
- [Lições aprendidas](LICOES-APRENDIDAS/erros-reais.md)

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

### Testar antes de commit

```powershell
python -m pytest -q
python -m ruff check .
python -m ruff format --check .
python -m mypy bot
python -m compileall bot
git diff --check
```

### Fluxo seguro do Git

```powershell
git status
git diff
git add .
git diff --cached
git commit -m "descrição da alteração"
git push origin main
```

## Como usar este repositório

1. consulte o índice;
2. copie somente o comando necessário;
3. confira o diretório e a branch;
4. leia alertas antes de comandos destrutivos;
5. registre novas lições depois de erros relevantes.

## Regra central

Antes de executar comandos destrutivos, confira:

```powershell
Get-Location
git status
git branch --show-current
```

Humanos conseguem apagar a pasta errada com uma eficiência admirável. A documentação existe para reduzir esse talento.
