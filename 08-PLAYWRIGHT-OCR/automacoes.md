# Playwright e OCR

## Playwright

```powershell
pip install playwright
python -m playwright install
python -m playwright install chromium
```

## Executar script

```powershell
python run.py
python scripts\healthcheck.py
```

## Atualizar navegadores

```powershell
python -m playwright install --with-deps
```

## Debug

```powershell
$env:PWDEBUG="1"
python run.py
```

## Regras de automação

- use esperas explícitas por elemento, não `time.sleep()` como estratégia principal;
- registre URL, etapa e erro;
- salve screenshot apenas quando houver falha;
- valide arquivo baixado antes de mover;
- mantenha diretórios de entrada, processados e pendências separados.

## OCR

Fluxo recomendado:

```text
PDF com texto → extração direta
PDF escaneado → OCR
confiança alta → processar
confiança baixa → revisão
```

Nunca aplique OCR em tudo por padrão. É mais lento, menos confiável e transforma um problema simples numa cerimônia computacional.

## Diagnóstico de PDF

Verifique:

- existe texto extraível;
- número de páginas;
- tamanho do arquivo;
- fornecedor;
- número do documento;
- valor;
- tipo documental;
- confiança de cada campo.
