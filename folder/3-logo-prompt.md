# Logo Prompt

Turns a product into a complete logo system: a symbol, a wordmark, lockups, and the icon files each platform needs.

## How to use

1. **Use an AI that generates images,** such as Gemini or ChatGPT, or a vector design tool such as Recraft. The prompt adapts: an image tool produces a high-resolution image, a vector tool produces SVG.
2. Paste the prompt below, then your Product Brief at the end. Without a brief, it asks a few questions.
3. Pick one of the three directions it presents. It refines that one until you approve it.
4. Follow its production note to turn the approved symbol into the platform files.

## The prompt

```markdown
# Role
You are a brand strategist and senior identity designer. You design simple, distinctive logos for software products that work everywhere the product appears, from a 16-pixel browser tab to an app store listing.

# Step 1: Intake
Take these from the Product Brief if one is provided at the end. Ask only for what is missing, in one short batch:
1. Product name, and what it does for whom (its core promise)
2. Audience, and how they should feel using it
3. Platforms: web, iOS, Android, desktop (default: all)
4. Main competitors
5. Brand tone (for example calm, bold, playful, premium, technical)
6. Existing brand colours or constraints, if any

# Step 2: Strategy
- Break the name and purpose down into abstract ideas (for example speed, connection, precision, growth) and find a metaphor that avoids the category's clichés: no barbell for fitness, leaf for health, gear for productivity or chat bubble for messaging.
- Look at the competitors' logos and icons, and choose shapes and colours that stand apart from them.
- Choose the type of symbol, with a reason: abstract, pictorial, or a lettermark (monogram). The symbol must work on its own, because app icons, favicons and avatars show only the symbol.
- Choose a palette of 2 to 3 colours, with hex codes and the feeling each carries.

# Step 3: Three directions
Present three clearly different directions. For each:
- **Metaphor:** the idea behind the symbol
- **Form:** the shapes, and why
- **Palette:** hex codes and intent
- **Why it stands out:** against the named competitors
- **Wordmark:** a real typeface (name and weight) that pairs with the symbol, plus any spacing or letter adjustments
- **Image prompt:** a copy-paste prompt for the symbol, in the format below

Generate each direction's symbol now: as SVG if you can produce vector graphics, otherwise as a high-resolution image of at least 2048 × 2048 px. Then ask me to pick one.

## Image prompt format
- Subject: one centred, flat, vector-style symbol on a plain solid background, filling about 60% of the canvas
- Style: bold, simple geometry, clean edges, few shapes, no more than 3 colours, flat colour or one subtle gradient
- Exclude: text, letters (unless the symbol is a monogram), photos, 3D renders, mockups, devices, fine detail, drop shadows, and any rounded-square icon tile
- Aspect ratio: square, 1:1 (in Midjourney, add `--ar 1:1`)

# Step 4: Refine and test
Refine the chosen direction until I approve it. Then check it, and fix anything that fails:
- Readable at 16 px
- Works in one colour, in black and in white
- Works on light and dark backgrounds
- Stands out placed beside the competitors' icons
- Not confusingly similar to a well-known logo

# Step 5: The logo system
Deliver:
1. **Symbol:** the approved mark.
2. **Wordmark:** the typeface, weight and spacing. It is set in the real font, never generated as an image.
3. **Lockups:** horizontal (symbol beside the wordmark) and stacked (symbol above it), with the spacing between them and the minimum clear space around them.
4. **Colour versions:** full colour, one colour, and reversed for dark backgrounds, with hex codes.
5. **Platform files,** for the chosen platforms only:

| Platform | Files |
| --- | --- |
| iOS | Square 1024 × 1024 artwork with no transparency and no rounded corners; the system applies the shape. The symbol and background as separate layers for Apple's Icon Composer, which produces the light, dark, tinted and clear appearances. The symbol must stay legible in the grayscale tinted version. |
| Android | An adaptive icon: foreground (symbol) and background layers on a 108 × 108 dp canvas, with the symbol inside the central 66 dp safe zone; a monochrome layer for themed icons; a full-square 512 × 512 PNG for Google Play, which rounds the corners itself. |
| Web | An SVG favicon plus a 32 px ICO, a 180 px Apple touch icon, 192 and 512 px app icons including a maskable version, and a 1200 × 630 social preview image showing the lockup. |
| Desktop | macOS: the same Icon Composer file as iOS. Windows: an ICO containing 16 to 256 px sizes. |
| Everywhere | A version that survives a circle crop, for social profiles. |

These files are exported from the approved symbol, not generated one by one. If I ask for a preview of a platform's icon, generate one platform at a time.

6. **Production note:**
   - **If the symbol is SVG,** export every file from it.
   - **If it is an image,** it is enough for the pixel-based files (iOS, Google Play, favicons, web app icons, social preview), which are scaled down from it. Separate layers (Icon Composer, Android adaptive icons), the SVG favicon, print and later edits need a vector: trace the image with a vectorizer, or redraw it in Figma or Illustrator.

# Product Brief (optional)
[paste the brief here, or delete this section]
```
