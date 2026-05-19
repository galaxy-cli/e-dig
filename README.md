# e-dig

A lightweight, high-performance CLI utility for music producers and crate-diggers to extract high-quality, metadata-embedded audio samples from the web.

### Prerequisites

- **yt-dlp**: The core download and metadata extraction engine
- **ffmpeg**: Required for audio conversion and extraction (`wav` encoding)
- **mpv**: Required for direct audio playback auditing (`--mpv` flag)

You can automatically configure and install all system requirements by running:
```bash
chmod +x e-dig
./e-dig -i
```

### Installation

Give the script execution permissions and move it into your local binary directory:

```bash
chmod +x e-dig
mv e-dig ~/.local/bin/          # Or anywhere else in your $PATH
```

### Usage

```bash
e-dig -u                       # Prompt mode: paste a URL interactively on launch
e-dig https://youtu.be...     # Direct mode: pass a URL straight to the command
e-dig --mpv -u                 # Audition mode: download and play instantly in the terminal
e-dig -p ~/Samples -u          # Target mode: download straight to a specific directory
e-dig -b links.txt             # Batch mode: process a text file of multiple URLs
```

### Options


| Option | Argument | Description |
| :--- | :---: | :--- |
| `-b, --batch`     | `FILE` | Batch process a list of tracking URLs from a text FILE |
| `-i, --initialize`| None | Install or update utility script requirements (`yt-dlp`, `ffmpeg`, `mpv`) |
| `--mpv`           | None | Simultaneously stream and play the audio instantly after downloading |
| `-p, --path`      | `DIR` | Specify a custom destination path download target DIR |
| `-u, --url`       | None | Trigger an interactive terminal prompt to paste a single URL stream |
| `-v, --version`   | None | Output current package and underlying engine version information |
| `--help`          | None | Show help message and exit |