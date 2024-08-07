
▒█ ▒█ █▀▀█ █▀▄▀█ █▀▀ ▀▀█▀▀ █▀▀ █▀▀█ ▒█ ▄▀ █▀▀█ █▀▄▀█ █▀▀▄ █▀▀█ ▀▀█▀▀ ▒█▀▀█ █▀▀█ ▀▀█▀▀
▒█▀▀█ █▄▄█ █ ▀ █ ▀▀█   █   █▀▀ █▄▄▀ ▒█▀▄  █  █ █ ▀ █ █▀▀▄ █▄▄█   █   ▒█▀▀▄ █  █   █
▒█ ▒█ ▀  ▀ ▀   ▀ ▀▀▀   ▀   ▀▀▀ ▀ ▀▀ ▒█ ▒█ ▀▀▀▀ ▀   ▀ ▀▀▀  ▀  ▀   ▀   ▒█▄▄█ ▀▀▀▀   ▀

> 🇷🇺 README на русском доступен [здесь](README.md)

## Functionality
| Functional                                                     | Supported |
|----------------------------------------------------------------|:---------:|
| Multithreading                                                 |     ✅     |
| Binding a proxy to a profile                                   |     ✅     |
| Auto-purchase of items if you have coins (tap, energy, charge) |     ✅     |
| Support tdata / pyrogram .session / telethon .session          |     ✅     |
| Automatic key collection                                       |     ✅     |

## [Settings file (.env)](https://github.com/lolyinseo/HamsterKombatBot/blob/main/.env)
| Setting name                          | Description                                                                                                   |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------|
| **API_ID / API_HASH**                 | Data for working with Telegram session _(more details below)_ |
| **UPGRADE_DAILY_COMBO**               | Enable daily combo upgrade clicker _(True / False)_ |
| **BALANCE_STRATEGY**                  | Coefficient in the formula balance = pph * x. When purchasing cards, the bot will follow this formula  _(10)_ |
| **AUTO_UPGRADE**                      | Whether to upgrade the passive earn _(True / False)_ |
| **AUTO_CLICKER**                      | Enable automatic clicker _(True / False)_ |
| **WAIT_FOR_MOST_PROFIT_UPGRADES**     | Save money for the most profitable upgrade |
| **APPLY_DAILY_ENERGY**                | Whether to use the daily free energy boost _(True / False)_ |
| **MIN_BALANCE**                       | Minimal balance that always will be availble |
| **MIN_TAPS_FOR_CLICKER_IN_PERCENT**   | Minimum percentage of taps (of the available number) at which the clicker will be launched. _Default 80%_     |
| **SLEEP_INTERVAL_BEFORE_UPGRADE**     | Sleep before every upgrade. _default: [10, 40]_ |
| **USE_PROXY_FROM_FILE**               | Path to file with proxy  |

## [Profile files](https://github.com/lolyinseo/HamsterKombatBot/blob/main/profiles/example.json)
Profiles are generated automatically if you use authorization through this bot. You can create a profile manually if you already have an authToken [read more](docs/android-auth-info-extraction-guide_en.md). In this case, rename ./profiles/example.json. Fill in name, id and token.
 
## Quick Start 📚
1. To install libraries on Windows click on `INSTALL.bat`.
2. To start the bot use `START.bat` (or in console: `python main.py`).

## Prerequisites
Before you begin, ensure you have the following installed:
- [Python](https://www.python.org/downloads/) version 3.12

## [Obtaining Hamster Kombat authToken on Android device](docs/android-auth-info-extraction-guide_en.md)

## Obtaining API Keys(API_ID / API_HASH)
1. Go to [my.telegram.org](https://my.telegram.org) and log in using your phone number.
2. Select **"API development tools"** and fill out the form to register a new application.
3. Note down the `API_ID` and `API_HASH` in `.env` file provided after registering your application.

## Installation
You can download [**Repository**](https://github.com/lolyinseo/HamsterKombatBot) by cloning it to your system and installing the necessary dependencies:
```shell
~ >>> git clone https://github.com/lolyinseo/HamsterKombatBot.git
~ >>> cd HamsterKombatBot

#Linux
~/HamsterKombatBot >>> python3 -m venv hamsterbot
~/HamsterKombatBot >>> source hamsterbot/bin/activate
~/HamsterKombatBot >>> pip3 install -r requirements.txt
~/HamsterKombatBot >>> nano .env # Here you must specify your API_ID and API_HASH (If you don't have authToken)
~/HamsterKombatBot >>> python3 main.py

#Windows
~/HamsterKombatBot >>> python -m venv hamsterbot
~/HamsterKombatBot >>> hamsterbot\Scripts\activate
~/HamsterKombatBot >>> pip install -r requirements.txt
~/HamsterKombatBot >>> # Specify your API_ID and API_HASH in .env (If you don't have authToken)
~/HamsterKombatBot >>> python main.py
```

Also for quick launch you can use arguments, for example:
```shell
~/HamsterKombatBot >>> python3 main.py --action (1/2)
# Or
~/HamsterKombatBot >>> python3 main.py -a (1/2)

#1 - Create session
#2 - Run clicker
```
