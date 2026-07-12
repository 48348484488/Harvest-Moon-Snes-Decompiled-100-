# ⚠️ Aviso Legal / Disclaimer

Este é um projeto de engenharia reversa de código aberto criado **estritamente para fins
educativos, pesquisa acadêmica e preservação histórica** da arquitetura de software da era
dos 16-bits (SNES, 1997).

## O que este repositório NÃO contém

- 🛑 **Nenhuma ROM comercial.** O projeto nunca incluiu e nunca incluirá arquivos `.sfc`,
  `.smc`, `.fig`, `.swc` ou qualquer dump binário do cartucho original.
- 🛑 **Nenhum áudio/música original.**

## O que este repositório CONTÉM (incluindo material sensível)

- Código assembly 65816 re-implementado/documentado através de *clean-room design* e tradução
  reversa.
- Ferramentas, documentação técnica e catálogos de dados textuais (nomes de labels, endereços
  de memória, estruturas de dados, referências cruzadas) produzidos durante o processo de
  análise.
- **Gráficos extraídos da ROM**: os diretórios `sprites/`, `tilemaps/` e
  `reports/decomp_pass08/sprites/` contêm imagens PNG geradas pelas ferramentas de extração
  (`tools/BitplaneToPng.py`, `tools/TilemapDecomp.py`, `tools/SpriteDecompressor.py`) a partir
  dos dados de tile da ROM. **Isso é a arte original do jogo** — personagens, tiles de mapa e
  atlases de sprite — apenas decodificada do formato interno da ROM para um formato de imagem
  legível. Decodificar não transforma o conteúdo em algo diferente do original; é a mesma
  arte, só num container diferente.

  Essa inclusão foi uma decisão deliberada de quem mantém este repositório, tomada com
  conhecimento de que esse material é protegido por direitos autorais da Marvelous Inc./Natsume
  e de que publicá-lo publicamente carrega risco de notificação de remoção (DMCA) ou outra ação
  do detentor dos direitos. Quem clona, faz fork ou redistribui este repositório assume esse
  mesmo risco.

## Validação de build

O código foi validado localmente (fora deste repositório) fazendo rebuild byte-perfect contra
uma ROM USA limpa (MD5 `c9bf36a816b6d54aed79d43a6c45111a`) — ver histórico em
[`decomp_process_log/`](./decomp_process_log). Para compilar e testar você mesmo, precisa
fornecer sua própria cópia legalmente adquirida da ROM (ver [`BUILD_GUIDE.md`](./BUILD_GUIDE.md)).

## Uso Aceitável

O objetivo declarado deste projeto é interoperabilidade, pesquisa e estudo educacional, sem
intenção comercial ou de lucro. Isso **não é uma garantia legal** de que o projeto está
protegido por "fair use" — fair use é uma defesa avaliada caso a caso por um tribunal, não algo
que um projeto possa simplesmente declarar sobre si mesmo. Isso vale ainda mais para os
gráficos extraídos listados acima, que são uma reprodução direta da arte original, não uma
reimplementação de lógica. Quem mantém e quem usa este repositório deve entender que isso
existe numa área juridicamente cinzenta (o código) a diretamente arriscada (os gráficos), e
agir de acordo com o próprio julgamento de risco.

A propriedade intelectual, o título "Harvest Moon" (atualmente "Story of Seasons"), os
personagens e conceitos pertencem exclusivamente à Marvelous Inc., Natsume e respectivos
detentores de direitos.

## Terceiros

O diretório [`third_party/`](./third_party) contém o código-fonte do assembler
[asar](https://github.com/RPGHacker/asar), ferramenta de terceiros open source usada para
montar o código assembly — licença própria incluída no zip.
