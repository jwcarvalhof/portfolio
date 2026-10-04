# Portfólio · Jhonatan Carvalho

Landing page única de portfólio de UX/UI e Web Design. Escura, bilíngue (PT/EN), feita para levar recrutadores e líderes de design direto aos três cases, com motion que prova a habilidade em vez de falar dela.

## O que tem nesta pasta

| Arquivo | O que é |
|---|---|
| `index.html` | O site inteiro em um arquivo só (HTML, CSS e JavaScript). Abre com duplo clique. |
| `docs/01-briefing-e-decisoes.md` | O briefing original, os ajustes críticos feitos nele e o histórico de cada decisão. |
| `docs/02-design-system.md` | Cores, tipografia, espaçamentos, raios, curvas de animação e camadas de ambiente. |
| `docs/03-estrutura-e-conteudo.md` | Todas as seções da página e toda a copy em PT e EN. |
| `docs/04-motion-e-interacoes.md` | Cada animação e interação, com tempos, faixas de scroll e comportamento. |
| `docs/05-responsividade-e-acessibilidade.md` | Como a página se adapta a desktop, tablet e celular, e os cuidados de acessibilidade. |
| `docs/06-como-editar.md` | Passo a passo para trocar cases, links, textos, cores e contato. |
| `docs/07-publicacao-e-proximos-passos.md` | O que falta antes de publicar e como colocar no ar. |

## Como visualizar

- **Rápido:** duplo clique em `index.html`. Abre no navegador e funciona por completo (não depende de vídeo nem de servidor).
- **Fontes:** carregam do Google Fonts, então precisa de internet para a tipografia correta. Sem internet, o navegador usa fontes de sistema parecidas.
- **Para sentir o motion:** abra no computador, role devagar pelo topo e depois rápido. Passe o mouse nos cases e clique em "Contato".

## Resumo da experiência

1. **Entrada:** seu nome sobre uma grade de colunas. Ao rolar, um site se desenha em linhas (navegador, menu, título, imagem, cards), ganha medidas em rosa e um cursor clica no card do meio, que acende em violeta.
2. **Galeria:** três cases em um eixo invisível e assimétrico, revelados um a um, ligados por um fio que se desenha com o scroll. No hover, uma caixa de seleção igual à do Figma mostra a medida real do card.
3. **Contato:** ao clicar em "Contato", o que está na tela se desfaz no próprio wireframe, as linhas se apagam e o contato se redesenha antes de ganhar cor.

## Estado atual

- Estrutura, motion, responsividade e idiomas: prontos.
- Cases: placeholders desenhados, marcados no código para troca.
- Contato: endereços de exemplo, marcados no código para troca.
- No ar: https://portfolio-pi-ecru-28.vercel.app (Vercel, publica sozinho a cada alteração na branch `main` deste repositório).
- Faltam trocar os placeholders (ver `docs/07-publicacao-e-proximos-passos.md`).
