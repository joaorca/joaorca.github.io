---
description: Salva memórias da sessão, atualiza docs, promove rules, versiona e commita o projeto.
disable-model-invocation: true
---

## Estado atual

Estado git:
!`git status --short`

Versão atual:
!`cat .claude/VERSION`

Revise toda a conversa atual e execute:

1. **Memórias** — salve memórias relevantes em `.claude/memory/` (user, feedback, project, reference). Leia o MEMORY.md antes para não duplicar. Não salve: padrões de código, histórico git, detalhes efêmeros.

2. **Índice** — atualize `.claude/memory/MEMORY.md` (uma linha por memória, máx 150 chars).

3. **CLAUDE.md** — adicione ou corrija informações novas: convenções, decisões técnicas, estrutura relevante. Não reescreva o que já está correto.

4. **Promoção para rules** — revise memórias do tipo `feedback` e identifique quais descrevem comportamentos universais. Promova-as para `.claude/rules/comportamento.md` e delete o arquivo de memória se virou inteiramente uma rule.

5. **Integridade do MEMORY.md** — entradas sem arquivo correspondente: remover do índice. Arquivos sem entrada: adicionar ao índice.

6. **Settings** — remova entradas de `allowedTools` e `additionalDirectories` acumuladas automaticamente por aprovações de sessão. Mantenha: hooks, theme, permissões intencionais. Delete `settings.local.json` se existir.

7. **VERSION** — incremente semver em `.claude/VERSION`:
   - `major` — mudança estrutural significativa
   - `minor` — novo comando, skill, rule ou agente
   - `patch` — memória, CLAUDE.md, settings, correções menores

8. **Varredura de dados sensíveis** — antes de commitar, verifique todos os arquivos staged: senhas, tokens, API keys, CPF, dados pessoais, credenciais. Se encontrar algo suspeito, interrompa e aguarde instrução.

9. **README** — verifique se as mudanças da sessão impactam o README. Atualize se necessário.

10. **Commit semântico** — `git add` nos arquivos do /salvar, commit com prefixo adequado (`chore:`, `feat:`, `docs:`) e descrição curta.

11. **Push** — `git push origin master` (SSH configurado via `gh auth`)

12. **Resumo** — memórias criadas/atualizadas/ignoradas, alterações no CLAUDE.md e rules, versão anterior → nova, hash do commit.
