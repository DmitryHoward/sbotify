## Inital Setup
This only needs to be done once.
```sh
$ openssl enc -d -aes-256-cbc -base64 -pbkdf2 -in .env.secrets -out .env
$ virtualenv venv -p /usr/bin/python3
$ source venv/bin/activate
$ pip install -r requirements.txt
```

## Hosting
Currently hosted in DigitalOcean. Login, go to `/srv/discord_playlist_manager` and run...
```sh
$ source venv/bin/activate
$ source .env
$ python main.py
```

## Re-encrypt keys
```sh
$ openssl enc -aes-256-cbc -base64 -pbkdf2 -in .env.secrets -out .env
```
