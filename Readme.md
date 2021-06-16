# Spotify Downloader
Downloads individual songs or playlists from Spotify as mp3 files. <br>
Songs are sourced from videos posted on youtube and song metadata is from the Spotify API.
<br>
<br>
## Features
* Downloads and writes song metadata
* Album Images, Artist Information, Track Title, embedded in mp3 file
* Concurrent downloading (multiple songs at a time) for playlists

## Dependencies
FFMPEG  - https://www.ffmpeg.org/

## Usage
```javascript
  var downloader = require('spotify-downloader');
  downloader.downloadTrack('spotify:track:2P4OICZRVAQcYAV2JReRfj', "song.mp3", function (err){
    if (err){
      console.log("download failed");
    }else{
      console.log("track download succeeded");
    }
  })

  downloader.downloadPlaylist('spotify:user:jackke1:playlist:02fquJWP9c20cobDsJrzfB', "playlist-directory", function (err){
    if (err){
      console.log("download failed");
    }else{
      console.log("playlist download succeeded");
    }
  })
```
