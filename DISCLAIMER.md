# ⚠️ Aviso Legal / Disclaimer

Este é um projeto de engenharia reversa de código aberto criado **estritamente para fins
educativos, pesquisa acadêmica e preservação histórica** da arquitetura de software da era
dos 16-bits (SNES, 1997).

## O que este repositório NÃO contém

- 🛑 **Nenhuma ROM comercial.** O projeto nunca incluiu e nunca incluirá arquivos `.sfc`,
  `.smc`, `.fig`, `.swc` ou qualquer dump binário do cartucho original.
- 🛑 **Nenhum gráfico extraído da ROM.** Durante o processo de engenharia reversa, as
  ferramentas de extração (`tools/BitplaneToPng.py`, `tools/TilemapDecomp.py`, etc.) *foram*
  usadas para decodificar sprites e tilemaps da ROM em PNG, como passo intermediário de análise
  — isso é dito aqui com todas as letras porque essas imagens chegaram a existir localmente
  durante o desenvolvimento. Elas foram deliberadamente removidas antes da publicação deste
  repositório, pois são a arte original do jogo, apenas decodificada para um formato legível —
  não deixam de ser um recurso protegido por isso. As ferramentas continuam em `tools/` caso
  você queira gerar essas imagens a partir da sua própria cópia legal da ROM.
- 🛑 **Nenhum áudio/música original.**

## O que este repositório contém

Código assembly 65816 re-implementado/documentado através de *clean-room design* e tradução
reversa, além de ferramentas, documentação técnica e catálogos de dados textuais (nomes de
labels, endereços de memória, estruturas de dados, referências cruzadas) produzidos durante o
processo de análise. Nada disso reproduz a arte, o áudio ou o texto narrativo original do jogo.

## Validação de build

O código foi validado localmente (fora deste repositório) fazendo rebuild byte-perfect contra
uma ROM USA limpa (MD5 `c9bf36a816b6d54aed79d43a6c45111a`) — ver histórico em
[`decomp_process_log/`](./decomp_process_log). Para compilar e testar você mesmo, precisa
fornecer sua própria cópia legalmente adquirida da ROM (ver [`BUILD_GUIDE.md`](./BUILD_GUIDE.md)).

## Uso Aceitável

O objetivo declarado deste projeto é interoperabilidade, pesquisa e estudo educacional, sem
intenção comercial ou de lucro. Isso **não é uma garantia legal** de que o projeto está
protegido por "fair use" — fair use é uma defesa avaliada caso a caso por um tribunal, não algo
que um projeto possa simplesmente declarar sobre si mesmo. Quem mantém e quem usa este
repositório deve entender que engenharia reversa de jogos comerciais existe numa área
juridicamente cinzenta, e agir de acordo com o próprio julgamento de risco.

A propriedade intelectual, o título "Harvest Moon" (atualmente "Story of Seasons"), os
personagens e conceitos pertencem exclusivamente à Marvelous Inc., Natsume e respectivos
detentores de direitos.

## Terceiros

O diretório [`third_party/`](./third_party) contém o código-fonte do assembler
[asar](https://github.com/RPGHacker/asar), ferramenta de terceiros open source usada para
montar o código assembly — licença própria incluída no zip.
