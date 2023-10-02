---
title: Ronhorn Bot
layout: page
description: A documentation of Ronhorn, Longhorn Riichi's Discord bot 
---

# {{ page.title }}

Ronhorn is Longhorn Riichi's Discord Bot, which supports two categories of slash commands:
1. commands specific to Longhorn Riichi's club operations (`/register`, `/enter_score`, etc.)
2. commands that provide utilities for online mahjong games like [Mahjong Soul] and [Tenhou] (`/skill`, `/parse`, etc.)

It also tracks and records online games played in the club's Mahjong Soul lobbies. This documentation only covers the active component (Discord slash commands).

# Club Operation Commands

## Help commands

#### `/help`
Privately displays help about club online games, including the [Mahjong Soul] lobby IDs and how to start club games.

#### `/help_commands`
Privately displays a list of bot commands and their usages.

#### `/help_officer_commands`
Privately displays a list of officer-only bot commands and their usages. (only usable by officers)

## Registration commands

#### `/register real_name [friend_id]`
Registers the user's Discord account with the club. Registration is required to show up on the club leaderboard. Must enter a preferred name, and optionally the user's Mahjong Soul account. Can be used to update an existing registration.

#### `/unregister`
Removes your own registration (from `/register`).

#### `/unregister_other server_member`
Unregister a given Discord user. (only usable by officers)

## Membership Management Commands

#### `/update_membership server_member membership`
Updates a given Discord user's paid membership status. (only usable by officers)

#### `/replace_role old_role [new_role]`
Removes a role from everyone, or replace a role with another one for everyone with that role. (only usable by officers)

E.g., replacing all "@Paid Member" with "@Past Paid Member" when a new season starts

## Club Game Commands

#### `/enter_scores game_type east_player east_score south_player south_score west_player west_score [north_player] [north_score] [riichi_sticks]`
Records scores for an in-person game. Inputs scores according to starting seats (e.g. `east_player` is the starting East player.) If the given scores don't total up to the expected total score, the submission is rejected. (only usable by officers)

#### `/submit_game lobby link`
Records scores for a given Mahjong Soul club game. (only usable by officers)

#### `/toggle_auto_match enabled`
Enables or disables auto-matching for a given lobby. (only usable by officers)

#### `/check_queues [check_voice_channel] [exclude1] [exclude2] [exclude3] [exclude4]`
Checks to see if everyone is queued up in the Mahjong Soul club lobbies. Has an option to check the voice channel for players instead.

#### `/start_queued_games`
Start games for everyone queued up in the Mahjong Soul club lobbies.

### Ongoing game commands (Officer Only)
#### `/terminate_any_game lobby nickname`
#### `/pause_any_game lobby nickname`
#### `/unpause_any_game lobby nickname`

### Ongoing game commands
#### `/terminate_own_game lobby`
#### `/pause_own_game lobby`
#### `/unpause_own_game lobby`

# Online Mahjong Utilities

## Injustice Judge Commands

#### `/injustice link [player]`
Analyzes your [Mahjong Soul] or [Tenhou] game log to find instances of *mahjong injustice* for a given player. *Mahjong injustice* is when the bot finds perceived unluckiness.

Detailed documentation can be found [here](https://github.com/Longhorn-Riichi/InjusticeJudge#injusticejudge).

![`/injustice` command example](https://res.cloudinary.com/djvg6ubiy/image/upload/v1695713305/Ronhorn/injustice_wxvqhi.png)

#### `/skill link`
Analyzes your [Mahjong Soul] or [Tenhou] game log to find instances of *mahjong skill* for all players. *Mahjong skill* is when the bot finds perceived luckiness.

Detailed documentation can be found [here](https://github.com/Longhorn-Riichi/InjusticeJudge#skills).

![`/skill` command example](https://res.cloudinary.com/djvg6ubiy/image/upload/v1695713305/Ronhorn/skill_jt6fav.png)

#### `/parse link [display_hands]`
Outputs a list of hands from your [Mahjong Soul] or [Tenhou] game, including info like round number, round result, and optionally the round winner's starting hand and/or winning hand (optionally only mangan+ hands, like the example below).

![`/parse` command example](https://res.cloudinary.com/djvg6ubiy/image/upload/v1695713306/Ronhorn/parse_ggx6lu.png)

## Miscellaneous Commands

#### `/display text`
Writes a message, replacing mahjong notation (like 123p 3z3Z3z) with mahjong tile emotes. `/display` can also display dora tiles, which is beyond the capabilities of the [Jekyll Mahjong plugin].

![`/display` command example](https://res.cloudinary.com/djvg6ubiy/image/upload/v1695713305/Ronhorn/display_iuuwco.png)

#### `/nodocchi tenhou_name`
Gets a Nodocchi link for a given tenhou.net username.

#### `/amae_koromo majsoul_name`
Gets an Amae-Koromo link for a given Mahjong Soul username.

# Club Tech Stack

For details about the club tech stack, including this website and all club bots, please visit [Longhorn Riichi GitHub]. As of September 2023, the primary contributors are [Peter](https://peterish.com/riichi-docs/my-riichi-presence/) and Dani (find us on [our server](/discord)).

[Mahjong Soul]: https://mahjongsoul.yo-star.com/
[Tenhou]: https://tenhou.net/
[Jekyll Mahjong plugin]: https://peterish.com/riichi-docs/jekyll-mahjong-plugin/
[Longhorn Riichi GitHub]: {{ site.data.socials.Github.url }}
