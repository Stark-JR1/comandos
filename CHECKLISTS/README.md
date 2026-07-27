# Checklists operacionais

## Novo projeto Python

- [ ] criar repositório;
- [ ] criar `.gitignore`;
- [ ] criar `.env.example`;
- [ ] criar `.venv`;
- [ ] instalar dependências;
- [ ] criar README;
- [ ] criar healthcheck;
- [ ] configurar logs;
- [ ] criar testes mínimos;
- [ ] executar primeiro commit.

## Antes do commit

```powershell
git status
git diff
python -m pytest -q
python -m ruff check .
python -m ruff format --check .
python -m mypy bot
python -m compileall bot
git diff --check
```

- [ ] sem `.env`;
- [ ] sem banco;
- [ ] sem logs;
- [ ] sem backups;
- [ ] sem token, senha ou chave;
- [ ] testes novos para comportamento novo.

## Antes do push

```powershell
git branch --show-current
git diff --cached
git log --oneline -5
git push origin NOME_DA_BRANCH
```

## Diagnóstico de erro

- [ ] reproduzir;
- [ ] capturar traceback completo;
- [ ] identificar primeiro erro real;
- [ ] conferir ambiente virtual;
- [ ] conferir versão do Python;
- [ ] conferir dependências;
- [ ] conferir `.env`;
- [ ] conferir banco e migrações;
- [ ] criar teste da regressão;
- [ ] corrigir causa, não sintoma.

## Antes de produção

- [ ] backup;
- [ ] migrações testadas;
- [ ] healthcheck aprovado;
- [ ] logs funcionando;
- [ ] tratamento de erro global;
- [ ] teste manual do fluxo principal;
- [ ] plano de rollback;
- [ ] apenas uma instância usando SQLite.
