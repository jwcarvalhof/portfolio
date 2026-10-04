# 03 · Estrutura e conteúdo

## Ordem da página

1. **Navegação fixa**: monograma JC (volta ao topo) · troca PT/EN · "Contato"
2. **Entrada** (260vh de scroll no desktop, 220vh no celular, com o palco fixo na tela)
3. **Galeria**: cabeçalho + 3 cases
4. **Contato**: frase + 3 links
5. **Rodapé**

## Textos em PT e EN

Todos os textos visíveis ficam no objeto `I18N`, no fim do `index.html`.

### Navegação e entrada

| Chave | Português | Inglês |
|---|---|---|
| `navContact` | Contato | Contact |
| `kicker` | UX/UI · Web Design | UX/UI · Web Design |
| (nome) | Jhonatan Carvalho | Jhonatan Carvalho |
| `sub` | Faço o complicado parecer **óbvio**. | I make the complicated feel **obvious**. |
| `band2` | Antes do pixel, a estrutura. | Structure before pixels. |
| `band3` | Do rascunho ao produto. | From sketch to shipped. |
| `seeWork` | Ver trabalhos | See the work |
| `scroll` | Role | Scroll |
| `skip` | Pular para os trabalhos | Skip to the work |

Alternativas de copy guardadas para a banda 3: "Do traço à tela." ou "Agora, a parte boa."

### Galeria

| Chave | Português | Inglês |
|---|---|---|
| `workLabel` | Trabalhos selecionados | Selected work |
| `workTitle` | Três projetos, *escolhidos a dedo.* | Three projects, *handpicked.* |
| `phTag` | imagem do projeto | project image |
| `seeCase` | Ver case | View case |
| `visitSite` | Acessar página | Visit live page |
| `c1cat` / `c1title` / `c1desc` | Categoria · Projeto 01 · Case em revisão final. Vale a espera. | Category · Project 01 · Final review in progress. Worth the wait. |
| `c2cat` / `c2title` / `c2desc` | Categoria · Projeto 02 · Ainda no forno. Cheiro bom, né? | Category · Project 02 · Still in the oven. Smells good, right? |
| `c3cat` / `c3title` / `c3desc` | Categoria · Projeto 03 · Esse aqui está tímido. Em breve. | Category · Project 03 · This one is shy. Coming soon. |
| `toast` | Esse case ainda está no forno. Volta logo! | This case is still in the oven. Come back soon! |
| `toastSite` | Essa página entra no ar em breve. | This page goes live soon. |

### Contato e rodapé

| Chave | Português | Inglês |
|---|---|---|
| `contactLabel` | Contato | Contact |
| `contactLine` | Gostou do que viu? *Vamos conversar.* | Like what you see? *Let's talk.* |
| `email` | Mandar um e-mail | Send an email |
| (links) | LinkedIn · Instagram | LinkedIn · Instagram |
| (rodapé) | © 2026 Jhonatan Carvalho | © 2026 Jhonatan Carvalho |
| `foot` | Feito à mão, pixel por pixel. | Handmade, pixel by pixel. |
| `backTop` | Voltar ao topo ↑ | Back to top ↑ |

## Anatomia de um case

Cada case tem, de cima para baixo:

1. **Mídia** (16:10 nos cases 1 e 3, 4:5 vertical no case 2, ideal para telas de app). Hoje: ilustração placeholder em SVG + etiqueta "imagem do projeto".
2. **Número** em mono (01, 02, 03) com um ponto rosa que aparece no hover.
3. **Categoria** em mono violeta.
4. **Título** em display.
5. **Descrição** curta.
6. **Ações:** "Ver case →" (o card inteiro também leva ao case) e "Acessar página ↗" (texto fino sublinhado, abre a página publicada em outra aba).

## Composição da galeria (eixo invisível)

| Case | Desktop | Tablet | Celular |
|---|---|---|---|
| 01 | 62% de largura, a 4% da esquerda | 72%, encostado à esquerda | 90%, à esquerda |
| 02 | 46%, à direita (3% da borda), descido 6vh | 58%, à direita | 80%, à direita |
| 03 | 56%, a 20% da esquerda, 14vh abaixo | 70%, a 12% | 88%, a 5% |

Placeholders diferentes para cada case: anéis concêntricos (01), tela de app (02), fluxo de telas (03). Sem inventar projetos.

## Regras de copy

- Sem travessões longos, sem palavras genéricas de marketing.
- Frases curtas, que cabem em uma rolada.
- Humor leve só nos estados vazios e avisos, nunca na estrutura.
