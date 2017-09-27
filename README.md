# CampChamp
Download the music you own from Bandcamp.

## TODOs
Needs permission to access the external storage for downloading files.
### Login Screen
- Login screen UI
- Grab cookie and use in all further HTTP requests
### Collection screen
- Send a request for https://bandcamp.com/<Username> page
- Gather the entire user's collection information from this page (URLs or images themselves if URLs are not static). Download link.
- Store collection information locally. Only update when local and remote collection count differs.
### Download Screen
- Display "Download To" which displays the last selected path the user chose for downloading their music. Pressing it should open a directory picker, with ability to create folder, or delete on long press.
- Display spinner while waiting for download link to appear in background. When download link appears (downloadReady() callback in JavaScript or download-title class is visible, also enable download button in UI.
- Show selector for file types. If user selects a different type, again display spinner and re-enable download button when link available.
- If user presses download, send to system download manager in a background task. In foreground return to collection screen.
- On download completed callback, unzip into user's chosen music folder.
