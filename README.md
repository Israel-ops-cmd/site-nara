# Site Nára Perêira, massoterapeuta em Natal

Site estático, sem etapa de build. HTML, CSS e JS ficam em `index.html`; GSAP 3.12.5 + ScrollTrigger e Lenis 1.1.13 ficam em `vendor/`.

## Rodar localmente

```
npx serve .
```
ou
```
python3 -m http.server 8080
```
e abra http://localhost:8080 (os caminhos são absolutos, então abra pela raiz do servidor, não pelo arquivo).

## Estrutura

- `index.html`: página única
- `img/`: fotos em WebP (800 e 1600 px; recortes em 700 e 1200 px)
- `vendor/`: bibliotecas com versão fixa
- `favicon.svg`, `apple-touch-icon.png`, `og-image.jpg` (1200x630, preview no WhatsApp)
- `vercel.json`: cleanUrls e cache longo para `img/` e `vendor/`
- `BRIEFING.md`: identidade, paleta, fontes, fotos e pendências

## Trocar uma foto

Gere as duas larguras em WebP com o mesmo nome (ex.: `img/02-sobre-700.webp` e `img/02-sobre-1200.webp`) e faça push.

## Publicar

Cada push na branch `main` publica sozinho na Vercel (projeto ligado ao repositório, Framework Preset: Other, sem Build Command, Output Directory `./`).

Ao ligar um domínio próprio, atualize `canonical`, `og:url`, `og:image`, `twitter:image` e a `url` do Schema.org em `index.html`.
