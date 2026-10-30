# 🕰️ DOWN WE FALL

### *A twisted Wonderland action platformer — 12 realms, 72 stages, 36 bosses. One file. Plays on your phone.*

**▶ Play it:** `https://YOUR-USERNAME.github.io/YOUR-REPO/`

Down We Fall is a fast, modern, mobile-first platformer set in a dark and broken Wonderland. The Queen of Hearts has stolen Alice's twelve Hours, and each one is held by a nightmare keeper at the bottom of a different realm. Fall through every realm, take the Hours back, and find out why the hole never ends.

It is one self-contained `index.html`: no build step, no assets, no dependencies, no ads, no tracking. Every sprite, background, sound effect and music loop is generated in code.

---

## ✨ Features at a glance

| | |
|---|---|
| 🌌 **12 distinct realms** | Each with its own palette, parallax backgrounds, decor, enemy roster, music key and boss |
| 🗺️ **72 stages** | 6 per realm: run, secret, mini-boss, warp run, chase, realm boss |
| 👹 **36 bosses** | A mini boss, a second mini boss and a realm boss in every realm, with multi-phase patterns |
| 🐇 **11 enemy types** | Cards, bats, hoppers, spitters, armored knights, shy ghosts, bombers, droppers, lobbers, tumblers, lantern fliers |
| ⚔️ **Real moveset** | Slash, blade wave, dash, double jump, wall jump, glide, coyote time, jump buffering, variable jump height |
| 📖 **Full story** | Prologue, per-realm intro and post-boss scenes, a twist ending and an epilogue, narrated by the Cheshire Cat |
| 🛒 **Meta-progression** | Spend watches in the Hatter's Shop on upgrades and dress cosmetics |
| ⭐ **Star ratings** | 3 stars per stage: clear it, collect 75% of the watches, finish without dying |
| 🔁 **New Game+** | Finish the game and the bosses hit harder, and so does the dark |
| 💾 **Auto-save** | Progress saves in your browser (`localStorage`) |

---

## 🎮 Controls

### Touch (phones and tablets)
The game always plays in landscape. On Android it requests a landscape lock on your first tap; on any phone held (or locked) in portrait, the whole game rotates itself to fill the screen, so just turn the phone sideways. The on-screen pad appears only during play.

| Button | Action |
|---|---|
| ◀ ▶ | Move |
| **JUMP** | Jump (hold for higher, tap again for double jump once unlocked, hold while falling to glide) |
| ⚔ | Slash / fire blade wave once unlocked |
| » | Dash (greyed out until you earn it) |
| **II** (top right) | Pause: resume, restart stage, world map, sound |

### Keyboard
| Key | Action |
|---|---|
| ← → / A D | Move |
| Space / ↑ / W / Z | Jump |
| X / J | Attack |
| C / K / Shift | Dash |
| P / Esc | Pause |

---

## 🧠 Abilities (earned from realm bosses)

| Boss realm | Power |
|---|---|
| 1. The Rabbit Hole | **Dash**: blur through danger with brief invulnerability, damages enemies |
| 2. The Hall of Doors | **Double Jump** |
| 3. The Mad Tea Party | **Wall Jump** |
| 4. The Pool of Tears | **Blade Wave**: your sword throws light |
| 5. The Caterpillar's Haze | **Glide** |

Levels are always completable with base moves, so powers make you faster and safer but never gate progress.

---

## 🌍 The twelve realms

1. **The Rabbit Hole**: boss *The Late Rabbit*, mini *The Doorman Card*
2. **The Hall of Doors**: boss *The Door That Eats Keys*, mini *The Key Spirit*
3. **The Mad Tea Party**: boss *The Hatter*, mini *The Dormouse Teapot*
4. **The Pool of Tears**: boss *The Drowned Mouse*, mini *The Weeping Eel*
5. **The Caterpillar's Haze**: boss *The Hookah Caterpillar*, mini *The Smoke Ring*
6. **The Duchess' Kitchen**: boss *The Duchess*, mini *The Pepper Cook*
7. **The Cheshire Wood**: boss *The Cheshire Cat*, mini *The Lost Grin*
8. **The Painted Garden**: boss *The Five of Spades*, mini *The Two of Spades*
9. **The Croquet Grounds**: boss *The Flamingo Knight*, mini *The Hedgehog Ball*
10. **The Mock Turtle Shore**: boss *The Mock Turtle*, mini *The Lobster*
11. **The Looking-Glass**: boss *The Jabberwock*, mini *The Reflection*
12. **The Queen's Court**: boss *The Queen of Hearts*, mini *The Executioner*

### The six stages in every realm
1. **Run**: a full-length stage with checkpoint lanterns
2. **Secrets**: a hidden portal leads to a bonus room full of watches and hearts
3. **Mini-boss arena**
4. **Warp run**: secrets plus a warp mirror to jump ahead to later realms, ending in a second mini boss
5. **Chase**: a wall of darkness advances, so keep moving
6. **Realm boss**: the keeper of the Hour

---

## ⚙️ Systems

- **Hearts, not lives**: take damage, get knocked back, get brief invulnerability. Falling in a pit costs a heart and returns you to your last safe footing.
- **Checkpoint lanterns** heal and save your place within a stage.
- **Combo counter, hit-stop, slow-mo boss kills, screen shake, squash and stretch** for game feel.
- **Hazards**: spikes, springs, crumbling bridges, moving platforms, ceiling droppers, fuse bombs.
- **Boss patterns**: chargers, jumpers, shooters, flyers, summoners, rain attacks and blinkers, with phases that change at HP thresholds.
- **Procedural levels**: stages are generated from seeded segments, so each stage is always the same for every player, and tuned to stay passable.
- **Shop upgrades**: More Hearts, Sharper Blade, Quick Dash, Watch Magnet, Spring Heels, plus 6 dress cosmetics.
- **Haptics** on supported phones, **auto-pause** when you switch apps, and a **install-to-home-screen** friendly page (full screen, no browser bars).

---

## 🚀 Deploy to GitHub Pages

1. Create a new GitHub repository (public).
2. Upload all the files from the folder (`index.html`, `manifest.webmanifest`, `icon.svg`, `README.md` and the empty `.nojekyll`) to the repository root.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to *Deploy from a branch*, choose **main** and **/ (root)**, then **Save**.
5. Wait a minute or two. Your game is live at `https://YOUR-USERNAME.github.io/YOUR-REPO/`.

### Add to your phone's home screen
- **iPhone (Safari):** Share → *Add to Home Screen*
- **Android (Chrome):** Menu → *Add to Home screen* / *Install app*

The game runs in full screen from there.

---

## 🛠️ Tech notes

- Pure HTML5 `<canvas>` (logical resolution 640×352, scaled to fit), vanilla JavaScript, no libraries.
- Fixed 60 Hz simulation step, so gameplay speed is identical on 60, 90 and 120 Hz screens.
- Audio: procedural WebAudio sound effects and a per-realm generated music loop (no audio files). Audio starts after the first tap, as browsers require.
- Save key: `dwf3` in `localStorage`. To reset progress, clear this site's data in your browser settings.
- Single file, roughly 100 KB.

---

## 🧪 Testing status

Automated headless tests cover: all 72 stages generate and run without errors, all 36 bosses activate, stay in bounds and can be defeated, and the full flow (story, map, shop, results, ability grants, ending, New Game+) completes. Real-device play-testing is still welcome, so if a jump feels off, a stage is too hard, or something breaks on your phone, open an issue.

---

## 📜 Credits and license

Inspired by the characters and mood of Lewis Carroll's public-domain *Alice's Adventures in Wonderland* and *Through the Looking-Glass*. All code, art, audio and story in this game are original.

Free to play and share. Add a license of your choice (for example MIT) before accepting contributions.

*Down. Always down.*
