# Budget Home Picks India - Storefront Site

A single-page interactive catalogue for the "Budget Home Picks India" affiliate
project. It is one self-contained file, `index.html` (HTML + CSS + vanilla JS,
no build step), ready to host on GitHub Pages as-is.

Visitors can search the picks, filter by category chips, sort by name, and tap
"Check Price on Amazon" on any card to open that product on Amazon.in with the
project's Associates tag (`budgethomep05-21`). Every card also has a
"Copy page link" button: it copies this page's URL plus `#p-<ASIN>`, and when
the page is opened with that hash it scrolls to that product and highlights it.
That per-product link is what goes on a Pinterest pin.

## Adding a product

Edit the `PRODUCTS` array in the script at the bottom of `index.html` and add
one entry:

```js
{name:"Short product name", category:"Kitchen", asin:"B0XXXXXXXX",
 why:"One line on why people buy it.",
 keywords:"extra words people might search for"}
```

Rules:

- `category` must be one of: Kitchen, Storage, Small Space, Clothing, Beauty,
  Home Decor, Sports and More.
- `asin` must be a real ASIN copied from the product's own Amazon.in page URL
  (`amazon.in/dp/<ASIN>`). Never guess or invent an ASIN.
- **Prices are never typed anywhere on this site.** No price in the card, no
  price in the text. The Amazon button always shows the live price, which is
  the only price a visitor sees. This is an Amazon Associates rule and a
  project rule.
- No Amazon product photos are used (licence). Cards use simple category
  icons instead.

## Notes

- The footer carries the required disclosure: "As an Amazon Associate I earn
  from qualifying purchases", and links to the About, Affiliate Disclosure,
  Privacy Policy and Contact pages on the project blog
  (budgethomepicksindia.blogspot.com).
