# e-dig
The ultimate lightweight CLI tool for high-quality audio sampling and crate-digging.

`e-dig` automates the process of pulling high-fidelity audio from the web, handling the heavy lifting of metadata tagging and file conversion so you can stay in the creative flow.

## Features
- **High-Fidelity:** Downloads in lossless FLAC format by default.
- **Auto-Tagging:** Automatically embeds Channel, Date, and Title into metadata.
- **Batch Processing:** Dig through entire lists of URLs via text files.
- **Instant Audition:** Use the `--mpv` flag to listen to your sample the second it finishes.
- **Clean Filenames:** Saves files using the video title for easy organization in your DAW.

## Installation
1. **Clone or download** the script.
2. **Make it executable**:
```
chmod +x e-dig.sh
```
3. **Initialize dependencies:**
`e-dig` uses `yt-dlp`, `ffmpeg`, and `mpv`. Run the built-in installer:
```
./e-dig.sh -i
```

## Usage
```
./e-dig.sh [OPTION]
```

Description
--help  Show help message
-u, --url   Prompt to paste one or more YouTube URLs
-b, --batch [FILE]  Process a text file of URLs
-p, --path [DIR]    Specify a custom download directory
--mpv   Play audio immediately after download
-i, --initialize    Install/Update all required dependencies

## Examples
**Quick Dig (downloads to current folder):**
```
./e-dig.sh -u
```
**Session (saves to a specific folder):**
```
./e-dig.sh -p ~/Music/Samples/DrumBreaks -u
```
**Crate-Digging:**
```
./e-dig.sh --batch digging_list.txt
```
**"Speed-Digger" (download and audition immediately):**
```
./e-dig.sh --mpv -u
```

## Requirements
- Linux (Ubuntu/Debian preferred)
- `pipx` (used for managing `yt-dlp`)`ffmpeg` & `mpv`