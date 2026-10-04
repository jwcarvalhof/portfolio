# 06 · Como editar

Abra `index.html` em qualquer editor de texto (VS Code recomendado). Use Ctrl+F para achar os trechos abaixo.

## Trocar um case

Procure `CASE 01` (ou 02, 03). Cada case tem um comentário com as instruções.

### 1. Imagem
Dentro do case, apague o bloco `<div class="case__ph" ...>...</div>` e coloque:

```html
<img src="assets/case-01.jpg" alt="Descrição curta da tela" loading="lazy" style="width:100%;height:100%;object-fit:cover">
```

Crie uma pasta `assets` ao lado do `index.html` e salve a imagem lá. Tamanhos ideais:
- Case 01 e 03: proporção 16:10, por exemplo 1600×1000
- Case 02: proporção 4:5 (vertical), por exemplo 1200×1500

Pode apagar também a etiqueta `<span class="case__tag" ...>imagem do projeto</span>`.

### 2. Textos
No fim do arquivo, no objeto `I18N`, edite as chaves do case nos **dois idiomas** (`pt` e `en`):

```js
c1cat:"Landing page", c1title:"Nome do projeto", c1desc:"Uma frase sobre o resultado.",
```

### 3. Links
No case, há dois links:
- `class="case__cta"` → "Ver case": troque `href="#"` pelo endereço do estudo de caso e **apague** `data-placeholder="case"`.
- `class="case__site"` → "Acessar página": troque `href="#"` pela URL publicada e **apague** `data-placeholder="site"`.

Enquanto o `data-placeholder` estiver lá, o clique mostra o aviso "em breve" em vez de navegar.

## Trocar o contato

Procure `CONTATO: troque` e edite:
- `mailto:seuemail@exemplo.com` → seu e-mail
- `https://www.linkedin.com/in/seu-perfil` → seu LinkedIn
- `https://www.instagram.com/seu-perfil` → seu Instagram

## Trocar textos gerais

Tudo está no objeto `I18N`. Edite sempre `pt` e `en`. Algumas frases usam `<br>` para quebrar linha e `<b>`, `<em>` ou `<span>` para destaque; mantenha essas marcas.

## Trocar cores

No topo do `<style>`, bloco `:root`. Exemplo: `--accent:#8E6BFF;` muda todo o violeta. Os SVGs dos placeholders e do monograma têm algumas cores escritas direto (`#8E6BFF`, `#FF6FAE`); troque também se mudar a paleta.

## Ajustar o ritmo da entrada

- Altura da entrada: `.hero{position:relative;height:260vh` (mais alto = animação mais lenta). No celular: `.hero{height:220vh}`.
- Quando cada parte se desenha: atributos `data-r=".35,.45"` em cada forma do SVG (início e fim, de 0 a 1).
- Quando cada frase aparece: `data-band="0.36,0.66"` nas divs `hero__band`.

## Adicionar mais links que usam a transição

Qualquer link com `href="#contato"` já usa a transição em linhas automaticamente.

## Idioma padrão

O site abre em português se o navegador da pessoa estiver em português, e em inglês nos outros casos. A escolha manual fica salva.
