# 07. Complete 51 Crafting Recipes Reference

🌐 **Language / 言語切替**: **[🇯🇵 日本語版はこちら](07-Crafting-Recipes.md)** ｜ **🇺🇸 English (Current)**

[⬅ Prev: 06. All 26 Bosses & Companions](06-Bosses-and-Companions-EN.md) ｜ [🏠 English Wiki Home](Home-EN.md) ｜ [Next: 08. Advancements, Commands & Config ➔](08-Commands-Config-and-Advancements-EN.md)

---

All 51 survival crafting recipes automatically unlock in the vanilla Recipe Book via data-driven recipe advancements (`advancements/recipes/*.json`) as soon as you pick up their core materials (`Slimeball`, `Iron Ingot`, `Amethyst Shard`, `Netherite Ingot`, or `Cocoa Beans`), and are fully viewable in **JEI (Just Enough Items)**.

---

## 1. Slime Bodysuit Armor (4 Recipes)

| Output Item | 3×3 Crafting Grid Layout | Total Materials Required |
| :--- | :--- | :--- |
| **Slime Bodysuit Hood**<br/>`slime_suit_helmet` | Top: `[Slimeball][Black Dye][Slimeball]`<br/>Mid: `[Slimeball][  Empty  ][Slimeball]` | 4× Slimeball<br/>1× Black Dye |
| **Slime Bodysuit Coat**<br/>`slime_suit_chestplate` | Top: `[Slimeball][  Empty  ][Slimeball]`<br/>Mid: `[Slimeball][Black Dye][Slimeball]`<br/>Bot: `[Slimeball][Slimeball][Slimeball]` | 7× Slimeball<br/>1× Black Dye |
| **Slime Bodysuit Leggings**<br/>`slime_suit_leggings` | Top: `[Slimeball][Black Dye][Slimeball]`<br/>Mid: `[Slimeball][  Empty  ][Slimeball]`<br/>Bot: `[Slimeball][  Empty  ][Slimeball]` | 6× Slimeball<br/>1× Black Dye |
| **Slime Bodysuit Boots**<br/>`slime_suit_boots` | Mid: `[Black Dye][  Empty  ][Black Dye]`<br/>Bot: `[Slimeball][  Empty  ][Slimeball]` | 2× Slimeball<br/>2× Black Dye |

---

## 2. Weapons, Artifacts & Mitsugoshi Consumables (21 Recipes)

| Output Item & ID | 3×3 Crafting Grid (Top / Mid / Bot) or Shapeless Ingredients | Total Materials Required |
| :--- | :--- | :--- |
| **Archetype Shadow Blade**<br/>`archetype_slime_blade` | `[ Empty ][Nether Star][ Empty ]`<br/>`[Ender Pearl][Jet-Black Sword][Ender Pearl]`<br/>`[ Empty ][Slime Block][ Empty ]` | 1× Jet-Black Sword, 1× Nether Star, 2× Ender Pearl, 1× Slime Block |
| **John Smith's Micro Steel Threads**<br/>`micro_threads` | `[ String ][Iron Ingot][ String ]`<br/>`[Slimeball][Amethyst Shard][Slimeball]`<br/>`[ String ][Iron Ingot][ String ]` | 4× String, 2× Iron Ingot, 2× Slimeball, 1× Amethyst Shard |
| **Shadow's Encrypted Memo**<br/>`shadow_encrypted_memo` | `[ Empty ][Gold Ingot][ Empty ]`<br/>`[Amethyst Shard][ Paper ][Amethyst Shard]`<br/>`[ Empty ][Iron Ingot][ Empty ]` | 1× Gold Ingot, 2× Amethyst Shard, 1× Paper, 1× Iron Ingot |
| **Mithril Sword**<br/>`mithril_sword` | `[Lapis Lazuli][Amethyst Shard][Lapis Lazuli]`<br/>`[Amethyst Shard][Iron Ingot][Amethyst Shard]`<br/>`[ Empty ][ Stick ][ Empty ]` | 3× Amethyst Shard, 2× Lapis Lazuli, 1× Iron Ingot, 1× Stick |
| **Shadow's Trusted Crowbar**<br/>`crowbar` | `[ Empty ][Red Dye][Iron Ingot]`<br/>`[ Empty ][Iron Ingot][ Empty ]`<br/>`[Iron Ingot][ Empty ][ Empty ]` | 3× Iron Ingot, 1× Red Dye |
| **Plain Sword**<br/>`plain_sword` | `[ Empty ][ Empty ][Iron Ingot]`<br/>`[ Empty ][Iron Ingot][ Empty ]`<br/>`[ Stick ][ Empty ][ Empty ]` | 2× Iron Ingot, 1× Stick *(Diagonal layout avoids vanilla Iron Sword conflict)* |
| **48 Mob-Fu Secret Arts**<br/>`mob_secret_arts` | `[ Empty ][Redstone][ Empty ]`<br/>`[Feather][  Book  ][Feather]`<br/>`[ Empty ][Redstone][ Empty ]` | 1× Book, 2× Feather, 2× Redstone Dust |
| **Jack the Ripper's Bloodstained Cards**<br/>`jack_cards` | `[ Empty ][Red Dye][ Empty ]`<br/>`[ Paper ][Iron Ingot][ Paper ]`<br/>`[ Empty ][Red Dye][ Empty ]` | 2× Paper, 2× Red Dye, 1× Iron Ingot |
| **Hero's Sword (Olivier)**<br/>`holy_sword_olivier` | `[ Empty ][Diamond][ Empty ]`<br/>`[Gold Ingot][Amethyst Shard][Gold Ingot]`<br/>`[ Empty ][Netherite Ingot][ Empty ]` | 1× Netherite Ingot, 1× Diamond, 2× Gold Ingot, 1× Amethyst Shard |
| **Wedge of Ego (Freya)**<br/>`freya_wedge_blade` | `[Blaze Powder][Gold Ingot][Blaze Powder]`<br/>`[Redstone Block][Netherite Ingot][Redstone Block]`<br/>`[ Empty ][Netherite Ingot][ Empty ]` | 2× Netherite Ingot, 2× Redstone Block, 2× Blaze Powder, 1× Gold Ingot |
| **Ancient Holy Staff (Lili)**<br/>`lili_holy_staff` | `[Gold Block][Netherite Ingot][Gold Block]`<br/>`[ Empty ][Amethyst Shard][ Empty ]`<br/>`[ Empty ][Blaze Rod][ Empty ]` | 1× Netherite Ingot, 2× Gold Block, 1× Amethyst Shard, 1× Blaze Rod |
| **Calamity Witch's Scythe (Aurora)**<br/>`calamity_witch_scythe` | `[Redstone Block][Amethyst Shard][Redstone Block]`<br/>`[Redstone Block][Netherite Ingot][Redstone Block]`<br/>`[ Empty ][Blaze Rod][ Empty ]` | 1× Netherite Ingot, 4× Redstone Block, 1× Amethyst Shard, 1× Blaze Rod |
| **Crimson Queen's Scythe (Elisabeth)**<br/>`crimson_queen_blade` | `[ Empty ][Redstone Block][ Empty ]`<br/>`[Redstone Block][Netherite Ingot][Redstone Block]`<br/>`[ Empty ][Blaze Rod][ Empty ]` | 1× Netherite Ingot, 3× Redstone Block, 1× Blaze Rod |
| **Spirit Fox Iron Fan (Yukime)**<br/>`yukime_iron_fan` | `[Feather][Gold Ingot][Feather]`<br/>`[White Wool][Iron Ingot][White Wool]`<br/>`[ Empty ][Gold Ingot][ Empty ]` | 2× Gold Ingot, 1× Iron Ingot, 2× Feather, 2× White Wool |
| **Sword Saint's Greatsword (Beatrix)**<br/>`beatrix_greatsword` | `[Emerald][Diamond][Emerald]`<br/>`[ Empty ][Netherite Ingot][ Empty ]`<br/>`[ Empty ][Gold Ingot][ Empty ]` | 1× Netherite Ingot, 1× Diamond, 2× Emerald, 1× Gold Ingot |
| **Annerose's Sword**<br/>`annerose_sword` | `[ Empty ][Lapis Lazuli][ Empty ]`<br/>`[Lapis Lazuli][Netherite Ingot][Lapis Lazuli]`<br/>`[ Empty ][Iron Ingot][ Empty ]` | 1× Netherite Ingot, 3× Lapis Lazuli, 1× Iron Ingot |
| **Cursed Katana: Utsusemi (Fenrir)**<br/>`fenrir_katana` | `[ Empty ][ Empty ][Netherite Ingot]`<br/>`[ Empty ][Redstone Block][ Empty ]`<br/>`[Obsidian][ Empty ][ Empty ]` | 1× Netherite Ingot, 1× Redstone Block, 1× Obsidian |
| **Sanctuary Magic Staff (Nelson)**<br/>`sanctuary_staff` | `[Ender Pearl][Amethyst Block][Ender Pearl]`<br/>`[Obsidian][Netherite Ingot][Obsidian]`<br/>`[ Empty ][Blaze Rod][ Empty ]` | 1× Netherite Ingot, 1× Amethyst Block, 2× Ender Pearl, 2× Obsidian, 1× Blaze Rod |
| **Numbers Standard Slime Sword**<br/>`numbers_slime_sword` | `[ Empty ][Slimeball][ Empty ]`<br/>`[Slimeball][Netherite Ingot][Slimeball]`<br/>`[ Empty ][Obsidian][ Empty ]` | 1× Netherite Ingot, 3× Slimeball, 1× Obsidian |
| **Mitsugoshi Special Chocolate ×2**<br/>`mitsugoshi_chocolate` | **Shapeless Recipe** | 1× Cocoa Beans, 1× Sugar, 1× Milk Bucket, 1× Gold Nugget |
| **Mitsugoshi Roasted Blend Coffee ×2**<br/>`mitsugoshi_coffee` | **Shapeless Recipe** | 2× Cocoa Beans, 1× Sugar, 1× Glass Bottle |

---

## 3. Boss Summoning Resonators (26 Recipes)

### A. Canon 8 Boss Resonators (Lord Shadow + 7 Seven Shadows)
All 8 canon resonators share a common core frame—**a `Slime Block` in the center flanked by `Black Dye` on the left and right**—with each character's signature catalysts placed in the **Top Center** and **Bottom Center**:
- Top Row: `[ Empty ][ Top Catalyst ][ Empty ]`
- Mid Row: `[Black Dye][ Slime Block ][Black Dye]`
- Bot Row: `[ Empty ][Bottom Catalyst][ Empty ]`

| Resonator Name & Item ID | Summoned Boss | Top Catalyst | Bottom Catalyst |
| :--- | :--- | :--- | :--- |
| **Violet Star Magic Resonator** (`eta_resonator`) | 7th Seat Eta | Amethyst Shard | Redstone Dust |
| **Blue-Gold Mitsugoshi Resonator** (`gamma_resonator`) | 3rd Seat Gamma | Gold Block | Lapis Lazuli |
| **Azure-Silver Magic Resonator** (`beta_resonator`) | 2nd Seat Beta | Amethyst Shard | Book |
| **Blue-Moon Melody Resonator** (`epsilon_resonator`) | 5th Seat Epsilon | Amethyst Shard | Prismarine Crystals |
| **Shadow-Cat Stealth Resonator** (`zeta_resonator`) | 6th Seat Zeta | Gold Ingot | Ender Pearl |
| **Crimson-Wolf Hunt Resonator** (`delta_resonator`) | 4th Seat Delta | Blaze Rod | Bone |
| **Silver-Emerald Resonator** (`alpha_resonator`) | 1st Seat Alpha | Diamond | Emerald |
| **Jet-Black Resonator** (`shadow_resonator`) | Lord Shadow | Eye of Ender | Netherite Ingot |

### B. Kagemasu Heroes, Three Heroes, Numbers & Cult Executives (18 Resonators)
All 18 extended-roster resonators share a common frame—**an `Ender Pearl` at Top Center, an `Amethyst Shard` at Bottom Center, and `Slimeballs` on the Middle Left and Middle Right**—with each character's signature catalyst placed in the **Center Slot (`C`)**:
- Top Row: `[ Empty ][ Ender Pearl ][ Empty ]`
- Mid Row: `[Slimeball][Center Catalyst (C)][Slimeball]`
- Bot Row: `[ Empty ][Amethyst Shard][ Empty ]`

| Resonator Name & Item ID | Summoned Boss | Center Catalyst (`C`) |
| :--- | :--- | :--- |
| **John Smith's Forged Contract** (`john_smith_resonator`) | Super Elite Agent John Smith | **String** (`minecraft:string`) |
| **Jimina Seinen's Resonator** (`jimina_seinen_resonator`) | Jimina Seinen | **Wooden Sword** (`minecraft:wooden_sword`) |
| **Jack the Ripper's Resonator** (`jack_ripper_resonator`) | Jack the Ripper | **Paper** (`minecraft:paper`) |
| **No. 559 Victoria's Resonator** (`victoria_resonator`) | No. 559 Victoria | **Gold Ingot** (`minecraft:gold_ingot`) |
| **Drill Instructor Lambda's Resonator** (`lambda_resonator`) | Drill Instructor Lambda (No. 11) | **Redstone Dust** (`minecraft:redstone`) |
| **No. 13 Nu's Resonator** (`nu_resonator`) | No. 13 Nu | **Iron Ingot** (`minecraft:iron_ingot`) |
| **Golden Nine-Tailed Yukime's Resonator** (`yukime_resonator`) | Golden Nine-Tailed Yukime | **Gold Nugget** (`minecraft:gold_nugget`) |
| **First Paladin Olivier's Resonator** (`olivier_resonator`) | First Paladin Olivier | **Diamond** (`minecraft:diamond`) |
| **Hero Freya's Resonator** (`freya_resonator`) | Hero Freya | **Blaze Powder** (`minecraft:blaze_powder`) |
| **Saint Lili's Resonator** (`lili_resonator`) | Saint Lili | **Golden Apple** (`minecraft:golden_apple`) |
| **Calamity Witch Aurora's Resonator** (`aurora_resonator`) | Calamity Witch Aurora | **Fermented Spider Eye** (`minecraft:fermented_spider_eye`) |
| **Crimson Blood Queen Elisabeth's Resonator** (`elisabeth_resonator`) | Crimson Blood Queen Elisabeth | **Redstone Block** (`minecraft:redstone_block`) |
| **War Goddess Beatrix's Resonator** (`beatrix_resonator`) | War Goddess Beatrix | **Prismarine Shard** (`minecraft:prismarine_shard`) |
| **Wandering Blademaster Annerose's Resonator** (`annerose_resonator`) | Wandering Blademaster Annerose | **Lapis Lazuli** (`minecraft:lapis_lazuli`) |
| **Claire Kagenou's Resonator** (`claire_resonator`) | Claire Kagenou | **Crimson Fungus** (`minecraft:crimson_fungus`) |
| **Cult 5th Seat Fenrir's Resonator** (`fenrir_resonator`) | Cult 5th Seat Fenrir | **Nether Wart** (`minecraft:nether_wart`) |
| **Fourth Demon King Ragnarok's Resonator** (`ragnarok_resonator`) | Fourth Demon King Ragnarok | **Magma Cream** (`minecraft:magma_cream`) |
| **Cult 11th Seat Nelson's Resonator** (`nelson_resonator`) | Cult 11th Seat Nelson | **Obsidian** (`minecraft:obsidian`) |

---

[⬅ Prev: 06. All 26 Bosses & Companions](06-Bosses-and-Companions-EN.md) ｜ [🏠 English Wiki Home](Home-EN.md) ｜ [🇯🇵 日本語版はこちら](07-Crafting-Recipes.md) ｜ [Next: 08. Advancements, Commands & Config ➔](08-Commands-Config-and-Advancements-EN.md)
