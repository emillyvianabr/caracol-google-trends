# Dashboard Google Trends — Parque do Caracol

Dashboard estático para GitHub Pages, adaptado a partir do dashboard do Bondinho/Pão de Açúcar.

## O que muda em relação ao original

- **Cor principal:** verde `#004B13` (era laranja).
- **Recorte:** apenas o mercado **Brasil** (o dashboard original comparava vários países).
- **Dimensão comparada:** em vez de países, o filtro "Atração" compara três atrações do parque:
  - Bondinhos Aéreos
  - Skyglass
  - Pé da Cascata
- **Removido:** o mapa mundial (GeoMap), o radar de "novos mercados" e a seção "Cristo × Bondinho" (específicos do dashboard do Rio de Janeiro) não fazem sentido aqui e foram retirados. Em vez do ranking geográfico, a seção de comparação agora mostra o **ranking de interesse atual entre as 3 atrações**, além de variação anual, momentum e volatilidade — todos calculados entre as atrações.

## Dados

O arquivo `data.js` está com **dados fictícios/ilustrativos** (não reais do Google Trends) só para o dashboard funcionar visualmente, com 3 anos de histórico mensal para as 3 atrações.

Para dados reais, você precisa adaptar o script `scripts/atualizar.py` do repositório original: em vez de coletar o mesmo termo em vários países, ele passaria a coletar termos diferentes (um por atração) dentro do mercado Brasil, e gravar em `data/dados.xlsx` no mesmo formato de colunas (`data`, `mercado_codigo`, `mercado`, `indice_trends`) — aqui "mercado_codigo"/"mercado" representam a atração, não o país.

## Publicação

Envie `index.html`, `caracol-premium.css`, `caracol-premium.js` e `data.js` para a raiz de um repositório com GitHub Pages ativado.
