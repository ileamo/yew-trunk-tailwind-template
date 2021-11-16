# How to set up Tailwind CSS with Yew and Trunk

Set tailwindcss globally

```sh
npm i -g tailwindcss
```

Get a single CSS file

```sh
tailwindcss -o ./tailwind.css
```

Add this to the head in index.html

```html
<link data-trunk href="./tailwind.css" rel="css" />
```

Run

```sh
trunk serve
```

Build for production

```sh
# Purge tailwind CSS classes
NODE_ENV=production tailwindcss -c ./tailwind.config.js -o ./tailwind.css --minify
# Build release
trunk build --public-url "/"  --release
# Optionally restore full tailwind.css file
tailwindcss -o ./tailwind.css
```
