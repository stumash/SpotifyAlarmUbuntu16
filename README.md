### SpotifyAlarmUbuntu16

Just like the name says, this repository has all the code you'll need to make an alarm clock out of Spotify on Ubuntu 16.  If all goes well, when Ubuntu's task scheduling tool, crontab, runs the script `playlist_alarm`, you'll see Spotify fire up, your volume get set low, the playlist/song of your choosing start playing and the volume gradually increase up to 85%.

#### Requirements
1. You already need to have Spotify (duh)
2. Your computer will need to be on for the alarm to work.

#### How to get it up and running
1.  Besides the files `README.md` and `crontab_excerpt`, this repository contains only bash scripts.  You'll need to move/copy/link them to /usr/local/bin and make them executable.
2. The script `playlist_alarm` relies on a username variable which is specific to you.  You'll need to write your Ubuntu username at the indicated location in that file.
3. The script `playlist_alarm` uses the "spotify URI" of the spotify playlist/song you want to play in order to play it.  You'll need to open Spotify, right click on the playlist/song you want and choose the 'Copy Spotify URI' option to copy it to the clipboard so you can paste it into `playlist_alarm` at the indicated location.
4. Read the `crontab_excerpt` file.  Then, type the command `crontab -e` and insert the appropriately formatted text as per the instructions in the `crontab_excerpt` file.  As mentioned in `crontab_excerpt`, the formatted text you insert after entering the command `crontab -e` will also require your username variable.

#### Enjoy!

----------

----------

#### Special Thanks
The `sp` program used in `playlist_alarm` for interacting with a running instance of Spotify was taken from [this gist](https://gist.github.com/wandernauta/6800547) on [Wander Nauta's Github](https://github.com/wandernauta).  