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

## Código do Google (Tag Manager)

O Google Tag Manager (`GTM-KSKP7QSQ`) já está instalado no topo de todas as páginas, entre as linhas `CÓDIGO DO GOOGLE` e `FIM DO CÓDIGO DO GOOGLE`. Pixels novos (Google Ads, Google Analytics, Meta, TikTok) você adiciona dentro do Tag Manager e publica lá, sem mexer no site.

O site envia estes eventos para o Tag Manager:

- `clique_afiliado`: alguém clicou em "Ver o produto" (vão junto `codigo`, `produto` e `link_url`)
- `busca_numero`: alguém achou um produto pelo número (vão junto `codigo` e `produto`)

Para usar um deles, crie no Tag Manager um acionador do tipo **Evento personalizado** com o nome do evento (por exemplo, `clique_afiliado`) e ligue esse acionador à tag de conversão.

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
