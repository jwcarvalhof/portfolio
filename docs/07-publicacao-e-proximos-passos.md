# 07 · Publicação e próximos passos

## Checklist antes de publicar

- [ ] Trocar as imagens dos 3 cases (ver `06-como-editar.md`)
- [ ] Preencher categoria, título e descrição de cada case em PT e EN
- [ ] Trocar os links "Ver case" e "Acessar página" e remover os `data-placeholder`
- [ ] Trocar e-mail, LinkedIn e Instagram
- [ ] Criar a imagem de compartilhamento (`assets/og.jpg`, 1200×630) para quando o link for enviado no WhatsApp, LinkedIn etc.
- [ ] Trocar `https://SEU-DOMINIO/` nas tags `og:url` e `og:image` (procure `DEPLOY STEP` no topo do arquivo) pelo endereço final
- [ ] Abrir no celular e no computador e passar pela página inteira

## Como colocar no ar

O site é um arquivo HTML estático, sem build e sem servidor. Qualquer hospedagem estática serve. O pacote a enviar é:

```
index.html
assets/   (imagens dos cases e og.jpg)
```

Se for compactar em .zip, compacte o **conteúdo** da pasta (o `index.html` precisa ficar na raiz do zip), não a pasta em si.

## O que existe hoje

- Site no ar na Vercel: https://portfolio-pi-ecru-28.vercel.app
- Código no GitHub: https://github.com/jwcarvalhof/portfolio (branch `main`).
- A Vercel está ligada ao repositório: qualquer alteração salva na `main` publica uma nova versão sozinha.
- Página de pré-visualização privada no Claude (artifact), atualizada a cada mudança.
- A pasta `entrega` com o `index.html` final e a documentação.

## Ideias para depois

- Páginas de case individuais seguindo o mesmo sistema (wireframe, seleção, transição em linhas).
- Seção "Sobre" curta, se o briefing mudar (hoje a página é só galeria e contato).
- Vídeos curtos dos cases em vez de imagens estáticas, com reprodução só ao passar o mouse.
