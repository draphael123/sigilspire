# SIGILSPIRE — Audio Shopping List

Goal: grab free, **legally clean** audio, drop the files into the folders below with the
exact names, and I'll wire them into the game (with a mute/volume toggle).

---

## ⚖️ Licensing rules (read once)
This game gets deployed publicly, so only use:
- **CC0 / Public Domain** — best. Use freely, no credit, commercial OK.
- **CC-BY** — fine, but you MUST credit the author (track them in the "Attribution" section below).
- **Pixabay Content License** — free, commercial OK, no attribution required.

❌ Avoid: "personal use only", "non-commercial", most YouTube Audio Library tracks.

---

## 📁 Folder layout (create these inside the `sigilspire/` folder)
```
sigilspire/
  audio/
    sfx/     ← sound effects go here
    music/   ← music loops go here
```
Save files with the **exact target filename** in each table. Keep whatever extension you get
(.ogg / .mp3 / .wav all fine) — just tell me which, or default to what's listed.

---

## 🔊 SOUND EFFECTS  → `audio/sfx/`

| Game event | Target filename | Where to get it |
|---|---|---|
| Play a card | `card_play.mp3` | **Kenney – Interface Sounds** (CC0): a soft "click"/"select" |
| Draw/deal cards | `card_draw.mp3` | Kenney – Interface Sounds: a light "swish"/"tick" |
| Reaction triggers (combo) | `reaction.mp3` | **Pixabay Sound Effects**: search *"magic sparkle"/"spell"* |
| Combo up / high combo | `combo.mp3` | Pixabay SFX: *"power up"/"rising magic"* |
| Hit an enemy | `hit_enemy.mp3` | **Kenney – Impact Sounds** (CC0): `impactSoft`/`impactMetal` |
| You take damage | `hit_player.mp3` | Kenney – Impact Sounds: a heavier "thud" |
| Gain Block | `block.mp3` | Kenney – Impact Sounds: a "clank"/"shield" |
| Heal | `heal.mp3` | Pixabay SFX: *"heal chime"/"holy"* |
| Chain broken | `combo_break.mp3` | Pixabay SFX: *"error"/"glass break (soft)"* |
| Relic gained / proc | `relic.mp3` | **Kenney – RPG Audio** (CC0): a "coin"/"chime" |
| UI button / node select | `button.mp3` | Kenney – Interface Sounds: a clean "click" |
| Victory | `victory.mp3` | **Kenney – Music Jingles** (CC0): a short win jingle |
| Defeat | `defeat.mp3` | Kenney – Music Jingles: a short fail jingle |

### SFX source links
- Kenney (all CC0, no attribution): https://kenney.nl/assets/interface-sounds ·
  https://kenney.nl/assets/impact-sounds · https://kenney.nl/assets/rpg-audio ·
  https://kenney.nl/assets/music-jingles
  *(Each is a free ZIP of many sounds — pick the ones you like and rename to the target names.)*
- Pixabay SFX (free, commercial OK): https://pixabay.com/sound-effects/search/magic/ ·
  https://pixabay.com/sound-effects/search/whoosh/ · https://pixabay.com/sound-effects/search/fireball/
- Freesound (filter License = **Creative Commons 0**): https://freesound.org/search/?f=license:%22Creative+Commons+0%22

**Tip:** you only strictly need these 6 to feel great — `card_play`, `hit_enemy`, `reaction`,
`block`, `victory`, `button`. The rest are polish. Missing files are skipped gracefully.

---

## 🎵 MUSIC  → `audio/music/`
Pick looping/ambient tracks. Aim for ~1–3 min loops.

| Slot | Target filename | Vibe | Where to get it |
|---|---|---|---|
| Title + Map | `map.mp3` | calm, dark, arcane ambient | see below |
| Combat | `combat.mp3` | tense, driving, low percussion | see below |
| Boss (optional) | `boss.mp3` | big, dramatic, orchestral | see below |

### Music source links
- **Pixabay Music** (free, commercial OK, no attribution) — *easiest*:
  - Dark/ambient: https://pixabay.com/music/search/dark%20ambient/
  - Fantasy: https://pixabay.com/music/search/fantasy/
  - Battle: https://pixabay.com/music/search/epic%20battle/
- **FreePD** (CC0, public domain): https://freepd.com/ — good picks under *Scoring*, *Horror*, *Epic*.
- **Incompetech / Kevin MacLeod** (CC-BY — must credit): https://incompetech.com/music/royalty-free/music.html
  - Fitting tracks to search: *"Crypto", "Ossuary", "Myst on the Moor", "Long Note Two",
    "Deliberate Thought", "Volatile Reaction"*.
- **OpenGameArt** (filter CC0/CC-BY): https://opengameart.org/art-search-advanced?field_art_type_tid%5B%5D=12

---

## ✍️ Attribution (fill in ONLY for CC-BY tracks you use)
If you use anything CC-BY (e.g. Incompetech), record it here and I'll add a credits line in-game:
```
- <track name> by <author> — <url> (CC-BY 4.0)
```
CC0 / Pixabay picks need nothing.

---

## When you're done
Drop the files in `audio/sfx/` and `audio/music/` with the target names and tell me which
you got. I'll build the audio manager (preloading, per-event playback, music crossfade between
map/combat/boss, and a mute + volume control in a settings menu). Any file you skip is just
silently ignored, so you can start with a handful.
