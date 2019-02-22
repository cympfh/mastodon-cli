# mastodon CLI client

cURL like command-line tool for mastodon,
supporting multiple instances/accounts!

## requiments

- bash/zsh
- curl
- jq

## reference

1. REST API: https://github.com/tootsuite/documentation/blob/master/Using-the-API/API.md
1. Streaming API: https://github.com/tootsuite/documentation/blob/master/Using-the-API/Streaming-API.md
1. for cURL: https://github.com/tootsuite/documentation/blob/master/Using-the-API/Testing-with-cURL.md

## usage

```bash
# set PATH
$ export PATH=~/path/to/mastodon-cli/bin:$PATH
# run
$ mast help
```

### init

```bash
# register a mastodon instance (server)
$ mast use mstdn.jp

# `mast use` command can switch to another instance
$ mast use friends.nico

# check the default instance
$ mast use
friends.nico

# make your app (API client)
$ mast create-app "(app-name)"

# this command saves a config file:
# ~/.mast/(server)/app.json

# auth your account
$ mast auth

# starting authorization on your browser
# Accept if you can
# and copy&paste the CODE

# this command saves a config file:
# ~/.mast/(server)/auth.json

```

#### toot

```bash
$ mast toot "Hi world!"
```

#### multiple accounts on an instance

First, `mast use <domain>` makes a directory `~/.mast/<domain>`,
and authorization files will be made in it.
The auth files will be overwritten when another account log-in the domain.
So please rename the directory

```bash
mv ~/.mast/<domain> ~/.mast/<username>@<domain>
```

before log-in with another account.

You can specify the directory name.

```bash
$ mast use ampeloss@mstdn.jp
Your mastodon server is https://ampeloss@mstdn.jp/
$ mast use
ampeloss@mstdn.jp
$ mast toot "Toot from ampeloss"
```
