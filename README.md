<!-- <div align="center" id="top"> 
  <img src="./.github/app.gif" alt="metatube" />

  &#xa0;

  <a href="https://metatube.netlify.app">Demo</a>
</div> -->
<h1 align="center">MetaTube</h1>

<p align="center">
  <img alt="Github top language" src="https://img.shields.io/github/languages/top/JVT038/metatube">

  <img alt="Github language count" src="https://img.shields.io/github/languages/count/JVT038/metatube">

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/JVT038/metatube">

  <img alt="License" src="https://img.shields.io/github/license/JVT038/metatube">

  <img alt="Github issues" src="https://img.shields.io/github/issues/JVT038/metatube" />

  <img alt="Github forks" src="https://img.shields.io/github/forks/JVT038/metatube" />

  <img alt="Github stars" src="https://img.shields.io/github/stars/JVT038/metatube" />
</p>

<h2 align="center">Status</h2>

<h4 align="center"> 
	🚧  MetaTube 🚀 Under construction...  🚧 <br/>
</h4>
<p>
  It's definitely not finished yet and these features are currently supported:

  - Fetch information from a YouTube video based on an URL
  - Query and fetch results from the Musicbrainz API
  - Set up templates and options for the YouTube download
  - Download YouTube videos based on a selected template
  - Exclude fragments (such as intros, outros, etc.) from the download
  - Metadata from either the user or Musicbrainz can be merged with MP3, Opus, FLAC, WAV, OGG, M4A & MP4 files
  - Hardware encoding using NVENC, Intel Quick Sync
  - Hardware encoding is supported, but not yet tested for Video Toolbox, Video Acceleration API (VAAPI), AMD AMF & OpenMax OMX
  - Manually set height and width, if a video type has been selected
  - Store the information about downloaded releases in the database, to edit the downloaded content later after the download

  To-Do before the first release:
  - Support more extensions to merge metadata with.
  - For some reason, Musicbrainz prefers to show singles over Albums, while I want the opposite.
  - Some decent mobile support
  - Docker support
</p>

<hr>

<p align="center">
  <a href="#dart-about">About</a> &#xa0; | &#xa0; 
  <a href="#sparkles-features">Features</a> &#xa0; | &#xa0;
  <a href="#rocket-technologies">Technologies</a> &#xa0; | &#xa0;
  <a href="#white_check_mark-requirements">Requirements</a> &#xa0; | &#xa0;
  <a href="#checkered_flag-starting">Starting</a> &#xa0; | &#xa0;
  <a href="#memo-license">License</a> &#xa0; | &#xa0;
  <a href="#disclaimer">Disclaimer</a> &#xa0; | &#xa0; 
  <a href="https://github.com/JVT038" target="_blank">Author</a>
</p>

<br>

## :dart: About ##

I made this project to download videos from YouTube easier, by automatically fetching music metadata from MusicBrainz Picard. 

## :sparkles: Features ##

:heavy_check_mark: Automatically download YouTube videos <br/>
:heavy_check_mark: Add metadata from the Musicbrainz Picard database <br/>
:heavy_check_mark: Set start and end point to cut off any outros  and/or intros

## :rocket: Technologies ##

The following tools were used in this project:

- [Python](https://python.org/)
- [Flask](https://flask.palletsprojects.com/en/2.0.x/)
- [JavaScript](https://www.javascript.com/)
- [Python Musicbrainz](https://github.com/alastair/python-musicbrainzngs)
- [Bootstrap 4.6](https://getbootstrap.com/docs/4.6)
- [jQuery 3.6.0](https://jquery.com/)
- [Friconix](https://friconix.com/)
- [Youtube-DLP](https://github.com/yt-dlp/yt-dlp)
- [Sponsorblock.py](https://github.com/wasi-master/sponsorblock.py)
- [FFmpeg 4.4.1](https://ffmpeg.org/)

For a complete list, visit the [Dependencies overview](https://github.com/JVT038/MetaTube/network/dependencies#requirements.txt) in the Insights.

## :white_check_mark: Requirements ##

Before starting :checkered_flag:, you need to have [Git](https://git-scm.com) and [Python](https://python.org) installed.

## :checkered_flag: Starting ##
```bash
# Clone this project
$ git clone https://github.com/JVT038/metatube

# Access
$ cd metatube

# Skip these steps if you don't want to use a virtual environment
# Install virtualenv
$ pip install virtualenv
# Create virtual environment in current directory
$ virtualenv .
# Activate environment
# Windows:
$ cd Scripts
$ activate
# Linux:
$ source bin/activate
 
# Navigate to the root directory
$ cd ../

# Install dependencies
$ pip install -r requirements.txt

# Run the project
$ py metatube.py

# The server will initialize in the <http://localhost:5000>
```

Additionally, you can set the following environment variables:
Name | Description | Default value
---|---|---
PORT|Set the port on which the MetaTube server will be available|5000
HOST|Set the address on which the MetaTube server will run | 127.0.0.1
DEBUG|Whether to enable debug mode or not | False
DATABASE_URL | The URL to your Database. Currently only SQLite3 is supported. | sqlite:///app.db
FFMPEG | An absolute path to the folder containing ffmpeg. | Empty
```bash
# On Windows 10, you can set an environment variable like this: 
$ set ENVIRONMENT_VARIABLE = Value

# On Linux and MacOS, you can set an environment variable like this:
$ export ENVIRONMENT_VARIABLE = Value
```
Additionally you can create a file called `.flaskenv` and set the environment variables in there.
An example is provided in [example.flaskenv](example.flaskenv). You can use that template and rename the file to `.flaskenv`.

## :memo: License ##

This project is under license from GNUv3. For more details, see the [LICENSE](LICENSE) file.<br/>
I am not responsible for any legal consequences the user may or may not face by using this project.


Made with :heart: by <a href="https://github.com/JVT038" target="_blank">JVT038</a>

## To-Do
- [X] Add support for the use of proxies to download YouTube videos
- [ ] Add Docker support
- [ ] Add Github action / workflow thing, to automatically create Docker image upon a new commit
- [ ] Add it to the PyPi library
- [ ] Add support for sites other than YouTube
- [ ] Add support for YouTube playlists
- [ ] Add custom YouTube-DLP options
- [ ] Add support for H.265 / HEVC
- [ ] Add authentication system with an optional reverse proxy
- [ ] Add support for TheAudioDB
- [ ] Add support for YouTube Music 
- [ ] Add support for Last.fm!
- [ ] Add translations
- [X] Add a nice progress bar
- [X] Add a function to allow users to download the song onto their device
- [ ] Add in-built file explorer, making manual paths optional
- [ ] Add some nice animations
- [ ] Add a cancel download button when the video is being downloaded
- [ ] Add button in settings to download the entire SQlite3 Database
- [ ] Add button in settings to download all the downloaded content
- [X] Add ability to manually set video width & height, if a video type has been selected
- [X] Build a logger
- [ ] Give the user the option which level of logs to show / log and whether to save the logs to a file
- [ ] Catch and show errors properly
- [ ] Support looking for YouTube videos and downloading them
- [ ] Support querying the Musicbrainz database and matching YouTube videos with them
- [ ] Support MySQL
- [ ] Make a CLI to download and match music
- [X] Store the information of downloaded songs in a SQL database
- [ ] Make it mobile-friendly
- [X] Use Sponsorblock and yt-dlp to automatically skip fragments
- [X] Manually edit metadata of file, before the download
- [ ] Manually edit metadata of file, after the download
- [X] Select output type (coding, extension, etc.)
- [X] Switch from AJAX to websockets
- [X] Hardware transcoding with NVENC, Intel Quick Sync, Video Acceleration API (VAAPI) & AMD AMF
- [X] Improve the automatic creation of the database, the tables and the default rows, because it's horrible right now.
- [X] Use multiprocessing and websockets to make the overview page faster
- [ ] Dark mode support
- [X] Fix error `Synchronous XMLHttpRequest on the main thread is deprecated because of its detrimental effects to the end user’s experience. For more help http://xhr.spec.whatwg.org/` in overview
- [ ] Make sure the search for downloaded song field works
&#xa0;

## Disclaimer
I made this project to educate myself about Python, and to learn how metadata works in combination with files.
Additionally, I want to emphasize I do NOT encourage any pirating, or any other illegal activities.
This project's purpose isn't to illegally download content from YouTube; its purpose is to educate and enlighten myself (and others viewing the source code) about Python, how Python interacts with metadata in files, and  metadata works, and how yt-dlp works.
I am not responsible if the user downloads illegal content, or faces any (legal) consequences.


<a href="#top">Back to top</a>
