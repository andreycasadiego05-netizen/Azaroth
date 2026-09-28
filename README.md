# Azaroth · Random Student Picker

A web page for picking students at random, built around the idea of a SQL query:

```sql
SELECT name
FROM students
WHERE already_picked = 0
ORDER BY RAND()
LIMIT 1;
```

## Features

- A table with **at least 26 slots** and no maximum: add as many names as you need.
- Add names by pasting text or uploading a `.txt` / `.csv` file.
- Three draw modes:
  - **One:** picks a single person.
  - **Several:** picks as many people as you specify.
  - **Pairs:** builds groups of 2 (or any size you set) from all the names.
- People who were already picked are not repeated, and you can return them to the draw with the **↺** button.
- Names are saved in the browser (`localStorage`).
- Four visual styles for the reveal: **Glow** (a light sweeps across the names), **Wheel** (a roulette wheel), **Slots** (a slot-machine reel), and **Radar** (a sweeping radar scan). The result is decided internally at random; the style only changes how it is shown.
- Names are auto-capitalized (for example `JOAN SEBASTIAN BLANCO` becomes `Joan Sebastian Blanco`).
- Automatic light and dark theme.

## Name format

One name per line:

```
Emily Carter
James Miller
Sophia Reed
```

You can also separate names with commas or semicolons. Leading numbers or dashes (`1. Emily`, `- James`) are removed automatically.

## Usage

Open `index.html` in your browser. No installation or server needed.

## Publish with GitHub Pages

1. Create a repository on GitHub and upload these files (`index.html` must be in the root).
2. Go to **Settings → Pages**.
3. Under **Source**, choose *Deploy from a branch*, branch `main`, folder `/ (root)`.
4. Save and wait a minute or two. Your site will be live at `https://YOUR-USERNAME.github.io/REPO-NAME/`.

## Tech

Plain HTML, CSS, and JavaScript in a single file. Google Fonts: Bricolage Grotesque and Fragment Mono.

## Creators

Andrey, Raul, Joan, and Andres R.
