# Soru-gotchi Evolution System

This document defines the full mechanics for the **Soru-gotchi**, a classic Tamagotchi-style mini pet system in Soru Shiti.

## Design Philosophy
- This is a **classic Tamagotchi** experience.
- It should feel and function like traditional 1990s–2000s Tamagotchi devices.
- All text related to the Soru-gotchi should be in **Japanese** (kanji and katakana).
- The device should have a nostalgic retro feel.

## 1. Tamagotchi Device Shell (Visual Style)

The Soru-gotchi should appear inside a **classic Tamagotchi-style shell** with the following characteristics:

- Small handheld device aesthetic (like the original Tamagotchi or Digimon devices).
- The device has a **frame/shell** around the screen (retro clean UI frame).
- Three buttons at the bottom (classic A / B / C layout):
  - **A Button**: Usually for selecting / feeding
  - **B Button**: Confirm / Play
  - **C Button**: Cancel / Status / Clean
- The device can be opened and closed (minimized) by the player.

## 2. Inner Screen (LCD Green Screen)

- The pet lives and interacts inside a **retro green LCD screen** style.
- The screen should have the classic low-resolution, pixelated green LCD look (similar to original Tamagotchi).
- All animations, the pet, poop, food, and mini-games should be displayed inside this green LCD area.
- The screen should feel separate from the main game’s painterly art style (intentionally retro).

## 3. Stage Distinction

| Stage     | Description                          | Examples |
|-----------|--------------------------------------|----------|
| **Baby**  | Initial form after hatching          | Various baby sprites |
| **Adult** | Intermediate evolution stage         | F_borg, M_borg, F_rogue, M_rogue |
| **Final** | Final evolution stage                | Butler, Seraphim, Porcelina, etc. |

**Evolution Flow:** Egg → Baby → Adult → Final

## 4. Adult Evolutions

| Adult Form   | Gender | Theme    | Leads Toward |
|--------------|--------|----------|--------------|
| F_borg       | Female | Cyborg   | Good Tier    |
| M_borg       | Male   | Cyborg   | Good Tier    |
| F_rogue      | Female | Rogue    | Bad Tier     |
| M_rogue      | Male   | Rogue    | Bad Tier     |

Gender is chosen randomly (50/50) when evolving from Baby to Adult and carries over to the Final stage.

## 5. Final Evolutions + Gender

### Good Tier
- Butler (M)
- Seraphim (M and F)
- Porcelina (F)
- Leo (M)

### Average Tier
- Robert (M)
- Reseda (F)
- Odessa (F)
- Fyodor (M)
- Coal (M)
- Junko (F)

### Bad Tier
- Lucan (M)
- Chatelaine (F)
- Ergot (F)
- Maleus (M)
- Yomi (F)
- Kreg (M)

## 6. Baby Stage Groups

| Baby Group       | Location in Sprite Sheet | Behavior |
|------------------|--------------------------|----------|
| **Good Babies**      | Top 2 rows               | Strongly leans toward Good finals |
| **Flexible Babies**  | Middle rows (3–5)        | Can go Good, Average, or Bad depending on care |
| **Bad Babies**       | Bottom 2–3 rows          | Strongly leans toward Bad finals |

## 7. Evolution Rules (Classic Tamagotchi Style)

- **Good care** → Higher chance of Good Tier finals
- **Average care** → Most likely Average Tier finals
- **Bad / Neglected care** → Higher chance of Bad Tier finals

The Flexible Babies have the most variance based on player interaction.

## 8. Classic Tamagotchi Mechanics

The Soru-gotchi should support traditional Tamagotchi features such as:

- Feeding
- Playing mini-games
- Cleaning (poop removal)
- Checking status / calling for attention
- Aging and evolution

All interface text should be in **Japanese**.

## 9. Unlock & UI

- Unlocks after building the first structure.
- Remains available only while the player has at least 1 structure.
- Appears as a small subtle tab labeled **ソルゴッチ** in the bottom left.
- Show an unlock notification the first time it becomes available.
- The full device (shell + green LCD screen) can be minimized or hidden.

## 10. Additional Rules

- Gender is locked once the creature reaches the Adult stage.
- The system should feel simple, nostalgic, and true to classic Tamagotchi.
- Evolution should feel rewarding for good care.