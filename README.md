# Site de indicações

Página de "link na bio" para os vídeos: cada produto indicado tem um número (o mesmo que aparece no vídeo) e um botão para o link de afiliado. Fica hospedada de graça no GitHub Pages.

## Arquivos

- `index.html`: a página principal (produtos e canais)
- `privacidade.html`: política de privacidade
- `404.html`: página de "não encontrado"
- `estilo.css`: cores, fontes e layout

## Como editar pelo próprio GitHub

1. Abra o arquivo aqui no repositório e clique no lápis (**Edit this file**).
2. Faça a mudança.
3. Clique em **Commit changes**. O site atualiza sozinho em 1 ou 2 minutos.

## Colar o código do Google (o "pixel")

No `index.html`, procure por `COLE AQUI O CÓDIGO DO GOOGLE` e cole o código que o Google te deu entre as duas linhas marcadas.

Com o código instalado, o site já envia estes eventos para o Google:

- `clique_afiliado`: alguém clicou em "Ver o produto" (vai junto o número e o nome do produto)
- `busca_numero`: alguém achou um produto pelo número

Opcional: se você criar no Google Ads uma conversão para esses cliques, cole o `send_to` dela (exemplo: `AW-123456789/AbCdEfGhIjK`) em `CONVERSAO_CLIQUE`, no fim do `index.html`.

## Adicionar um produto

No `index.html`, copie um bloco `<article class="item" ...>` inteiro e troque:

- o número em `id="n04"`, `data-codigo="04"` e dentro de `<p class="codigo">`
- o nome no `<h3>` e a frase no `<p>` logo abaixo
- o `<span class="botao botao--espera">Link em breve</span>` por:

```html
<a class="botao" href="SEU-LINK-DE-AFILIADO" rel="sponsored nofollow">Ver o produto</a>
```

## Trocar o seu @, o e-mail e os canais

- Procure por `@seuperfil` nos arquivos e troque pelo seu.
- Em `privacidade.html`, troque `seuemail@exemplo.com` pelo seu e-mail.
- Na lista "Onde eu posto vídeos", troque cada `href="#"` pelo link do seu perfil.

## Mudar a cor

Em `estilo.css`, troque o valor de `--tela` (o azul). Troque também o `theme-color` no topo dos arquivos `.html`, que é a cor da barra do navegador no celular.
