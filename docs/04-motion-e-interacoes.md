# 04 · Motion e interações

## 1. Carregamento

- **Grade de colunas** (12 no desktop, 4 no celular) se desenha de cima para baixo em 1,8s, coluna por coluna (50 a 80ms entre elas).
- **Nome:** cada letra sobe de uma máscara, com 35ms entre letras e 120ms entre as duas linhas, curva com overshoot curto.
- **Frase de apoio:** entra 0,5s depois, subindo 12px.
- **Kicker:** ponto violeta pulsando a cada 2,6s.
- **Dica "Role":** linha vertical que se desenha e se apaga em loop. Some assim que a pessoa começa a rolar.

## 2. Entrada: o site se desenhando (scroll)

O progresso do scroll vai de 0 a 1 ao longo da entrada. Ele é suavizado (lerp com fator 0,12 normalizado pelo tempo), então o desenho continua assentando depois que o dedo para.

| Faixa do scroll | O que se desenha |
|---|---|
| 0,05 a 0,29 | Janela do navegador, barra superior, 3 bolinhas, barra de endereço |
| 0,27 a 0,39 | Logo (violeta), links do menu, botão do menu (violeta) |
| 0,35 a 0,57 | Duas barras de título, rótulo "Display · 64", linhas de texto, botão (violeta), imagem com X |
| 0,51 a 0,79 | Três cards, imagens internas, linhas de texto |
| 0,70 a 0,81 | Medidas em rosa: "900" na largura e "56" no espaçamento |
| 0,76 a 0,87 | Cursor entra pela direita em arco e para no card do meio |
| 0,82 a 0,90 | Card do meio acende em violeta |
| 0,86 a 0,95 | Anel rosa de clique se expande e some |
| 0,86 a 1,00 | O wireframe todo sobe 5% e encolhe 5%, abrindo espaço para a frase final |

**Textos sobre o desenho (bandas):**

| Banda | Faixa | Texto | Entrada |
|---|---|---|---|
| 1 | 0 a 0,30 | Nome + frase | Visível no início, sai subindo |
| 2 | 0,36 a 0,66 | Antes do pixel, a estrutura. | Foco: de desfocado para nítido, subindo 22px |
| 3 | 0,72 a 1,00 | Do rascunho ao produto. + Ver trabalhos | Mesmo foco, fica até o fim |

Rampas de entrada e saída de 0,06 do progresso; o resto é platô totalmente visível, para dar tempo de ler em roladas normais.

**Luz e véu:** a luz violeta da base cresce de 18% a 100% com o progresso. Um véu escuro à esquerda protege a leitura do nome e clareia depois de 0,25. No fim da entrada, um degradê funde a base do palco com o fundo da galeria, sem corte seco.

No celular, o desenho é uma tela de app (moldura de telefone, menu hambúrguer, cards empilhados, medida "208") e o "cursor" é um ponto de toque.

## 3. Galeria

- **Revelação:** cada case entra quando 18% dele aparece na tela. Sobe 70px, vem de um lado diferente (case 1 da esquerda, 2 da direita, 3 da esquerda), cresce de 96,5% e se abre por uma máscara de baixo para cima. 1,3s com saída rápida e assentamento lento.
- **Textos do case:** entram em cascata, 80ms entre cada item.
- **Parallax:** cada case flutua em velocidade diferente (+5%, -4%, +3%) conforme passa pela tela. Só no desktop.
- **Fio:** uma linha pontilhada liga os três cases pelo centro de cada imagem. Por cima, uma linha violeta se desenha conforme o avanço na galeria. Escondida no celular.
- **Luz ambiente:** cresce com o avanço na galeria.

## 4. Hover dos cases (assinatura)

Só em dispositivos com mouse:
- Card sobe 6px e cresce 1,2%, com overshoot curto.
- Borda fica mais forte, ganha sombra violeta.
- Luz violeta segue o cursor dentro da imagem.
- A ilustração cresce 4% e se desloca de leve na direção oposta ao cursor (profundidade).
- **Caixa de seleção estilo Figma:** contorno violeta, quatro alças nos cantos que surgem em sequência (40ms entre elas) e uma etiqueta com a medida real do card em pixels (ex.: "820 × 513").
- Título desliza 8px para a direita, ponto rosa aparece ao lado do número, seta de "Ver case" avança.
- **Clique:** anel rosa se expande a partir do ponto clicado.
- **"Acessar página":** sublinhado fica rosa, seta sobe na diagonal.

## 5. Transição para o contato

Disparada por qualquer link para `#contato` (hoje, o "Contato" da navegação). Duração total de cerca de 2 segundos.

1. **Tela vira wireframe (0 a 0,64s):** o JavaScript lê o que está visível e cria o contorno de cada elemento no lugar exato. Textos viram linhas (uma por linha real de texto), títulos grandes viram barras, cards viram contornos com um X rosa, botões e links de ação viram contornos violeta. O conteúdo real some com desfoque. As linhas se desenham de cima para baixo.
2. **Linhas se apagam (0,64 a 1,24s):** continuam o traço até sumir, sobem 28px e perdem opacidade.
3. **Troca de lugar invisível:** a página vai para o contato enquanto não há nada na tela.
4. **Contato se redesenha (até 1,94s):** o wireframe do contato surge subindo 24px e se desenha.
5. **Cor volta (até 2,44s):** o conteúdo real reaparece e as linhas somem. O foco do teclado vai para a seção de contato.

Com "reduzir movimento" ligado no sistema, vai direto para o contato.

## 6. Outros detalhes

- **Navegação:** some ao rolar para baixo, volta ao rolar para cima.
- **Troca de idioma:** a pílula clara desliza com overshoot; os textos somem com desfoque por 0,26s e voltam no outro idioma. A escolha fica salva no navegador.
- **Monograma:** gira 90° no hover.
- **Links do contato:** um fundo claro sobe de baixo e preenche a pílula; texto inverte de cor.
- **Aviso (toast):** pílula no rodapé da tela, entra com overshoot, some em 2,6s.

## 7. Desempenho

- Uma única malha de animação (requestAnimationFrame) para tudo.
- O DOM só é tocado quando um valor muda de verdade.
- Animações só em opacidade, transform e traço de SVG (nada que force relayout).
- O desenho do topo para de ser calculado quando o topo sai da tela.
