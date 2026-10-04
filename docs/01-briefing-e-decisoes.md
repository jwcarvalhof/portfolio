# 01 · Briefing e decisões

## O pedido original, em resumo

- Landing de portfólio pessoal focada em UX/UI e experiências digitais.
- Só a landing por enquanto. Os cases entram depois; usar 3 placeholders.
- Estética dark, sofisticada, preto dominante. Roxo como luz ambiente vinda de baixo. Rosa só como acento em interações.
- Tipografia limpa, bordas controladas, muito espaço negativo, contraste forte.
- Personalidade: **seriedade na composição, personalidade nas interações.**
- Entrada simples, levando rápido para a galeria.
- Galeria assimétrica e intencional, revelada com o scroll.
- Hover sofisticado nos cases. Motion com referência no Jitter: easing trabalhado, nada linear.
- Responsivo desde o início, sem simplesmente empilhar cards no celular.
- Navegação mínima.
- O site deve provar a habilidade sem dizer que é bom.

## Respostas da conversa de refinamento

| Pergunta | Resposta |
|---|---|
| Quem impressionar | Recrutadores e líderes de design |
| Tom de voz | Leve e espirituoso |
| Assinatura | Interação nos cases ao passar o mouse (hoje: seleção estilo Figma) |
| Entrada | Animação ligada ao scroll (hoje: site se desenhando em linhas, feito em código) |
| Idioma | Bilíngue, com troca PT/EN |
| Nome | Jhonatan Carvalho |
| Sensações | Curiosidade, calma de galeria, sorriso discreto. Muito respiro, objetivo, tudo puxando para a galeria |
| Página | Única, sem outros links além do necessário |
| Contato | LinkedIn, Instagram e e-mail |
| Título profissional | UX/UI · Web Design |

## Ajustes críticos feitos no briefing (antes de construir)

1. **Cases não ficam escondidos atrás de muito scroll.** Recrutador decide em segundos. A entrada é curta e a galeria aparece logo depois.
2. **Hover não existe no celular.** Nome, categoria e links dos cases ficam sempre visíveis. O hover só acrescenta.
3. **A luz roxa é uma camada fixa só,** animada por opacidade e escala. Gradiente redesenhado a cada pixel de scroll trava em notebook comum.
4. **No celular, nada de carrossel lateral.** A assimetria continua com larguras e deslocamentos diferentes numa coluna.
5. **Uma assinatura forte em vez de várias graças espalhadas.**

## O que a pesquisa mostrou

Recrutadores de design têm pouco tempo por portfólio, querem chegar rápido no trabalho e desconfiam de efeito chamativo que fica na frente do conteúdo (NN/g, UX Design Institute). Por isso cada animação tem uma função: guiar o olho para baixo, até os cases.

## Histórico de decisões

| # | Decisão | Motivo |
|---|---|---|
| 1 | Primeira versão com uma lente de vidro em shader (WebGL) no topo | Conceito "design é como você olha". O gerador de vídeo por IA não conectou, então foi feito em código |
| 2 | Lente trocada por **um site se desenhando em linhas** | A lente passava vibe de fotógrafo. Wireframe fala direto do ofício |
| 3 | Animação em código, não em vídeo de IA | IA entorta linhas de interface. Em código ficam nítidas, precisas e no ritmo do scroll, e funcionam no celular |
| 4 | Copy "Três cases. Zero enrolação." removida | Não pegou bem. Entrou "Antes do pixel, a estrutura." e "Do rascunho ao produto." |
| 5 | Cursor-lente trocado por **caixa de seleção estilo Figma** | Mesma razão da lente. A seleção conversa com o wireframe do topo |
| 6 | Clique em "Contato" vira **transição em linhas** | Pedido: não pular seco. A tela se desfaz no próprio wireframe e o contato se redesenha |
| 7 | Link **"Acessar página ↗"** ao lado de "Ver case" | Os cases são landing pages publicadas; o link deixa óbvio que leva ao site no ar |
| 8 | "Product Design" virou **"Web Design"** | Pedido direto |

## Princípio que guia tudo

O site é uma demonstração do processo de um designer: estrutura primeiro (grade, wireframe, medidas), depois produto vivo. Cada interação repete essa ideia em escala menor.
