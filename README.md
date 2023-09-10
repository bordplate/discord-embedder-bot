# Discord Embedder Bot

## Overview

This project provides a Discord bot that automatically downloads video clips from Twitch and Streamable when shared in a chat and re-uploads them directly to the Discord server. The bot also supports transcoding and recontainerizing .mkv files attached to Discord messages. It uses Python3 and relies on various libraries like discord.py, asyncio, ffmpeg, ffprobe, and requests.

## Prerequisites

1. Python 3.x
2. Discord Developer account to obtain a bot token
3. Twitch Developer account to obtain client_id and client_secret
4. ffmpeg and ffprobe installed in your system path

## Dependencies

Install Python dependencies using pip:

```bash
pip install discord.py requests
```

## Configuration

Open the script and populate the following variables:

- `TOKEN`: Discord Bot token
- `client_id`: Twitch API client ID
- `client_secret`: Twitch API client secret

## How the Bot Works

1. **Twitch Clips**: Whenever a Twitch clip link is posted in the Discord server, the bot will automatically download the video clip and then upload it to the Discord server.

2. **Streamable Clips**: Similar to Twitch clips, the bot will download and re-upload clips from Streamable.

3. **File Attachments**: For file attachments that are .mkv files, the bot can automatically transcode or recontainerize the video before uploading it to the Discord server.

### Additional Notes

- The bot automatically calculates the bitrate needed for transcoding based on a target file size of 23 MB (Discord's upload limit is 25 MB).

## Usage

Simply run the script:

```bash
python3 bot.py
```

## Contributing

Pull requests are welcome.

## License

This project is licensed under the MIT License.

