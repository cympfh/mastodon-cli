# mastodon CLI client

suppoting mutli instances

## requiments

- bash/zsh
- curl
- jq

## reference

1. https://github.com/tootsuite/documentation/blob/master/Using-the-API/API.md
1. https://github.com/tootsuite/documentation/blob/master/Using-the-API/Testing-with-cURL.md

## usage

```bash
./mast help
```

### init

```bash
# register a mastodon instance (server)
$ ./mast use kirakiratter.com

# `mast use` command can switch to another instance
$ ./mast use friends.nico

# check the default instance
$ ./mast use
friends.nico

# make your app (API client)
$ ./mast create-app "(app-name)"

# this command save a config file:
# ~/.mast/(server)/app.json

# auth your account
./mast auth
(auth on your browser)
(copy&paste code)

# this command save a config file:
# ~/.mast/(server)/auth.json

```

#### toot

```bash
./mast toot "Hi world!"
```

