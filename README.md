# 🌾 Harvest Moon (SNES, 1997) — Decompilação / Engenharia Reversa

Projeto de engenharia reversa em código aberto do *Harvest Moon* original de SNES (1997),
com foco em documentar e reconstruir a lógica do jogo (código 65816, sistemas de simulação
agrícola, event scripts, NPCs, etc.) para fins educacionais e de preservação histórica.

> ⚠️ **Leia o [`DISCLAIMER.md`](./DISCLAIMER.md) antes de usar o projeto.** Este repositório
> **não contém a ROM do jogo** nem gráficos/áudio extraídos dela. Veja detalhes abaixo em
> "O que NÃO está incluído".

## 📂 Estrutura do repositório

| Pasta | O que tem |
|---|---|
| [`src/`](./src) | Código-fonte em assembly 65816, organizado por banco de ROM (`code_banks/`, `data_banks/`, `constants/`, `maps/`) — o núcleo reconstruído do jogo |
| [`tools/`](./tools) | ~60 scripts Python usados para extrair, analisar e descompilar dados da ROM (descompressão de gráficos, decodificador de texto, catálogos de itens, etc.) + o assembler `asar` |
| [`docs/`](./docs) | Documentação técnica de cada sistema do jogo (agricultura, NPCs, save, menus, texto, etc.), pseudocódigo e material de onboarding |
| [`sprites/`](./sprites) | Atlases de sprite dos personagens extraídos da ROM, um por banco de gráficos (10 arquivos) |
| [`tilemaps/`](./tilemaps) | Tilemaps das telas/mapas do jogo extraídos da ROM (66 arquivos) |
| [`reports/`](./reports) | Catálogos de dados gerados pelas ferramentas (CSV/JSON/MD/HTML) — itens, mapas, diálogos, e também os atlases de componentes de sprite em `reports/decomp_pass08/sprites/` |
| [`patches/`](./patches) | Diffs aplicados durante o processo de renomeação/organização de labels |
| [`examples/`](./examples) | Exemplos pontuais de edição de texto/patches |
| [`decomps/`](./decomps) | Arquivos de labels/símbolos para debuggers (Mesen), formato `.diz`/`.xml` |
| [`decomp_process_log/`](./decomp_process_log) | Histórico bruto do processo de decompilação (37 "passes" de progresso, 37 relatórios de validação de build, logs de build, relatórios de status) — mantido para transparência e reprodutibilidade, **não é leitura necessária** para quem só quer usar o código |
| [`third_party/`](./third_party) | Código-fonte do assembler [asar](https://github.com/RPGHacker/asar) (ferramenta de terceiros, open source) |
| `BUILD_GUIDE.md` | Como compilar o projeto |
| `MODDING_GUIDE.md` | Como modificar/hackear o jogo usando este código |

## ✅ O que ESTÁ incluído

- Código assembly 65816 reconstruído (74 arquivos `.asm`, todos os bancos de código e dados)
- Ferramentas de extração/análise (Python) usadas para gerar o código a partir da ROM
- Documentação técnica de ~39 sistemas do jogo
- Catálogos de dados em texto (CSV/JSON) — nomes, endereços, estruturas, referências cruzadas
- Histórico completo do processo de decompilação (passes incrementais)
- **Gráficos extraídos da ROM**: sprites de personagens (`sprites/`), tilemaps de mapas
  (`tilemaps/`) e atlases de componentes de sprite (`reports/decomp_pass08/sprites/`) — arte
  original do jogo, decodificada do formato interno da ROM para PNG. Ver `DISCLAIMER.md` para
  o que isso implica em termos de direitos autorais.

## ❌ O que NÃO está incluído

- **A ROM do jogo** — nunca esteve no repositório
- **Áudio/música original**
- Duas pastas de snapshot antigas/duplicadas do zip original (`source_decompilada/` e cópias
  soltas de `docs/`, `reports/`, `tools/`, `logs/` na raiz) — eram versões redundantes e
  desatualizadas do que já está em `src/`, `docs/`, `reports/`, `tools/` aqui

## 🔨 Build rápido

Veja [`BUILD_GUIDE.md`](./BUILD_GUIDE.md) para o passo a passo completo (requer `asar` — já
incluso em `tools/bin/`, e sua própria ROM legalmente adquirida).

```bash
./build_linux.sh    # Linux
build_windows.bat   # Windows
```

## 📜 Licença / Uso

Veja [`DISCLAIMER.md`](./DISCLAIMER.md).
