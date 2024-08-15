# Download Youtube Transcripts

## Introduction

Download all transcriptions of a specific language from a given YouTube channel.

## Differences with the original project

-   Transcripts are saved in multiple files in a directory
-   Only saves transcriptions that weren't auto-generated
-   Ask for channel ID and language within the console
-   No need to edit the script, just the `.env` file
-   Show statistics while the process is running

## Dependencies

Make sure you have [Python](https://www.python.org/downloads/) installed.

You can check running `python --version` on your terminal.

## Setup

1. Clone this project and enter its directory

```bash
  git clone https://github.com/ElenaRgC/download-yt-transcripts
  cd download-yt-transcripts
```

2. Create a virtual enviroment and run it

```bash
  python -m venv venv
  source venv/Scripts/activate
```

3. Install dependencies

```bash
pip install -r requirements.txt
```

4. Create `.env` file

```bash
cp .env.example .env
```

5. Open the `.env` file and add your API KEY

```bash
nano .env
```

6. Run the script

```bash
  pyhton download-scripts.py
```

## How to obtain a YouTube API key

1. Login to [Google Developers Console](https://console.developers.google.com/project)
2. Click on _New project_
3. Give your project a name
4. Open the project dashboard if doesn't open automatically
    1. Click the three dots at the end of the project row and click on _Configuration_
5. On the search bar write "API" and click on "APIs and services"
6. On the left menu, click on _Credentials_
7. Click on the button _Create Credentials_ unther the search bar
8. Select _API Key_ and copy its value.
    1. This is what you need to add in the `.env` file
9. Back to the left menu, now open the _Library_
10. Search for "youtube data api v3" and open it
11. Authorize this API

## How to know a channel's ID

1. Open the desired YouTube channel in your browser
2. Click on **more** to open the channel info
3. Scroll down until you find _Share channel_ and click on _Copy channel ID_
4. The Channel ID is now on your clipboard

## Next steps

-   Check if the channel ID and language code are valid
-   Give different choices for transcriptions:
    -   None (just show statistics)
    -   Any (manually and autogenerated)
    -   Manually generated only
-   Multiple languages at the same time
-   Create directory as channel name and transcripcion files as video name
-   Save error logs
-   Improve the documentation
-   Show available languages
