# audible-extractor
A collection of scripts to de-DRM audible files so that you can listen to them on any device

## Installation
1. Make sure you have the necessary dependencies installed
    * Python 2.7
    * Google Chrome
    * FFmpeg
    * libmp3lame (should be part of the `lame` package)
2. Download ChromeDriver from [here](https://sites.google.com/a/chromium.org/chromedriver/downloads) and place the extracted binary in the `./audible-activator` directory
3. Install necessary Python dependencies
    * `pip install requests selenium`
4. Run audible-activator
    * `python ./audible-extractor/audible-activator/audible-activator.py`
    * It will ask for the credentials to your Audible account and then will use ChromeDriver to log in and obtain the activation token
5. Copy the 8-character alphanumeric activation code
6. Run AAXtoMP3 (or FLAC) on the `.aax` file you want to extract
    * `bash ./audible-extractor/AAXtoMP3/AAXtoMP3.sh`
    * Usage: `bash ./audible-extractor/AAXtoMP3/AAXtoMP3.sh [--flac] [--single] AUTHCODE {FILES}`
