# Battleship AI Game

A smart, Python-powered twist on the classic Battleship game — where you face off against a learning AI bot that improves its aim using Reinforcement Learning (RL) and MDP-style logic.

---

## Overview

This project is a desktop version of Battleship built with Python and Tkinter. It features an intelligent bot opponent that doesn't shoot randomly — it adapts based on hit patterns, uses a Q-table for reinforcement learning, and applies open-book strategies like checkerboard scanning and directional follow-ups.

Game outcomes are saved in a `reinforcement_data.json` file, allowing the bot to improve performance over time.

---

## My Role – *Aamna Khan*

As part of this team-based AI semester project, I contributed primarily to the **AI logic design**:

- **Designed and implemented** the AI decision-making in `bots.py`  
- Implemented basic **Q-table-based reinforcement learning**  
- Applied **MDP-style logic** for shot decisions (hunt, target, destroy)  
- Added smart features like **checkerboard scanning** and **orientation-based targeting**  
- Managed **game memory using JSON** so the bot could learn across sessions

---

## Features

- 🤖 AI bot with open-book strategy and RL-based learning
- 🧠 Smart targeting using hit-tracking and Q-value updates
- 🔄 Memory stored in JSON for persistent bot behavior
- 🖼 GUI built with Tkinter (with or without image backgrounds)
- 🧩 Supports custom bot integration

---

## 🛠️ Setup Instructions

1. (Optional) Install Pillow for background images:
   ```bash
   pip install pillow

2. Run the game:

   * With image support:

     ```bash
     python main.py
     ```
   * Without image support:

     ```bash
     python main_without_image.py
     ```

---
````
## 📂 Project Structure
.
├── main.py                  # Game launcher with images
├── main_without_image.py    # Game launcher without images
├── bots.py                  # AI logic and all bot classes
├── reinforcement_data.json  # Stores Q-table for RL
├── drawable/                # Background images (optional)
├── frames.py                # GUI frames
├── res.py, objects.py       # Game logic, helpers, resources
├── exceptions.py            # Custom error handling
````
---

## 🤖 Create Your Own Bot

Want to challenge the default bot? You can create your own strategy:

### 1. Define a Bot Class

In `bots.py`, add your custom bot class like this:

```python
class MyBot:
    def say(self, value: str):
        # return (x, y) coordinates based on the current game state
        return 5, 5 #placeholder values
```
Where `value` can be:

* `"shoot"` – it's the bot’s turn
* `"hit"` – bot hit a ship (not sunk)
* `"destroyed"` – bot sunk a ship

### 2. Register Your Bot

In `main.py`, find:

```python
self.__bot = bots.Fati()
```

Replace with:

```python
self.__bot = bots.MyBot()
```

Do the same in `on_game_back_button_pressed()` if needed.

---

> “It doesn’t just guess — it hunts.”
> — Battleship AI Bot

---

**Tags:**
`Python` · `Tkinter` · `Reinforcement Learning` · `Game AI` · `MDP` · `Battleship` · `Semester Project` · `Q-Learning`

```
