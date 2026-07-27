# Codex — prompts e fluxo de trabalho

## Prompt de correção

```text
Leia o projeto antes de alterar.
Reproduza o erro.
Identifique a causa raiz com arquivo e linha.
Corrija somente o escopo solicitado.
Não refatore módulos não relacionados.
Adicione testes específicos da regressão.
Execute pytest, Ruff, MyPy, compileall e git diff --check.
Não execute git push.
No final, informe arquivos alterados, causa raiz, testes e pendências reais.
```

## Prompt de implementação

```text
Implemente a funcionalidade descrita reutilizando services e repositories existentes.
Não duplique regras de negócio.
Mantenha compatibilidade com o banco atual.
Crie testes para o novo comportamento.
Não declare concluído sem validação manual do fluxo principal.
```

## Prompt de auditoria

```text
Não altere código inicialmente.
Revise arquitetura, sessões de banco, concorrência, tratamento de erros, segurança e testes.
Liste problemas por severidade, com evidência no código e correção recomendada.
Separe fatos de hipóteses.
```

## Fluxo recomendado

1. `git status`;
2. criar branch;
3. entregar prompt em Markdown;
4. exigir diagnóstico antes da alteração;
5. revisar `git diff`;
6. executar testes;
7. testar manualmente;
8. só então fazer commit.

## Sinais de alerta

- “Tudo concluído” sem testes novos;
- relatório menciona Ruff pendente;
- código foi alterado em muitos módulos sem necessidade;
- regra de negócio duplicada;
- `except Exception: pass`;
- resposta baseada apenas em testes antigos.
