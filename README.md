# 🫐 Blackberrys — Unblocked Games

> The freshest unblocked games hub. Play anything, anytime.

## 📁 Project Structure

```
blackberrys/
├── index.html          ← Main homepage (game browser)
├── icons/              ← Game icons (PNG, named by game ID)
│   ├── snake.png
│   ├── 2048.png
│   └── tetris.png
└── games/              ← Individual game folders
    ├── snake/
    │   └── index.html
    ├── 2048/
    │   └── index.html
    └── tetris/
        └── index.html
```

## ➕ Adding a New Game

### 1. Create the game folder
```
games/
└── mygame/
    └── index.html   ← your game code here
```

### 2. Add an icon
Drop a square PNG into `icons/mygame.png`  
(if missing, the emoji fallback will show automatically)

### 3. Register in `index.html`
Find the `games` array near the top of the `<script>` tag and add:

```js
{
  id: 'mygame',           // must match folder name + icon filename
  name: 'My Game',
  desc: 'Short description of the game.',
  emoji: '🎮',            // fallback if icon is missing
  tag: 'arcade',          // arcade | puzzle | strategy | action
  tagClass: 'tag-arcade', // tag-arcade | tag-puzzle | tag-strategy | tag-action
  color: '#f59e0b',       // accent color for the card glow
  hot: false,             // show 🔥 Hot badge?
  new: true,              // show ✦ New badge?
  path: 'games/mygame/index.html'
}
```

That's it — the card and modal load automatically!

## 🚀 Deploy to GitHub Pages

1. Push to a GitHub repo
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)`
4. Your site will be live at `https://yourusername.github.io/blackberrys/`

## 📬 Contact

Request a game or report a bug: **blackberryggames@gmail.com**
