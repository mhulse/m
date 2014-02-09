## Note: Full credit for this answer goes to [@yakunins](http://graphicdesign.stackexchange.com/users/5791/yakunins) and his [answer above](http://graphicdesign.stackexchange.com/a/25853/10258).

---

Using FontLab Studio v5.1.3, Mac:

### 1) Open `.vfb`:

Assuming you already have your icon/logo setup:

![screen][1]

### 2) Enable desired "blank" glyphs:

For this font, here's a list of characters I want to be non-spacing and non-marking:

> @ : / . C E H I K L M O P S T U Y c e h i k l m o p s t u y

**Note:** The above will allow me to type my domain name, real name, web address or e-mail, where only the "M" or "m" will produce a visible/marking character.

**Note:** I'm not applying blank characters to all glyphs because I'm going to subset only the characters above when generating the web font versions at [Font Squirrel](http://www.fontsquirrel.com/tools/webfont-generator) (using the "Expert" mode).

Double-click to "enable" each desired glyph. The end result should look something like this:

![screen][2]

**Note:** After double clicking, you'll notice that the "Glyph Properties" window will assign that glyph default values:

![screen][3]

### 2) Select only the blanks:

Using <kbd>Command</kbd> `+` <kbd>Click</kbd>, select all of the blank glyphs:

![screen][4]

### 3) Make all the glyphs to have zero width:

Choose: `Tools` → `Action...` → `Metrics` → `Set width (0 C)`.

In the "Set width to" input field, type `0` and click "Ok".

![screen][5]

**Note:** If prompted, click "yes" to apply to all selected glyphs.

### 4) Scale all the contours in glyphs to zero sized area:

Choose: `Tools` → `Action...` → `Contour` → `Scale`.

Check the "Proportional Scale" checkbox and type "0.01" into the "Horizontal Scale" input field.

**Do not** apply to entire font (as we only want to apply the scale to the selected glyphs).

![screen][6]

**Note:** If prompted, click "yes" to apply to all selected glyphs.

Repeat three or more times.

### 5) Remove all hints, classes and kerning pairs:

Choose: `Tools` → `Action...` → `Hints and Guidelines` → `Remove hints/guides [BL N]`.

![screen][7]

**Note:** If prompted, click "yes" to apply to all selected glyphs.

### 6) Remove all contours and points:

Choose: `Tools` → `Action...` → `Contour` → `CleanUp [E,4]` → `Simplify paths`.

Uncheck "Insert nodes at extremes (recommended)" box and type "1" into the "Simplify paths" input field.

![screen][8]

**Note:** If prompted, click "yes" to apply to all selected glyphs.

---

### Notes:

Feedback? Did I miss a step or do something wrong?

~~The only thing I could not find/figure out was the "classes and kerning pairs" removal. Any tips on how to do this?~~


  [1]: http://i.stack.imgur.com/v7Kqu.png
  [2]: http://i.stack.imgur.com/eVHy5.png
  [3]: http://i.stack.imgur.com/DYI42.png
  [4]: http://i.stack.imgur.com/HUZCs.png
  [5]: http://i.stack.imgur.com/9EUpc.png
  [6]: http://i.stack.imgur.com/0YCLC.png
  [7]: http://i.stack.imgur.com/EfVTa.png
  [8]: http://i.stack.imgur.com/KYYfg.png