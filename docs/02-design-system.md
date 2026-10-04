# 02 · Design system

Tudo fica no bloco `:root` no topo do `<style>` dentro de `index.html`.

## Cores

| Token | Valor | Uso |
|---|---|---|
| `--canvas` | `#08070C` | Fundo. Preto com leve tom violeta, nunca `#000` puro |
| `--panel` | `#110F17` | Superfície dos cards |
| `--panel-2` | `#16131E` | Superfície elevada (aviso/toast) |
| `--line` | `#2A2535` | Bordas e divisórias discretas |
| `--line-strong` | `#4A4060` | Bordas interativas e sublinhados |
| `--accent` | `#8E6BFF` | Violeta: luz, foco, seleção, botões principais |
| `--accent-hover` | `#A68BFF` | Violeta no hover |
| `--accent-muted` | `rgba(142,107,255,.2)` | Violeta sussurrado |
| `--pink` | `#FF6FAE` | Rosa: só em momentos de interação (medidas, clique, hover de link, ponto do botão de e-mail) |
| `--text-primary` | `#EEEBF4` | Texto principal |
| `--text-secondary` | `#9A95A8` | Texto de apoio |

**Regra de dose:** o violeta é luz e ação; o rosa aparece em no máximo 2 ou 3 momentos por tela. Nada de gradiente decorativo, neon ou vidro exagerado.

## Tipografia

| Papel | Fonte | Pesos | Onde |
|---|---|---|---|
| Display | Bricolage Grotesque | 500, 600 | Nome, frases do scroll, títulos dos cases, frase do contato |
| Corpo | Geist | 400, 500 | Textos, botões, navegação |
| Utilitária | Geist Mono | 400 | Rótulos, números dos cases, categorias, medidas, rodapé |

Carregadas do Google Fonts com `preconnect`. Fallback para fontes de sistema.

**Escala principal**
- Nome: `clamp(52px, 11vw, 176px)`, peso 600, entrelinha .92, tracking -0.035em
- Frases do scroll: `clamp(34px, 6vw, 88px)`, peso 500
- Frase do contato: `clamp(40px, 7.4vw, 120px)`, peso 600
- Título do case: `clamp(26px, 3vw, 44px)`, peso 600
- Corpo: 15 a 20px
- Rótulos mono: 11 a 12px, caixa alta, tracking .08 a .14em

## Espaço e forma

- Margem lateral: `--gutter: clamp(16px, 4vw, 56px)`
- Largura máxima de conteúdo: 1440px
- Raio dos cards: 20 a 22px. Botões e pílulas: 999px (totalmente arredondados). Caixa de seleção: 3px (reta, como em ferramenta de design)
- Muito respiro vertical: seções com 10vh a 22vh de padding

## Curvas de animação (estilo Jitter)

Nenhum `ease-in-out` genérico. Quatro curvas desenhadas:

| Token | Curva | Sensação | Onde |
|---|---|---|---|
| `--ease-out` | `cubic-bezier(.16,1,.3,1)` | Sai rápido, assenta devagar | Entradas, revelações, fades |
| `--ease-snap` | `cubic-bezier(.34,1.45,.64,1)` | Overshoot curto, com personalidade | Hover dos cards, alças da seleção, botões, letras do nome |
| `--ease-inout` | `cubic-bezier(.76,0,.24,1)` | Troca de estado firme | Indicadores pulsantes |
| traço | `cubic-bezier(.65,0,.35,1)` | Desenho de linha natural | Transição do contato |

No scroll do topo, o desenho das linhas usa uma curva cúbica de entrada e saída em JavaScript, e o progresso do scroll é suavizado (lerp) para o desenho "assentar" depois do gesto.

## Camadas de ambiente (fixas atrás de tudo)

- **Luz ambiente:** brilho violeta radial na base da tela. Cresce em opacidade e escala conforme a pessoa avança na galeria. Tem uma respiração rosa quase invisível que cruza a tela em 64 segundos.
- **Grão:** textura de ruído a 6% de opacidade sobre a página inteira, para tirar o aspecto "digital limpo demais".

## Ícone e marca

Monograma "JC" com um ícone de dois círculos (violeta e claro) e um ponto rosa. O mesmo desenho é o favicon.
