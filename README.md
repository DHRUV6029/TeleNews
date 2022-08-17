# TeleNews, a Telegram news bot

![PyPI](https://img.shields.io/pypi/pyversions/Django.svg)

Contents:

1. [Introduction](#introduction)
2. [Requirements](#requirements)
3. [Setup](#setup)
4. [Usage](#usage)

# 1. Introduction

[Prototype] Jolt is a Telegram bot for users to read news and to create their own personal news bulletins.

# 2. Requirements

* newsapi-python == 0.2.5
* newspaper3k == 0.2.5
* python-telegram-bot == 12.1.1

# 3. Setup

1. Create a bot with Telegram's [Bot Father](https://telegram.me/botfather) bot. A guide to creating a bot with Bot Father can be found [here](<https://core.telegram.org/bots#6-botfather>).
2. Pass in your bot's API token in `main.py`:
```python
TOKEN = 'token'  # insert your telegram bot token here
```
3. Create an account with [newsapi.org](https://newsapi.org/) to get your newsapi key.

4. Pass in your key for newsapi in `newsfeed.py`:
```python
KEY = 'key'  # insert your newsapi key here
```
5. The bot is now ready. Run `main.py` to run the bot.

# 4. Usage


### Commands
Jolt uses slash commands to execute tasks.

* `/start` sends the news bulletin.
* `/search` initiates a news search. Use `/search <your search query>` to immediately get Jolt to search for `<your search query>`.
* `/help` shows the user what Jolt can do.

### News bulletin menus

Jolt uses [inline keyboards](https://core.telegram.org/bots/2-0-intro#new-inline-keyboards) to build its menus.

#### Main menu
The main menu presents the user with a list of five of the top headlines for Singapore news from newsapi.org.

#### Sub-menu
Clicking to read the story from the bulletin's main menu shows the individual news stories that have been summarised using newspaper3k. 

Users may also:

* read the full story by clicking the `Read full story here` hyperlink;
* toggle to other stories of the same topic using the story's navigation buttons, `Prev` or `Next`;
* or return to the main menu with the `Return to stories` button.


