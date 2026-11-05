# Brand assets

Not published on the site (the deploy workflow copies only the four site files).

- `kofi-1024.png`, `kofi-400.png` — Ko-fi profile image, mark at 580px on a 1024px canvas
- `discord-512.png`, `discord-1024.png` — Discord avatar, mark at 640px on a 1024px canvas
- `kofi.svg`, `discord.svg` — sources for the above; render with ImageMagick, e.g.
  `magick -background none -density 96 discord.svg -resize 1024x1024 discord-1024.png`

Colours: paper `#F6F2E9`, ink `#1E1B16`. The mark is `../logo.svg`.
