# 05 · Responsividade e acessibilidade

## Pontos de quebra

| Faixa | O que muda |
|---|---|
| Acima de 1024px (desktop) | Composição completa: galeria assimétrica, parallax, fio entre cases, hover com seleção |
| 641 a 1024px (tablet) | Cases mais largos, deslocamentos menores, mesma lógica de eixo |
| Até 640px (celular) | Wireframe vira tela de app; entrada mais curta (220vh); cases em uma coluna com larguras e alinhamentos alternados; fio escondido; links de contato ocupam a largura |
| Altura até 520px | Dica "Role" escondida para não colidir com o texto |

No celular, a assimetria continua: 90% à esquerda, 80% à direita, 88% recuado. Nada de carrossel lateral. A página nunca rola para o lado.

## Toque

- Hover é só um extra. Número, categoria, título, descrição e os dois links ficam sempre visíveis.
- Áreas de toque de pelo menos 44px em botões, links de contato, troca de idioma e navegação.

## Acessibilidade

- **Link "Pular para os trabalhos"** aparece ao navegar por teclado.
- **Estrutura semântica:** `nav`, `header`, `main`, `section`, `footer`, títulos em ordem (h1 nome, h2 seções, h3 cases).
- **Foco visível** em violeta em todos os elementos interativos. No card, o foco do "Ver case" contorna a imagem inteira.
- **Decorações escondidas de leitores de tela:** wireframe, luz, grão, seleção e transição têm `aria-hidden`.
- **Nome:** lido como "Jhonatan Carvalho" mesmo animado letra por letra.
- **Avisos** anunciados por `role="status"`.
- **Idioma:** o atributo `lang` da página troca entre `pt-BR` e `en`.
- **Contraste:** texto principal `#EEEBF4` e de apoio `#9A95A8` sobre `#08070C`, ambos acima de 4,5:1.
- **Movimento reduzido:** com a preferência do sistema ligada, o wireframe aparece completo e parado, os cases aparecem sem animação, parallax, fio e transição do contato ficam desligados. Funciona também se a pessoa ligar a preferência com a página aberta.

## Testes feitos

- Capturas em 1440×900 e 375×812, nas três fases da entrada, na galeria e no hover.
- Transição do contato saindo da galeria, sem erros no console.
- Largura de rolagem igual à largura da tela nos dois tamanhos (sem rolagem lateral).
- Verificação de texto: zero travessões e zero palavras genéricas de marketing.
