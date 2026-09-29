# Illustration ideas and image-generation prompts

Suggested two-panel illustrations for the వ్రతకథ, in reading order. Each
pair is shown side by side through `\illus{left}{right}{left caption}{right caption}`,
same as the existing Chandra-curse and Jambavanta pairs.

## Existing

In reading order. Panels are cropped into `<source>-1.png` / `<source>-2.png`.

| # | Section | Left | Right | Source |
|---|---|---|---|---|
| 1 | శ్రీ వినాయక వ్రతకథ (start) | పాండవుల వనవాసము | సూతమహాముని వ్రతోపదేశము | `images/pandavas-vanvas.png` |
| 2 | శ్రీ వినాయక వ్రతకథ (after Shiva's speech) | కుమారస్వామి శివుని ప్రశ్నించుట | వినాయక వ్రత విధానము | `images/kumaraswamy-asking.png` |
| 3 | శ్యమంతకోపాఖ్యానం (mid-section) | సూర్యుడు సత్రాజిత్తుకు శ్యమంతకమణి ఇచ్చుట | జాంబవంతుడు మణిని గొనుట | `images/syamantaka-mani.png` |
| 4 | శ్యమంతకోపాఖ్యానం (end) | పాలలో చంద్రుని ప్రతిబింబము చూచుట | బలరాముని ఆదేశంతో కృష్ణుని వ్రతాచరణ | `images/krishna-moon-in-milk.png` |
| – | శ్రీ వినాయకుడు చంద్రుని శపించుట | తాండవ గణపతిని చంద్రుడపహసించుట | గణపతి చంద్రుని శపించుట | `images/ganesha-curse.png` |
| – | జాంబవత్యుపాఖ్యానము… | శ్రీ కృష్ణ జాంబవంతుల యుద్ధము | శ్రీకృష్ణ సత్యభామా కళ్యాణము | `images/jambavanta-war.png` |
| 5 | Before “హరిః ఓం తత్సత్” | ధర్మరాజు వినాయక వ్రతాచరణ | ధర్మరాజు పట్టాభిషేకము | `images/pandavas-pattabhiskam.png` |

All five proposed scenes are done; `#` matches the prompt number below.
The prompts are kept for regeneration.

## Image requirements

- One image per pair: **portrait 896×1200 (3:4)**, two landscape panels
  stacked top and bottom, like `images/jambavanta-war.png`. They are
  cropped apart and placed side by side.
- Keep important figures away from panel edges; keep watermarks or
  sparkles out of the corners (they get trimmed).
- **No text in the image.** Captions are typeset in Anek Telugu, and
  generators garble Telugu script.
- Use one style for all images. The prompts below use the traditional
  miniature style of the Jambavanta pair.

## Prompts

Each prompt is self-contained: paste it as-is. Append the negative prompt
where the model supports one.

**Negative prompt (all):** text, letters, captions, Telugu script, words,
watermark, signature, logo, blood, gore, extra limbs, extra fingers,
deformed hands, distorted faces, modern clothing, photorealistic, 3D render,
blurry, cropped heads

### Pandava scenes (1 and 5): keeping the family consistent

Generators tend to get the headcount wrong, swap costumes between panels
and redraw faces. The prompts below counter this with a fixed **character
sheet** pasted into every prompt, the same left-to-right order everywhere,
one signature colour and prop per person, and an explicit headcount.

| Pos | Person | Look (fixed) | Exile costume | Royal costume (5 bottom only) |
|---|---|---|---|---|
| 1 | Yudhishthira (ధర్మరాజు) | eldest, ~40, wheatish-brown skin, short neat black beard, hair in a top-knot, calm gentle eyes | plain white cotton dhoti and white shawl, rudraksha mala | white-and-gold silk, tall gold crown |
| 2 | Draupadi (ద్రౌపది) | ~30, dusky dark-brown skin, large eyes, long black braid, small red bindi | plain maroon cotton saree, no jewellery | red silk saree, gold jewellery, queen's crown |
| 3 | Bhima (భీముడు) | tallest and broadest, very muscular, dark brown skin, thick curled moustache, no beard | saffron dhoti, bare chest, golden mace on his shoulder | saffron-and-gold silk, crown, mace |
| 4 | Arjuna (అర్జునుడు) | lean athletic, dark brown skin, thin moustache, no beard | green dhoti, bow over shoulder, quiver on back | green-and-gold silk, crown, bow |
| 5 | Nakula (నకులుడు) | youngest-looking, light wheatish skin, short black hair, clean-shaven, handsome, identical twin of Sahadeva | light blue dhoti, sword at waist | blue-and-gold silk, small crown |
| 6 | Sahadeva (సహదేవుడు) | same face, black hair and light wheatish skin as Nakula (twins), clean-shaven | purple dhoti, palm-leaf manuscript bundle | purple-and-gold silk, small crown |

**Retry tips**

- **Generate one panel at a time** (landscape 4:3) instead of the stacked
  page. `\illus` takes two separate images, so no stacking is needed; name
  them `<name>-1.png` / `<name>-2.png`.
- Generate the first panel, then generate the second **with the first as
  a reference image** (ChatGPT/DALL·E: "same characters as this image";
  Midjourney: `--cref <url> --cw 100`; Leonardo/SD: Character Reference or
  IP-Adapter). Keep the same seed where supported.
- If the count is still wrong, **fix by inpainting** (erase the extra or
  missing person and re-prompt just that area with their row from the table)
  rather than regenerating the whole image. To remove someone, prompt the
  erased area as "empty woven mat and forest floor", not with a person.
- In a chat-style editor, don't paste the full prompt again to fix one
  detail; that re-rolls the scene and adds people. Say only "Remove the man
  sitting in the foreground with his back to the viewer; change nothing
  else."
- **Puja composition:** models default to a circle around the idol (which
  adds a person in the foreground, back to the viewer) or put the idol in
  front of the family with everyone behind it. Prompt 5 uses a **side view**
  instead: the idol sits on the right facing left, all six sit on the left
  facing right, and nothing is behind or in front of the idol.
- Check before accepting: **5 men + 1 woman**, everyone facing the idol,
  nobody behind the idol or with their back to the viewer, all with black
  hair, twins alike, Bhima the largest, only Draupadi in a saree.

**Extra negative prompt for 1 and 5:** more than five men, fewer than five
men, two women, extra women, children, duplicate person, seventh person,
person with back to viewer, person in foreground, people sitting in a
circle, people behind the idol, idol facing the viewer, blond hair, golden
hair, light hair, crowns in exile, jewellery in exile, mismatched costumes,
changing skin tone, different faces
### 1. Naimisharanya — పాండవుల వనవాసము / సూతమహాముని వ్రతోపదేశము

```text
Portrait 3:4 illustration in traditional Indian miniature painting style (Tanjore / Mysore mythological art), rich earthy colours with gold accents, aged parchment background, ornate floral border of red flowers and green vines around the whole page. The page holds two landscape panels stacked vertically, each framed, separated by a decorative floral band. No text anywhere.

CHARACTERS (identical in both panels: same faces, skin tones, hair, costumes and props; exactly SIX family members: FIVE men and ONE woman, no one else from the family):
1. Yudhishthira: eldest man, about 40, wheatish-brown skin, short neat black beard, hair in a top-knot, calm gentle eyes; plain white cotton dhoti and white shawl, rudraksha mala; no crown, no jewellery.
2. Draupadi: the only woman, about 30, dusky dark-brown skin, large eyes, long black braid, small red bindi; plain maroon cotton saree, no jewellery.
3. Bhima: tallest and broadest man, very muscular, dark brown skin, thick curled moustache, no beard; saffron dhoti, bare chest, golden mace on his shoulder.
4. Arjuna: lean athletic man, dark brown skin, thin moustache, no beard; green dhoti, bow over his shoulder, quiver on his back.
5. Nakula: youngest-looking man, light wheatish skin, short black hair, clean-shaven, handsome; light blue dhoti, sword at his waist.
6. Sahadeva: Nakula's identical twin, same face, black hair and light wheatish skin, clean-shaven; purple dhoti, holds a palm-leaf manuscript bundle.
All six have black hair; no blond or light hair. All wear simple forest-exile clothing: barefoot, no crowns, no gold.

TOP PANEL: The six characters walk in a single row from left to right along a forest path toward a peaceful rishi hermitage at Naimisharanya, in this exact left-to-right order: Yudhishthira (leading, at the front), Draupadi, Bhima, Arjuna, Nakula, Sahadeva. All six fully visible head to toe, faces clearly shown in three-quarter view. Tall banyan trees, deer grazing, small thatched ashram huts, soft morning light.

BOTTOM PANEL: Under a large banyan tree, Suta Maharshi, an elderly sage with a long white beard in saffron robes and rudraksha beads, sits on a raised stone platform on the left, one hand raised in blessing, with a few seated sages (Shaunaka and others, all old men with white beards and saffron robes) beside him. On the right, Yudhishthira kneels before him with folded hands; behind Yudhishthira stand the other five in the same order: Draupadi, Bhima, Arjuna, Nakula, Sahadeva, all with folded hands. Same six characters exactly as described: same faces, skin tones and costumes as the top panel. Sacred fire (homa) smoke, palm-leaf manuscripts, serene devotional mood.
```
### 2. Kailasa — కుమారస్వామి శివుని ప్రశ్నించుట / వినాయక వ్రత విధానము

```text
Portrait 3:4 illustration in traditional Indian miniature painting style (Tanjore / Mysore mythological art), rich earthy colours with gold accents, aged parchment background, ornate floral border of red flowers and green vines around the whole page. The page holds two landscape panels stacked vertically, each framed, separated by a decorative floral band. No text anywhere.
TOP PANEL: Snowy Mount Kailasa. Lord Shiva, blue-throated with matted hair, crescent moon, Ganga flowing from his locks, tiger-skin and trident, sits on a tiger skin beside Goddess Parvati in a green silk saree. Young Kumaraswamy (Kartikeya), six-faced or single-faced youthful prince with a vel spear, stands beside his peacock with folded hands asking a question. Nandi the bull rests nearby. Divine golden halo light.
BOTTOM PANEL: A traditional South Indian home puja for Vinayaka Chavithi. A clay Ganesha idol sits on a small wooden mandapa over a heap of rice grains shaped with an eight-petal lotus design. Around it: 21 kinds of sacred leaves (patri), wood apple, jamun fruit, sugarcane stalks, bananas, modaks and kudumulu on banana leaves, brass oil lamps, incense smoke, flower garlands, mango-leaf toranam above, kalasham with coconut. A devotee family in traditional clothes sits in worship. Warm golden lamplight.
```

### 3. Syamantaka — సూర్యుడు సత్రాజిత్తుకు మణి ఇచ్చుట / జాంబవంతుడు సింహమును చంపి మణిని గొనుట

```text
Portrait 3:4 illustration in traditional Indian miniature painting style (Tanjore / Mysore mythological art), rich earthy colours with gold accents, aged parchment background, ornate floral border of red flowers and green vines around the whole page. The page holds two landscape panels stacked vertically, each framed, separated by a decorative floral band. No text anywhere.
TOP PANEL: Surya, the Sun God, radiant and golden, crowned, standing on a chariot drawn by seven white horses amid sunrise clouds, handing a brilliantly glowing red-gold jewel (the Syamantaka gem) to King Satrajit, who kneels on a riverbank with raised hands in devotion, wearing royal Yadava jewellery and a crown. Rays of light spreading from the gem.
BOTTOM PANEL: Deep dense forest. Jambavanta, a mighty crowned bear king with dark fur, golden ornaments and a red waist sash (same character design as the Krishna–Jambavanta battle painting), wrestles a large maned lion that holds the glowing red jewel in its jaws. Dramatic but not violent: no blood, no dead bodies. Tall trees, vines, rocks, dappled light.
```

### 4. Krishna's blame — పాలలో చంద్రుని ప్రతిబింబము / బలరాముని ఆదేశంతో వ్రతాచరణ

```text
Portrait 3:4 illustration in traditional Indian miniature painting style (Tanjore / Mysore mythological art), rich earthy colours with gold accents, aged parchment background, ornate floral border of red flowers and green vines around the whole page. The page holds two landscape panels stacked vertically, each framed, separated by a decorative floral band. No text anywhere.
TOP PANEL: Night in a palace courtyard in Dwaraka. Young Lord Krishna, blue-skinned, peacock feather in his crown, yellow pitambara, holds a large brass pot of milk and looks into it with a startled expression, seeing the reflection of the crescent moon on the milk surface. The crescent moon glows in the starry sky above. Oil lamps, carved pillars, deep blue night tones.
BOTTOM PANEL: Krishna, seated cross-legged, performs Ganesha puja with devotion, offering flowers to a decorated Ganesha idol surrounded by lamps, modaks and fruits. Standing beside him, his elder brother Balarama, fair-skinned with a plough on his shoulder, blue garments and a crown, rests a guiding hand on Krishna's shoulder. Temple interior with garlands and incense smoke.
```

### 5. Ending — ధర్మరాజు వినాయక వ్రతాచరణ / ధర్మరాజు పట్టాభిషేకము

```text
Portrait 3:4 illustration in traditional Indian miniature painting style (Tanjore / Mysore mythological art), rich earthy colours with gold accents, aged parchment background, ornate floral border of red flowers and green vines around the whole page. The page holds two landscape panels stacked vertically, each framed, separated by a decorative floral band. No text anywhere.

CHARACTERS (identical faces, skin tones and hair in both panels; each keeps the same signature colour and prop; exactly SIX family members: FIVE men and ONE woman):
1. Yudhishthira: eldest man, about 40, wheatish-brown skin, short neat black beard, calm gentle eyes; signature colour WHITE, rudraksha mala.
2. Draupadi: the only woman, about 30, dusky dark-brown skin, large eyes, long black braid, small red bindi; signature colour MAROON/RED.
3. Bhima: tallest and broadest man, very muscular, dark brown skin, thick curled moustache, no beard; signature colour SAFFRON, golden mace.
4. Arjuna: lean athletic man, dark brown skin, thin moustache, no beard; signature colour GREEN, bow.
5. Nakula: youngest-looking man, light wheatish skin, short black hair, clean-shaven, handsome; signature colour LIGHT BLUE, sword.
6. Sahadeva: Nakula's identical twin, same face, black hair and light wheatish skin, clean-shaven; signature colour PURPLE, palm-leaf manuscript.
All six have black hair; no blond or light hair.

TOP PANEL (forest exile, simple cotton clothes in each person's signature colour, barefoot, no crowns, no jewellery): SIDE-VIEW composition of a puja in a forest hermitage, seen from the side like a stage. RIGHT third of the panel: a small clay Ganesha idol on a low altar (rice-heap mandapa with an eight-petal lotus design, a banana-leaf canopy), turned to face LEFT toward the family; behind the altar only a tree trunk and bushes, no people. LEFT two-thirds of the panel: exactly six people sitting cross-legged on a woven mat in two short rows, all turned to the RIGHT to face the idol, shown in profile or three-quarter view so their faces are visible. Front row, nearest the idol, from right to left: Yudhishthira (closest to the idol, offering flowers with both hands), Draupadi, Bhima. Back row, slightly raised behind them, from right to left: Arjuna, Nakula, Sahadeva. Everyone except Yudhishthira holds folded hands. Between the family and the altar, on the ground: patri leaves, fruits and modaks on banana leaves, brass lamps, incense. Nobody sits behind, beside or in front of the idol, nobody sits in the foreground, and nobody has their back to the viewer. Count: five men and one woman, six people total, no seventh person. Devotional, hopeful mood, soft morning light.

BOTTOM PANEL (coronation, same six people, same faces and skin tones; now in rich silk in their signature colours with gold borders, gold jewellery and crowns): A grand royal court in Indraprastha. Yudhishthira sits at the centre on a golden throne being crowned by two elderly white-bearded sages pouring sacred water from gold kalashas. Draupadi sits beside him on the throne to his left as queen. Standing, two on each side: Bhima and Arjuna on the left of the throne, Nakula and Sahadeva on the right. Courtiers in the background, flower petals falling. Above the throne, a small glowing image of Lord Ganesha blesses the scene with a raised hand. Festive, triumphant mood.
```