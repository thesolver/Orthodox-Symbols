# Changelog

*Designed by Alan Fahrner with Juno, his AI assistant (built on Grok Bot). The glyphs were drawn by AI from Alan's direction and reviewed by him.*

## 0.2.000 PRE-RELEASE (2026-10-25)

**This is a pre-release. During this pre-release stage we may change or remove any symbol.** Until version 1.0, existing symbols, key assignments and private-use codes may change or be remapped as feedback arrives, and the author reserves the right to do so. This replaces the earlier "assignments never change once released" rule until 1.0.

Versioning changed: the project is now numbered as pre-releases (0.x) until a stable 1.0. This build was first made as "v2.000" and is renumbered 0.2.000 (head.fontRevision 0.2, name table "Version 0.200; pre-release"). The first draft tagged `v1.000` on GitHub is now treated as pre-release 0.1.

### Update to 0.2.000 (2026-10-25, night): Reserved Font Name, traced blessing hand, slimmer fish

Still version 0.2.000 pre-release; replaces the earlier 0.2.000 files. No keys or codes changed. 65 glyphs total.

- **General pre-release note:** During this pre-release stage we may change or remove any symbol. This sentence is now in the README banner, the guide/PDF banner and here.
- **Reserved Font Name:** "Orthodox Symbols" is now declared a Reserved Font Name under the SIL OFL 1.1. The copyright line (OFL.txt, font name table nameID 0, README, guide/PDF) is now `Copyright 2026 Alan Fahrner, with Reserved Font Name "Orthodox Symbols".` The license description (nameID 13) mentions the Reserved Font Name; nameID 14 is still https://openfontlicense.org. In plain words: people who just use the font are not affected; anyone who shares a **modified** version must give it a different name.
- **Blessing hand (`B`, U+E0AB, unchanged) is now a traced, experimental drawing.** It was traced from Alan's icon reference (the hand was cut out of the picture, made solid black and turned into a vector outline, with a flat cuff band added): index and middle fingers raised, ring finger curled to the thumb with a small loop, little finger out on the left. It is rough, and it may change or be removed in a future version, so please don't depend on it. This replaces the side-profile drawing below. The guide's key chart and sample rows show the new hand.
- **Fish (`j`, U+E0AC, unchanged) slimmed:** a longer, thinner almond body whose two arcs cross into the tail, so it reads lighter, with the tail loop still open at small sizes.

**Weak at 12 px:** the traced blessing hand's finger gaps and loop only read from about 16 px.

### Update to 0.2.000 (2026-10-25, late evening): side-profile blessing hand, credit line, web instructions

Still version 0.2.000 pre-release; replaces the earlier 0.2.000 files. No keys or codes changed. 65 glyphs total.

- **Blessing hand redrawn in side profile** (`B`, U+E0AB, unchanged), after the icon reference Alan sent (original simplified drawing, not a trace): the sleeve and a banded cuff come in from the lower right; the hand rises to the upper left with the palm facing left; index finger extended and leaning slightly, middle finger curving over toward it, ring finger and thumb touching in a round loop on the left. Fingers are smooth tapered strokes with a wide gap between the two free fingers so they stay apart at small sizes. The little finger is folded away behind the ring finger (not drawn separately) so the loop stays open at 12 to 16 px. Replaces the two front-facing drawings.
- **Biretta** (`K`, U+E0E1) is the solid silhouette drawn earlier today (wide square cap, raised side ridges, pompom; no white lines). Two pinholes where the pompom met the ridges are now filled, so it is one solid shape.
- **Credit line** added to the README, this changelog, the first page of the Word guide and PDF, and the font's name table (nameID 10 description; nameID 9 designer "Alan Fahrner with Juno, his AI assistant (built on Grok Bot)"). The copyright line stays "Copyright 2026 Alan Fahrner".
- **"Use it on a website"** section in the README and the Word guide/PDF: uploading the WOFF2 (and TTF fallback), a ready-to-paste `@font-face` rule with `font-display: swap`, a `.orthodox-symbols` class, typing symbols as HTML character references with their private-use codes (`&#xE02D;`) versus typing the key, accessibility (`aria-hidden`, or `role="img"` with `aria-label`), the pre-release warning, and a placeholder "CDN-hosted version: coming later."

**Weak at 12 px:** the blessing hand reads as a hand with a raised finger and a loop, but the middle finger's curl and the cuff only show from about 16 px; clear from 24 px.

### Update to 0.2.000 (2026-10-25, evening): headwear, second deep bow, cassock priest, new blessing hand

Still version 0.2.000 pre-release; this replaces the earlier 0.2.000 files. 65 glyphs total.

**Moved (keys changed; private-use codes kept unless noted, since codes are the stable address):**

| Symbol | Old key | New key | Code |
|---|---|---|---|
| Blessing hand (redrawn) | `Y` | `B` (B for Blessing) | U+E0AB (unchanged) |
| Sanctus bell tree, outline / filled | `b` / `B` | `l` / `L` | U+E02C / U+E02D (unchanged) |
| Cross in a circle | `L` | `Q` (letter-like: a circle with a mark) | U+E0B1 (unchanged) |
| Clerical collar | `:` | `"` (and curly “ ”) | U+E083 (unchanged) |
| Priest in cassock (added earlier today) | `/` | `:` (shares the key with the Orthodox priest) | U+E082 → U+E087 (odd code, like every symbol without an outline) |
| Deep bow / metania (now "Eastern deep bow") | `.` | `>` | U+E095 (unchanged) |
| Kneel | `>` | `/` | U+E097 (unchanged) |

Postures now run along the bottom-right keys from shallowest to deepest: `,` stand, `<` bow, `.` Western deep bow, `>` Eastern deep bow / metania, `/` kneel.
`Y` and `y` now hold the mitres; `"` and curly “ ” no longer show the placeholder.

**Added:**
- Priest in a plain cassock (bare head, beard, row of buttons, no kamilavka, no side lines), `:`, U+E087.
- Western deep bow (profound bow from the waist: legs straight, torso level, hands hanging well above the floor), `.`, U+E099. The existing deep bow is now named the Eastern deep bow / metania (reaching to the ground).
- New group **Headwear** U+E0E0–E0FF on `k t z f y`; lowercase = Eastern hat (even code), Shift = its nearest Western counterpart (odd code):
  `k` kamilavka (Russian) U+E0E0, `K` biretta U+E0E1, `t` kalimavkion (Greek, "kalpaki") U+E0E2, `T` saturno U+E0E3,
  `z` skufia U+E0E4, `Z` zucchetto U+E0E5, `f` klobuk U+E0E6 (`F` / U+E0E7 free), `y` Eastern mitre U+E0E8, `Y` Western mitre U+E0E9.

**Changed (drawing):** the blessing hand is redrawn as a simpler, bolder silhouette after an icon reference Alan sent (original drawing, not a trace):
index finger straight up, middle finger curving over toward it, ring finger and thumb closing a round loop, little finger curled, wide gaps between the fingers, and a banded sleeve cuff at the wrist.

**Weak at 12 px (clear from about 16 to 24 px up):** zucchetto vs saturno (both low domes; the saturno's wide brim is the only difference), biretta vs kamilavka, the Eastern mitre's medallion and the blessing hand's loop.

### Remapped: grouped key map (breaking; allowed because this is a pre-release)

**Every key and every private-use code has changed** from the 0.1 draft and from the first "v2" build.
Documents made with either earlier file will show different symbols with 0.2.000. 54 glyphs total (0.1 had 22).

- Symbols are grouped by theme, each with its own keyboard area and PUA block, with spare keys and codes in every group:
  Crosses U+E000–E01F (digit row), Worship vessels and objects U+E020–E05F (mnemonic letters),
  Buildings U+E060–E07F (`- = [ ]`), People and postures U+E080–E09F (`; : '` and `, < . >`),
  Icon and Christ symbols U+E0A0–E0BF (letters), Service-book marks U+E0C0–E0DF (V, R).
- Pairs share one key: plain key = thin outline (even code), Shift = filled (next odd code).
  Symbols without an outline take the Shift key and odd code, leaving the plain key and even code for a future outline.
- Letter-like symbols take their letter in both cases, first come first served: IC `I`, XC `X`, Chi-Rho `P`, Versicle `V`, Response `R`;
  fish (ICHTHYS) moved to `j` because I was taken.
- Mnemonic letters for objects: `w/W` Western thurible, `e/E` Eastern censer, `c/C` candle, `d/D` candlestick, `u/U` chalice,
  `a/A` altar, `b/B` bell tree, `h/H` hymnal, `G` Gospel Book, `N` Bible.
- Icon group: `O` cruciform halo, `M` mandorla, `Y` blessing hand, `S` eight-pointed star, `L` cross in a circle.
- **The Mac Option-key outline twins are gone** (∞ § ¶ • ﬁ ﬂ ‡ ° · ‚ no longer map to anything); every outline now has a normal key.
- Curly ‘ ’ map to the choir symbol (Word autoformats `'`); curly “ ” show the placeholder.
- PUA codes are documented as the stable address of each symbol (they will not move if a key ever does), frozen from 1.0.
- Guide and test sheet show the map grouped, with the key under each symbol; README has the grouped table and the reasoning.

### Changed (drawings)
- **Bell:** the single hand bell is replaced by a Sanctus bell tree with three bells.
- **Outlined crosses:** outline stroke thinned from 62 to 44 units (of 1000), checked to stay visible at 12 px.

### Added
- Budded cross **with** the slanted footrest (outline and filled).
- Latin cross and Greek cross (outline and filled).
- Candle in an altar candlestick and altar (outline and filled).
- IC and XC, each with a titlo.
- Priest, clerical collar, choir member, fish (outline style).
- Cross in a circle, cruciform halo, blessing hand, mandorla.
- Bible and Gospel Book.
- Thin outline twins of the bell tree, Western thurible, Eastern censer, candle, chalice, hymnal, both churches, steeple and onion tower.
- `OrthodoxSymbols.woff2` web font built alongside the TTF.
- README: pre-release banner; install steps for Windows, macOS and Linux.
- OS/2 fsType 0 (installable), so Word and PDF can embed the font.
- User guide (`OrthodoxSymbols_Guide.docx` and `.pdf`): font embedded in the .docx as obfuscated .odttf; (font embedded as obfuscated .odttf) and PDF: grouped key chart with the key and code under each symbol, sizes 10/14/24/48 pt, how-to, boxed pre-release banner, install steps for Windows/macOS/Linux, boxed reserved-keys note, sample cue sheet, license summary and full OFL text.

### Reserved keys
- New **placeholder glyph**: every printable ASCII key not in the README tables now shows one small hollow square with broken edges instead of falling back to another font. Space is still a space.
- Reserved keys show a placeholder square; they may become symbols in later versions, so don't use them. They must not be relied on for ordinary text. When a key gets a real symbol, its placeholder is replaced.
- Pre-release (before 1.0): listed keys and codes may also change or be remapped. From 1.0 on, released key assignments and private-use codes will never change.

### Not done / weak
- Posture figures and V/R deliberately have no outline versions.
- Chi-Rho and the eight-pointed star have no outline versions yet.
- At 12 px the blessing hand, cruciform halo, Gospel Book and clerical collar read only as rough shapes; they are clear from about 24 px up.
- Headwear: no outline versions (none planned).

## 0.1 (first draft, tagged v1.000 on GitHub, 2026-10-25)

First draft: 22 glyphs on digits, Shift+digits, V and R, duplicated at U+E000 to U+E015. SIL OFL 1.1.
