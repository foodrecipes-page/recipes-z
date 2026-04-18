# recipes-z

Recipe cache shard for **[foodrecipes.page](https://foodrecipes.page)** — AI-generated recipes whose slug starts with **the letter 'z'**.

## What's this?

This repo is one of 27 public "cache shards" that back foodrecipes.page. When the app generates a recipe, a GitHub Action batch-commits the JSON file here, then [jsDelivr](https://www.jsdelivr.com/) serves it globally over CDN. Splitting by first letter keeps each repo small and keeps git operations snappy.

Layout:

```
recipes/
  <cuisine>/
    <diet>/
      <slug>.json
```

Example: `recipes/indian/vegetarian/paneer-butter-masala.json`

## How to use these recipes

jsDelivr URL pattern:

```
https://cdn.jsdelivr.net/gh/foodrecipes-page/recipes-z@main/recipes/<cuisine>/<diet>/<slug>.json
```

Free to fetch. No auth. Globally cached.

## License

Recipes in this repo are published under **[CC BY-NC-SA 4.0](./LICENSE)** — share, adapt, and cook freely for non-commercial use; attribute foodrecipes.page and keep derivative works under the same license.

Application code that consumes this cache is MIT-licensed and lives in a separate repo.

---

Generated and maintained automatically.
