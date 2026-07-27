# SQLite e SQLAlchemy

## SQLite CLI

```powershell
sqlite3 data\banco.db
```

```sql
.tables
.schema
PRAGMA table_info(processos);
SELECT * FROM processos LIMIT 10;
.quit
```

## Backup

```powershell
Copy-Item data\banco.db backups\banco-$(Get-Date -Format yyyyMMdd-HHmmss).db
```

## SQLAlchemy

Padrão seguro:

```python
with SessionLocal() as session:
    service = MeuService(session)
    resultado = service.executar()
```

Não devolva objeto ORM para uso depois de a sessão fechar. Converta para dataclass, dicionário ou schema.

## Migrações

Antes de alterar banco existente:

1. criar backup;
2. verificar se coluna/tabela já existe;
3. aplicar migração idempotente;
4. registrar versão;
5. testar em cópia do banco.

## Locks

Se aparecer `database is locked`:

- verifique processos usando o arquivo;
- reduza transações longas;
- feche sessões corretamente;
- evite múltiplas instâncias do bot no mesmo banco.
