# Palawan Local Goods — Dawn Learning Reference

This theme was prepared with AI assistance so its owner can study Shopify theme development. It is not client work, is not a portfolio sample, and should not be represented as one.

This project uses [Shopify Dawn](https://github.com/Shopify/dawn), Shopify's reference theme, as a starting point. The base theme is licensed under the MIT License; see [`LICENSE.md`](LICENSE.md). The additions below are small examples for learning Liquid, theme sections, blocks, and product metafields.

## What this theme demonstrates

- **Editable homepage section:** `sections/why-shop-local.liquid` defines a heading and up to three merchant-editable benefit blocks. Its schema controls the settings shown in Shopify's theme editor, and `templates/index.json` places the section on the homepage.
- **Metafield-driven product block:** `sections/main-product.liquid` recognizes the custom block and renders `snippets/product-origin-details.liquid`. The snippet displays product details only when their metafields have values.
- **Section styling:** `assets/section-why-shop-local.css` contains the small set of styles used by the homepage section.

## Preview locally

### Requirements

- Node.js 22.12 or newer
- Git 2.28.0 or newer
- [Shopify CLI](https://shopify.dev/docs/api/shopify-cli)
- A Shopify development store that you own or can access

From the theme directory, run:

```powershell
shopify theme dev --store your-store.myshopify.com
```

Sign in to Shopify in the browser if prompted. The CLI creates a temporary development theme and prints a local preview URL, usually `http://127.0.0.1:9292`. Open that URL in Google Chrome while the command is still running. This does not publish the theme.

## Try the product metafields

In the development store admin, define these product metafields and add values to a demo product:

| Namespace and key | Suggested type | Example value |
| --- | --- | --- |
| `custom.origin` | Single line text | Example only: Palawan, Philippines |
| `custom.shelf_life` | Single line text | Example only: 6 months |
| `custom.ingredients` | Multi-line text | Example only: Cashews, sea salt |

These are illustrative values, not verified claims about real products. The block stays hidden when all three fields are empty. Use accurate information before displaying product claims on any real storefront.

## Check the theme

Run Shopify's theme linter from the theme directory:

```powershell
shopify theme check
```

At the time this reference was prepared, Theme Check reported nine existing warnings in Dawn files and no warnings in the added section or metafield snippet. Review warnings against the current Dawn and Theme Check versions rather than assuming they are errors.
