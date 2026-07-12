# sprites/

Atlases de sprite extraídos da ROM, um arquivo por banco de gráficos (10 arquivos,
`bank_88.png` até `bank_91.png`). Gerados com `tools/BitplaneToPng.py` /
`tools/SpriteDecompressor.py` a partir dos dados de tile comprimidos da ROM.

Cada imagem é uma folha de sprites (spritesheet) com os frames de animação dos personagens
daquele banco — ciclos de caminhada em várias direções, poses e variações usadas pelo jogo em
tempo de execução.

| Arquivo | Banco de origem |
|---|---|
| `bank_88.png` | `src/data_banks/bank_88.asm` |
| `bank_89.png` | `src/data_banks/bank_89.asm` |
| `bank_8A.png` | `src/data_banks/bank_8A.asm` |
| `bank_8B.png` | `src/data_banks/bank_8B.asm` |
| `bank_8C.png` | `src/data_banks/bank_8C.asm` |
| `bank_8D.png` | `src/data_banks/bank_8D.asm` |
| `bank_8E.png` | `src/data_banks/bank_8E.asm` |
| `bank_8F.png` | `src/data_banks/bank_8F.asm` |
| `bank_90.png` | `src/data_banks/bank_90.asm` |
| `bank_91.png` | `src/data_banks/bank_91.asm` |

> Nota: estas são imagens da arte original do jogo, decodificadas do formato interno da ROM
> para PNG. Ver `DISCLAIMER.md` na raiz do repositório para contexto sobre direitos autorais.
