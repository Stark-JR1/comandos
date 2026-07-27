# Git e GitHub — comandos essenciais

## Configuração inicial da identidade

O Git precisa registrar o autor de cada commit. Na primeira utilização, configure nome e e-mail:

```powershell
git config --global user.name "Seu Nome"
git config --global user.email "seu_email@exemplo.com"
```

Prefira usar o mesmo e-mail cadastrado no GitHub ou o endereço privado no formato `ID+usuario@users.noreply.github.com`.

### Verificar a configuração

```powershell
git config --global --list
git config user.name
git config user.email
```

### Configurar somente no repositório atual

Execute dentro da pasta do projeto, sem `--global`:

```powershell
git config user.name "Seu Nome"
git config user.email "seu_email@exemplo.com"
```

### Erro: `user.name` e `user.email` não configurados

Sintomas comuns:

```text
Verifique se você configurou "user.name" e "user.email" no git.
```

```text
Author identity unknown
Please tell me who you are.
fatal: unable to auto-detect email address
```

Correção:

```powershell
git config --global user.name "Seu Nome"
git config --global user.email "seu_email@exemplo.com"
```

Depois, repita o commit:

```powershell
git add .
git commit -m "descrição da alteração"
git push origin main
```

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
