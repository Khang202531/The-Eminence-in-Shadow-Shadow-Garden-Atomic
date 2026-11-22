# Changelog — The Eminence in Shadow: Shadow Garden & Atomic

## [1.0.5] - Spec Consistency, Combat Bugfixes & Polish (NeoForge 1.21.1 & Forge 1.20.1)

### English
- **Combat Marks & Boss Penetration**:
  - Added dedicated `eminence_shadow:combat_mark` DamageType (in `minecraft:bypasses_armor` tag) so Hellfire (*Gouka*) and Bleed DoTs properly damage Fire/Magic-immune bosses (Shadow, Seven Shadows, Ragnarok, etc.), while staying safely non-lethal (`health > dmg + 1.0`).
  - Changed armor-piercing damage floors (`ShadowCombatHelper`, `ManaBoltEntity`) from `DamageTypes.MAGIC` to `indirectMagic` attributed to the attacker so Shadow's raw magic immunity no longer negates them.
  - Cleared Combat Mark trackers cleanly on player logout.
- **Bosses & Companions**:
  - Fixed `ShadowAtomicGoal` so Shadow correctly switches into Recovery Atomic when eligible and no longer gets stuck re-triggering Atomic.
  - Restored Shadow's Phase 0 Crowbar spawn on `ShadowResonatorItem` usage.
  - Fixed Shadow's Phase 2 single-hit damage cap (honoring `bossSingleHitDamageCapRatio` config and expanding cap cleanly to `1.4x` during Posture Break) and added safe barrier-dome return position probing.
  - Fixed `EpsilonEntity` canceling Feather Glide immediately upon Posture Break.
  - Fixed `KagemasuHeroEntity` (Ragnarok Atomic immunity & exact `2.0x` Posture-Break multiplier; Nelson 99% Nine-Shadow conductivity respect, stopping MP drain after Sanctuary shatter, and `687.0` HP cap for Olivier Clones; Yukime Speed I + Strength I aura near John Smith).
  - Fixed `SevenShadowEntity` sparring HP baseline preservation (`baseUnscaledMaxHealth`) upon recruitment and added persistent tactical `Hold Position` anchor (`12m`/`14m` leash).
- **Atomic Engine, Mana Shield & Weapons**:
  - Wired `Config.BLAST_DAMAGE` into `AtomicBlastEntity`, fixed `a <= getExpandEnd()` final expansion frame, delayed `"i_am_atomic"` advancement grant until release after MP check, added partial mana drain (`PlayerMana.drainUpTo`), extended All-Range lifetime cleanly for large radii, fixed `isFast` client swirl/magic-circle speedup, and updated Recovery Atomic (ally hunger restore + Resistance II + ally-safe `180` boss damage).
  - Fixed `SlimeArmorEvents` (`isActiveAtomicRunning()`, `applySlimeBarrierMitigation` in full-suit absorption, excluding Atomic blasts from Combat Mark multiplier double-dip, reachable shield-flash FX, projectile Posture Break within `24m`, offhand Beta Bow parry AoE, `root` advancement on any Slime piece, `OwnableEntity` kill credit, and Shadow rank-up chat notification).
  - Prevented post-parry friendly bleed-through on `ManaArrowEntity`, `ManaBoltEntity`, and `ManaSlashEntity`.
  - Unified all 20 `AbstractSevenShadowWeapon` subclass weapons to exact spec values (`+3.0` sword base damage), unconditional `Zekka` application on `ArchetypeBladeItem` Skill 1, full-suit check for `V` morph and server crouch check for Shadow Mastery sword materialization, Mithril HUD label, and added all 11 missing items/weapons to `CreativeModeTabs.COMBAT`.
- **Recipe Advancements, Localization & Documentation**:
  - Added 5 data-driven recipe unlock advancements covering all 51 recipes.
  - Added missing `en_us.json` / `ja_jp.json` keys (`combat_mark` death messages, Mithril HUD, Alpha Sword passive tooltip, Shadow Mastery chat fix, gender-neutral companion error; `650` keys parity).
  - Synchronized `WIKI_SPECIFICATION.md`, `README.md`, and `wiki/01`–`08` (completely rewriting corrupted `wiki/03`–`08` files).

### 日本語
- **戦闘印（火傷・業火・出血）とボス貫通修正**:
  - 専用ダメージ種別 `eminence_shadow:combat_mark`（`bypasses_armor` タグ所属）を新設し、炎・通常魔法耐性を持つシャドウやラグナロク等のボスにも業火・出血DoTが非致死ガード付きで正常に通るよう修正。
  - `ShadowCombatHelper` / `ManaBoltEntity` の貫通保証ダメージを攻撃者帰属の `indirectMagic` に変更し、シャドウの魔法無効化に遮断されないよう修正。
- **ボス＆仲間の挙動修正**:
  - シャドウの「リカバリー・アトミック」判定タイミングを修正し、発動可能時の即時遷移および通常アトミックの無限ループを解消。
  - `ShadowResonatorItem` 召喚時に第0形態のバールが消失する不具合を修正、第2形態の単発上限設定連動＋体勢崩壊時の `1.4倍` 緩和、結界ドーム引き戻しの安全着地探索を実装。
  - イプシロンの体勢崩壊時にフェザーグライドを即解除するよう修正。
  - ラグナロク（アトミック完全無効＋体勢崩壊倍率を正確に合算 `2.00倍` へ修正）、ネルソン（味方七陰の99%伝導率適用、聖域崩壊後のMP吸収停止、オリヴィエ・クローンHP上限 `687.0`）、ユキメ（ジョン・スミス近接時の移動速度I付与）を修正。
  - 七陰の模擬戦スケーリング前の基礎HP保持と、追従モード「待機（Hold Position）」アンカー（半径12m/14m・NBT永続化）を実装。
- **アトミック・魔力シールド・武器の修正**:
  - `Config.BLAST_DAMAGE` をアトミック威力の計算に接続し、最大膨張フレーム（`a <= getExpandEnd()`）、解放成功後の実績付与、不足時の部分消費（`drainUpTo`）、極大半径時の寿命延長、`isFast` 魔法陣高速化、リカバリー・アトミックの満腹度回復＋耐性II＋ボス180ダメージを追加。
  - `SlimeArmorEvents` でチャージ中のみの無敵化・通常バリア軽減併用・パリィ時ボス体勢崩壊（24m以内）・オフハンドベータ弓対応・ペット/ドローン撃破クレジット帰属を修正し、反射後の弾体味方貫通バグを修正。
  - 七陰武器共通基底（`AbstractSevenShadowWeapon`）の剣基礎ダメージ `+3.0` を含め全20種を仕様値へ統一。開闢剣技1の無条件『絶禍』付与、クリエタブ未登録11種追加、ミスリルSword専用HUD表記、フルスーツ必須の `V` 変身、サーバー側スニーク検証を実装。
- **レシピブック解放・翻訳・ドキュメント全面改訂**:
  - 全51レシピを素材入手で段階解放する5つのレシピ進捗（Advancement）を追加し、翻訳漏れ（`650` キー完全一致）と破損していた `wiki/03`〜`08` を全面修正。

---

## [1.0.0] - Initial Release (NeoForge 1.21.1 & Forge 1.20.1)

### English
- **Initial Official Release (`v1.0.0`) for Minecraft NeoForge 1.21.1 (`21.1.252`) and Forge 1.20.1 (`47.4.28`).**
- **Core Mana & Slime Bodysuit System**:
  - Added 99% Mana Conductivity Slime Bodysuit (4 armor pieces), Mana Shield damage-to-MP conversion, full 3D Shadow transformation with dynamic coat physics, civilian disguise toggle, and empty-hand Jet-Black Sword materialization.
- **Four Canonical Stances of *"I am Atomic."***:
  - Implemented Standard Sphere, Directional Piercing Beam (Ep. 5), Skyward Pillar (Ep. 20), *All-Range Atomic*, *Recovery Atomic*, *Archetype Atomic*, and *Catastrophe Atomic* with cinematic chant typography, pre-blast silence contrast, and procedural audio synthesis.
- **Combat Mechanics**:
  - Added Slime Guard, Just-Guard Parry Counter (+25 MP & Posture Break), Shadow Garden Mastery Rank progression (Rank 0–8), and high-speed aerial/ground dashes (`Space × 2`).
- **25+ Custom 3D Weapons & Consumables**:
  - Added signature 3D weapons and multi-skill kits (`Z` key cycling) for Shadow, John Smith, Jimina Seinen, Cid (48 Mob-Fu Secret Arts), all Seven Shadows (Alpha, Beta, Gamma, Delta, Epsilon, Zeta, Eta), the Three Heroes (Olivier, Freya, Lili), Aurora, Elisabeth, Yukime, Beatrix, Annerose, Jack the Ripper, Fenrir, Nelson, and Numbers.
  - Added Mitsugoshi Fine Chocolate, Mitsugoshi Blended Coffee, Shadow's Encrypted Memo, and 26 Boss Resonators & Spawn Eggs.
- **26 Multi-Phase Bosses & Companion System**:
  - Added 4-phase Lord Shadow boss encounter, 7 awakened Seven Shadows bosses, John Smith, and 17 Kagemasu/canon hero & Diabolos Cult bosses with allied recruitment pacts, AI mode switching, sparring duels, and character banter.
- **Performance & Release Hardening**:
  - Optimized spherical/directional block excavation with async slice precomputation and 16×16 chunk-section locality, batched S2C particle networking (`ParticleFxPayload`), and eliminated per-frame HUD/renderer allocations.

### 日本語
- **Minecraft NeoForge 1.21.1 ＆ Forge 1.20.1 向け初回正式リリース（`v1.0.0`）。**
- **魔力システム＆スライムスーツ**:
  - 魔力伝導率99%のスライムスーツ4部位、被ダメージ魔力変換シールド、3D物理演算コート付きシャドウ変身＆日常服偽装切替、素手スニークによる『漆黒の剣』具現化を実装。
- **究極奥義『I am Atomic.』全形態**:
  - 通常球体・指向性貫通ビーム（第5話）・天蓋昇華ピラー（第20話）・All-Range Atomic・Recovery Atomic・Archetype Atomic・Catastrophe Atomic を実装（詠唱タイポグラフィ・静寂演出・プロシージャル合成音響対応）。
- **アクション戦闘システム**:
  - スライムガード、ジャストガード・パリィ反撃（+25 MP＆ボスの体勢崩し）、シャドウガーデン格付けランク（Rank 0〜8）、2段ジャンプ高速移動（瞬駆／連閃）を実装。
- **全25種以上の専用3D武器・魔道具・アイテム**:
  - シャドウ、ジョン・スミス、ジミナ・セーネン、モブ式奥義四十八手、七陰全7名（アルファ〜イータ）、三英雄（オリヴィエ・フレイヤ・リリ）、アウロラ、エリザベート、ユキメ、ベアトリクス、アンネローゼ、切り裂きジャック、フェンリル、ネルソン、ナンバーズらの専用3D武器・共鳴核・スポーンエッグ・ミツゴシ商会アイテムを追加。
- **全26体の多段階覚醒ボス＆仲間化システム**:
  - 4段階覚醒の「シャドウ」、七陰7名、ジョン・スミス、英雄・ディアボロス教団幹部ら全26体のボス戦、および撃破後の盟約（仲間化・AIモード切替・模擬戦・掛け合いセリフ・アトミック連動）を実装。
- **最適化＆リリースビルド整備**:
  - 非同期スライス計算とチャンク局所化による低負荷クレーター生成、パーティクル通信の単一パケットバッチ化（`ParticleFxPayload`）、HUD・3D描画のフレーム毎アロケーション削減を実施。
