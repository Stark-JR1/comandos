# Git e GitHub — comandos essenciais

## Conferir estado

```powershell
git status
git branch --show-current
git remote -v
git log --oneline -10
```

## Fluxo seguro de commit

```powershell
git status
git diff
git add .
git diff --cached
git commit -m "feat: descreva a alteração"
git push origin main
```

Antes de `git add .`, confira se `.env`, bancos, logs, backups e arquivos pessoais não aparecem no `git status`.

## Primeiro envio

```powershell
git init
git branch -M main
git remote add origin URL_DO_REPOSITORIO
git add .
git commit -m "chore: versão inicial"
git push -u origin main
```

## Atualizar projeto local

```powershell
git pull origin main
```

## Branches

```powershell
git checkout -b feature/nome
git checkout main
git merge feature/nome
git branch -d feature/nome
```

## Desfazer com segurança

```powershell
git restore arquivo.py
git restore --staged arquivo.py
git revert SHA_DO_COMMIT
```

Evite `git reset --hard` sem backup. É uma serra elétrica com sintaxe curta.

## Diagnóstico

```powershell
git diff --check
git status --ignored
git log --graph --oneline --all
```

## Convenção de commits

```text
feat: nova funcionalidade
fix: correção de erro
docs: documentação
refactor: reorganização sem mudar comportamento
test: testes
chore: manutenção
```
