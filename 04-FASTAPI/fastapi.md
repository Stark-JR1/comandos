# FastAPI

## Instalar

```powershell
pip install fastapi uvicorn
```

## Executar desenvolvimento

```powershell
uvicorn app.main:app --reload
```

## Executar indicando host e porta

```powershell
uvicorn app.main:app --host 0.0.0.0 --port 8000
```

## Ver documentação

```text
http://127.0.0.1:8000/docs
http://127.0.0.1:8000/redoc
```

## Testes

```powershell
python -m pytest -q
```

## Diagnóstico

```powershell
netstat -ano | findstr :8000
Get-Process -Id PID
Stop-Process -Id PID
```

## Estrutura recomendada

```text
app/
├── main.py
├── api/
├── models/
├── schemas/
├── services/
├── repositories/
├── templates/
└── static/
```

Separe endpoint, regra de negócio e acesso ao banco. Colocar tudo em `main.py` funciona até o projeto desenvolver opinião própria e começar a retaliar.
