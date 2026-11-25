# Changelog — v1.0.7 (Forge 1.20.1)

## [1.0.7] - Zenith Atomic Overhaul, Utsusemi Homing Blades & Dragon, Aurora Blood Magic & Balance (Forge 1.20.1)

### English
- **Skyward "I am Atomic" (`CAST_MODE_ZENITH`) Overhaul**:
  - Changed skyward Zenith Atomic to deal zero entity damage (`doesCastModeDealDamage`).
  - Added rapid pre-release dome collapse (`computeZenithCollapseScale`) followed immediately by sustained purple-white light emission (`computeZenithLightEmissionIntensity`).
  - Emphasized deep purple dome hues and added digital/geometric shell effects evoking an atomic nucleus, orbiting electron orbitals, and stepped PCB electronic circuit traces (`AtomicBlastRenderer`), alongside a dome-sized ground magic circle matching the dome radius while keeping the effects around the caster identical to Normal Atomic.
  - Reduced interior screen overlay & fog tinting inside the dome to a subtle light-purple wash (`AtomicClientEffects.computeZenithInteriorTintAlpha`).
- **Utsusemi Blood Fang (`空蝉の血牙`) & Utsusemi Atomic (`空蝉の亜斗美吊苦`) Overhaul**:
  - Implemented `UtsusemiSwordEntity` & `UtsusemiSwordRenderer`:
    - *Utsusemi Blood Fang* summons 5 swords around the caster, points their blade tips toward the target, and launches them in homing arcs.
    - *Utsusemi Atomic* (Fenrir's Katana & Jet-Black Sword) summons 9 swords with all tips pointing straight upward (`+90°`), then transforms them sequentially one by one into 9 `UtsusemiDragonEntity` (`UtsusemiDragonRenderer`) dragons that swarm, chase targets, and execute two-stage jaw crunch attacks.
- **Witch's Scythe (`魔女の大鎌`) & Blood Queen's Scythe (`血の女王の鎌`) Overhaul (`AuroraMagicAttackEntity` & `AuroraMagicAttackRenderer`)**:
  - *Witch's Scythe — Crimson Lance Assault (`赤き槍の強襲`)*: Spawns a pulsing crimson mana orb that shoots fluid, water-like magic jets curving in mid-air to track targets.
  - *Witch's Scythe — Fragment of Calamity: Dark Scythe (`災厄の一端・暗き大鎌`)*: Unleashes dark crimson-violet scythe waves, Bleed + Magic Inhibition, and blood-lightning bursts.
  - *Blood Queen's Scythe — Blood Downpour (`血の驟雨`)*: Manifests airborne undulating blood pools that extend curved blood lances bending through mid-air to track and impale targets.
  - *Blood Queen's Scythe — Blood Twin Shadows (`血の双影`)*: Enriched with abundant blood effects—erupting 6 airborne blood pools with curving lances alongside two crossing slashes and a central slash, deep Bleed (`+3`), Magic Inhibition, dual blood rings, and vampiric healing.
- **Game Balance Adjustments**:
  - Tuned Aurora (boss stats & *Witch's Scythe*) to be strictly stronger than Utsusemi/Fenrir (*Demon Katana: Utsusemi* & *Jet-Black Sword* Utsusemi Atomic).
  - Scaled Zeta's (`ZetaEntity` and `ZetaDaggerItem`) overall attack damage, melee magic bonuses, and skill/parry damage to `0.8x`.

### 日本語
- **空に向かって放つ「I AM ATOMIC」(`CAST_MODE_ZENITH`) の改修**:
  - ダメージを与えない仕様へ変更しました。
  - 発動時にドームが一瞬で収縮し、直後に瞬時発光して一定時間維持する演出へ刷新しました。
  - ドームの紫色を強調し、原子核・電子軌道・電子回路を連想させるデジタル＆幾何学エフェクトでドームを包むとともに、ドーム展開と同じ円の大きさの魔法陣を地面に展開し、プレイヤー周囲の演出は通常のアトミックと共通化しました。
  - ドーム内部の画面・霧の着色を、視界を妨げない薄紫程度に抑えました。
- **空蝉の血牙の改修 (`UtsusemiSwordEntity`)**:
  - 使用者周囲に5本の剣を召喚し、剣先が攻撃対象の方向を向いたうえで、各剣が対象を追尾しながら飛翔して攻撃するよう刷新しました。
- **空蝉の亜斗美吊苦の改修 (`UtsusemiSwordEntity` / `UtsusemiDragonEntity`)**:
  - 使用者の周囲に9本の剣をすべて剣先上向きで召喚し、発動時に剣が1本ずつ順番に9体のドラゴンへと変化して、9体それぞれが対象を追尾し噛み砕くように攻撃する仕様へ刷新しました（『妖刀・空蝉』および『漆黒の剣』へ実装）。
- **魔女の大鎌＆血の女王の鎌の改修 (`AuroraMagicAttackEntity`)**:
  - **魔女の大鎌『赤き槍の強襲』**: 赤い魔力の球を生成し、水を噴射するような流動的エフェクトの魔力を放出して空中で曲がりながら対象を追尾します。第2スキルは **『災厄の一端・暗き大鎌』** として暗紅紫の大鎌連撃＆紫電血魔力バーストを放ちます。
  - **血の女王の鎌『血の驟雨』**: 空中に血液の溜まりを生成し、そこから伸びた血液の槍が空中で軌道を曲げながら対象を追尾して突き刺さります。
  - **血の女王の鎌『血の双影』**: 血液演出を大幅強化し、空中の血液溜まり6基からの曲折追尾槍・深紅の交差斬撃2発と中央斬撃1発・出血3スタック・血霧＆吸血回復を放ちます。
- **ゲームバランス調整**:
  - 空蝉の技のオリジナルであるアウロラ（ボス性能・『魔女の大鎌』）が、フェンリル／『妖刀・空蝉』／空蝉の亜斗美吊苦より強くなるよう性能を調整しました。
  - ゼータ（ボス『ゼータ』および『影の双剣』）の全体の攻撃力・スキル火力を `0.8倍` に調整しました。

---

## [1.0.6] - Visual Overhaul, Ep. 20 Dome Atomic & Dedicated 3D Models (Forge 1.20.1)

### English
- **New Mod Icon**:
  - Updated `logo.png` and documentation/release icon assets (`400x400` RGBA PNG) with the newly provided Shadow artwork.
- **3D Sculpted Shadow Coat Overhaul & Dynamic Billowing Physics (`ShadowCoatModel`, `SlimeArmorModel`)**:
  - Overhauled Shadow's 3D coat geometry and `256x256` double-sided texture (`shadow_coat.png`) + full-bright emissive overlay (`shadow_coat_glow.png`) and custom Slime Suit armor item icons (`slime_suit_*.png`):
    - **Hood & Gold-Aglet Ribbons**: 45-degree rotated 3D forehead diamond crest (`♦`), sloped purple-lined brow arches, neck drapes, 2-stage tapered assassin hood peak, and 3-joint billowing ribbons terminating in 3D gold aglet ornaments.
    - **3-Stage Giant Wing Collar, Amethyst Brooch & Chevron Breastplate**: Continuous throat-to-shoulder collar sweeps, recessed royal-purple inner liners, pointed wing apexes, rear gold collar crest, 45-degree gold-bezeled glowing amethyst throat brooch (`♦`), 3D chevron-ribbed slime breastplate, gold-notched lapels, enclosed side walls, dorsal spine diamond core, and wrapped front/back X-belts.
    - **Sleeves, 3-Joint 9-Panel Tattered Skirt, Glider Wings & V-Winged Boots**: Bicep strap buckles, twin raised forearm gold rings, 2-stage flared royal-purple bell cuffs, 3-joint 9-panel tattered trench coat skirt (adding front-diagonal lapel sweeps and alpha-cutout ragged streamer tips `_tip`), 2-stage articulated slime glider wings, diamond-filigree thigh plates, and 3D V-winged knee boots.
  - Added traveling multi-panel wind wave physics (`CoatPhysics.computePanelRipple`) across all coat skirt panels with phase offsets, organic wind-gust envelopes, and amplified amplitude while sprinting, charging *I am Atomic*, or gliding.
- **Episode 20 Colossal Pre-Blast Dome & Zenith Sublimation Pillar**:
  - Faithfully reproduced the TV Anime Season 1 Episode 20 sequence (`CAST_MODE_ZENITH`) in `AtomicBlastEntity`, `AtomicBlastRenderer`, and `AtomicClientEffects`: **prior to the explosion**, a colossal city-enclosing hemispherical mana dome (`computeZenithPreDomeRadius`, expanding rapidly to 100% `maxRadius` by `"I"`) unfolds over the entire battlefield with 3 concentric dome shells, 16 geodesic meridian circuit ribs, 5 latitude rings, 16 vertical perimeter Nakanishi pylons, city-wide ground circuit traces, ascending zenith convergence waves, a top apex crown seal, and dome boundary containment.
  - Upon `"atomic"` release, instead of cratering the ground, the pre-deployed colossal dome redirects and sublimates straight upward into a massive 3-layer **Zenith Sublimation Pillar** (`computeZenithPillarRadius`) with counter-rotating double helices and 4-tier cloud-parting sky canopy rings—clearing rain/thunderstorms into a starry sky while keeping ground blocks 100% intact.
  - Updated Boss Shadow (`ShadowEntity`) to automatically unleash the Episode 20 Zenith Dome Atomic when casting Normal Atomic during rain or thunderstorms.
- **Dedicated High-Detail Skins, Glow Maps & 3D Attire Models**:
  - **Aurora (`AuroraAttireModel`, `aurora.png`, `aurora_glow.png`, `aurora_attire.png`)**: Rebuilt Aurora's 64×64 slim skin (ruby-crimson eyes, gothic corset with crimson cross-lacing, velvet choker, thigh-high stockings) and added a dedicated 3D model featuring a crimson rose hairpin, 2-joint cheek locks, 3-stage flowing violet hair, 6-panel billowing gothic dress, undulating blood-mana tendrils, detached bell sleeves, and buckled boots.
  - **Yukime — Legendary Golden Nine-Tailed Kitsune (`YukimeAttireModel`, `yukime_glow.png`, `yukime_attire.png`)**: Added sky-blue eye & obi glow map and a dedicated 3D model (`256x256` atlas) featuring 2-stage fox ears, ornate Oiran kanzashi hairpins & chignon, plush white-gold fox-fur shoulder stole, sapphire-indigo & gold brocade Oiran Obi, 5-panel kimono skirt, **9 × 4-segment voluminous golden-furred Kitsune tails** with golden prayer-bead rings, gravity-draped furisode sleeves, white tabi, and lacquered black-gold geta sandals.
  - **Complete 17-Character Canon Skins, Glow Maps & Dedicated 3D Models**: Replaced every remaining shared placeholder (`KagemasuAttireModel`) with anime / *Master of Garden* bespoke 64×64 skins, emissive glow overlays (`lambda_glow.png`, `freya_glow.png`, `lili_glow.png`, `beatrix_glow.png`, `annerose_glow.png`, etc.), dedicated attire atlases (`128x128` / `256x256`), and articulated `AbstractAttireModel` classes across all 17 `KagemasuArchetype` entities:
    - **No. 559 Victoria (`VictoriaAttireModel`)**: Lavender bangs shadowing her left eye, dark veil headpiece with blue diamond gem & horns, gold-trimmed Shadow Garden collar, and 5-panel tattered cape with pale-pink inner lining.
    - **No. 11 Lambda (`LambdaAttireModel`)**: Tanned dark-elf drill instructor skin, ash-grey swept hair, right black eyepatch, officer epaulets & crimson-gold aiguillette cord, belt pouches, and 3-panel split military coat.
    - **No. 13 Nu (`NuAttireModel`)**: Seamless dual-form toggle between Shadow Garden stealth assassin attire (shawl, dagger belt, 3-panel coat) and Mitsugoshi clerk disguise (ribbon tie & vest lapels) with persistent 3-stage chestnut hair.
    - **Blood Queen Elisabeth (`ElisabethAttireModel`, upgraded `256x256`)**: Blood-Moon tiara with ruby veil chains, tall crimson-lined vampire wing collar, 3-stage cascading snow-white hair + side hair wings, floating Blood-Moon sovereign halo, dual-layered progenitor bat wings, undulating crimson blood ribbons, and 5-panel velvet ballgown.
    - **Olivier (`OlivierAttireModel`, `256x256`)**: Elf ears, golden paladin circlet with azure gem, white-gold pauldrons & cuirass, 3-joint radiant angel light wings, floating Sanctum Halo, cerulean-lined cape, and armored skirt.
    - **Hero Freya (`FreyaAttireModel`)**: Royal gold crown-diadem, platinum-silver braids, sovereign mantle & lion-crest pauldrons, 3-joint golden-crimson heroic wings, crimson-lined royal cape, and tassets.
    - **Saintess of Salvation Lili (`LiliAttireModel`)**: 2-stage golden leopard ears, saintess circlet & veil, white-gold priestess shawl, 3-joint radiant saintess wings, 3-segment golden leopard tail, and 4-panel flowing saintess robes with front sash.
    - **War Goddess Beatrix (`BeatrixAttireModel`)**: Elf ears, pale platinum-blonde locks, lowered traveler hood collar & shoulder mantle, 5-panel billowing traveler cloak, slim combat bracers, and thigh-high riding boots.
    - **Claire Kagenou (`ClaireAttireModel`)**: Jet-black hair with crimson rear ribbon, Midgar navy-gold academy collar & ribbon, pleated skirt, glowing left-arm Aurora stigma band, plus awakened Aurora mana veil ribbons & seal ring.
    - **Annerose Nichtsehen (`AnneroseAttireModel`)**: Cobalt-blue bob cut with silver-gold hairband, silver-cobalt Vegalta cuirass, asymmetric pauldrons, articulated half-cape, and pleated combat tunic skirt.
    - **Jack the Ripper (`JackRipperAttireModel`)**: Cracked porcelain jester mask, 2-joint drooping bell hat tails, crimson ruffled collar, 4-panel harlequin coattails, 3 orbiting lethal playing cards, and curled jester boots.
    - **Jimina Seinen (`JiminaAttireModel`)**: Overhanging shaggy dark bangs, messy rear hair, shabby shoulder mantle, plain worn left-hip scabbard (`saya`), tattered apprentice cloak, and cloth-wrapped boots.
    - **Aurora, Yukime (9×4-segment golden kitsune tails), Ragnarok, Fenrir & Nelson**: Complete dedicated 3D models & textures wired via `EminenceShadowClient` and `KagemasuHeroRenderer`.
- **100%-Fidelity Performance Optimization**:
  - Added precomputed dome-vein, meridian rib, latitude ring, and magic-circle LUTs, double-precision helix angle-addition recurrence, zero-allocation camera-relative math, and hoisted integer RGBA colors in `AtomicBlastRenderer`, `AtomicClientEffects`, and projectile renderers.
  - Eliminated per-frame heap allocations across coat skirt ripple and Yukime 9-tail kinematics (`PanelRippleScratch`, `KitsuneTailScratch`), cached HUD string/component widths in `ManaHudOverlay`, and cached `ForgeConfigSpec` reads in `Config` via `ModConfigEvent`.
  - Added lock-free volatile idle fast-paths on active server/client tracking sets (`SlimeArmorEvents`, `AtomicBlastEntity`, `ShadowEntity`, `JohnSmithEntity`, `KagemasuHeroEntity`, `CombatMarkHelper`), cached synced entity metadata and projectile velocity rotations, merged barrier containment entity scans, and tightened chunk/section/Y-bounds loops in `SphereDestroyer` and `DirectionalDestroyer` while preserving 100% visual, numerical, and claim/permission fidelity.

### 日本語
- **新MODアイコンの刷新**:
  - 新アイコン画像を `400×400` RGBA PNG へ変換し、`logo.png` およびドキュメント／リリース用アイコン一式へ反映しました。
- **シャドウの3Dロングコート全面改修＆多関節揺らめき物理演出 (`ShadowCoatModel`, `SlimeArmorModel`)**:
  - シャドウの3Dコート造形および表裏塗り分け `256×256` テクスチャ（`shadow_coat.png`）・3Dコート発光レイヤー（`shadow_coat_glow.png`）・スライムスーツ防具アイコン4種（`slime_suit_*.png`）を全面的に作り込みました：
    - **目深フード＆3関節金金具リボン**: 45°回転立体ダイヤ紋章（`♦`）、紫裏地付き傾斜ブラウアーチ、首元ドレープ、2段テーパー後頭部フード、先端に金の飾り金具（アグレット）を備えた3関節リボン。
    - **3段巨大立ち襟・紫宝玉ブローチ・V字リブ胸甲・金ノッチ付きラペル**: 喉元からの連続襟スイープ、段差付きロイヤルパープル内張り、鋭角な襟先端、45°金枠アメジスト宝玉ブローチ（暗所発光）、V字シェブロン構造の3Dスライム胸部装甲、金ノッチピーク付きラペル、脇腹サイドパネル、背骨ダイヤコア、表裏交差Xベルト。
    - **袖・3関節9パネル裂け裾・2関節滑空翼・V字ウィング長靴**: 二の腕金バックル、前腕2連金リング、2段フレアのロイヤルパープル×金ベルカフス、前身頃からのフロントスイープを加えた **3関節×9パネル構成の裂けたロングコート裾**（先端アルファ抜きダメージ加工）、2関節スライム滑空翼、太ももダイヤ紋様プレート、立体V字ウィング付きニーブーツ。
  - 各コート裾パネルに左右位相差の伝播波と突風エンベロープを与える `CoatPhysics.computePanelRipple` を実装し、待機時の微風・ダッシュ・Atomic詠唱・滑空に応じて上段→中段→裂けた裾先端へと立体的に波打つよう強化しました。
- **アニメ第20話 事前展開・超巨大ドーム＆天蓋昇華ピラー完全再現**:
  - `CAST_MODE_ZENITH` の演出・物理をアニメ1期第20話（王都決戦 vs ベアトリクス＆アイリス）通りに全面刷新：**爆発前の溜め・詠唱段階から**、王都全域を包み込む **超巨大な3層青紫半球魔力ドーム（`computeZenithPreDomeRadius`：詠唱『I』の時点で最大半径 `maxRadius` に到達）** を事前展開します。ドーム表面の測地線回路リブ（経線16本＋緯線5段）、外周16本の垂直魔力パイロン、全域へ走る直角魔力回路網、ドーム壁面を頂点へ駆け上がる天頂収束リング、ドーム頂上の天蓋魔法陣、およびドーム外周の逃走阻止結界を実装しました。
  - 発射（`releaseTick`）の瞬間、地上のブロックを一切破壊せず、事前展開された超巨大ドームの全魔力を垂直真上（天頂）へ偏向・昇華させ、二重螺旋を伴う極大の3層 **天蓋昇華ピラー**（`computeZenithPillarRadius`）と4層の雲割りスカイリングで雨雲・雷雲を一撃で吹き飛ばし快晴の星空へと変えます（シャドウボスも雨天・雷雨時に自動発動）。
- **アウロラ・伝説の金毛九尾 ユキメ・敵ボス専用の精細スキン＆3Dモデル**:
  - **アウロラ (`AuroraAttireModel`)**: スキン（紅玉の瞳、チョーカー、深紅編み上げゴシックコルセット、ニーハイ）を刷新し、薔薇髪飾り・2段姫カット・3段ロング紫髪・6枚2関節ドレス・血魔力触手・ベル袖・ゴシックブーツを備えた専用3Dモデルを構築しました。
  - **伝説の金毛九尾 ユキメ (`YukimeAttireModel`)**: 空色の瞳＆帯宝石の発光レイヤーを追加し、2段狐耳・花魁簪＆日本髪・白金狐毛皮ストール・紺金錦帯＆垂れ帯・5枚着物・**金色珠輪付きの9×4関節「金毛九尾」**・振袖垂れ・白足袋＆黒金高下駄の専用3Dモデル（256×256）を構築しました。
  - **全17体 Kagemasu／アニメ原作キャラクター専用スキン・発光レイヤー＆3Dモデル完全刷新**:
    - **559番 ウィクトーリア (`VictoriaAttireModel`)**: 左目を隠す藤色前髪、青宝玉＆角装飾付き黒ベール、金縁七陰立ち襟、桃色裏地の5枚ボロマント。
    - **11番 鬼教官 ラムダ (`LambdaAttireModel`)**: 褐色ダークエルフ肌＆右目黒眼帯、灰髪スイープ、教官用エポレット＆紅金飾緒、腰ポーチ、3枚軍服ロングコート。
    - **13番 ニュー (`NuAttireModel`)**: 3段波打ち栗毛を維持したまま、シャドウガーデン暗殺装備とミツゴシ店員変装（リボンタイ＆ベスト襟）をリアルタイム切替。
    - **紅き血の女王 エリザベート (`ElisabethAttireModel`, `256×256`超強化)**: ルビー鎖付きブラッドムーン・ティアラ、真紅裏地の吸血鬼翼襟、3段雪白髪＋横髪翼、浮遊血月輪、二重始祖蝙蝠翼、うねる血のリボン、5枚ベルベット・ボールガウン。
    - **始まりの聖騎士 オリヴィエ (`OlivierAttireModel`, `256×256`)**: エルフ耳、青宝玉付き聖騎士サークレット、白金胸甲＆大肩甲、3関節光の天使翼、浮遊聖域ヘイロー、水色裏地マント＆腰鎧スカート。
    - **不可逆の英雄 フレイヤ (`FreyaAttireModel`)**: 黄金戴冠、白銀三つ編み横髪、獅子肩甲、3関節金紅英雄翼、真紅裏地王マント＆タセット鎧。
    - **救世の聖女 リリ (`LiliAttireModel`)**: 2関節黄金豹耳、聖女サークレット＆ベール、白金ショール、3関節聖女翼、3関節黄金豹尾、4枚聖女ローブ＆前帯。
    - **白銀の剣聖 ベアトリクス (`BeatrixAttireModel`)**: エルフ耳、白金ブロンド髪、フード襟＆肩マント、5枚旅装ロングクローク、金籠手＆乗馬長靴。
    - **クレア・カゲノー (`ClaireAttireModel`)**: 黒髪＆真紅後髪リボン、ミドガル学園襟＆胸リボン、プリーツスカート、左腕アウロラ聖痕バンド、覚醒時ベールリボン＆封印輪。
    - **アンネローゼ (`AnneroseAttireModel`)**: 蒼髪ボブ＆銀金カチューシャ、銀蒼胸甲＆非対称肩甲、片側マント＆プリーツ戦衣。
    - **切り裂きジャック (`JackRipperAttireModel`)**: ひび割れ道化師仮面、2関節ベル帽尾、真紅フリル襟、4枚道化師燕尾コート、周回トランプ3枚、先端カール長靴。
    - **ジミナ・セーネン (`JiminaAttireModel`)**: 目元を覆うボサ髪前髪＆後ろ髪、薄汚れた肩マント、安物木鞘、ボロ修行マント＆布巻きブーツ。
    - **アウロラ・ユキメ・ラグナロク・フェンリル・ネルソン** を含む全17 `KagemasuArchetype` が専用3Dモデルで描画されます。
- **再現度100%維持・徹底パフォーマンス最適化**:
  - `AtomicBlastRenderer`・`AtomicClientEffects`・飛び道具レンダラーに事前計算LUT（ドーム脈動位相・測地線リブ・緯線リング・魔法陣）、倍精度角度漸化式による二重螺旋、ゼロアロケーション視点相対座標、およびRGBA整数色事前変換を実装しました。
  - シャドウのコート波打ちとユキメ九尾モーションの毎フレームレコード生成をゼロ化（`PanelRippleScratch` / `KitsuneTailScratch`）し、`ManaHudOverlay` の文字列幅キャッシュおよび `Config` の `ModConfigEvent` キャッシュを導入しました。
  - アイドル時のロック取得を完全排除する `volatile` 高速パス（`SlimeArmorEvents` / `AtomicBlastEntity` / `ShadowEntity` / `JohnSmithEntity` / `KagemasuHeroEntity` / `CombatMarkHelper`）、同期データ＆速度回転角キャッシュ、結界エンティティ走査の統合、さらに `SphereDestroyer` / `DirectionalDestroyer` のチャンクセクション・Y範囲絞り込みを実施し、描画・数値・保護判定・仕様の再現度100%を維持したまま大幅な軽量化を達成しました。

---

## [1.0.5] - Spec Consistency, Combat Bugfixes & Polish (Forge 1.20.1)

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
  - Fixed missing `+3.0` sword base damage in `AbstractSevenShadowWeapon` (all 20 subclass weapons match exact spec values), unconditional `Zekka` application on `ArchetypeBladeItem` Skill 1, full-suit check for `V` morph and server crouch check for Shadow Mastery sword materialization, Mithril HUD label, and added all 11 missing items/weapons to `CreativeModeTabs.COMBAT`.
- **Recipe Advancements, Localization & Documentation**:
  - Added 5 data-driven recipe unlock advancements covering all 51 recipes.
  - Added missing `en_us.json` / `ja_jp.json` keys (`combat_mark` death messages, Mithril HUD, Alpha Sword passive tooltip, Shadow Mastery chat fix, gender-neutral companion error).
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
  - 七陰武器共通基底（`AbstractSevenShadowWeapon`）に欠落していた剣基礎ダメージ `+3.0` を復元し全20種を仕様値へ統一。クリエタブ未登録11種追加、ミスリルSword専用HUD表記、フルスーツ必須の `V` 変身、サーバー側スニーク検証を実装。
- **レシピブック解放・翻訳・ドキュメント全面改訂**:
  - 全51レシピを素材入手で段階解放する5つのレシピ進捗（Advancement）を追加し、翻訳漏れ（`650` キー完全一致）と破損していた `wiki/03`〜`08` を全面修正。

## [1.0.0] - Initial Release (Forge 1.20.1)

### English
- **Initial Official Release (`v1.0.0`) for Minecraft Forge 1.20.1 (`47.4.28` / `[47,)`).**
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
- **Minecraft Forge 1.20.1 向け初回正式リリース（`v1.0.0`）。**
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
