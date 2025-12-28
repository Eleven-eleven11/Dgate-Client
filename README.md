# Dgate-Client
This is the current build for the DGATE Client.
Markdown

# 🐉 Dragon's Gate: Modern Client

A specialized, Python-based MUD (Multi-User Dungeon) client designed for **Dragon's Gate**. Built with **PySide6** and **asyncio**, it combines the nostalgia of text-based gaming with modern power-user features like a GUI dashboard, automated scripting, and real-time mapping hooks.

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## ✨ Features

* **Modern Dashboard:** 3-pane layout with dedicated windows for Chat, Telepathy, Inventory, and Equipment.
* **Visual HUD:** Real-time health, fatigue, and encumbrance bars that parse server data automatically.
* **Scripting Engine:** Automate gameplay with a custom scripting language supporting variables (`$target`), math, and conditionals (`if/then`).
* **Triggers & Aliases:** Create complex regex triggers and command shortcuts.
* **Smart Scrolling:** Chat windows that don't jump to the bottom while you are reading history.
* **Async Networking:** Non-blocking connection ensuring the interface never freezes, even during complex scripts.

---

## 🛠️ Setup & Installation

### 1. Prerequisites
You need **Python 3.10** or higher installed. You can download it from [python.org](https://www.python.org/).

### 2. Install Dependencies
This client relies on `PySide6` for the interface and `qasync` to handle network tasks. Open your terminal or command prompt and run:

```bash
pip install PySide6 qasync
3. Download the Client
Clone this repository or download the client.py file to a folder on your computer.

Bash

git clone [https://github.com/yourusername/dragons-gate-client.git](https://github.com/yourusername/dragons-gate-client.git)
cd dragons-gate-client
🚀 How to Run
Open your terminal/command prompt.

Navigate to the folder containing the script.

Run the client:

Bash

python client9.py
(Note: Replace client9.py with whatever you named your file).

A connection dialog will appear. Enter the Host IP and Port for Dragon's Gate (defaults are usually provided).

📖 Automation Guide
This client includes powerful tools to automate your gameplay. You can access these managers via the Automation menu in the top bar.

1. Aliases (Shortcuts)
Aliases let you type short commands to execute long actions.

Manager: Ctrl+A

Variables: Use $1, $2 to pass arguments.

Example:

Alias: k

Command: kill $1

Usage: Typing k goblin sends kill goblin.

2. Triggers (Reflexes)
Triggers watch the game text and react automatically.

Manager: Ctrl+T

Regex: Use (.*) to capture text into variables like $1.

Example (Auto-Eater):

Pattern: You are hungry

Action: eat bread

3. Scripting (Logic)
The client has a built-in scripting language for complex tasks.

Variables:

$myvar = User variables (set by you).

@hp, @max_hp, @fatigue = System variables (read-only stats).

Commands:

if [condition] then [action]

wait [seconds]

set $variable = value

call [sequence_name]

Example Script (Auto-Heal):

Plaintext

if @hp < 30 then drink potion
Example Sequence (Combat Loop): Create a sequence named auto_attack:

Plaintext

kill $target
wait 3
if $combat_active == 1 then call auto_attack
🤝 Contributing
This is an open project! If you want to improve the regex parsing for specific MUD server messages or add new GUI panels:

Fork the repo.

Create your feature branch (git checkout -b feature/AmazingFeature).

Commit your changes (git commit -m 'Add some AmazingFeature').

Push to the branch (git push origin feature/AmazingFeature).

Open a Pull Request.

📄 License
Distributed under the MIT License. See LICENSE for more information.
