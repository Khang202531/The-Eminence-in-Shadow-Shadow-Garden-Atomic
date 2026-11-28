# 🌑 The Eminence in Shadow: Shadow Garden & Atomic — Official English Wiki

<div align="center">
<img src="../docs/images/icon.png" alt="Shadow Garden Icon" width="140" />

**Welcome to the Official English Strategy & Technical Specification Wiki for _The Eminence in Shadow: Shadow Garden & Atomic_ (`v1.0.8` — Forge 1.20.1 / NeoForge 1.21.1)!**

🌐 **Language / 言語切替**: **[🇯🇵 日本語 Wiki (Switch to Japanese)](Home.md)** ｜ **🇺🇸 English Wiki (Current)**
</div>

---

## What's new in 1.0.8

- **Demon Sword: Bloodfang (`fenrir_katana`) Overhaul**: Rebuilt as a towering fiery crimson odachi (`+1.55` reach) with corrected upper-edge curvature across first-person and third-person views.
- **Lambda's Black Whip (`lambda_whip`) & Eta's Slime Eruption Skill**: Added `lambda_whip` (pulling slime spears + Bleed/Blindness lashes & ally heal/buffs), Eta's 6th skill (*Slime Eruption: Falling Blades*) and matching boss AI attack, plus increased red mana orbs and outer glow halos for Aurora.
- **Dimension Travel Mana & Disguise Fix**: Fixed `PlayerManaProvider` capability invalidation across dimension travel, End return, and death respawn so max MP scaling and `V`-key Slime Suit disguise persist reliably.
- **Ergonomic WCAG AAA HUD & Canon Localization**: Overhauled the HUD with >= 7:1 contrast, non-overlapping responsive layout above `ChatScreen` and offhand/subtitles, softer edge vignettes, and unified EN/JA canon terminology.

[Installation](01-Getting-Started-and-Controls-EN.md) | [Zenith Atomic](04-I-Am-Atomic-EN.md) | [Weapon stats](05-Weapons-and-Artifacts-EN.md) | [Boss guide](06-Bosses-and-Companions-EN.md)

---

## 🧭 English Wiki Chapters Navigation

> 🇯🇵 日本語のWikiページ一覧は **[日本語 Wiki ホーム (`Home.md`)](Home.md)** をご覧ください。

| Chap. | English Page Link | Japanese Page Link | Contents Overview |
| :-: | :--- | :--- | :--- |
| **01** | **[Getting Started, Controls & Progression Guide](01-Getting-Started-and-Controls-EN.md)** | **[JA Chap. 01](01-Getting-Started-and-Controls.md)** | Installation requirements, complete keybindings reference, and the **8-Step Survival Progression Route from 7th Seat Eta to Lord Shadow** |
| **02** | **[Mana (MP), 99% Conductivity & Slime Bodysuit](02-Mana-and-Slime-Bodysuit-EN.md)** | **[JA Chap. 02](02-Mana-and-Slime-Bodysuit.md)** | Mana Conductivity formulas (`10% → 50% → 99%`), `7,000` Max MP resonance scaling, Mana Shield Defense (`1 DMG = 10 MP`), **`v1.0.6` 3D Sculpted Shadow Coat (3-joint 9-panel skirt & emissive glow)** & Civilian Disguise (`V`) |
| **03** | **[Action Combat, Just-Guard Parry & 7 Status Marks](03-Combat-Parry-and-Status-Marks-EN.md)** | **[JA Chap. 03](03-Combat-Parry-and-Status-Marks.md)** | Slime Guard, Just-Guard Parry (`7 ticks` window & 6 parry rewards), **Posture Break** damage multipliers, High-Speed Dash, and the **7 Combat Marks (Twin Fang, Bleed, Steel Thread, Hellfire, Calamity Break, Depravity, Magic Inhibition)** |
| **04** | **[Ultimate Art: "I am Atomic." Engine & All Modes](04-I-Am-Atomic-EN.md)** | **[JA Chap. 04](04-I-Am-Atomic.md)** | Chant timeline & Nakanishi Pre-Blast Silence, **3 Posture-Controlled Modes (Standard Sphere / Ep.5 Directional Beam / Ep.20 Zenith Dome and Magic Circle)**, and all 5 Atomic variants |
| **05** | **[All 30 3D Weapons, Artifacts & Consumables Catalog](05-Weapons-and-Artifacts-EN.md)** | **[JA Chap. 05](05-Weapons-and-Artifacts.md)** | Complete stats, MP costs, cooldowns, and damage formulas for all 9 Shadow/Cid weapons, **7 Seven Shadows weapons (5–6 skills each)**, 12 Hero/Witch/Cult/Lambda weapons, and 2 Mitsugoshi rations |
| **06** | **[All 26 Boss Entities & Shadow Garden Covenant](06-Bosses-and-Companions-EN.md)** | **[JA Chap. 06](06-Bosses-and-Companions.md)** | **4-Phase Lord Shadow** (44m barrier dome), **Seven Shadows (7)**, **Super Elite Agent John Smith**, **17 Kagemasu Heroes & Cult Bosses with dedicated 3D attire models**, and the **22-Character Companion System, AI Tactics & Sparring** |
| **07** | **[Complete 52 Crafting Recipes Reference](07-Crafting-Recipes-EN.md)** | **[JA Chap. 07](07-Crafting-Recipes.md)** | Full 3×3 crafting grids for all 4 Slime Bodysuit pieces, 22 weapons/artifacts/foods, 8 canon boss resonators, and 18 Kagemasu/Cult boss resonators |
| **08** | **[Advancements, `/mana` Commands, Config & Architecture](08-Commands-Config-and-Advancements-EN.md)** | **[JA Chap. 08](08-Commands-Config-and-Advancements.md)** | All 13 gameplay advancements, `/mana` commands, all 13 `eminence_shadow-common.toml` options, and **`v1.0.6` LUT & Zero-Allocation optimizations** |
| **📄** | **[Single-File Master Specification (`WIKI_SPECIFICATION.md`)](../WIKI_SPECIFICATION.md)** | — | Combined bilingual master technical specification in a single document |

---

## 🗺️ System Architecture Overview

```mermaid
flowchart TD
    subgraph PlayerCore["1. Mana & Slime Bodysuit Core (Chap. 02)"]
        Suit["Slime Bodysuit (4 Pieces)<br/>Mana Conductivity 10% → 99%"]
        Shield["Mana Conversion Shield<br/>1 DMG = 10 MP / 10 MP Fall Absorption"]
        Morph["v1.0.6 3D Sculpted Shadow Coat & Disguise (V)<br/>3-Joint 9-Panel Skirt, Glow Layer & Blade Materialization"]
    end

    subgraph CombatCore["2. Action Combat & 7 Status Marks (Chap. 03)"]
        Parry["Just-Guard Parry (Shift 7t)<br/>+25 MP, Projectile Deflect & Weapon Counter"]
        Break["Posture Break<br/>Cancels Mist/Stealth/Armor & 1.45x-2.0x Damage"]
        Marks["7 Combat Marks & Status Engine<br/>Twin Fang / Bleed / Steel Thread / Hellfire / Calamity / Depravity / Inhibition"]
    end

    subgraph ArsenalCore["3. All 30 3D Weapons & I am Atomic (Chap. 04 & 05)"]
        Weapons["30 3D Weapons, Artifacts & Items<br/>Cycle Multi-Skill Arts with Z / Shift+Z"]
        Atomic["Ultimate Art: 'I am Atomic.'<br/>3 Posture Modes (Sphere / Ep.5 Beam / Ep.20 Pre-Dome & Zenith Pillar) × 5 Variants"]
    end

    subgraph BossCore["4. All 26 Bosses & Shadow Garden Covenant (Chap. 06)"]
        Rank["Canon 8 Bosses & Shadow Garden Rank (0→8)<br/>+96% Attack / +2,000 MP / +48 MP/s / +32% Mitigation"]
        Allies["22 Recruitable Companions & 26 Custom 3D Models<br/>Follow Guard / Aggressive Hunt / Hold Position / Sparring / Unison"]
    end

    Suit --> Shield
    Suit --> Morph
    Suit --> Weapons
    Parry --> Break
    Break --> Rank
    Marks --> Rank
    Weapons --> Atomic
    Atomic --> Rank
    Rank --> Allies
```

---

## 📊 Content Summary at a Glance

| Category | Count | Breakdown & Highlights |
| :--- | :---: | :--- |
| **Custom 3D Weapons, Artifacts & Consumables** | **30** | 9 Shadow/Cid weapons & artifacts + 7 Seven Shadows weapons (5–6 skills each) + 12 Three Heroes/Kagemasu/Cult/Lambda weapons + 2 Mitsugoshi rations |
| **Slime Bodysuit Armor Pieces** | **4** | Hood, Coat, Leggings, Boots (Full set grants 99% Mana Conductivity, 100% Mana Shield & `v1.0.6` 3D sculpted/glowing Shadow Coat transformation) |
| **Multi-Phase Boss Entities** | **26** | 4-Phase Lord Shadow + 7 Seven Shadows + John Smith + **14 Kagemasu Heroes/Numbers & 3 Cult of Diablos Executives with dedicated 3D attire models** |
| **Recruitable Companions (Covenant)** | **22** | Every boss except the 3 Cult Executives (Fenrir, Ragnarok, Nelson) and Lord Shadow himself can be recruited as an AI companion |
| **Boss Summoning Resonators & Spawn Eggs** | **26 each** | 26 craftable 3D Resonators (also summon defeated bosses directly as allied companions via `Shift + Right-Click`) + 26 creative Spawn Eggs |
| **Survival Crafting Recipes** | **52** | Automatically unlocked in the vanilla Recipe Book and fully viewable in JEI |
| **Custom Advancements** | **13** | Full progression tree from equipping the Slime Bodysuit to conquering the Seven Shadows, defeating Lord Shadow, and unleashing `I am Atomic.` |
