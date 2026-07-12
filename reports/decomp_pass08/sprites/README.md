# reports/decomp_pass08/sprites/

Saída completa do Pass 08 do processo de decompilação: catalogação dos "GOBJ" (game objects,
os objetos/sprites dinâmicos do jogo) e seus componentes visuais.

## Imagens

- `component_atlas_bank_88.png` até `component_atlas_bank_91.png` (10 arquivos) — atlases dos
  componentes de sprite de cada banco, extraídos da ROM. Complementam (com outro recorte/
  agrupamento) as spritesheets já presentes em `sprites/` na raiz do repositório.

## Dados/catálogos

- `gobj_sprite_catalog.{csv,json,md}` — catálogo de todos os GOBJ identificados, com endereço,
  banco e referências
- `component_graphics_map.{csv,json}` — mapa de qual componente gráfico pertence a qual GOBJ
- `replacement_candidates.md` — candidatos a substituição/consolidação de sprites duplicados
- `sprite_gobj_viewer.html` — visualizador HTML standalone pra navegar pelo catálogo

Ver `DISCLAIMER.md` na raiz do repositório para contexto sobre direitos autorais das imagens.
