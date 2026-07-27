# Windows e PowerShell

## Navegação

```powershell
Get-Location
Set-Location "C:\caminho\projeto"
Get-ChildItem
explorer .
code .
```

## Arquivos e pastas

```powershell
New-Item -ItemType Directory pasta
New-Item arquivo.txt
Copy-Item origem destino
Move-Item origem destino
Remove-Item arquivo.txt
Remove-Item -Recurse -Force pasta
```

## Processos e portas

```powershell
Get-Process
Get-Process python
Stop-Process -Id PID
netstat -ano | findstr :8000
```

## Variáveis de ambiente

```powershell
$env:NOME="valor"
Get-ChildItem Env:
Remove-Item Env:NOME
```

## Execução de scripts

```powershell
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```

## Caminhos dos projetos atuais

Use aspas em caminhos com espaços. OneDrive, naturalmente, faz questão de tornar caminhos longos ainda mais emocionantes.
