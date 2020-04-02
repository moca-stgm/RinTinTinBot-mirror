# RinTinTin - a better GroupHelpBot for your network friend groups

## Table of contents:
- [Introduction](#introduction)
- [Scope of the software](#scope%20of%20the%20software)
- [Installation](#installation)



## Introduction

RinTinTin is a group helper bot to manage a network of groups with the same settings, welcome message, rules, permissions and all alike.

It was mainly created for the lack of features and the unaddressed bugs present in [GroupHelp](https://t.me/GroupHelpBot),
but then expanded to feature a more network-oriented approach for the [Computer Science Italia](https://t.me/CSItalia) network of friend groups.



## Scope of the software

RinTinTin doesn't aim to be a I-Do-Your-Job bot, but rather a helper to address and automate common tasks such as muting, warning and banning of a user.



## Installation

Prerequisites:
- Mysql (_or_)
- MariaDB (_or_)
- PostgreSQL (_or_)
- SQLite3 (defaults to `./data.db`)

Prerequisites for running the Docker image:
- Docker
- Docker-Compose

One-Command-Installation (preferred method):
```
curl https://git.bjphoster.com/bryanpedini/RinTinTinBot/glob/master/one-command-installer.sh -O - | sudo sh -
```
from inside the directory you want the bot to be running (prerequisite: `curl`)
<br>

Manual installation:<br>
First, get the binary executable in the desired directory (prerequisite `curl` || `wget`, latter as default)
```
VERSION=<version> wget https://git.bjphoster.com/bryanpedini/RinTinTinBot/releases/download/`echo $VERSION`/RinTinTin-`echo $VERSION`-`uname -s`-`uname -m`-bin -O RinTinTin
```
Then, let the program generate the example configuration file, and adjust that as you see it fit your needs
```
./RinTinTin --generate-default-config
```
Now, optionally, install the custom service file to let the bot be ran at startup, quickly reloaded, and restarted (assuming `systemd` instead of `init.d`)
```
sudo wget https://git.bjphoster.com/bryanpedini/RinTinTinBot/glob/master/conf/RinTinTin.service -O /usr/lib/systemd/system/RinTinTin.service
```
