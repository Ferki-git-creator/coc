# COC (Chars One Color)

## What is it?
This is a way of representing colors using only 2 ASCII characters, this method is useful for those who are bored: x1b[48;5;10m, RGB(255, 0, 0), green,red,light gray...

---
 
## How can this be implemented?

### 1. Use the full power of ASCII

In the ASCII table, there are 128 characters (7 bits).

In the extended ASCII — 256 characters (8 bits).

If each character holds 8 bits → 2 characters = 16 bits.

And 16 bits = RGB565 format → almost 65,536 colors.

So, AB (two ASCII characters) can be directly used as one color.


---

### 2. Special characters as “palette markers”

You can come up with:

,X → red shades

/X → green

[X → blue

And so on

Where X = intensity in HEX (0–F).
Example:

,F = pure red

/8 = medium green

[C = blue at 75% brightness

This already looks like color code words.

Where X = intensity in HEX (0–F).
Example:

,F = pure red

/8 = medium green

[C = blue at 75% brightness

This already looks like color code words.


---

### 3. Full encoding in 2 characters

For example, let's take a base of 94 characters (printable ASCII: ! to ~).

One character = 94 values.

Two characters = 94² = 8836 unique codes.

This can be represented in a color palette (not 16 million, but enough).


Example:

A! = black

Az = red

Z/ = blue

~~ = white



---

### 4. Full 2-byte format

If you don't limit yourself to only visible characters, you can use all 256 codes.

2 characters = 65,536 colors (analogous to RGB565).

Very "hard" and as short as possible.



---

To test, visit the website: https://ferki-git-creator.github.io/coc/