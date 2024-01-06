# Music-CLI 🎹

Music-CLI is a toolbox with multiple scripts.

It uses speech recognition to play any song audio in MPD (Music Player Daemon). It uses YouTube as a source to fetch music and integrates with various libraries and tools to provide a seamless music playback experience.

- The `play-voice` script takes the model folder as argument (I renamed them for quick use).
- The `play` script doesn't use the voice recognition. It takes the prompt as argument.

## Prerequisite
- python (I use 3.11.6)
- ffmpeg
- mpd & mpc (`pacman -Ss mpd` you'll find both)
- [mpv](https://archlinux.org/packages/extra/x86_64/mpv/)
- unzip or any decompresser for the models
- [Desktop Notifications](https://wiki.archlinux.org/title/Desktop_notifications)
optional if you don't care or remove the last line of both scripts

## Installation

To install Music-CLI, follow these steps:

1. Clone the repository from GitHub: [github.com/SounaVR/music-cli](https://github.com/SounaVR/music-cli)

2. Copy both scripts into `~/.local/bin` on your system.

3. Install the required Python packages by running the following commands:

```
pip3 install vosk
pip3 install yt-dlp
```

4. Download the Vosk model from [alphacephei.com/vosk/models](https://alphacephei.com/vosk/models). It is recommended to download the lighter model with a smaller file size.

5. Put the model directory in `~/.local/share/models/`, or change the `VOSK_MODEL_PATH` variable to the path where you downloaded the Vosk model.

## Usage

Once installed and configured, you can use the scripts to play songs by following these steps:

### | play-video
- `play-video video_name` (use quotes for spaces like "4k wildlife")

### | play-music

- `play-music song_name` (use quotes for spaces like "Still Alive - Portal")

### | play-music-voice

- `play-music-voice model_folder`

- Speak the name of the song or artist you want to play.

- The will fetch the audio from YouTube and play it using MPD.

- Enjoy your music!

Please note that a working internet connection is required to fetch music from YouTube.

### Fun
Took me 4 FUCKING SECONDS TO GET A VIDEO WITH AUDIO ???? HELLO ??? EXCUSE ME ??
Goodbye YouTube fr fr

Between 3-4 sec to start a song with `play-music`.

Around 10 with `play-music-voice`

## License
- GPL-3

## Credit
- Did you missed it ? It's a fork but okay, here's the goat : [Bugswriter](https://github.com/Bugswriter/music_fairy) 🥇 (tysm btw 😘)
