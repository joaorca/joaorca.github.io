---
name: projeto-reestruturacao-2025
description: Reestruturação completa do site portfolio em junho 2025 — decisões de layout e conteúdo
metadata:
  type: project
---

Reestruturação completa realizada em jun/2025. Principais decisões:

- Zero JavaScript — jQuery, Bootstrap JS e scripts.js removidos
- Font Awesome 4.7.0 via cdnjs (substituiu FA5 kit e arquivos locais)
- Foto no header à esquerda com nome + cargo + contatos inline
- Formação movida para coluna direita (acima de Certificações)
- Nova seção Certificações (substituiu Skills de barras animadas)
- Skills voltou como tags CSS simples
- Idiomas e Hobbies fundidos em um box; estrelas via FA (sem imagens)
- Contatos movidos para o header (removido box dedicado)
- Experiências: layout stacked com `.job-header` (empresa em vermelho · período / cargo bold / descrição)
- Fonte base normalizada em 1.2em em todos os boxes (Sobre Mim, Experiências, Formação, Certificações)
- Fonte trocada de Open Sans para Montserrat (400,600,700,800) a 1.1em base
- Bug corrigido: aspas curvas tipográficas (`"`) substituídas por aspas retas ASCII em todo o index.html (impediam CSS selectors de funcionar)

**Why:** Modernizar visual, reduzir dependências, melhor adequação ao perfil de gerente sênior.

**How to apply:** Ao sugerir mudanças, respeitar zero-JS e FA4. Não reintroduzir arquivos de `js/` ou `fonts/`.
