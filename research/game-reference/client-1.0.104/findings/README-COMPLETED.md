# Last Asylum: Plague project — completed static client reference

Authoritative package: com.phs.global 1.0.104.
The decoder blocker is resolved. Earlier FAILED/INCOMPLETE checkpoints are historical.
Open encyclopedia/Last-Asylum-Encyclopedia.html or the desktop Last Asylum Encyclopedia shortcut.

Completed:
- 750 base and 253 English tables, 123,853 records, zero extraction errors.
- 6,187 decoded program resources across 396 bundles; all reconstructed sources pass Lua 5.4 syntax checks.
- 316 hero/NPC records, 14 UR dossiers, 2,086 hero-skill variants, zero missing direct Skill definitions.
- Effective Lua metatable defaults, localized names, skill/effect/state links, progression costs, equipment and all table systems.
- Current-level awakening-cost indexing verified in UIHeroAwakenPart. Cynthia 30 to 40 = 1,650.
- HeroUtils display parameters substitute n1 with the skill level; unlock preview uses 1.
- Fresh XAPK hash, source/decoded hashes, declared table counts, SQLite integrity and source syntax checked.

Evidence and use:
- encyclopedia/Last-Asylum-Report.md: conclusions, provenance and scope.
- encyclopedia/final-verification.json: final check results.
- decoded-tables/manifest.json, last-asylum.sqlite, json/: full data.
- client-code/manifest.json, decompilation.json, source/: full recovered Lua code.
- Standalone Qwen launcher uses this folder; Hermes is not needed for it.

Completion means the recovered static client reference for this package.
Live account behavior, server logic and a full combat/DPS simulator are not validated.
Decompiled source is reconstructed and syntax validity does not prove behavioral equivalence.


## LDPlayer capture
Latest snapshot: C:\Users\Nocturnal\LocalAI\last-asylum-analysis\live-data\LDPlayer-20261010T011131Z
Installed APK version: 1.0.104. Root verified. Installed APKs and private/external/OBB files collected and hashed.
Account state is not yet fully decoded; snapshot may contain account credentials and is kept separate from public reference archive. See structure-review.json.
