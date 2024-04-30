# Dungeon Days site

## Local Dev

Do this:

```bash
npm i
npm run dev
```

Edit page content in `./src/pages/`
Some of the pages use components which are made in the `./src/components/` folder.

### NavBar

The links for the navigation bar are all in the `./src/components/Nav/links.json` file. First item is the href, second is the display text

### Styling

The site uses Tailwind - TL;DR:
Rather than writing CSS files you just add classes to elements to change them - i.e The website has really good docs that will explain anything you need to know.

```html
<div class="px-5 my-2">
  Give me 5 pixels of padding in the X, and 2 pixels of margin in the Y
</div>
```

### Colors

Tailwind has a MASSIVE palette of colors you can use: https://tailwindcss.com/docs/customizing-colors
The basic syntax is {target}-{color} i.e

```html
<div class="bg-red-500 text-emerald-200">
  Give me a red background and green text
</div>
```

### Typography

I've also added the Tailwind Prose plugin that has a bunch of sensible defaults, but you might need to override some of them.
Most of this is applied in the `src/components/page.astro` file.  
Here's some docs on how to target specific elements: https://github.com/tailwindlabs/tailwindcss-typography?tab=readme-ov-file#element-modifiers

## Building

Do this:

```bash
npm run build
```

You'll need to make sure the build files aren't excluded from git via `.gitignore`
You may need to amend github pages to point at the new folder generated by the build step

## TODO

- [x] Use the right fonts
- [x] Tweak the typography
- [] Create some new images for the stories which are a bit nicer
- [] ~Add some of the background content images?~
- [x] Reinstate the Google analytics stuff (@Ollie - you can do this in `src/components/Layout.astro`)
- [x] Reinstate some of the links to emails etc (see `src/pages/index.astro`)

## Tech Stack

Astro JS (ftw): https://astro.build/
Tailwind CSS: https://tailwindcss.com/
Tailwind Prose: https://github.com/tailwindlabs/tailwindcss-typography
Alpine: https://alpinejs.dev/ (for the mobile nav, cld probably replace it)
