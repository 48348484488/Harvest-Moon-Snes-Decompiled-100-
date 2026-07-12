# tilemaps/

Tilemaps extraídos da ROM (66 arquivos, `Tilemap0x<endereço>.png`). Gerados com
`tools/TilemapDecomp.py`. O nome do arquivo é o endereço hexadecimal da tilemap dentro da ROM,
o que facilita cruzar com os catálogos em `reports/` e com o código em `src/`.

Cada imagem é o layout de tiles de uma tela/área do jogo (terrenos da fazenda, interiores de
casas, vila, mapas do mundo, etc.) — a "planta baixa" visual que o motor de renderização de
mapas (`docs/map_renderer_system/`) usa para montar a cena, remontada a partir dos índices de
tile + a paleta correspondente.

> Nota: estas são imagens da arte original do jogo, decodificadas do formato interno da ROM
> para PNG. Ver `DISCLAIMER.md` na raiz do repositório para contexto sobre direitos autorais.
