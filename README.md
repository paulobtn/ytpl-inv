#ytpl-inv

I wanted a way to transfer my youtube playlists to Invidious so I created this
small script to extract youtube playlists to a json format accepted by some invidious instance.

## Install

put the bm file somewhere you can run it:
```bash
([ -d "$HOME/.local/bin" ] || mkdir -p "$HOME/.local/bin") && \
curl -sSL https://raw.githubusercontent.com/paulobtn/ytpl/main/ytpl -o "$HOME/.local/bin/ytpl" && \
sudo chmod +x "$HOME/.local/bin/ytpl"
```
to launch as "ytpl" you need to add $HOME/.local/bin to your path
```bash
export PATH="$HOME/.local/bin:$PATH"
```

### Dependencies

* [youtube-dl](https://github.com/ytdl-org/youtube-dl) to fetch the metadata in json format
* [jq](https://github.com/stedolan/jq) to parse the json data

## Usage

extract the playlist to a json file
```bash
ytpl [playlist-url] >> playlist.json
```

On your favorite invidious instance, import the created json with "Import invidious data" 

## License
License GPLv3<br>
This is free software: you are free to change and redistribute it.<br>
Written by Paulo Neto

