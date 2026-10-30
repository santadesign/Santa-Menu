# Cardápio digital global

## Como funciona
- `index.html` é o cardápio único (layout, carrinho, WhatsApp).
- Cada cliente = 1 arquivo em `restaurantes/NOME.json`.
- Acesse: `https://SEU-USUARIO.github.io/SEU-REPO/?r=NOME`
  (ou `.../#NOME`). Sem parâmetro, abre `demo`.

## Publicar no GitHub Pages
1. Suba esta pasta num repositório (index.html na raiz).
2. Settings > Pages > Deploy from a branch > `main` / root.
3. Para um novo cliente: copie `restaurantes/demo.json`, renomeie (ex.: `pizzariax.json`), edite e envie.

## Campos do JSON
- nome, slogan, logo, capa (URLs ou caminhos como `img/logo.png`), whatsapp (DDI+DDD+número, só dígitos)
- tema: primaria, secundaria, fundo, texto, fonte_titulo (qualquer fonte do Google Fonts)
- endereco, mapa_url, mapa_embed (opcional: link "Incorporar mapa" do Google Maps)
- horarios: seg..dom -> "18:00-23:00", lista ["12:00-15:00","18:00-23:00"] ou null (fechado). Pode passar da meia-noite.
- categorias[].itens[]: nome, descricao, preco, preco_promocional (opcional), promocao (true), selo, imagem
  - sem `imagem` = o item aparece sem foto
  - itens com preco_promocional ou promocao:true entram sozinhos na aba "Promoções"
