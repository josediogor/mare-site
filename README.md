# Maré — landing page

Página única, estática (`index.html` + `assets/`). Sem build, sem dependências. Tema deep-ocean, identidade derivada de `app/lib/theme.ts`. Screenshots são capturas reais do app, em molduras de iPhone montadas em CSS (com uma status bar limpa cobrindo a barra do TestFlight).

## No ar
- **Domínio:** https://marevicio.com (custom domain do GitHub Pages)
- **Repo:** github.com/josediogor/mare-site (branch `main`, root)
- **Cole no campo Marketing URL** da App Store Connect: `https://marevicio.com`

## Preview local
Abra `index.html` no navegador (duplo clique). Sem servidor necessário.

## Deploy / atualizar
Edite os arquivos e: `git commit -am "..." && git push`. O GitHub Pages republica em ~1 min.

O arquivo `CNAME` (contém `marevicio.com`) fixa o domínio no Pages. As 3 metatags de Open Graph (`og:url`, `og:image`, `twitter:image`) já apontam pra `https://marevicio.com`.

## DNS (na GoDaddy)
Apex `marevicio.com` → 4 registros A pro GitHub Pages:
`185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
E `www` como CNAME → `josediogor.github.io`. Remover o domain forwarding/parking da GoDaddy. Depois ativar "Enforce HTTPS" em Settings → Pages.

## CTAs
Todos apontam para a App Store live: `https://apps.apple.com/br/app/id6773973582`. Botão Android = "em breve".

## Notas de conteúdo
- Privacidade honesta: diário/marés/âncora ficam on-device; mensagens do **faroleiro** passam por servidor + provedor de IA (OpenAI) sem identificação. Por isso a página fala "100% anônimo" e nunca "sem nuvem".
- Planos reais: Mensal R$19,90 · Anual R$99,90 (melhor, -58%) · Lifetime R$249,90 · 7 dias grátis.
- Bloco de segurança CVV 188 em registro grave (sem metáfora).
- Sem nome/menção pessoal ou de localização (decisão do José). Sem travessão na copy.

## Debug (só roda em localhost/file://)
`?v=1` revela tudo na hora · `?y=N` rola pra Y · `?probe=1` mede offsets. Gated por hostname, não roda no domínio live.
