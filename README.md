# doughbot
This bot is created with the [discord.py](https://discordpy.readthedocs.io/en/latest/whats_new.html#v1-4-2) version 1.4.2

## Installation
1. Install [Python](https://www.python.org/downloads/) (version 3.8 or higher)
2. Install [Poetry](https://python-poetry.org/docs/)
3. Install [MongoDB](https://www.mongodb.com/try/download/community)
4. Clone the repository and run `poetry install` within the project directory

## Setup
To actually run the bot you need to create a file called `config.json` in the top level of the project.

The config file has this format:
```
{
  "token": "<bot token>",
  "pixbay-key": "<pixbay API key>"
}
```
`<bot token` is the bot's token given by discord.
`<pixbay API key>` is the API key from pixbay.

Both of these are free to obtain so if doing any development you should get your own credentials so that nothing you do is will affect the live bot.

### MongoDB
Once you have MongoDB installed you need to create a database called `doughmee_server` with a collection called `muted_users`

## Running the bot
To run the bot type the following commands into your terminal (from within the project directory)
```
poetry shell
python doughbot/run_bot.py
```

## Lay of the Land
The bot has three main files, `doughbot/bot.py`, `doughbot/bot_helpers.py`, and `doughbot/run_bot.py`

`bot.py` contains all the main code of the bot.

`bot_helpers.py` contains general helper functions and decorators that are used within the bot.

`run_bot.py` is a simple script that will run the bot.
