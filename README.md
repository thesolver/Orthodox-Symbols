# Orthodox Symbols (version 0.2.001, PRE-RELEASE)

*Designed by Alan Fahrner with Juno, his AI assistant (built on Grok Bot). The glyphs were drawn by AI from Alan's direction and reviewed by him.*

> ## ⚠️ PRE-RELEASE: NOT FINAL
> **Version 0.2.001 is a pre-release test version, shared for feedback.**
> **During this pre-release stage we may change or remove any symbol.**
> Existing symbols may be redrawn, replaced or removed, and **key assignments and private-use codes may be changed or remapped** as feedback arrives. The author reserves the right to do so.
> Documents made with a pre-release may look different after you install a later version.
> Key assignments will be frozen only at **version 1.0**. Until then, nothing is guaranteed to stay the same.

A Wingdings-style symbol font for liturgical documents. Every glyph is original,
drawn for this font.
Nothing is traced or copied from Wingdings or any other font. (The one exception to "drawn from scratch" is the
experimental blessing hand, which was traced from Alan's own icon reference; see the note above.)

> **Blessing hand (`B`) is experimental.** It is a rough drawing traced from Alan's icon reference.
> It may change or be removed in a future version, so please don't depend on it in documents you need to keep.

Single-color glyphs: color them in Word like any text (e.g. dark red).
Outlined glyphs use a thin line (44 of 1000 units) so they look delicate at large
sizes but still show at 12 px.

## Installing the font

In short: **install `OrthodoxSymbols.ttf` whichever way your system normally installs fonts**, then restart the program you want to use it in (Word, LibreOffice, etc.).

- **Windows 10 / 11:** right-click `OrthodoxSymbols.ttf` and choose **Install** (just you) or **Install for all users** (needs an administrator). On Windows 11 you may need **Show more options** first. You can also drag the file onto **Settings > Personalization > Fonts**.
- **macOS:** double-click `OrthodoxSymbols.ttf`; Font Book opens; click **Install**. If Font Book shows a validation warning, choose to install anyway.
- **Linux** (the standard fontconfig way, works on most desktops):
  ```sh
  mkdir -p ~/.local/share/fonts
  cp OrthodoxSymbols.ttf ~/.local/share/fonts/
  fc-cache -f
  ```
  For all users, copy it to `/usr/local/share/fonts/` with `sudo` and run `sudo fc-cache -f`. Many desktops also install a font when you double-click it.
- **Updating to a newer version:** remove or replace the old copy first (Windows: Settings > Fonts > Orthodox Symbols > Uninstall; macOS: remove it in Font Book; Linux: overwrite the file and rerun `fc-cache -f`), then install the new one and restart the program.
- **Websites:** nothing to install; upload the font files to your site instead (see "Use it on a website" below).

## Use it on a website

You can host the font on your own website today. **CDN-hosted version: coming later.**

> The font is a **pre-release**: symbols, keys and private-use codes may still change before 1.0.
> Keep the copy you uploaded, and check the README of any newer version before you replace it.

1. **Upload the font files** to your site, for example into a `fonts/` folder:
   `OrthodoxSymbols.woff2` (what browsers use) and `OrthodoxSymbols.ttf` (fallback for very old browsers).
   Keep `OFL.txt` with them; the license allows web use. If the fonts live on a *different* domain from
   your pages (for example a separate static or media server), that server must send the header
   `Access-Control-Allow-Origin` for your site, or browsers will refuse the font.
2. **Paste this CSS** into your stylesheet (adjust the paths if your folder is different; they are
   relative to the CSS file):

   ```css
   @font-face {
     font-family: "Orthodox Symbols";
     src: url("fonts/OrthodoxSymbols.woff2") format("woff2"),
          url("fonts/OrthodoxSymbols.ttf") format("truetype");
     font-weight: 400;
     font-style: normal;
     font-display: swap;
   }
   .orthodox-symbols {
     font-family: "Orthodox Symbols";
     font-weight: normal;
     font-style: normal;
     line-height: 1;
   }
   ```

   `font-display: swap` shows the page text at once and swaps the symbols in when the font has loaded.
3. **Type a symbol** inside an element with that class. The most reliable way is the symbol's
   **private-use code** written as an HTML character reference, `&#x` + the code + `;`:

   ```html
   <span class="orthodox-symbols" aria-hidden="true">&#xE02D;</span> Ring the bells.
   <span class="orthodox-symbols" aria-hidden="true">&#xE097;</span> Kneel.
   ```

   The codes are in the key mapping tables below (U+E02D is the filled Sanctus bell tree, so it is
   written `&#xE02D;`; U+E000 is the Russian cross outline, `&#xE000;`). They are the **stable address**
   of each symbol: if a symbol's key ever moves, its code stays. While the font is still loading, or if
   it fails, a code shows as nothing or an empty box instead of a wrong letter.

   You can also type the **keyboard character** (`<span class="orthodox-symbols">L</span>`), the same
   as in Word. It is easier to read in the HTML, but it shows a plain "L" until the font loads (or if it
   fails), and it would show a different symbol if that key is ever reassigned.
4. **Accessibility.** Screen readers do not understand private-use characters (they say nothing,
   "private use", or the plain letter), so:
   - if the words next to the symbol already say what it means, hide the symbol: `aria-hidden="true"`;
   - if the symbol stands on its own, give it a name:
     `<span class="orthodox-symbols" role="img" aria-label="Kneel">&#xE097;</span>`;
   - never rely on a symbol (or its red color) alone for meaning; keep the written instruction too.
   Copy and paste and search engines see the code or key, not the meaning; that is normal for symbol fonts.
5. **Color and size** work like text: `color: #b00000;` for rubric red, `font-size: 1.5em;` to enlarge.

Example page:

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <link rel="stylesheet" href="style.css">   <!-- contains the CSS above -->
</head>
<body>
  <p><span class="orthodox-symbols" style="color:#b00000" aria-hidden="true">&#xE0C1;</span>
     Blessed are they that dwell in thy house.</p>
  <p>At the Sanctus, ring the bells
     <span class="orthodox-symbols" role="img" aria-label="bells">&#xE02D;</span>, then kneel
     <span class="orthodox-symbols" role="img" aria-label="kneel">&#xE097;</span>.</p>
</body>
</html>
```

## How the keys are laid out (0.2.000 grouped map)

The symbols are grouped by theme. Each group has its own area of the keyboard and its own
block of private-use codes, and **every group keeps spare keys and spare codes** so a new
symbol can later go next to its relatives instead of wherever a key happens to be free.

Rules used, in order:

1. **Letter-like symbols sit on their letter, both cases**, first come first served:
   IC on **I**, XC on **X**, Chi-Rho on **P** (X was already taken by XC, and the Rho looks like a P),
   Versicle on **V**, Response on **R**. When a second symbol wanted a taken letter it went to a nearby
   key in its group (fish/ICHTHYS wanted I, so it is on **J**, the old Latin form of I, right next to I on the keyboard).
2. **Pairs share one key: plain key = thin outline, Shift = filled.** Lowercase/uppercase for letters
   (c = candle outline, C = filled candle), unshifted/shifted for digits and punctuation (1 and !).
   There are **no Option-key tricks** any more; everything is typeable on Windows, Mac and Linux.
3. A symbol that has **no outline yet** is on the **Shift** key (uppercase or shifted), and its plain key
   is kept free for a future outline (for example G is the Gospel Book and g is waiting for its outline).
4. Objects use **mnemonic letters** where possible (A altar, C candle, H hymnal, G Gospel, B Blessing hand).
   When the letter was taken, the symbol went to a neighboring or free key (candlestick D next to C, Bible N next to B, bell tree L).
5. **Unused keys show the placeholder square.**

Word tip: Word may capitalize the first letter of a line, which turns an outline (c) into its filled twin (C).
Press Ctrl+Z (Cmd+Z) right after, or turn off "Capitalize first letter of sentences" in AutoCorrect.
Word also turns `'` into a curly quote; both give the choir symbol.

## Key mapping

Codes: in each pair the outline is the even code and the filled twin the next odd code. A symbol without
an outline uses the odd code and leaves the even one free.

**Private-use codes (PUA) are the stable address of each symbol.** If a symbol's key ever has to move,
its code stays the same, so text entered by code (Insert > Symbol, Alt+X in Word, `&#xE0A1;` on the web)
keeps working. During the pre-release, codes may still change too (see the banner); from 1.0 on they are frozen.

### Crosses (U+E000 to U+E01F) · digit row; 6 to 0 kept free for more crosses

| Key | PUA | Symbol |
|---|---|---|
| `1` | U+E000 | Russian Orthodox cross, thin outline |
| `!` (Shift+1) | U+E001 | Russian Orthodox cross, filled |
| `2` | U+E002 | Budded (trefoil) cross, no footrest, outline |
| `@` (Shift+2) | U+E003 | Budded cross, no footrest, filled |
| `3` | U+E004 | Budded cross with slanted footrest, outline |
| `#` (Shift+3) | U+E005 | Budded cross with slanted footrest, filled |
| `4` | U+E006 | Latin cross, outline |
| `$` (Shift+4) | U+E007 | Latin cross, filled |
| `5` | U+E008 | Greek cross, outline |
| `%` (Shift+5) | U+E009 | Greek cross, filled |
| `6` to `0`, `^ & * ( )` | U+E00A to U+E01F | free for future crosses |

### Worship vessels and objects (U+E020 to U+E05F) · letters, lowercase = outline, uppercase = filled

| Key | PUA | Symbol |
|---|---|---|
| `w` / `W` | U+E020 / U+E021 | Western Rite thurible (W for Western), outline / filled |
| `e` / `E` | U+E022 / U+E023 | Eastern Rite censer (E for Eastern, next to W), outline / filled |
| `c` / `C` | U+E024 / U+E025 | Candle, outline / filled |
| `d` / `D` | U+E026 / U+E027 | Candle in altar candlestick (C taken; D is next to C), outline / filled |
| `u` / `U` | U+E028 / U+E029 | Chalice (C taken; U is cup-shaped), outline / filled |
| `a` / `A` | U+E02A / U+E02B | Altar, outline / filled |
| `l` / `L` | U+E02C / U+E02D | Sanctus bell tree, three bells, outline / filled (moved from `b`/`B` in this build: B is now the Blessing hand; L was the nearest sensible free pair) |
| `h` / `H` | U+E02E / U+E02F | Hymnal, outline / filled |
| `G` | U+E031 | Gospel Book, ornate cover (`g` / U+E030 kept for an outline) |
| `N` | U+E033 | Bible (B taken; N is next to B) (`n` / U+E032 kept for an outline) |
| | U+E034 to U+E05F | free for future vessels and objects |

### Buildings (U+E060 to U+E07F) · top-right punctuation; `\` and `|` kept free

| Key | PUA | Symbol |
|---|---|---|
| `-` / `_` | U+E060 / U+E061 | Western church, outline / filled |
| `=` / `+` | U+E062 / U+E063 | Orthodox church (dome), outline / filled |
| `[` / `{` | U+E064 / U+E065 | Steeple, outline / filled |
| `]` / `}` | U+E066 / U+E067 | Onion-dome bell tower, outline / filled |
| | U+E068 to U+E07F | free for future buildings |

### People and postures (U+E080 to U+E09F) · people on `; : ' "`, postures on `, < . > /` from shallow to deep; `?` kept free

| Key | PUA | Symbol |
|---|---|---|
| `;` | U+E081 | Priest, Orthodox (kamilavka, beard, phelonion, pectoral cross) |
| `:` (Shift+;) | U+E087 | Priest in a plain cassock (bare head, beard, buttons); shares the key with the Orthodox priest |
| `'` (also curly ‘ ’) | U+E085 | Choir member (book and note) |
| `"` (Shift+', also curly “ ”) | U+E083 | Clerical collar |
| `,` | U+E091 | Posture: stand |
| `<` (Shift+,) | U+E093 | Posture: bow (moderate, upper body inclined) |
| `.` | U+E099 | Posture: Western deep bow (profound bow from the waist; torso level, hands well above the floor) |
| `>` (Shift+.) | U+E095 | Posture: Eastern deep bow / metania (reaching down to touch the ground) |
| `/` | U+E097 | Posture: kneel |
| | U+E080, U+E082, U+E084, U+E086, U+E088 to U+E08F, U+E098, U+E09A to U+E09F | free for more people (E08x) and postures (E09x) |

The postures run left to right along the bottom row from shallowest to deepest. Their codes did not change
when their keys moved (codes are the stable address); the new Western deep bow got the next free code.

### Icon and Christ symbols (U+E0A0 to U+E0BF) · their letters, or nearby letters

| Key | PUA | Symbol |
|---|---|---|
| `I` `i` | U+E0A1 | IC (with titlo) |
| `X` `x` | U+E0A3 | XC (with titlo) |
| `P` `p` | U+E0A5 | Chi-Rho |
| `O` | U+E0A7 | Cruciform halo (a circle with a cross: letter-like O) |
| `M` | U+E0A9 | Mandorla |
| `B` | U+E0AB | Blessing hand (IC XC), EXPERIMENTAL: a rough drawing traced from Alan's icon reference (index and middle fingers raised, ring finger curled to the thumb, little finger out on the left, cuff band at the wrist). It may change or be removed in a future version, so don't depend on it. B for Blessing; `b` kept for an outline |
| `j` | U+E0AC | Fish (ichthys), outline style: a long, slim almond body whose two arcs cross into the tail (ICHTHYS wanted I; J is the old form of I). `J` / U+E0AD kept for a filled fish |
| `S` | U+E0AF | Eight-pointed star |
| `Q` | U+E0B1 | Cross in a circle (letter-like: Q is a circle with a mark; moved from `L`). `q` kept for an outline |
| | U+E0B2 to U+E0BF | free for future icon symbols |

### Service-book marks (U+E0C0 to U+E0DF)

| Key | PUA | Symbol |
|---|---|---|
| `V` `v` (also U+2123) | U+E0C1 | Versicle ℣ |
| `R` `r` (also U+211F) | U+E0C3 | Response ℟ |

### Headwear (U+E0E0 to U+E0FF) · `k t z f y`: lowercase = Eastern hat, Shift = its nearest Western counterpart

These are the only symbols that do not follow the outline/filled rule (there are no hat outlines).
On each key the lowercase letter (even code) is an Eastern hat and Shift (odd code) is the Western hat that plays the closest role.

| Key | PUA | Symbol |
|---|---|---|
| `k` | U+E0E0 | Kamilavka, Russian style (stiff, widening upward, flat top) |
| `K` | U+E0E1 | Biretta (solid silhouette: wide square cap, a raised ridge at each side, pompom) |
| `t` | U+E0E2 | Kalimavkion, Greek style (straight "stovepipe" with a flat brim at the top; this is the hat called "kalpaki") |
| `T` | U+E0E3 | Saturno (cappello romano: low round crown, very wide brim) |
| `z` | U+E0E4 | Skufia (soft cap rising to a soft point, folds shown as seams) |
| `Z` | U+E0E5 | Zucchetto (shallow skullcap with a little stem) |
| `f` | U+E0E6 | Klobuk (kamilavka with the monastic veil down both sides). `F` / U+E0E7 free (no Western counterpart) |
| `y` | U+E0E8 | Eastern (Byzantine) mitre: crown with icon medallion and cross |
| `Y` | U+E0E9 | Western mitre: pointed, with orphreys and two lappets |
| | U+E0EA to U+E0FF | free for more headwear |

### Free keys today

`6 7 8 9 0 ^ & * ( )` (crosses), `\ |` (buildings), `?` (postures), `` ` ~ ``, `F` (headwear),
the lowercase keys kept for future outlines `b g n o m s q`, and `J` (kept for a filled fish).
All of them show the placeholder square.

## Reserved keys

Reserved keys show a placeholder square; they may become symbols in later versions, so don't use them.

Every printable key not listed in the tables above (see "Free keys today") shows the same small, broken-edged hollow square. It is a plain
"nothing here yet" mark, not a symbol, and it has no private-use code. Reserved keys must not
be relied on for ordinary text. The author reserves the right to map any key to a symbol in a
future version; when that happens, the placeholder on that key is replaced.

**Pre-release rule (before 1.0):** listed keys and codes may also change or be remapped (see the
banner at the top). This replaces the earlier rule that assignments never change once released.
**From version 1.0 on:** released key assignments and private-use codes will never change; new
symbols will only go on reserved keys and new codes.

## Files

- `OrthodoxSymbols.ttf`: the font, version 0.2.001 pre-release (name table: "Version 0.201; pre-release") (1000 units/em, ascent 850, descent 200; OS/2 fsType 0 = installable, so it can be embedded in Word and PDF)
- `OrthodoxSymbols.woff2`: the same font compressed for websites
- `OrthodoxSymbols_Guide.docx` (Word, font embedded) and `OrthodoxSymbols_Guide.pdf`: pre-release banner, install steps for Windows/macOS/Linux, key chart, sizes, how-to, website use, reserved-keys note, sample cue sheet, license
- `CHANGELOG.md`: what changed in each version, including any keys that moved
- `OFL.txt`: the SIL Open Font License 1.1

## Feedback

Please report problems or ideas (a symbol that reads badly, a missing symbol, a key that feels wrong) in this repository's **Issues**.

## Version numbers

Pre-releases are numbered 0.x (this is 0.2.001; the font's `head.fontRevision` is 0.201 and the name table says "Version 0.201; pre-release", following the Google Fonts MAJOR.MINOR style). The first draft published on GitHub as `v1.000` is now treated as pre-release 0.1. Version 1.0 will be the first stable release, when key assignments freeze.

## License

SIL Open Font License 1.1. See `OFL.txt`.
Copyright 2026 Alan Fahrner, with Reserved Font Name "Orthodox Symbols".

This font is a free pre-release, provided as is, without warranty. See OFL.txt for the full terms.

**What the Reserved Font Name means, in plain words** (this summary is not the license; `OFL.txt` is what counts):

- **If you just use the font** (install it, type with it, embed it in Word files or PDFs, put it on your website, share
  the unchanged files): **nothing changes for you.** You don't have to do anything.
- **If you make a modified version** (change, add or remove glyphs, or convert it in a way that changes it) and share it,
  that version **must use a different name**, not "Orthodox Symbols". This keeps people from confusing a changed copy
  with the original.

Designed by Alan Fahrner with Juno, his AI assistant (built on Grok Bot). The glyphs were drawn by AI from Alan's direction and reviewed by him.
