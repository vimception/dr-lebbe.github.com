# Website Dr-Lebbe

## Development

```
npm run dev
```

Opening a browser tab

```
npm run dev -- --open
```

## Build

See also: https://kit.svelte.dev/docs/adapter-static

```
npm run build
```

Serving the production build:

```
cd build
python3 -m http.server
```

## Publish

Merge the dist folder into te live branch:

```
git subtree split --branch live --prefix dist/
git push -u origin live
```
