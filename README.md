# Static-app-testing-structured

A minimal static HTML/CSS/JS demo, structured for deployment on Velona.

## Layout

```
index.html
style.css
script.js
README.md
```

`index.html` is at the top level with no wrapper folder, so Velona detects
it as a static site.

## Run locally

```
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Package for Velona

Build the zip from inside the project directory so paths have no folder
prefix:

```
cd project && zip -r ../project.zip . -x ".git/*" -x ".env"
unzip -l project.zip
```

Every path in the listing should start directly with `index.html`,
`style.css`, etc. — not `project/index.html`. Don't use macOS Finder's
"Compress" option; it adds a wrapper folder and a `__MACOSX` directory.
