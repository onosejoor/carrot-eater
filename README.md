# 🐰 Glitch Bunny Loop

> *A puzzle game where the hardest enemy is the version of you from 30 seconds ago.*

---

## 🎮 About the Game

**Glitch Bunny Loop** is a top-down grid-based puzzle game built in GameMaker. You control a bunny hopping across a dark arena, collecting golden carrots. But every time you eat a carrot, a **Shadow Bunny** appears and replays your exact past moves — and you have to avoid it.

The more carrots you collect, the more shadow versions of yourself fill the screen. Can you collect all the carrots without colliding with your own past?

---

## 🕹️ How to Play

| Key | Action |
|-----|--------|
| ← → ↑ ↓ | Hop in that direction |
| Hold key | Auto-move continuously |

- **Eat a carrot** → a new shadow of your past self appears
- **Touch a shadow** → Merge Conflict! The loop resets
- **Collect 5 carrots** → BUILD SUCCESSFUL! You win!

---

## 🏆 Win Condition

Collect **5 carrots** without being caught by any Shadow Bunny.

Each carrot eaten adds **+1 extra carrot** to the field, making each loop harder than the last.

---

## 👻 The Shadow System

Every time you eat a carrot:
- Your last **20 moves** are recorded
- A **blue ghost bunny** spawns and replays those moves exactly
- You must navigate around your own past self
- Shadows disappear after replaying their full path

---

## 🛠️ Built With

- **Engine:** GameMaker Studio 2 (GMS2 v2024.14.3)
- **Language:** GML (GameMaker Language)
- **Sprites:** [Kenney.nl](https://kenney.nl) — Animal Pack Redux (Public Domain)
- **Version Control:** GitHub

---

## 📁 Project Structure

```
/objects
  obj_bunny       — Player character, movement & path recording
  obj_shadow      — Ghost bunny, replays recorded path
  obj_carrot      — Collectible, triggers shadow spawn
/sprites
  sbunny2         — Player bunny sprite
  s_alpha         — Shadow bunny sprite
/rooms
  Room1           — Main game room
```

---

## 🚀 How to Run

1. Open the `.yyp` file in **GameMaker Studio 2**
2. Press the **Play** button (F5) to run
3. Use arrow keys to move your bunny
4. Collect carrots, avoid your shadows!

---

## 📜 Game Objects

### `obj_bunny`
The player. Moves on a 32px grid using arrow keys. Records every hop into a `ds_list`. When a carrot is eaten, the path is handed off to a new shadow.

### `obj_shadow`
The ghost. Receives a copy of the bunny's recorded path and replays it hop by hop. Tinted blue and semi-transparent. Destroys itself after finishing the path.

### `obj_carrot`
The goal. When eaten, it spawns a shadow, moves to a new random position, and adds one more carrot to the field.

---

## 💡 Inspiration

Inspired by the concept of **Git version control** — each shadow represents a "commit" of your past actions. Colliding with a shadow is a **Merge Conflict**. Winning the game means your **Build is Successful**.

---

## 📄 License

Art assets from [Kenney.nl](https://kenney.nl) are Public Domain (CC0).  
Game code is open source — feel free to fork and build on it!

---

*Made with ❤️ in GameMaker Studio 2*
