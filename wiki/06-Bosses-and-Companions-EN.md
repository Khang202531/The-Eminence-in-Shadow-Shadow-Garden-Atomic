# 06. All 26 Boss Entities & Shadow Garden Covenant (Companions)

🌐 **Language / 言語切替**: **[🇯🇵 日本語版はこちら](06-Bosses-and-Companions.md)** ｜ **🇺🇸 English (Current)**

[⬅ Prev: 05. All 29 3D Weapons & Artifacts](05-Weapons-and-Artifacts-EN.md) ｜ [🏠 English Wiki Home](Home-EN.md) ｜ [Next: 07. All 51 Crafting Recipes ➔](07-Crafting-Recipes-EN.md)

---

## 1. Shared Boss Specifications & Immunities (`v1.0.6` Dedicated 3D Models & Glow Maps)

All 26 bosses are summoned 6 blocks in front of the player by `Right-Clicking` their corresponding **Resonator** item (all 26 creative Spawn Eggs are also included).
In `v1.0.6`, in addition to Lord Shadow, the Seven Shadows, and John Smith, **all 17 Kagemasu & Anime characters (including Aurora, the 36-part 9×4-joint Golden Nine-Tailed Kitsune Yukime, and 256×256 Ultra-HD Elisabeth & Olivier) feature dedicated 3D attire models (`AbstractAttireModel`) and full-bright emissive glow textures (`*_attire_glow.png`)**.

- **Complete Anti-Cheese Environmental Immunity**: Immune to suffocation, drowning, fall damage, fire, lava, freezing, cactus, sweet berry bushes, and fly-into-wall kinetic damage. If a player attempts to pillar-camp or trap them in water/cobwebs, bosses use **Shadow Step (tactical teleportation)** to blink behind the player.
- **Combat Mark DoT Bypass (`eminence_shadow:combat_mark`)**: Uses a dedicated damage type so percentage-based `[Hellfire]` and stack-based `[Bleed]` DoTs deal consistent damage to all fire/magic-resistant bosses (non-lethal, leaving 1 HP for a direct finishing blow).
- **Anti-One-Shot Single-Hit Damage Cap**: Non-*Atomic* single hits are capped at **`20%` of a boss's Max HP (`28%` during [Posture Break])** (configurable via `bossSingleHitDamageCapRatio` in `eminence_shadow-common.toml`; set to `0.0` to disable).

---

## 2. Final Showdown Boss: Lord Shadow (`eminence_shadow:shadow`)

- **Summoning Item**: *Jet-Black Resonator* (`shadow_resonator`)
- **Max HP**: **`1,000.0`** (500 Hearts) ｜ **Knockback Resistance**: `100%` ｜ **Experience**: `5,000 XP`
- **`v1.0.6` 3D Model**: Overhauled `ShadowCoatModel` (3-joint 9-panel skirt, clear hood face arch with glowing crimson eyes, 45° forehead gold diamond & glowing amethyst throat brooch, 3-stage giant wing collar, 2-stage slime wings & full-bright emissive pass)
- **Guaranteed Drops**: **`1× Jet-Black Sword`**, **`1× Slime Bodysuit Coat`**, `2× Netherite Ingot`, `2× Emerald Block`, `1× Enchanted Golden Apple` + **Permanently Unlocks Empty-Hand "Jet-Black Sword" Materialization Mastery**

### 2.1 Four-Phase Awakening Table (Phase 0 – Phase 3)

| Phase (Boss Bar Tag) | HP Threshold | Equipped Weapon | Armor (Toughness) | Melee Attack | Move Speed | Mana Slash Power | Physical / Magic Damage Taken | Hardening Immunity Threshold | Afterimage Evade / Arrow Slice |
| :--- | :---: | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Phase 0: `[Holding Back]`**<br/>*(手加減)* | `100% – 80%` | Trusted Crowbar | `12.0`<br/>(`4.0`) | `16.0` | `0.39` | `18.0` | Phys `1.00×`<br/>Magic `1.00×` | `0.0` (None) | Evade `18%`<br/>Slice `35%` |
| **Phase 1: `[Serious]`**<br/>*(本気)* | `<= 80%`<br/>(800 HP) | Jet-Black Sword | `40.0`<br/>(`20.0`) | `40.0` | `0.44` | `40.0` | Phys `0.80×`<br/>Magic `0.50×` | Ignores `< 4.0` | Evade `22%`<br/>Slice `65%` |
| **Phase 2: `[Hardened]`**<br/>*(硬化・黒鉄)* | `<= 55%`<br/>(550 HP) | Jet-Black Sword<br/>**(Dual-Wield)** | `64.0`<br/>(`30.0`) | `76.0` | `0.49` | `72.0` | Phys `0.65×`<br/>Magic `0.35×` | **Ignores `< 8.0`** | Evade `26%`<br/>Slice `72%` |
| **Phase 3: `[Abyssal Awakening]`**<br/>*(深淵覚醒)* | `<= 25%`<br/>(250 HP) | Jet-Black Sword<br/>**(Dual-Wield)** | **`80.0`**<br/>(`40.0`) | **`115.0`** | **`0.54`** | **`100.0`** | Phys `0.55×`<br/>Magic `0.28×` | **Ignores `< 12.0`** | Evade `30%`<br/>Slice `78%` |

### 2.2 Lord Shadow's Signature Mechanics & Strategy Guide
1. **Phase 0 (Holding Back — Crowbar Martial Arts)**: Every 42 ticks, counters melee attacks with a **Crowbar Just-Parry (`26.0` damage + 2s Blindness + heavy knockback)** and unleashes a `28.0`-power crowbar shockwave on every 3rd swing.
2. **Phase 1 (Drawing the Jet-Black Sword)**: Summons lightning and materializes the *Jet-Black Sword*. Uses flash-step teleports to unleash **3 simultaneous afterimage crescent slashes (`38.0 × 3`)** and a pulling **Jet-Black Slime Tentacle Lance + 4 slime needles**.
3. **Phase 2 (Dual-Wielding, Black-Iron Hardening, Sky Meteor Dive & Normal/Zenith/Recovery Atomic)**:
   - Shifts the weather to a thunderstorm and dual-wields two *Jet-Black Swords*. Executes **Sky Command: Meteor Dive (`82.0–115.0` damage)** from high altitude.
   - In Phase 2, Shadow casts **I am Atomic.** at 5,000 base damage with the sphere mode. In rain or thunderstorms he uses **Zenith Atomic** to clear the weather with zero damage. At or below 42% HP, he casts **I am Recovery Atomic.** once to restore 30% of his max HP.
4. **Phase 3 (Abyssal Awakening — 44m Escape-Proof Barrier Dome & All-Range Atomic)**:
   - Encases the battlefield in an **inescapable 44m violet-black barrier dome**! Attempting to leave teleports you back inside, **Ender Pearls thrown toward the boundary are shot down mid-air, and Elytra flight is forcibly disabled**.
   - Inside this arena, chants **`I am the All-Range Atomic.` (`7,500` damage + forcibly disables player shields & drains `-320 MP`)**.
5. **🎯 How to Defeat Lord Shadow**:
   - **Land a `Just-Guard Parry` against Shadow's melee strikes, tentacle lances, or mana slashes to trigger [Posture Break (3.0s)], reducing his Armor by `-24`, disabling his Black-Iron immunity threshold, halving his hardening mitigation, multiplying damage taken by `1.45×`, and locking out his afterimage evasion!**
   - To survive his *I am Atomic* detonation: **① Time a Just-Guard Parry right at detonation (grants 24 ticks of invulnerability)**, **② Use a Mist Form invulnerability skill**, or **③ Activate Slime Barrier (75% mitigation) while wearing the full 99% Slime Bodysuit**!

---

## 3. The Seven Shadows (All 7 Bosses) Stats & Strategy Guide

Defeating each member of the Seven Shadows drops **their exclusive 3D weapon (`1×`)**, `1× Netherite Scrap`, `2× Diamond`, `6× Amethyst Shard`, and `1× Golden Apple`, while advancing your **Shadow Garden Ranking (Rank)**.

| Seat & Name (ID) | Recommended Order | Max HP | Attack<br/>*(Awakened)* | Armor (Tough) | Move Speed | Arrow Deflect | Slime Mitigation | Awaken HP | Signature Mechanics, Tag Synergies & Weakness (Counter Strategy) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| **7th Seat Eta**<br/>`eta` | **Step 1**<br/>(Rank 0+) | `600` | `26.0` | `16.0`<br/>(`4.0`) | `0.27` | `15%` | `25%` | `<= 60%`<br/>(360 HP) | **[Gravity Analysis & Autonomous Drones]** Deploys up to 4 destructible *Magic Slime Drones (28 HP)*, gravity levitation spheres, and **Mana Jamming Fields (drains `-80 MP` + Depravity + Magic Inhibition + full buff wipe when awakened)**.<br/>💡 **Counter**: Sweep her drones with AoE slashes and pressure her in close quarters. |
| **3rd Seat Gamma**<br/>`gamma` | **Step 2**<br/>(Rank 1+) | `950` | `20.0` | `24.0`<br/>(`10.0`) | `0.25` | **`0%`** | `45%`<br/>*(15% tripped)* | `<= 55%`<br/>(522 HP) | **[Overwhelming Mana & Clumsy Trip]** Periodically deploys Absorption & projectile-erasing barriers. **55% of her swings cause her to trip and fall**, triggering a **massive 8.5–9.5m mana explosion (`72–96` damage)**!<br/>💡 **Counter**: **Right after tripping, Gamma enters a `36-tick (1.8s)` `[Tripped!]` state where her mitigation drops from 45% → 15%** and her barriers lock out. Guard the blast and punish immediately! |
| **2nd Seat Beta**<br/>`beta` | **Step 3**<br/>(Rank 2+) | `720` | `34.0` | `20.0`<br/>(`6.0`) | `0.38` | `25%` | `28%` | `<= 60%`<br/>(432 HP) | **[Tactical Sniping & Lock-On]** Vaults away with silver-mist blasts when approached and heals with Healing Rain. Every 3rd shot triggers `[Target Locked]` rapid fire.<br/>💡 **Counter**: **`10 ticks (0.5s)` before firing, a red laser sight and audio cue appear**—press `Shift` to Just-Guard Parry and reflect her snipe arrow right back at her!<br/>🤝 **Synergy**: Triggers **[Rival Concerto]** with Epsilon. |
| **5th Seat Epsilon**<br/>`epsilon` | **Step 4**<br/>(Rank 3+) | `800` | `42.0` | `24.0`<br/>(`8.0`) | `0.40` | `40%` | `35%` | `<= 58%`<br/>(464 HP) | **[Sky-Walk & 99% Compressed Sonic Blades]** Glides mid-air (`[Aerial Control]`) in circular orbits while firing 45% armor-piercing sonic discs and 7-arc Moonlight Symphonies.<br/>💡 **Counter**: Breaking her posture with a parry **immediately shatters her feather-glide, scattering slime pads with a unique voice line and knocking her to the ground**! |
| **6th Seat Zeta**<br/>`zeta` | **Step 5**<br/>(Rank 4+) | `880` | `40.0` | `26.0`<br/>(`10.0`) | `0.50` | `35%` | `32%` | `<= 55%`<br/>(484 HP) | **[Complete Stealth & Blind-Spot Ambush]** Erases footsteps and particles while invisible to deliver a **2.6× damage backstab (`104.0`) + Blindness & Wither II**.<br/>💡 **Counter**: **`8 ticks (0.4s)` before her ambush lands, a chime sound and crimson eye glint trigger behind you**—press `Shift` on the audio cue to parry her out of stealth! |
| **4th Seat Delta**<br/>`delta` | **Step 6**<br/>(Rank 5+) | `1,050` | `62.0`<br/>*(`82.0`)* | `28.0`<br/>(`12.0`) | **`0.52`**<br/>*(`0.62`)* | `18%` | `30%` | `<= 60%`<br/>(630 HP) | **[Crimson Wolf Frenzy, MP Shred & Lifesteal]** Sniffs out and cancels player invisibility, heals on hit, and **shreds `-45 to -65 MP` per hit**!<br/>🤝 **Synergy**: Shares **[Twin Fang Stamp]** stacks with Zeta.<br/>💡 **Counter**: Parry her linear feral leaps and claw combos to inflict Posture Break. |
| **1st Seat Alpha**<br/>`alpha` | **Step 7**<br/>(Rank 6+) | **`1,350`** | `58.0`<br/>*(`78.0`)* | **`34.0`**<br/>(`16.0`) | `0.45` | **`50%`** | **`40%`** | `<= 55%`<br/>(742 HP) | **[Leader of the Seven Shadows, Tri-Form & Imitation Atomic]** Morphs her slime weapon between 3 forms on every strike and casts **Imitation Art: `I am Atomic!` (28t charge + 7.5m lightning blast)** below 35% HP!<br/>💡 **Counter**: Time your Just-Guard Parry right as she materializes from Mist Form to attack. |

---

## 4. Super Elite Agent "John Smith" (`eminence_shadow:john_smith`)

- **Summoning Item**: *John Smith's Forged Contract* (`john_smith_resonator`)
- **Base Stats**: Max HP **`1,150.0`** ｜ Attack **`38.0`** ｜ Armor **`32.0`** (Toughness `16.0`) ｜ Move Speed **`0.45`**
- **Arrow Deflect**: `45%` (**`65%`** after mask break) ｜ **Slime Mitigation**: `40%` (**`55%`** after mask break)
- **Guaranteed Drops**: **`1× John Smith's Micro Steel Threads`** + **`1× Shadow's Encrypted Memo (SS+ Artifact)`**
- **Signature Mechanics & Canon Synergies**:
  1. **[Steel Thread Counter Stance]**: Wraps himself in `[Steel Thread]` stacks (up to 3), intercepting melee attackers with a **3-second (60t) full stun snare + `28.0` damage** (bypassed by Alpha during Mist Form).
  2. **[Mana Disruption Wave (-85% MP Regen)]**: Unleashes an 8-way thread wave (10m) that suppresses player MP regeneration by **`-85%` for `6.0 seconds (120 ticks)`**.
  3. **[Timed Wire Cage (Ten Steel Threads)]**: Collapses for **`58.0`** damage + Slowness (**deals `1.35×` bonus damage and heavy snare against Therianthropes [Delta, Lili, Yukime, Fenrir]**, with canon dialogue against Delta).
  4. **[Mask Shattered]**: Below `50%` HP or when struck by **Alpha**, his mask shatters off his 3D model and he enters high-evasion serious mode.
  5. **[Yukime Co-Op Synergy]**: Fighting within 18m of an allied Yukime grants both of them permanent **Strength I & Speed I**.

---

## 5. Kagemasu Heroes, Three Heroes, Numbers & Cult Executives (All 17 Bosses)

In `v1.0.6`, all 17 characters below feature **dedicated 3D attire models (`*_attire.png`) and full-bright emissive glow layers (`*_attire_glow.png`)**.

| Category | Boss Name & ID | Max HP | Attack | Armor | Speed | Deflect / Mitigation | Weapon Drop | Recruitable | Signature Mechanics & `v1.0.6` 3D Model Highlights |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: | :--- | :---: | :--- |
| **Cid Persona** | **Jimina Seinen**<br/>`jimina_seinen` | `900` | `24.0`<br/>*(Awakened `60.0`)* | `22.0` | `0.30`<br/>*(Awakened `0.48`)* | Deflect `35%`<br/>Mitig `25%` | *Plain Sword* | **Yes** | Roleplays a weak mob in Phase 1; **below 50% HP releases his limiter (`2.5×` Attack `60.0` & Speed `0.48`)**! (3D cape & scarf attire model) |
| **Cid Persona** | **Jack the Ripper**<br/>`jack_ripper` | `1,050` | `46.0` | `26.0` | `0.48` | Deflect `48%`<br/>Mitig `50%` | *Bloodstained Cards* | **Yes** | Mist backstabs + `[Bleed]` + **18-tick delayed execution card bombs (`64.0 × Bleed multiplier`)**. (3D jester mask, top hat & tailcoat model) |
| **Numbers** | **No. 559 Victoria**<br/>`victoria` | `950` | `44.0`<br/>*(Zeal `59.4`)* | `26.0` | `0.44` | Deflect `45%`<br/>Mitig `48%` | *Standard Slime Sword* | **Yes** | **[Zealous Devotion]** Fighting near Lord Shadow, John Smith, or a full-suit player boosts her **Attack by `1.35×` + Speed II**! (3D saint veil & gold-trimmed slime vestments) |
| **Numbers** | **Drill Instructor Lambda (No. 11)**<br/>`lambda` | `880` | `34.0` | `28.0` | `0.40` | Deflect `42%`<br/>Mitig `44%` | *Standard Slime Sword* | **Yes** | **[Instructor's Command]** Commander buffer granting allies within 12–14m **permanent Strength I–II & Speed I**. (3D officer cap & gold-epaulette coat) |
| **Numbers** | **No. 13 Nu**<br/>`nu` | `840` | `32.0` | `22.0` | `0.42` | Deflect `40%`<br/>Mitig `42%` | *Standard Slime Sword* | **Yes** | **[Master of Disguise]** Her ultimate **strips 100% of enemy beneficial buffs** while cleansing ally debuffs. (Dual-form 3D combat slime suit & Mitsugoshi attire) |
| **Lawless City** | **Golden Nine-Tailed Yukime**<br/>`yukime` | `1,020` | `42.0` | `24.0` | `0.46` | Deflect `40%`<br/>Mitig `45%` | *Spirit Fox Iron Fan* | **Yes** | **[36-Part (9 Tails × 4 Segments) 3D Nine-Tails Model]** 9 golden tails wave with independent physics! Unleashes 9-fan barrages & **`[Depravity]`**. |
| **Lawless City** | **Crimson Blood Queen Elisabeth**<br/>`elisabeth` | `1,450` | `54.0` | `32.0` | `0.44` | Deflect `55%`<br/>Mitig `55%` | *Crimson Queen's Scythe* | **Yes** | Enters mist form for her ultimate and creates up to five blood pools that launch homing lances at enemies within 16 blocks. Applies Bleed and Magic Inhibition and follows with crossing blood slashes. 3D royal gown and blood wings. |
| **Ancient Legend** | **Calamity Witch Aurora**<br/>`aurora` | `1,650` | `64.0` | `36.0` | `0.46` | Deflect `55%`<br/>Mitig `56%` | *Calamity Witch's Scythe* | **Yes** | Fires homing jets from a crimson mana orb. Her ultimate applies Bleed, Magic Inhibition and Poison. In her awakened phase it adds two crossing scythe waves. 3D witch shawl, floating blood crystals and layered dress. |
| **Three Heroes** | **First Paladin Olivier**<br/>`olivier` | `1,250` | `50.0` | **`34.0`** | `0.44` | Deflect `58%`<br/>Mitig `52%` | *Hero's Sword* | **Yes** | **[256×256 Ultra-HD 3D Paladin Valkyrie Armor & Circlet]** Paladin parry counter (`52.0`) & awakened `[Hellfire]` 7-wave overdrive. |
| **Three Heroes** | **Hero Freya**<br/>`freya` | `1,180` | **`56.0`** | `30.0` | `0.44` | Deflect `45%`<br/>Mitig `48%` | *Wedge of Ego* | **Yes** | Empowers herself with **`[Calamity Break]`** to deliver 45% armor-piercing guard-crushing charges. (3D crimson plate armor & cape) |
| **Three Heroes** | **Saint Lili**<br/>`lili` | `980` | `36.0` | `26.0` | `0.45` | Deflect `42%`<br/>Mitig `46%` | *Ancient Holy Staff* | **Yes** | Heals allies within 14m for **18% Max HP + cleanses debuffs + grants Absorption II**. (3D beast ears, saint veil & white-gold vestments) |
| **Sword Saint** | **War Goddess Beatrix**<br/>`beatrix` | `1,220` | `52.0` | `30.0` | `0.47` | Deflect **`62%`**<br/>Mitig `48%` | *Sword Saint's Greatsword* | **Yes** | Highest arrow deflection rate (`62%`) + godspeed behind-the-back 3-slash combo. (3D elf ears, silver tiara & sword-saint tunic) |
| **Sword Saint** | **Wandering Blademaster Annerose**<br/>`annerose` | `960` | `40.0` | `24.0` | `0.46` | Deflect `50%`<br/>Mitig `40%` | *Annerose's Sword* | **Yes** | *Azure Sky Soar* **dispels up to 5 beneficial buffs from her target at once**. (3D bandana & azure traveler jacket) |
| **Heroine** | **Claire Kagenou**<br/>`claire` | `940` | `38.0` | `24.0` | `0.42` | Deflect `35%`<br/>Mitig `42%` | P1: *Mithril Sword*<br/>P2: *Witch's Scythe* | **Yes** | Misfires *"...I am Atomic"* (`88.0`) below 55% HP; below 50% HP, Aurora awakens in her left arm with glowing sigils! (3D Midgar uniform) |
| **Rounds 5th Seat** | **Fenrir**<br/>`fenrir` | `1,400` | `52.0` | `32.0` | `0.48` | Deflect `45%`<br/>Mitig `50%` | *Cursed Katana: Utsusemi* | **No** | Utsusemi Blood Fang summons five homing blades with 34.0 base damage each. Two area hits during its 90-tick window trigger a 100-tick Posture Break. 3D white wolfskin cloak. |
| **4th Demon King** | **Ragnarok**<br/>`ragnarok` | **`2,200`**<br/>*(Highest)* | **`72.0`** | **`46.0`** | `0.36` | Deflect `20%`<br/>Mitig `62%` | *(Rare Materials & Huge XP)* | **No** | **[Demon Realm Break Armor]** Normally immune to `I am Atomic.` and takes only `0.35×` damage (65% reduction), but **a single Parry or `[Calamity Break]` hit shatters his armor for `90 ticks (4.5s)`, causing him to take `2.00×` damage (~5.7× normal)!** (3D demon horns, abyssal wings & armor) |
| **Rounds 11th Seat** | **Nelson (The Sanctuary)**<br/>`nelson` | `1,350` | `38.0` | `32.0` | `0.34` | Deflect `35%`<br/>Mitig `50%` | *Sanctuary Magic Staff* | **No** | **[Sanctuary Mana Drain & Hero Clones]** Drains `35 MP` every 2s from players below 99% conductivity and reduces non-99% damage to `0.25×`. Summons up to 2 **Hero Olivier Clones (687 HP)**. **99% full Slime Suit deals 100% full damage, and casting `I am Atomic.` shatters his Sanctuary mana drain!** |

---

## 6. Shadow Garden Covenant (Recruitment, AI Tactics, Sparring & Unison)

All **22 characters** (every boss except the 3 Cult Executives—Fenrir, Ragnarok, Nelson—and Lord Shadow himself) can be recruited as permanent AI companions!

1. **How to Recruit**:
   - Wear the full 4-piece Slime Bodysuit and **`Right-Click`** a boss you have previously defeated (or weakened below **`15%` HP** during combat).
   - Or wear the full Slime Bodysuit and **`Shift + Right-Click` with a defeated boss's Resonator** to summon them directly as an allied companion.
2. **Tactical AI Mode Cycling** (`Right-Click` ally above `92%` HP):
   - 🟢 **Follow & Guard**: Follows at 6.5m and safely teleports if more than 26m away.
   - 🔴 **Aggressive Hunt**: Actively seeks out and engages hostile mobs and modded bosses within a 28m radius.
   - 🟡 **Hold Position**: Saves their anchor coordinates in NBT and defends a 12–14m perimeter without teleporting after you.
3. **Mana Supply Healing** (`Right-Click` ally below `92%` HP): Holding any mod item transfers `20 MP` to **instantly heal 25% of the companion's Max HP (minimum `40 HP`)**.
4. **Friendly Sparring (`Shift + Right-Click`)**: Companions have normalized `1.0×` base HP while allied, and re-apply `bossPowerMultiplier` when you start a sparring match.
5. **Companion Resonance Aura & Pair Banter**: Each companion within 20m supplies **`+2.5 MP/s`** to you and engages in canon ambient banter with nearby paired characters out of combat.

---

[⬅ Prev: 05. All 29 3D Weapons & Artifacts](05-Weapons-and-Artifacts-EN.md) ｜ [🏠 English Wiki Home](Home-EN.md) ｜ [🇯🇵 日本語版はこちら](06-Bosses-and-Companions.md) ｜ [Next: 07. All 51 Crafting Recipes ➔](07-Crafting-Recipes-EN.md)
