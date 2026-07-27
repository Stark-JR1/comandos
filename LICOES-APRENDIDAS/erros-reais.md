# Lições aprendidas com erros reais

## Discord

### O aplicativo não respondeu

- use `defer()` antes de operações demoradas;
- não consulte banco no `__init__` da View;
- não responda a mesma interação duas vezes;
- registre traceback globalmente;
- teste comandos e botões no Discord, não apenas services.

### Views persistentes

- `timeout=None`;
- `custom_id` fixo;
- registrar no `setup_hook`;
- manter apenas IDs e snapshots simples;
- reconsultar processo em cada callback.

## SQLAlchemy

### DetachedInstanceError

Não use objeto ORM depois de fechar sessão. Copie valores dentro do bloco ou converta para objeto simples.

### SQLite bloqueado

Não execute duas instâncias apontando para o mesmo banco. Feche sessões e evite transações longas.

## Git

- conferir `git status` antes de `git add .`;
- nunca subir `.env`, banco, logs ou backups;
- conferir branch antes do push;
- preferir `git revert` para desfazer commit já publicado.

## OCR

- extração de texto deve vir antes do OCR;
- documentos globais exigem regras genéricas, não exemplos codificados;
- confiança deve ser por campo;
- escaneados devem ir para revisão quando a confiança for baixa.

## Codex

- não aceitar “concluído” sem testes novos;
- pedir causa raiz, arquivos e linhas;
- limitar escopo;
- exigir teste manual quando a funcionalidade depende de Discord, navegador ou arquivos reais;
- revisar o diff antes do push.
