# Sebayt Theme

The Shopify theme behind [sebaytlabs.com](https://sebaytlabs.com), written by hand in Liquid and plain CSS. There's no build step, no JavaScript framework and no app.

It's small on purpose: 24 sections, 3 snippets and one stylesheet. It covers what a studio shop needs:

- **Home page:** a hero, a featured product, beliefs, a quote, a follow row and a notes section, all editable in the theme editor
- **Products:** product pages, collections and the list of all collections
- **Writing:** a blog and articles
- **Pages:** regular pages, contact, search, cart, 404, and the password page for before launch

Colors, layout and social links live in **Theme settings**, so you can change them without touching code.

## Why this exists

A small shop needs a few things: a home page that says what you're about, product pages, a blog and a cart. The usual way to get them:
- **Buy a premium theme.** These typically cost a few hundred dollars and come with dozens of features and a thick layer of JavaScript.
- **Add an app for each missing piece.** Each one usually brings its own monthly fee and its own script slowing the page down.

When something looks wrong, you're digging through code you didn't write.

We wanted a theme we could read top to bottom in an afternoon. So we wrote this one by hand: Liquid and one CSS file, and nothing else. It's what runs our own store, and we're giving it away so the next small studio can start from a working shop instead of a blank page.

## What it can replace

| If you'd use… | It's good at… | What this theme is |
|---|---|---|
| **Dawn**, Shopify's free theme | A polished, well-supported default | Dawn is excellent and the safe choice. This one is far smaller and plainer, for when you want to understand every line you ship. |
| **Premium themes** from the Theme Store | Lots of built-in features and styles | Free, with no license to renew. You get only what a studio shop uses, written to be changed. |
| **Page builders** (PageFly, Shogun…) | Drag-and-drop layouts | No monthly app and no extra script. Sections are edited in Shopify's own theme editor. |
| **Squarespace, Wix** | All-in-one sites | Keep Shopify's checkout, payments and tax handling, with a site that's this simple. |
| **"One more app"** for a quote, a follow row or a notes section | One feature each | Those sections are built in. |

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

## Related

Everything else Sebayt Labs makes is listed on the [profile page](https://github.com/sebaytlabs). [SimpleBrain](https://github.com/sebaytlabs/simplebrain) can publish your notes as pages on a Shopify store like this one.

## Limits, plainly

- It's built for a small catalog. There are no product filters, mega menus or multi-currency switchers.
- One language.
- You'll want to change the words: the home sections ship with studio-style placeholders.

## License

MIT. Made by [Sebayt Labs](https://sebaytlabs.com). Change the words, colors and name and make it yours.
