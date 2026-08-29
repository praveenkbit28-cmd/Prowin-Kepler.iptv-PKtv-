 ProwinKepler IPTV v18

ProwinKepler is a Python-based desktop multimedia hub with a **Neon Aurora** interface. It combines live TV, FM radio, movies, YouTube, music, podcasts, audiobooks and local media playback in one application.

## Features

### Live TV

- IPTV/M3U playlist support
- Loads local `tv.txt` files first
- IPTV-org fallback when no local playlist is available
- Tamil, Telugu, Hindi, Malayalam, Kannada, Bengali, Marathi and other regional categories
- News, sports, movies, entertainment, kids, cartoon, education and documentary sections
- Supports HLS `.m3u8` streams through VLC
- Automatic channel filtering and duplicate removal

### FM Radio

- Tamil FM stations
- Local and international radio categories
- Music, news, sports, devotional, classical, jazz, rock and other genres
- ON AIR indicator for radio playback

### Movies and YouTube

- YouTube search through `yt-dlp`
- Movie trailers and video search
- Trending, popular, recommended and category-based searches
- YouTube live streams
- Automatic playback URL extraction
- Auto-next playback
- Download support through `yt-dlp`

### Music

- Tamil, Hindi, English and regional music searches
- iTunes and YouTube Music sources
- Music categories including melody, romantic, devotional, remix, pop, rock, EDM and classical
- Audio playback with visualiser
- Lyrics and subtitle panel
- MP3 download support

### Podcasts

- Podcast search using iTunes and YouTube
- Technology, motivation, comedy, education, business, health, sports and storytelling categories
- Tamil, Hindi, English and regional podcast sections
- Podcast playback and download support

### Audiobooks

- Tamil stories and audiobook searches
- Fiction, non-fiction, mystery, thriller, romance, history, science and self-help categories
- Regional and English audiobook sections
- Audio playback and MP3 download support

### AV-Player

- Open local video and audio files
- Scan Downloads, Music and Videos folders
- Supported video formats include:

  `.mp4`, `.mkv`, `.avi`, `.webm`, `.mov`, `.flv`, `.wmv`, `.m4v`, `.ts`, `.m3u8`

- Supported audio formats include:

  `.mp3`, `.m4a`, `.aac`, `.ogg`, `.opus`, `.flac`, `.wav`, `.wma`, `.aiff`

### Advanced Player

- Play, pause, stop, previous and next controls
- Seek forward and backward by 10 minutes
- Volume control and mute
- Loop playback
- Playback speed control
- Subtitle and closed-caption support
- Custom subtitle file support
- Audio track information
- Player sizes: S, M, L and XL
- Fullscreen mode
- Progress bar for recorded media
- Live playback indicator for TV and radio
- Unified player for TV, music, podcasts, audiobooks and local files

### User Interface

- CustomTkinter dark theme
- Neon Aurora colour scheme
- Icon navigation rail
- Expandable nested menus
- Search bar for global media searches
- Lyrics and subtitles panel
- Status and playback indicators
- Date and time display
- Local media library support

## Requirements

- Python 3.10 or newer
- 64-bit VLC Media Player
- Windows, Linux or macOS
- Internet connection for online media sources

## Installation

### 1. Clone or download the project

```bash
git clone https://github.com/your-username/ProwinKepler.git
cd ProwinKepler
```

Alternatively, download the project ZIP file and extract it.

### 2. Create a virtual environment

#### Windows

```bash
python -m venv.venv
.venv\Scripts\activate
```

#### Linux or macOS

```bash
python3 -m venv.venv
source.venv/bin/activate
```

### 3. Install Python dependencies

```bash
pip install -r requirements.txt
```

If a `requirements.txt` file is not available, install the main packages manually:

```bash
pip install customtkinter requests python-vlc yt-dlp pygame
```

### 4. Install VLC Media Player

Download and install the **64-bit version of VLC Media Player**:

<https://www.videolan.org/vlc/>

The Python package `python-vlc` requires the VLC application and its media libraries to be installed separately.

Make sure the VLC version matches your Python architecture:

- 64-bit Python → 64-bit VLC
- 32-bit Python → 32-bit VLC

64-bit Python and 64-bit VLC are recommended.

## Running the Application

```bash
python ProwinKepler.py
```

If your file has a different name, use that filename instead:

```bash
python main.py
```

## Local TV Playlist

ProwinKepler searches for `tv.txt` in several locations, including:

- The project folder
- The current working directory
- Downloads
- Desktop
- Documents
- Other configured application locations

A basic M3U playlist should look like this:

```text
#EXTM3U
#EXTINF:-1,Tamil News Channel
https://example.com/channel/stream.m3u8

#EXTINF:-1,Music Channel
https://example.com/music/stream.m3u8
```

Save the playlist as:

```text
tv.txt
```

The application loads local channels first. If no local channels are found, it attempts to load channels from IPTV-org.

## Downloads

Downloaded content is saved in:

```text
ProwinKepler_Downloads
```

The folder is created automatically in the user's home directory.

Download support is available for:

- YouTube videos
- Music
- Podcasts
- Audiobooks

Downloads may require `ffmpeg` for audio conversion and video merging.

## Optional FFmpeg Installation

Some `yt-dlp` operations require FFmpeg.

Download FFmpeg from:

<https://ffmpeg.org/download.html>

After installation, add the FFmpeg `bin` directory to your system PATH.

You can verify the installation with:

```bash
ffmpeg -version
```

## Configuration

The application includes the following configurable features:

- Playback speed
- Volume
- Subtitle files
- Audio tracks
- Closed captions
- Player size
- Fullscreen mode
- Download folder
- Local media folders

The AI Chat section may require an API key depending on the configured provider.

## Troubleshooting

### VLC is not available

Install the 64-bit VLC Media Player and ensure that it matches your Python architecture.

Then reinstall the Python VLC package:

```bash
pip uninstall python-vlc
pip install python-vlc
```

### `customtkinter` is missing

```bash
pip install customtkinter
```

### `yt-dlp` is missing

```bash
pip install -U yt-dlp
```

### YouTube playback fails

Update `yt-dlp`:

```bash
python -m pip install -U yt-dlp
```

Some videos may be unavailable because of region restrictions, age restrictions, copyright restrictions or changes made by YouTube.

### Audio playback does not work

Install the required audio dependencies:

```bash
pip install pygame
```

Also verify that VLC is installed correctly.

### A stream does not play

Online streams may become unavailable, move to a different URL or require authentication. Try another channel or update your local `tv.txt` playlist.

## Project Structure

```text
ProwinKepler/
│
├── ProwinKepler.py
├── requirements.txt
├── README.md
├── LICENSE
├── tv.txt
└── ProwinKepler_Downloads/
```

The exact filename of the main Python script may be different depending on your project setup.

## Technology Stack

- Python
- CustomTkinter
- Tkinter
- python-vlc
- VLC Media Player
- yt-dlp
- Requests
- Pygame
- iTunes Search API
- IPTV-org playlists
- YouTube services

## Legal and Content Disclaimer

ProwinKepler is a media-player and content-discovery application. It does not host, own or control third-party streams, videos, podcasts, radio stations, music, movies or audiobooks.

Users are responsible for:

- Ensuring they have permission to access, stream or download media
- Following the terms of each third-party service
- Respecting copyright and intellectual-property laws
- Using legally obtained playlists and media
- Protecting API keys and other credentials
- Confirming that downloaded content may legally be stored or converted

Third-party streams and services may be unavailable, unreliable or subject to change.

## Licence

This project is licensed under the MIT License.

See the [`LICENSE`](LICENSE) file for details.

## Author

```text
Praveen Kalidass
```

## Version

```text
ProwinKepler v18
```

## Acknowledgements

ProwinKepler uses and integrates with open-source projects and public services, including:

- CustomTkinter
- VLC
- python-vlc
- yt-dlp
- Pygame
- Requests
- IPTV-org
- iTunes Search API

Please review the individual licences and terms of use for each dependency and service.
