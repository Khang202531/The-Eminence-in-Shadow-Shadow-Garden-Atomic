# Changelog — v1.0.0 (Initial Release — NeoForge 1.21.1)

## [1.0.0] - Initial Release (NeoForge 1.21.1)

### English
- **Initial Official Release (`v1.0.0`) for Minecraft NeoForge 1.21.1 (`21.1.252` / `[1.21.1,1.22)`).**
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

---

### 日本語
- **Minecraft NeoForge 1.21.1 向け初回正式リリース（`v1.0.0`）。**
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
