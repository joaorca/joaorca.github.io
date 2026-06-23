---
description: Regras gerais de comportamento para este projeto
---

- Responda sempre em português do Brasil
- Não use emojis a menos que o usuário peça explicitamente
- Respostas curtas e diretas; sem resumos ao final de cada resposta
- Não crie arquivos de documentação (*.md, README) a menos que o usuário peça
- Sempre use commits semânticos: `feat:`, `fix:`, `chore:`, `docs:`, `refactor:`, `style:`, `test:` seguido de descrição curta em português
- Nunca fazer git add, commit ou operações que afetam o remoto (push, criar PR, merge, fechar issue) sem confirmação explícita do usuário — usar `gh` para push e operações GitHub
- Antes de qualquer commit, varrer os arquivos staged em busca de dados sensíveis (senhas, tokens, API keys, CPF, dados pessoais, credenciais) e dados que violem LGPD — interromper e alertar o usuário se encontrar algo suspeito
- Em `permissions.allow` do `settings.json`, incluir apenas `Read`, `Write` e `Edit` — nunca comandos Bash de escrita (`mkdir`, `mv`, `rm`, `ln`, `touch`, `sed -i`, `git *`); read-only como `ls` e `git status` já são auto-permitidos
- Não adicionar ao CLAUDE.md informações deriváveis lendo os arquivos do projeto — manter apenas o que não seria inferível: estrutura não óbvia, decisões técnicas, comandos operacionais. Conteúdo redundante desperdiça tokens em toda sessão
- Para operações de limpeza: classificar riscos, apresentar tabela resumida e executar sem pedir confirmação por item. Perguntar apenas antes de ações irreversíveis sobre dados pessoais (fotos, documentos, perfis)
- Ao escrever ou editar HTML, usar sempre aspas ASCII retas (`"`) nos atributos — nunca aspas curvas tipográficas (`"` `"`). Aspas curvas impedem seletores CSS de funcionar
