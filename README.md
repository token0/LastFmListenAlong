# LastFmListenAlong - A program to listen along a Last.fm user with Spotify

## Description

LastFmListenAlong is a program allowing you to listen along a Last.fm user, playing the songs the user is listening to on Spotify, in real time.

## Configuration

First, you have to register an app on the [Spotify developper page](https://developer.spotify.com/dashboard/).
Do not forget to whitelist a callback URL for the app (eg. `http://localhost/`). Note the API key and secret and populate it in the code.

Then you need to get an API key and secret on the [Last.fm API page](https://www.last.fm/api/account/create), and populate it in the code.

## Dependencies

This program relies on the `spotipy` and `pylast` libraries. They also require `requests`. Install them with :

```bash
pip install spotipy
pip install pylast
pip install requests
```

Note that, at the date this program was created, the spotipy version installed by pip is a bit outdated and do not contain a method we need to play a song on Spotify.
You may need to get the last version of spotipy yourself here : [plamere/spotipy](https://github.com/plamere/spotipy) and place it in the current directory.


## Quick Start

Once everything is configured, you just have to run the program with two parameters:

```bash
python listen.py lastfm_user_to_listen_along your_spotify_username
```