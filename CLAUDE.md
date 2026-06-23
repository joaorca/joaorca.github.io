# joaorca.github.io

Site de currículo/portfólio pessoal hospedado no GitHub Pages.

## Decisões técnicas

- **Zero JavaScript** — jQuery, Bootstrap JS e scripts.js foram removidos intencionalmente; não reintroduzir
- **Font Awesome 4.7.0** via cdnjs — classes usam prefixo `fa fa-*` (não `fas`/`far` do FA5)
- **Google Fonts** carregado no `main.css` via `@import`, não no HTML — não adicionar `<link>` para fontes no `index.html`
- **Fonte atual: Montserrat** (400,600,700,800) a `font-size: 1.1em` no body
- Domínio customizado configurado via `CNAME`

## Comandos

```bash
# Ver o site localmente
python3 -m http.server 8080

# Deploy
git push origin master
```
