# Sebayt Theme

The Shopify theme behind [sebaytlabs.com](https://sebaytlabs.com), written by hand in Liquid and plain CSS. There's no build step, no JavaScript framework and no app.

It's small on purpose: 24 sections, 3 snippets and one stylesheet. It covers what a studio shop needs:

- **Home page:** a hero, a featured product, beliefs, a quote, a follow row and a notes section, all editable in the theme editor
- **Products:** product pages, collections and the list of all collections
- **Writing:** a blog and articles
- **Pages:** regular pages, contact, search, cart, 404, and the password page for before launch

Colors, layout and social links live in **Theme settings**, so you can change them without touching code.

## Use it on your store

```
npm install -g @shopify/cli
git clone https://github.com/sebaytlabs/sebayt-theme
cd sebayt-theme
shopify theme push --store YOUR-STORE.myshopify.com --unpublished --theme "My theme"
```

`--unpublished` uploads it as a new theme beside your live one, so nothing changes until you press **Publish** in Shopify admin. To work on it with live reload, run `shopify theme dev --store YOUR-STORE.myshopify.com`.

## Layout

```
layout/theme.liquid      the page shell: head, header group, footer group
sections/home-*.liquid   the home page blocks
sections/main-*.liquid   one per page type
snippets/                price, product card, CSS variables from the theme settings
assets/theme.css         all the styling
config/                  settings schema (colors, fonts, social links)
templates/*.json         which sections each page type uses
```

## License

MIT. Made by [Sebayt Labs](https://sebaytlabs.com). Change the words, colors and name and make it yours.
