# Last Asylum: Plague v1.0.104 → v1.0.106 Changes

**Extraction Date:** 2026-10-23
**Source:** APKMirror APKM `com.phs.global_1.0.106-106_1arch_24lang_1feat_d29ac148b4aeffa7896c4ea37625597e_apkmirror.com.apkm`

## Summary

| Metric | v1.0.104 | v1.0.106 | Change |
|--------|----------|----------|--------|
| Base Tables | 750 | 790 | +40 |
| New Tables | - | 40 | - |
| Removed Tables | 0 | - | -0 |
| Tables with Row Changes | - | 67 | - |
| Total Differing Rows | - | 10347 | - |

## New Content Categories

### ActivitySquadBattle (17 tables)
New squad-based PvP/guild battle system with coordinates, forts, zones, stages, matchmaking, rankings, prohibits, records.

- ActivitySquadBattleBlock (4 rows)
- ActivitySquadBattleCoordinate (20 rows)
- ActivitySquadBattleDescription (7 rows)
- ActivitySquadBattleFort (15 rows)
- ActivitySquadBattleFortPrototype (4 rows)
- ActivitySquadBattleMessage (9 rows)
- ActivitySquadBattleParameter (40 rows)
- ActivitySquadBattlePersonalAchievement (18 rows)
- ActivitySquadBattlePersonalReward (6 rows)
- ActivitySquadBattlePlayerIntegralSource (20 rows)
- ActivitySquadBattleProhibit (14 rows)
- ActivitySquadBattleRank (5 rows)
- ActivitySquadBattleRankNew (13 rows)
- ActivitySquadBattleRecord (7 rows)
- ActivitySquadBattleStage (1 rows)
- ActivitySquadBattleTime (3 rows)
- ActivitySquadBattleZone (11 rows)

### Monopoly (8 tables)
Halloween-themed board game event with 26 cells, dice mechanics, token `halloween_raffle_ticket`, lucky box rewards.

- MonopolyBase (1 rows)
- MonopolyBoardEvent (5 rows)
- MonopolyCell (26 rows)
- MonopolyCellLevel (76 rows)
- MonopolyDrawWeightShow (2 rows)
- MonopolyEventGift (24 rows)
- MonopolyEventGiftGroup (12 rows)
- MonopolySpecialTreasure (4 rows)

### Volcano (12 tables)
Volcanic resource gathering event with 9 reward tiers, stages, resource refresh cycles, server groupings, ranking rewards.

- VolcanoActivityReward (9 rows)
- VolcanoConfig (1 rows)
- VolcanoGteItem (4 rows)
- VolcanoGuide (4 rows)
- VolcanoModelConfig (15 rows)
- VolcanoRankingReward (15 rows)
- VolcanoResource (3 rows)
- VolcanoResourceRefresh (5 rows)
- VolcanoResourceTime (57 rows)
- VolcanoServerGroup (6 rows)
- VolcanoStage (5 rows)
- VolcanoSystemDesc (11 rows)

### Other (3 tables)
- ActivitySquadMatchTime (10 rows)
- ActivitySquadMatchWinRate (7 rows)
- ConditionReward (72 rows)

## Top Changed Tables (by row differences)

| Table | v104 Rows | v106 Rows | Added | Removed | Diff Rows |
|-------|-----------|-----------|-------|---------|-----------|
| SlgMonsterAttr | 4879 | 4879 | 0 | 0 | 4879 |
| SlgArmyAttr | 2254 | 2254 | 0 | 0 | 2254 |
| GiftBase | 1626 | 1732 | 106 | 0 | 1626 |
| Item | 1600 | 1618 | 18 | 0 | 389 |
| CollegeTech | 348 | 348 | 0 | 0 | 348 |
| MiniEliminateMasterPassFloor | 234 | 468 | 234 | 0 | 234 |
| ActivityDisplay | 210 | 220 | 10 | 0 | 210 |
| WorldPlayerBirth | 100 | 100 | 0 | 0 | 64 |
| MapSkinInfo | 63 | 67 | 4 | 0 | 63 |
| BattlePass | 46 | 48 | 2 | 0 | 46 |
| LordJobSkill | 44 | 44 | 0 | 0 | 44 |
| RadarTreasure | 37 | 37 | 0 | 0 | 37 |
| BuildingLevel | 1318 | 1332 | 14 | 0 | 31 |
| DropInfo | 1720 | 1802 | 82 | 0 | 21 |
| MiniEliminateMasterPass | 20 | 40 | 20 | 0 | 20 |
| ArenaActivityShop | 18 | 18 | 0 | 0 | 18 |
| ExchangeShop | 294 | 293 | 0 | 1 | 14 |
| WarZoneConf | 11 | 11 | 0 | 0 | 11 |
| ActivityGetItem | 39 | 39 | 0 | 0 | 5 |
| Parameter | 836 | 841 | 5 | 0 | 5 |

## Notable Changes

1. **GiftBase** (1,626 rows differ) — Major shop/pack restructuring
2. **CollegeTech** (348 rows differ) — Tech tree updates  
3. **ActivityDisplay** (210 rows differ) — Event UI/visibility changes
4. **Item** (389 rows differ) — Item stats/effects modifications
5. **MiniEliminateMasterPassFloor** (234 rows differ) — Minigame progression updates

## Unchanged Core Systems

- **HeroInfo** (316 heroes) — No new heroes, no stat changes
- **HeroSkillBase / NewHeroSkill** — No skill changes
- **Unit/combat tables** — No balance changes detected
- **UR hero roster** — Identical to v1.0.104

## Files Generated

- `tables-json/` — 790 JSON files (one per base table)
- `tables-csv/` — 790 CSV files + `00-TABLE-INDEX.csv`
- `findings/v104-to-v106-changes.json` — Full diff data
- `index.json` — File index with paths and sizes
