# Ollama e modelos locais

## Verificar instalação

```powershell
ollama --version
ollama list
```

## Baixar e executar modelo

```powershell
ollama pull phi3
ollama run phi3
```

## Servidor local

```powershell
ollama serve
```

Endpoint padrão:

```text
http://localhost:11434
```

## Diagnóstico

```powershell
Get-Process ollama
netstat -ano | findstr :11434
```

## Remover modelo

```powershell
ollama rm nome-modelo
```

## Escolha de modelo

Para máquina com 16 GB de RAM, prefira modelos pequenos e quantizados. Teste consumo real antes de integrar ao projeto. Um modelo que abre e transforma o computador em aquecedor não é exatamente uma vitória técnica.

## Integração segura

- defina timeout;
- trate indisponibilidade;
- registre latência;
- não envie dados sensíveis sem necessidade;
- mantenha fallback determinístico para classificação crítica.
