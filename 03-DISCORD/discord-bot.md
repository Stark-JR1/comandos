# Discord.py — operação do bot

## Executar

```powershell
python run.py
python scripts/healthcheck.py
python scripts/init_db.py
```

## Intents

```python
intents = discord.Intents.default()
intents.message_content = True
```

Ative também `MESSAGE CONTENT INTENT` no Developer Portal quando o bot precisar ler mensagens e anexos.

## Interações demoradas

```python
await interaction.response.defer(ephemeral=True, thinking=True)
await interaction.edit_original_response(content="Concluído")
```

Depois de `defer()`, não use `interaction.response.send_message()` novamente.

## Modal

Para abrir modal, não use `defer()` antes:

```python
await interaction.response.send_modal(MeuModal())
```

## Views persistentes

- `timeout=None`;
- `custom_id` fixo em todos os componentes;
- registrar com `bot.add_view()` no `setup_hook`;
- não consultar banco no `__init__` da View.

## Erros comuns

### O aplicativo não respondeu

Causas prováveis:
- callback demorou mais de cerca de 3 segundos;
- faltou `defer()`;
- exceção antes da primeira resposta;
- operação síncrona bloqueou o event loop.

### InteractionResponded

A mesma interação foi respondida duas vezes. Use `interaction.response.is_done()` e, se necessário, `followup.send()`.

### DetachedInstanceError

Objeto SQLAlchemy foi utilizado depois do fechamento da sessão. Copie dados simples dentro da sessão ou mantenha o uso do objeto dentro do mesmo bloco.

## Avisos de inicialização

```powershell
pip install "discord.py[voice]"
```

PyNaCl e davey são relacionados a voz. Message Content Intent é necessário para leitura de mensagens comuns.
