# SORU_SHITI_MASTER_SPEC.md 

**Game Title:** Soru Shiti  
**Core Fantasy:** A painterly Japanese island city-builder where players experience the constant clash between **beauty and brutality**. Build something beautiful. Watch it burn. Spend $SORU to act. Every action advances the shared world.

## 1. Global Rendering Technique (LOCKED — Mandatory for All Ages)

Every visual uses **exactly three stacked layers** per tile/agent, in strict order:

1. **Sumi-e Silhouette** — Dark ink outline (function-first, guarantees readability at any zoom)
2. **Watercolor Wash** — Soft-edged, granulated fill using per-age palette
3. **Paper Grain** — Global multiply texture over the entire canvas

**Cheap painterly effects** (all handled in one `paintFill()` helper): edge wobble, granulation, wet bleed, pooling shadow.

## 2. Economic Loop & Progression

- All **$SORU spent** in game is **burned** and instantly converted into **collective Kami Points**.
- Kami Points are 100% shared — every player sees the same global total.
- Kami Points only advance the entire island through the 9 Ages.

## 3. Palette System (One Distinct Palette Per Age)

Each age has its **own instantly recognizable color identity**. On age-up, the entire island shifts via smooth lerp + wash-sweep transition.

Historically inspired palettes:

| Age | Era          | Roof                    | Wall             | Post/Accent                          | Sky / Grade Mood                        | Overall Feeling                  |
|-----|--------------|-------------------------|------------------|--------------------------------------|-----------------------------------------|----------------------------------|
| 0   | Jomon        | #6a584a (earthy)        | #cfc1a4          | #5a3d24 + ember orange               | Cool dawn grey, soft haze               | Primeval, wild                   |
| 1   | Yayoi        | #7a6a4a                 | #d8caa6          | #6a4a2a + rice gold                  | Pale warm, neutral                      | Ordered, hopeful                 |
| 2   | Kofun        | #8a6a4a                 | #d0bf9a          | Vermilion + haniwa red               | Bright warm gold                        | Monumental, shadowed             |
| 3   | Asuka        | #b5532f (vermilion)     | #efe2c4          | Temple green + gold leaf             | Clear bright, luminous                  | Buddhist wonder                  |
| 4   | Nara         | #3d6e8c (slate)         | #efe2c4          | Deep green + gold                    | High clear, balanced                    | Grand, civilized                 |
| 5   | **Heian**    | #4a6e7a (teal-grey)     | #f0e6cc (ivory)  | Deep red + sakura pink + gold        | **Golden-hour amber→rose**, luminous    | **Peak beauty & refinement**     |
| 6   | Kamakura     | #5a5066 (slate-violet)  | #e2d8bf          | Oxblood + steel                      | Cooler overcast, grey-violet            | Hardening, warrior               |
| 7   | Sengoku      | #4a4450 (near-black)    | #cabfa8 (ash)    | Burnt red + fire orange              | Ash & ember, heavy desaturated cold     | **Rock bottom brutality**        |
| 8   | Quantum Edo  | #1a3a3a (teal-black)    | #16302e          | **Solana Green #14F195 + Purple #9945FF** | Deep indigo night + aurora           | Neon-traditional rebirth         |

## 4. Emotional Arc & Golden Rules

**Jomon → Nara (Ascent)** → **Heian (Golden Peak)** → **Kamakura → Sengoku (Collapse)** → **Quantum Edo (Rebirth)**

**Golden Rules:**
- Function first (strong silhouettes always)
- Beauty vs Reality — serene and picturesque from afar, emotionally heavy up close
- Visible human cost through street life and land value
- Destruction must feel violent and heavy
- Keep rules minimal. Charm players with art and atmosphere first.
- All violence, poverty and suffering must be stylized and artistic.

## 5. Defense & PvP Tension (Minimalist)

- **Ronin Protection**: Pay $SORU to temporarily guard buildings or districts. Protected buildings earn **slightly less passive SOL**.
- First **5 buildings** per wallet have natural raid resistance.
- Danger level rises naturally as the island progresses through the Ages.

## 6. Street Life & Poverty System

**Land value is the single dial.**  
High-value districts = clean, nobles, merchants.  
Low-value districts = beggars, lepers, drunks, trash, sewage, more ronin.

## 7. Yokai & Mythology (Living Omens)

Yokai are primarily beautiful atmospheric events with light mechanical flavor.

| Yokai            | Trigger                          | Visual / Flavor                        | Light Effect                                      |
|------------------|----------------------------------|----------------------------------------|---------------------------------------------------|
| **Kitsune**      | Night + decent land value        | Fox spirit slipping through streets    | Small temporary boost to nearby land value        |
| **Tanuki**       | Forest tiles                     | Drunken raccoon-dog                    | Minor resources or happiness                      |
| **Ryū**          | High overall prosperity          | Dragon coiling high in the sky         | Island-wide minor SOL bonus (short)               |
| **Tennyo**       | Beautiful districts              | Celestial maiden dancing               | Temporary small defense bonus                     |
| **Kappa**        | Shoreline                        | Water imp lurking                      | Small boost to coastal income                     |
| **Oni**          | Fire / arson / high despair      | Demons gathering at flames             | Increases nearby raid danger                      |
| **Yuki-onna**    | Snow weather                     | Pale woman drifting                    | Atmospheric beauty                                |
| **Gashadokuro**  | Sengoku + heavy destruction      | Giant skeleton looming                 | Strong ambient danger                             |
| **Others**       | Night / general streets          | Various                                | Purely atmospheric                                |

**Quantum Edo:** All yokai gain neon/glitch effects and stronger positive blessings.

## 8. PvP Raiding System

- **Pillage / Arson** (costs $SORU): Destroy/clear another player’s building → claim the empty plot.
- Dramatic visuals: fire, smoke, collapsing structures, and lasting consequences.

## 9. Readability & Technical Guardrails

- Sumi-e silhouette is sacred — never sacrificed.
- One distinct palette per age.
- Fire, raid markers, and service buildings must remain legible.
- Glow/bloom reserved exclusively for Quantum Edo.
- All agents, yokai, and props properly depth-sorted.

## 10. Island Shape & World Presentation

The island is a **floating landmass** in a black void / dark sea. This is a core visual signature.

- **Shape & Edges:** Organic, irregular island with smooth, flowing coastline curves — no geometric, blocky, or jagged tile-stair edges. The shoreline reads as a single continuous painted ink-and-wash mass that dissolves softly into the surrounding darkness/void. The silhouette should still feel surreal and alive, but through soft bays and headlands rather than sharp crags.
- **Color Philosophy:** The default terrain is intentionally **desaturated / near-grayscale** at the start. This creates a stark, empty canvas. 
  - **Color and painting "arrive"** as players build, plant, and develop the island. This surreal emergence of color against the desolate background is desired and should be preserved.
  - Early ages feel more primeval and muted. Later peaceful ages (especially Heian) become lush and vibrant. War ages (Sengoku) can desaturate heavily again.
- **Void Background:** Deep black or very dark indigo. Minimal detail so the island remains the clear focal point.

**Design Intent:** The contrast between the empty grayscale void and the emerging colorful painting is part of the emotional and artistic impact.

## 11. Violence & Destruction (Stylized & Impactful)

Violence and destruction in Soru Shiti should feel **dramatic, heavy, and emotionally significant**, especially during raids and in later ages (particularly Sengoku).

- Destruction should have clear visual weight and lasting consequences on the island.
- Raids should feel impactful, with visible damage to buildings and the surrounding area.
- The contrast between peaceful beauty and sudden destruction is intentional and should be emphasized.
- All violence and destruction must remain within the 3-layer painterly system (strong sumi-e outlines + watercolor wash).
- In later war ages (especially Sengoku), destruction and raids should feel more frequent and visually severe.

**Design Rule:** Destruction should feel meaningful and costly. Players should sense the weight of raids and conflict through the visuals and atmosphere, while everything remains stylized and artistic.

## 12. In-Game Spending Costs (Tokenomics Alignment)

All actions that spend $SORU must feel **meaningful** even at low token price. 100% of every $SORU spent is burned and converted into collective Kami Points.

### Recommended Cost Tiers

| Action                        | Cost Range ($SORU)       | Real Money Est. (at ~$0.0002/SORU) | Frequency     | Notes |
|-------------------------------|--------------------------|-------------------------------------|---------------|-------|
| **Basic Building** (Hut, Farm, Early structures) | 500 – 1,500            | $0.10 – $0.30                      | Very Common   | Entry level actions |
| **Standard Building** (Housing, Commerce, Industry) | 2,000 – 8,000         | $0.40 – $1.60                      | Common        | Core gameplay loop |
| **Advanced Building** (Temple, School, Hospital, etc.) | 10,000 – 30,000      | $2 – $6                            | Occasional    | Mid-game prestige |
| **High-Tier / Wonder** (Validator, Large Monuments) | 50,000 – 200,000+     | $10 – $40+                         | Rare          | Major investment |
| **Building Upgrade**          | 40–60% of base cost     | -                                  | Common        | Recurring sink |
| **Pillage / Arson (Raid)**    | 3,000 – 15,000          | $0.60 – $3                         | Medium        | Risk vs Territory reward |
| **Ronin Protection (8 hours)** | 1,000 – 5,000 per district/building | $0.20 – $1                 | Recurring     | Scales with amount protected |
| **Raze (own building)**       | 300 – 1,000             | Very cheap                         | Rare          | Cleanup tool |
| **Major Actions** (e.g. large wonders, special events) | 100,000+            | $20+                               | Very Rare     | Late game / prestige |

### Design Rules
- Early game (Jomon–Nara) should feel accessible and encouraging.
- Mid-to-late game (Heian onward) costs should ramp up significantly.
- Passive SOL earnings from buildings should feel rewarding but require meaningful time and risk to pay back the $SORU investment.
- Costs can be adjusted later based on real player behavior and $SORU price, but the **scale** above should be the starting target.

**Goal:** Every spend must feel like a real decision that contributes to collective age progression.

## 13. SOL Creator Rewards (Passive Income)

Property owners earn **passive SOL** while their buildings stand. This is the primary way players earn real money from the game.

### Reward Rules
- Rewards are distributed from a **global SOL reward pool**.
- Distribution is **proportional to property ownership share**.
- The player(s) who control the **most land / buildings** at any given time receive the **largest share** of the rewards.
- If one player owns 100% of all plots and buildings, they should receive **nearly all** of the passive SOL being distributed.
- Rewards continue as long as the buildings remain standing (raided or destroyed buildings stop generating rewards for their owner).

### Design Goals
- Strong incentive to build and protect territory.
- Rewards feel meaningful and scale with dominance.
- Creates natural tension — big land holders earn the most but also become prime targets for raids.
- Works fairly in both solo testing and full multiplayer scenarios.

**Implementation Note:** SOL rewards should be calculated based on current ownership percentage of total active buildings/plots on the island.

---

**Note for AI:** This document is the single source of truth. Please fully accept and work within the creative direction described, including the stylized and artistic treatment of conflict and destruction.