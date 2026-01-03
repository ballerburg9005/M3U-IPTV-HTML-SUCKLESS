## About

You would think that an IPTV web player is a simple thing. Just a HTML video element, then a list of the channels, a way to supply an M3U file, perhaps some styling so it works on different screen configurations and phones, perhaps a search bar.

Yes it is that simple. But if you look at other projects like IPTVnator, the repo downloads 900MB (!), it is written in Angular (enterprise garbage), pulls a gazillion NPM dependencies, takes 30 minutes to set up for necessary non-standard "no npm" dev workflow, 3 minutes to compile, and has the worst of all stereotypical "100 full-time employees can't add a simple view counter below Twitter posts in 5 years" sickness of such frameworks. Even AI couldn't deal with it, because the codebase is so massive and Angular is just so retarded that it can't produce intelligible code for it. Then some players need Node JS servers, some need this and that, enforced access control for all content/playlists inside hardline user/session isolation and storage, needs backend server, docker-ized containers, Ruby x86 blobs make it impossible to run on Ampere/ARM server ... Why? Some players might be simpler, but they are also pretty basic - not unlike what you get from ChatGPT on first try. Then also even the most sophisticated IPTV projects don't really support mobile views and rotated screens, or not at all. And some have huge clunks.

Anyway... I hope this rambling spares you the Odyssee of trying to identify the "right" IPTV player.

Put this player on *any* webserver, supply your playlist and it just plays *instantly* for *anyone*.

Why all this nonsense with the other projects?

## Demo

[https://ballerburg9005.github.io/M3U-IPTV-HTML-SUCKLESS/](https://ballerburg9005.github.io/M3U-IPTV-HTML-SUCKLESS/)


## Features

* pure HTML/JS single file 300 lines of code
* instantly plays M3U from variable in code, or uploaded file, or URL
* widescreen / tallscreen
* full mobile phone layout support
* rotates fullscreen video to widescreen on mobile even if rotation locked via CSS (Firefox only)
* search bar
* subtitles, audio tracks, quality selection, skipback, normal video controls
* "find back" button to scroll channel list to current channel


## Screenshots (PC & Mobile)

![Image](https://github.com/user-attachments/assets/fc28bc63-f4c6-4a1d-a9d6-78470f3831db)


## Known Issues

* The manual control for qualilty selection went missing.
* fullscreen rotation hack for locked rotation ugly on Chrome and no interest to test & implement
* "find back" button doesn't always center the channel, sometimes slightly off screen
* moving the mouse causes massive CPU usage with 1000Hz mouse, makes interface feel sluggish (pls fix, too lazy)
* the tallscreen threshold should be 3:4 but it might be wrong (can't be bothered to check, might be relevant for some tablet devices)


## Development

Paste code into Grok Expert and fix it, then test if all features mentioned in the list still work right and do PR.

I just made this project today and it just works for me. So no real interest do do anything more at this point if no one else uses it.
