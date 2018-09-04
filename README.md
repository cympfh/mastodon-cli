# mastodon CLI client

Supporting mutli instances!

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

