# Last Asylum: Plague â€” verified client encyclopedia

Package com.phs.global, version 1.0.104. Built 2026-10-09T23:25:13.797564+00:00.

## Completed coverage

- All 876 marked resources decoded and accepted by Lua 5.4.
- 750 base tables and 253 English localization tables, totaling 123,853 records.
- 316 hero/NPC records; 14 records in the UR 50000â€“59999 ID range.
- 2,086 hero-skill variant records joined to Skill, SkillEffect and SkillState.
- Lua metatable defaults are resolved before export. Original XAPK and extracted resources remain unchanged.

## What is available

- Last-Asylum-Encyclopedia.html: offline hero dossiers and searchable complete table explorer.
- encyclopedia.json: joined hero dossiers, factions, formation, equipment and table catalog.
- UR-hero-dossiers.json: full UR skill variants, effects, states and awakening records.
- table-index.csv: complete system index.
- ../decoded-tables/last-asylum.sqlite: searchable table records.
- ../decoded-tables/json/: all extracted tables; ../decoded-tables/bytecode/: all decrypted chunks.
- ../decoded-tables/lua-source/: original 126 program files; ../client-code/source/: all 6,187 recovered program resources across 396 bundles, with syntax validation manifests.

## Factions and formation

- Hero Class: Ranger: Rangers take 20% less damage from Warriors (base damageSubPercent=0.2; restrainType=3).
- Hero Class: Warlock: Warlocks take 20% less damage from Rangers (base damageSubPercent=0.2; restrainType=1).
- Hero Class: Warrior: Warriors take 20% less damage from Warlocks (base damageSubPercent=0.2; restrainType=2).

Formation bonuses are +5% for three of one faction, +10% for a 3+2 split, +15% for four of one faction and +20% for five. Both numeric base records and localized descriptions agree.

## UR heroes

| ID | Hero | Faction | Skill variants | Awakening 20â†’30 | Awakening 30â†’40 |
|---|---|---|---:|---:|---:|
| 50001 | Daskal | Hero Class: Warrior | 21 | 670 | 1650 |
| 50002 | Harper | Hero Class: Warrior | 17 | 670 | 1650 |
| 50003 | Zoya | Hero Class: Warrior | 17 | 670 | 1650 |
| 50004 | Shadow | Hero Class: Ranger | 17 | 670 | 1650 |
| 50005 | Louis | Hero Class: Ranger | 21 | 670 | 1650 |
| 50006 | Cynthia | Hero Class: Ranger | 21 | 670 | 1650 |
| 50007 | Red Lady | Hero Class: Ranger | 17 | 670 | 1650 |
| 50008 | Bell | Hero Class: Ranger | 17 | 670 | 1650 |
| 50009 | Billy | Hero Class: Warlock | 17 | 670 | 1650 |
| 50010 | Ulfrid | Hero Class: Warlock | 21 | 670 | 1650 |
| 50011 | Annie | Hero Class: Warlock | 21 | 670 | 1650 |
| 50012 | Joker | Hero Class: Warlock | 17 | 670 | 1650 |
| 50013 | Nicole | Hero Class: Warlock | 17 | 670 | 1650 |
| 50020 | Claire | Hero Class: Warrior | 17 | Not configured | Not configured |

Costs sum current-level records [start, end). Recovered UIHeroAwakenPart._refreshUpgradeCost and upgrade handlers read curCfg.cost at the current awakening level. Unlocking awakening is a separate cost; the 0-to-10 subtotal does not include the unlock fee.

## Skill evidence

Every hero dossier preserves each star/awakening variant, unlock conditions, original parameter expression, localized description and direct Skill/SkillEffect/SkillState links. For example, Cynthia 50006 has separate awaken unlocks at 1, 10, 20 and 40; these must not be collapsed into one unawakened skill.

Recovered HeroUtils.getHeroSelectSlotImpDes uses heroObject:GetSkillLevel(slot) for n1 in param1/param2, selects the eligible star/hero-level/awakening variant, and evaluates the next level with skillLevel+1. UIHeroSkillUnlockPanel previews n1=1. These establish displayed skill parameters; runtime scaling, target selection, stacking order and the server combat implementation remain outside this static reference. Do not infer DPS or win rates from a description alone.

## Equipment and other systems

All base systems are indexed, including EquipmentBase/Promotion/Strengthen, HeroUniqueEquipment/Smelt, research, buildings, items, troop training, activities, guild systems, PvP and season content. Raw attribute types are retained and linked to DefineBenefit names where available.

## Verification and limitations

Extraction errors: 0. Direct missing Skill definitions in hero-skill joins: 0.
Record counts were checked against each base chunk's declared len. Source and decoded hashes are retained per resource. The final verifier checks JSON/SQLite coverage, inherited defaults, links and a fresh XAPK hash.
This completes the recovered client-data reference for this package. It does not imply every asset in the app, native engine method, live account or server-side formula has been reverse engineered. Decompiled scripts are reconstructed source; syntax validation is not a proof of behavioral equivalence.

## Decoder evidence

The literal eyugame_lua_zombiesrpg exists in stringliteral.json at 0x5740888. Repeating XOR using its UTF-8 bytes transforms 7e350006 into the complete standard Lua 5.4 header; the resulting chunks load successfully. The sample AbTestConfigs returns an ordinary table with data/len/key metadata. This structural validation supersedes earlier unresolved-loader notes.

## Reproduce

Run decode_all_tables.py, decompile_scripts.py, extract_client_code.py, decompile_client_code.py, build_encyclopedia.py and verify_completed_project.py using Python 3.12. Lupa is isolated under decoder-work/python-libs. Read the generated manifests rather than old failed handoffs.
