# 03. Action Combat, Just-Guard Parry, Posture Break & 7 Status Marks

🌐 **Language / 言語切替**: **[🇯🇵 日本語版はこちら](03-Combat-Parry-and-Status-Marks.md)** ｜ **🇺🇸 English (Current)**

[⬅ Prev: 02. Mana, 99% Conductivity & Slime Bodysuit](02-Mana-and-Slime-Bodysuit-EN.md) ｜ [🏠 English Wiki Home](Home-EN.md) ｜ [Next: 04. Ultimate Art "I am Atomic." ➔](04-I-Am-Atomic-EN.md)

---

## 1. Slime Guard & Just-Guard Parry

| Mechanic | Value & Specification |
| :--- | :--- |
| **Activation Input** | Hold **`Shift` (Sneak)** while holding any mod skill weapon or wearing at least 1 Slime Bodysuit piece |
| **Standard Slime Guard Mitigation** | Holding Weapon: **`85%` damage reduction** / Unarmed in Suit: **`75%` damage reduction** (Costs `1.5 MP` per hit; `50%` reduction if out of MP) |
| **Just-Guard Parry Window** | First **`7 ticks (0.35 seconds)`** after pressing Sneak (HUD displays `⚡ Just-Guard Ready (Parry)`) |
| **Parry Re-Stance Cooldown** | `14 ticks (0.70 seconds)` — **Automatically resets to `0` immediately upon a successful parry**, enabling chained parries against multi-hit combos! |
| **Auto-Parry Charges** | Casting *I am Archetype Atomic.* with the *Archetype Shadow Blade* (3 charges) or *Progenitor Paladin: Hellfire Release* with Olivier's *Holy Sword* (2 charges) grants **Auto-Parry charges that automatically trigger a Just-Guard Parry upon taking damage even without pressing Shift**. |

### The 6 Rewards of a Successful Just-Guard Parry
1. **100% Damage Immunity & Invulnerability Frames**: Completely nullifies the triggering attack and grants `12 ticks` of invulnerability (`24 ticks` of invulnerability when parrying an enemy's *I am Atomic* wave).
2. **Instant MP Recovery & Self-Buffs**: Immediately restores **`+25.0 MP`** and grants **Resistance II (0.7s) + Speed II (2.0s)**.
3. **Hyper-Velocity Projectile Deflection**: Parrying an enemy arrow or magic projectile rewrites its ownership to you and reflects it back at the shooter at **1.75× speed (minimum speed 1.8)** while firing a `90.0`-damage magic counter slash (reflected projectiles are safely prevented from friendly-fire or secondary explosion loops).
4. **Weapon-Specific Parry Counter Art**: Automatically unleashes a unique counterattack tailored to your held weapon (healing, behind-the-back teleportation, status mark application, cross slashes, etc.—also supports Beta's bow held in the offhand).
5. **Attacker Knockback & Debuffs**: Blasts melee attackers backward and inflicts Slowness III (2.25s), Weakness II (3.0s), and Glowing (2.0s).
6. **Triggers Boss [Posture Break]**: Parrying a boss's melee strike or any projectile fired from within **24m** shatters the boss's posture for **`60 ticks (3.0 seconds)`** (**`90 ticks (4.5 seconds)`** against Ragnarok, King of the Fourth Demon Realm)!

---

## 2. [Posture Break] Internal Mechanics

Landing a **Just-Guard Parry** against a boss or striking them while empowered by the **[Calamity Break (Zekka)]** buff inflicts **[Posture Break]** (turning their boss bar yellow and displaying the `[POSTURE BROKEN!]` tag):

- **Immediately Cancels & Locks Out Mist Form and Complete Stealth** (also shatters Epsilon's aerial feather-glide, knocking her to the ground with a unique voice line).
- **Disables Afterimage Evasion (Sway Evade), Projectile Slicing, and Boss Counter-Parries**.
- **Halts Slime Coat Natural Regeneration**.
- **Halves Slime Hardening Mitigation & Multiplies Final Incoming Damage by `1.45×` (`2.00×` against Ragnarok)**.
- **Relaxes the Single-Hit Damage Cap**: Expands the standard `20%` Max HP single-hit cap to **`28%`** (`1.4×` of `bossSingleHitDamageCapRatio`).
- **Additional Penalty vs. Lord Shadow**: Reduces Lord Shadow's Armor by **`-24.0`** and completely disables his Phase 2–3 Black-Iron Slime Hardening damage immunity threshold while broken.

---

## 3. High-Speed Movement (Shadow Dash / Rapid Dash)

- **Trigger Input**: Double-tap jump (`Space × 2` within `8 ticks`) on the ground or in mid-air.
- **Holding *Jet-Black Sword* or Unarmed in Full Slime Bodysuit**: Unleashes **unlimited Shadow Dash** (except while holding Beta's bow).
- **Holding Alpha's *Blade of Shadow***: Unleashes **3-charge Rapid Dash**.
- **Fall Damage Protection**: Grants `36 ticks (1.8 seconds)` of complete fall damage immunity after dashing.

---

## 4. The 7 Combat Marks & Status Engine

Marks and custom status effects applied to your current target are synchronized in real time to the on-screen target indicator (`Fang:X Bleed:Y Thread:Z [Fire:* Dep:* Inh:*]`) and Eta's Magic Analysis HUD.

| Mark / Status Name | Max Stacks / Duration | Application Sources | Detailed Effects & Formulas |
| :--- | :---: | :--- | :--- |
| **Twin Fang Stamp**<br/>*(双牙の刻印)* | Up to `5` Stacks<br/>(`160 ticks / 8.0s`) | Delta (*Claws of Shadow*) & Zeta (*Daggers of Shadow*) melee hits and skills | Detonated by Delta's *Destruction* or Zeta's *Shadow Dance* (or automatically at 3 stacks by boss Delta/Zeta) to deal **45% armor-piercing** burst damage: $\text{Damage} = \text{Base} \times (1.0 + 0.32 \times \text{Stacks})$ (up to **2.60×**) + Slowness IV (2s). |
| **Bleed**<br/>*(出血)* | Up to `5` Stacks<br/>(`120–180 ticks`) | Aurora, Elisabeth, Jack the Ripper & Fenrir weapons and skills | ① Deals $\min(12.0,\ 1.5 \times \text{Stacks})$ true DoT (`eminence_shadow:combat_mark`, bypasses boss fire/magic immunity, non-lethal leaving 1 HP) every `25 ticks`.<br/>② Multiplies the bonus magic damage (and select skills) of Bleed-resonance weapons (*Witch's Scythe*, *Crimson Queen's Scythe*, *Bloodstained Cards*, *Cursed Katana Utsusemi*) by **$(1.0 + 0.16 \times \text{Stacks})$× (up to 1.80× at 5 stacks)**! |
| **Steel Thread**<br/>*(鋼糸)* | Up to `3` Stacks | Right-clicking *Shadow's Encrypted Memo*, Boss John Smith | Defensive counter stacks applied to self. Upon taking a non-projectile hit, consumes 1 stack to **completely nullify the attack** and deal **`28.0` damage (35% armor-piercing) + `60 ticks (3.0s)` of Slowness VI & Weakness III + `24 ticks (1.2s)` of Blindness** to the attacker. |
| **Hellfire (Gouka)**<br/>*(業火)* | `100–140 ticks`<br/>(5.0–7.0s) | Olivier's *Holy Sword* critical hits & skills, Bosses Olivier & Ragnarok | Every `20 ticks (1.0s)`, inflicts **`3.5%` of the target's Max HP** (clamped between `2.0` and `20.0`) as `eminence_shadow:combat_mark` damage (effective against all fire/magic-immune bosses; non-lethal). |
| **Calamity Break (Zekka)**<br/>*(絶禍)* | `60–180 ticks`<br/>(3.0–9.0s) | *Archetype Shadow Blade*, Freya's *Wedge of Ego*, Olivier's *Holy Sword* | Self-empowerment breaker buff:<br/>① Passively multiplies all damage dealt by **`1.18×`** (**`1.45×` against shield-blocking targets + forcibly disables vanilla shields**).<br/>② Every hit **directly triggers Boss [Posture Break] (45–90 ticks) without needing a parry** (the only way to shatter Ragnarok's Break Armor head-on). |
| **Depravity (Daraku)**<br/>*(堕落)* | `80–140 ticks`<br/>(4.0–7.0s) | Yukime's *Spirit Fox Iron Fan* crits & ultimate, Bosses Eta & Ragnarok | Inflicts Weakness I, **reduces the target's outgoing damage by `-20% (0.80×)`**, and **increases all damage the target takes by `+25% (1.25×)`**. |
| **Magic Inhibition**<br/>*(魔力阻害)* | `60–160 ticks`<br/>(3.0–8.0s) | *Calamity Witch's Scythe*, *Crimson Queen's Scythe*, *Sanctuary Magic Staff* | **Reduces all HP healing received by the target (natural regen, lifesteal, healing skills, potions) by `-70% (0.30×)`**. |

---

[⬅ Prev: 02. Mana, 99% Conductivity & Slime Bodysuit](02-Mana-and-Slime-Bodysuit-EN.md) ｜ [🏠 English Wiki Home](Home-EN.md) ｜ [🇯🇵 日本語版はこちら](03-Combat-Parry-and-Status-Marks.md) ｜ [Next: 04. Ultimate Art "I am Atomic." ➔](04-I-Am-Atomic-EN.md)
