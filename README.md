# Boden — Landing Page

Landing page de cafés especiais personalizados (Boden Club), extraída do projeto
"Design System" para um projeto independente em 2026-07-29.

## Estrutura

```
Boden/
├── index.html              página única (HTML + CSS + JS inline)
├── assets/images/           todas as imagens de produto e o favicon
└── .claude/launch.json      config de servidor local para dev
```

## Rodando localmente

```
npx serve . -p 3333
```

Depois abra `http://localhost:3333/`.

## Stack

- HTML/CSS/JS puro, sem build step.
- Fontes (Google Fonts): **Alegreya** (títulos/destaques), **Montserrat** (texto
  corrido), **Satisfy** (destaques em script).
  - ⚠️ A marca especifica **Gotham** para texto corrido, mas é fonte paga sem
    licença embutível via Google Fonts/CDN gratuito. Montserrat foi usada como
    substituta mais próxima. Se a licença da Gotham (arquivos `.woff2`) estiver
    disponível, trocar via `@font-face` em vez do link do Google Fonts.
- Paleta de cores: tokens CSS custom properties no `:root` do `<style>`,
  seguindo a marca oficial (Vermelho #66271B, Marrom #302621, Bege #EEC29E +
  paleta secundária).
- Formulário de orçamento integrado à API de submissão de formulários do
  HubSpot (portal `47243991`, form `440b93fe-b3f2-43bb-ba8d-b29643d3442a`),
  com máscara de telefone/CEP, validação client-side e preview de embalagem
  conforme o tamanho selecionado.
- Sem dependências de build (Webflow, Next.js etc.) — é uma página estática
  para hospedar em qualquer serviço de arquivos estáticos.

## Notas

- Este projeto foi extraído de `Design System/output/boden-landing.html`; o
  arquivo original e os assets continuam lá também (nada foi removido de lá).
