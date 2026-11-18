# Licence notice — YUNG's Better Witch Huts (Horizon port)

This package is a port of **YUNG's Better Witch Huts** by **YUNGNICKYOUNG** and
**Acarii** (`com.yungnickyoung.minecraft.betterwitchhuts`), and it carries that
mod's structure data: its structure sets, pools, processor lists, structure
templates, loot table, biome and structure tags and language files.

- **Upstream licence: GNU Lesser General Public License v3.0 only**
  (`META-INF/neoforge.mods.toml` → `license="LGPLv3"`; the jar ships the full
  LGPL-3.0 text as `LICENSE_YungsBetterWitchHuts`; Modrinth project
  `t5FRdP87` → `LGPL-3.0-only`).
- A verbatim copy of that text travels with this port as `LICENSE` (and inside
  the built `.hmod` as `assets/betterwitchhuts/license.txt`, because a package
  holds `assets/` and `data/` only and its paths are lower case).
- This port is distributed under the **same licence** (LGPL-3.0-only). The
  complete corresponding source — this content root, `tools/carry_content.py`
  and `notes.md` — travels with it.
- Upstream: <https://github.com/YUNG-GANG/YUNGs-Better-Witch-Huts>
  (branch `1.21.1`; the analysed jar is recorded in `notes.md` with its SHA-256).

## What this port changes

The files are copied from the 1.21.1 NeoForge jar, byte for byte, except:

- `data/betterwitchhuts/worldgen/processor_list/main.json` — the mod's five
  processors are Java classes with no JSON fields; two are carried as
  `horizon:yung_pillar` (the game's implementation of YUNG's pillar
  processors), the witch-circle and potted-mushroom ones as `horizon:pick` and
  `horizon:yung_pillar`, and the brewing-stand one is dropped (recorded as a
  gap in `notes.md`);
- `data/betterwitchhuts/loot_table/chests/hut_0.json` — rewritten to 26.3's
  loot shape (`modifier`/`type`, fully qualified component ids);
- `data/morevillagers/tags/worldgen/structure/on_swamp_hut_explorer_maps.json`
  is left out: it is another mod's namespace.

`notes.md` records every change with its evidence.
