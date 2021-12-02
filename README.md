# Win When They're Singing Quiz

## Introduction

Inspired by the Win When They're Singing round of the popular TV show "Richard Osman's House of Games", where contenstants have to guess when the singing starts on a given music track...however, the music fades out after a few seconds, so you have to keep time to the music, and know when the singing may start.

Unlike the TV show, this version does not give a buzzer to let contestants stop the stop watch, but does give the two ways to play the track (faded after a few seconds, plus not faded and stops the stop watch at the correct point)

## How it works

This simple adaptation gives you a web page that will show
1. A list of tracks
2. A prominant stop watch in the center of the page.

It is written in pure Javascript, so no need to download any additional frameworks etc. It should just run straight out of the box. 

Each track will have a Question link and an Answer link. 

The Question link will fade out the track from 5 seconds onwards (modify the fadeBeginAt constant to lower or increase this value). The fade takes 2.5 seconds (2 percent per 50ms). The timer will continue to tick for 25 seconds.

The Answer link will NOT fade the track, but the timer will stop at the predefined point (intended for when the singing begins).

Note - the timer should not start until the MP3 is downloaded. This should only really be noticable on first load, as the MP3 will be cached by the browser after it is downloaded once.


## How To Use

To use this for your own quizzes, you need to follow a few simple steps.

1. Download the (index.html) HTML file
2. Modify the source code of the HTML to point to your own MP3 tracks. Just edit the JSON `tracks` data near the bottom of the code. Make sure each ID is unique, set the URL to the MP3 you wish to play, and set the `stopAt` value to be the millisecond value of when the singing starts on the track.
3. Run on a simple HTTP server. My recommendation would be to save the file in it's own folder, and if you have python installed, use the built-in python http server by running `python -m http.server`. This will launch the server on http://localhost:8000
 

And that is it; you should be good to go! Tested in Chrome, Edge and Vivaldi browsers.


## Cloud Hosting

If you don't want to run locally, or you want others to access your quiz, then Cloud hosting should work fine. For example, you should be able to host this on a public cloud storage (like Google Cloud Storage), and make it internet visible. Just make sure the MP3s (if you are saving them to cloud storage too), are also accessible from the specified URL.


## Feedback

Enjoy and let me know how you get on. 
