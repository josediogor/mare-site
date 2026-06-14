# Maré — landing page

Página única, estática (`index.html` + `assets/`). Sem build, sem dependências. Tema deep-ocean, identidade derivada de `app/lib/theme.ts`. Screenshots são capturas reais do app, em molduras de iPhone montadas em CSS (com uma status bar limpa cobrindo a barra do TestFlight).

## Preview local
Abra `index.html` no navegador (duplo clique). Sem servidor necessário.

## Deploy (GitHub Pages, igual ao mare-legal/hanko-site)
1. Crie um repo público, ex. `mare-site`.
2. Suba o conteúdo desta pasta (`index.html` + `assets/`) na raiz.
3. Settings → Pages → branch `main` / root. Sai no ar em `https://josediogor.github.io/mare-site/`.
4. Cole essa URL no campo **Marketing URL** da App Store Connect.

## ⚠️ Antes de publicar: trocar a base de URL do Open Graph
No `<head>` do `index.html`, 3 metatags usam um domínio placeholder. Troque pelo domínio real de deploy para o preview de link (WhatsApp/iMessage/X) funcionar:
- `og:url`
- `og:image`  → aponta pra `assets/og.jpg` (card 1200×630 já gerado)
- `twitter:image`

Hoje estão como `https://josediogor.github.io/mare-site/...`. Se for outro repo/domínio (ex. `mareapp.com.br`), ajuste lá.

## CTAs
Todos apontam para a App Store live: `https://apps.apple.com/br/app/id6773973582`.

## Notas de conteúdo
- Privacidade descrita com honestidade: o diário/marés/âncora ficam on-device; as mensagens do **faroleiro** passam por servidor + provedor de IA (OpenAI) sem identificação — por isso a página fala "100% anônimo" e **não** "sem nuvem".
- Planos refletem os reais: Mensal R$19,90 · Anual R$99,90 (melhor, -58%) · Lifetime R$249,90 · 7 dias grátis.
- Bloco de segurança CVV 188 em registro grave (sem metáfora).
- Nota do fundador (José Diogo) antes dos planos como prova social honesta (o app ainda não tem reviews).

## Debug (só roda em localhost/file://)
`?v=1` revela tudo na hora · `?y=N` rola pra Y · `?probe=1` mede offsets. Gated por hostname — não roda no domínio live.
