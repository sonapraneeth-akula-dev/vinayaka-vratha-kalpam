# Illustration ideas and image-generation prompts

Suggested two-panel illustrations for the వ్రతకథ, in reading order. Each
pair is shown side by side through `\illus{left}{right}{left caption}{right caption}`,
same as the existing Chandra-curse and Jambavanta pairs.

## Existing

| Section | Left | Right | Source |
|---|---|---|---|
| శ్రీ వినాయకుడు చంద్రుని శపించుట | తాండవ గణపతిని చంద్రుడపహసించుట | గణపతి చంద్రుని శపించుట | `images/ganesha-curse.png` |
| జాంబవత్యుపాఖ్యానము… | శ్రీ కృష్ణ జాంబవంతుల యుద్ధము | శ్రీకృష్ణ సత్యభామా కళ్యాణము | `images/jambavanta-war.png` |

## Proposed

| # | Placement | Left caption | Right caption | File |
|---|---|---|---|---|
| 1 | Start of శ్రీ వినాయక వ్రతకథ | పాండవుల వనవాసము | సూతమహాముని వ్రతోపదేశము | `images/naimisharanya.png` |
| 2 | After Shiva's speech, before the దమయంతి paragraph | కుమారస్వామి శివుని ప్రశ్నించుట | వినాయక వ్రత విధానము | `images/vratha-vidhanam.png` |
| 3 | శ్యమంతకోపాఖ్యానం | సూర్యుడు సత్రాజిత్తుకు శ్యమంతకమణి ఇచ్చుట | జాంబవంతుడు సింహమును చంపి మణిని గొనుట | `images/syamantaka.png` |
| 4 | End of శ్యమంతకోపాఖ్యానం, before the curse section | పాలలో చంద్రుని ప్రతిబింబము చూచుట | బలరాముని ఆదేశంతో కృష్ణుని వ్రతాచరణ | `images/krishna-apavadu.png` |
| 5 | Before “హరిః ఓం తత్సత్” | ధర్మరాజు వినాయక వ్రతాచరణ | ధర్మరాజు పట్టాభిషేకము | `images/pattabhishekam.png` |

All five add roughly two pages.

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

### 1. Naimisharanya — పాండవుల వనవాసము / సూతమహాముని వ్రతోపదేశము

```text
Portrait 3:4 illustration in traditional Indian miniature painting style (Tanjore / Mysore mythological art), rich earthy colours with gold accents, aged parchment background, ornate floral border of red flowers and green vines around the whole page. The page holds two landscape panels stacked vertically, each framed, separated by a decorative floral band. No text anywhere.
TOP PANEL: The five Pandava brothers and Draupadi in simple forest-exile clothing (ochre and saffron dhotis, bark-cloth shawls, no crowns), walking barefoot along a forest path into a peaceful rishi hermitage at Naimisharanya. Dharmaraja leads, calm and dignified; Bhima carries a mace, Arjuna a bow; Draupadi in a plain maroon saree. Tall banyan trees, deer grazing, small thatched ashram huts, soft morning light.
BOTTOM PANEL: Suta Maharshi, an elderly white-bearded sage in saffron robes with rudraksha beads, sits on a raised platform under a large banyan tree, one hand raised in blessing, teaching a circle of seated sages led by Shaunaka. Dharmaraja kneels before him with folded hands, his brothers and Draupadi behind him. Sacred fire (homa) smoke, palm-leaf manuscripts, serene devotional mood.
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
TOP PANEL: In a forest hermitage, Dharmaraja, his four brothers and Draupadi, still in simple exile clothing, sit together performing Vinayaka Chavithi puja before a clay Ganesha on a rice mandapa, offering flowers, patri leaves, fruits and modaks, with brass lamps and incense. Devotional, hopeful mood, soft morning light.
BOTTOM PANEL: A grand royal court in Indraprastha. Dharmaraja, now in rich royal robes and jewels, sits on a golden throne being crowned by sages pouring sacred water, with Draupadi as queen beside him and his four brothers standing proudly. Courtiers celebrate, flower petals fall. Above the throne, a small glowing image of Lord Ganesha blesses the scene with raised hand. Festive, triumphant mood.
```
