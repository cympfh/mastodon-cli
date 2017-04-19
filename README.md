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
# mastodon server
./mast server https://kirakiratter.com/

# make your app
./mast create-app "(app-name)"

# auth your account
./mast auth
(auth on your browser)
(copy&paste code)
```

All auth files are saved in `~/.mast`.

#### toot

```bash
./mast toot "Hi world!"
```

