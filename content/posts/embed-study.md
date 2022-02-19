---
title: "How to embed a lishogi study in your website"
date: 2022-02-19T5:30:37Z
draft: true
---

1. Open a study.
2. Click on the button that looks like a share button.
3. Scroll a bit lower and you will see an option "Embed in your website or blog". Under that there is a html code. Copy and use it in your website to embed lishogi studies.
4. If you want a different theme, piece set or background use the following parameters:
- **`theme`** to change the theme. The available options to set `theme` are `solid-orange`, `solid-natural`, `wood1`, `kaya1`, `kaya2`, `kaya-light`, `oak`, `solid-brown1`, `solid-wood1`, `blue`, `dark-blue`, `gray`, `Painting1`, `Painting2`, `Kinkaku`, `space1`, `space2`, `whiteBoard`, `darkBoard`, `doubutsu`, `transparent`, `transparent-white`.
- **`pieceSet`** to change the piece set. The available options to set `pieceSet` are `kanji_light`, `kanji_brown`, `Ryoko_1Kanji`, `orangain`, `kanji_red_wood`, `Portella`, `Portella_2Kanji`, `1Kanji_3D`, `2Kanji_3D`, `Shogi_cz`, `Kanji_Guide_Shadowed`, `Valdivia`, `Vald_opt`, `shogi_BnW`, `Intl_Colored_2D`, `Intl_Colored_3D`, `Intl_Shadowed`, `Intl_Monochrome_2D`, `Intl_Wooden_3D`, `international`, `simple_kanji`, `doubutsu`, `Logy_Games`, `western`.
- **`bg`** to change the background. The available options to set `bg` are `light`, `dark`.

Given below is an example html code for embedding a lishogi study on your website with the `Kinkaku` theme, `Shogi_cz` piece set and `dark` background.

```
<iframe width=600 height=371 src="https://lishogi.org/study/embed/no04bWUq/s739levF?theme=Kinkaku&pieceSet=Shogi_cz&bg=dark" frameborder=0></iframe>
```

Embeded Study (works differently on netlify):

{{< lishogi-embed src="https://lishogi.org/study/no04bWUq/s739levF" >}}