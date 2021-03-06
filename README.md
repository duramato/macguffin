MacGuffin
=========

Automated tools for handling Scene and P2P film releases:
- Gather and verify metadata
- Take screenshots and upload them to an image host
- Create a .torrent file and upload it to a BitTorrent tracker


Requirements
------------

- Debian or Ubuntu (Mac OSX and Windows should work as well, with the right paths in config.py)
- Python 2.7, 3.2, or 3.3
- ffmpeg or avconv
- mediainfo
- unrar
  - On Debian 7 and above, you may need to pull the .deb for unrar from the squeeze repo:
    http://packages.debian.org/squeeze/i386/unrar/download
- python:beautifulsoup4
- python:requests


Installation
------------

- `sudo apt-get install unrar ffmpeg ffprobe mediainfo python-pip`
- `sudo pip install requests beautifulsoup4`
- [Download](https://github.com/hwkns/macguffin/archive/master.zip) or `git clone` this project's files
- Edit config.py with your details
  - If you don't already have an API key from [TMDB](http://www.themoviedb.org), just
    [sign up](https://www.themoviedb.org/account/signup) and request one from your
    [account page](https://www.themoviedb.org/account).


Usage (auto-upload)
-------------------

- `/path/to/macguffin/auto_upload.py -h`
- `/path/to/macguffin/auto_upload.py /path/to/Release.You.Want.To.Upload [/path/to/Another.Release ...]`
- `/path/to/macguffin/auto_upload.py *`
- Don't use sudo to run this script.  If you see "Permission denied" errors, add your user to the group that owns the
referenced directory and make sure it has group write permissions.


Usage (screenshots)
-------------------

- `/path/to/macguffin/screens.py -h`
- `/path/to/macguffin/screens.py /path/to/video.file.mkv`