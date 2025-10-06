fd
# Mood-Terminal-
When you run the script; it asks how you're feeling (happy,sad,tired,etc ).It prints a unique motivational message or quote.It changes the terminal text colors .Logs your mood to a text file to track patterns over time. 
    example output How are you feeling today? sad
💬 “Tough times don’t last — tough people do.”
Your mood has been logged. Come back stronger tomorrow! 💪# 🌈 Mood Terminal

![import random
import datetime
import os

# Colors for fun
colors = ['\033[91m', '\033[92m', '\033[93m', '\033[94m', '\033[95m', '\033[96m']
reset = '\033[0m'

# Motivational messages
messages = {
    'happy': [
        "Keep spreading those good vibes 🌞",
        "Your smile is your superpower 😄"
    ],
    'sad': [
        "Tough times don’t last — tough people do 💪",
        "It’s okay to rest, but don’t quit ❤️"
    ],
    'tired': [
        "You’ve done enough today. Rest, recharge 💤",
        "Even machines need sleep — power down 😌"
    ],
    'angry': [
        "Breathe in peace, breathe out fire 🔥",
        "Channel that energy into greatness ⚡"
    ],
    'default': [
        "Stay consistent — small steps lead to big wins 🚀",
        "Every day is a new chance to level up 🎯"
    ]
}

# Ask user’s mood
mood = input("How are you feeling today? ").lower()

# Pick a random message
msg = random.choice(messages.get(mood, messages['default']))
color = random.choice(colors)

# Print with style
print(color + f"\n💬 {msg}" + reset)

# Log the mood
with open("mood_log.txt", "a") as log:
    log.write(f"{datetime.datetime.now()} - {mood}\n")

print("\nYour mood has been logged. Come back tomorrow! 💖")                         

How are you feeling today? tired
💬 You’ve done enough today. Rest and recharge 💤
🩷 Your mood has been logged. Come back tomorrow!

---

## 🧠 About

**Mood Terminal** is a fun, colorful Python project that checks in with your mood and gives you a motivational quote based on how you feel.

Each time you run it:
- 💬 You enter your current mood  
- 🌈 It responds with a random motivational message  
- 🗂 It logs your mood history in `mood_log.txt`

Perfect for developers who love self-care *and* clean code.

---

## 🚀 How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/YOUR-USERNAME/mood-terminal.git
   cd mood-terminal