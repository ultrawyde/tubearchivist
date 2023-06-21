PLEASE NOTE

This fork is only to fix an issue with the URL parser (tubearchivist/home/src/ta/urlparser.py) and allow downloading of the auto-generated "Favorites" playlist on older youtube accounts.

The original method of determining whether an ID is a playlist was to check the length of the ID. That meant the script did not identify these playlists as playlists because they are a shorter length ID than the check allowed for. To get around this, I modified the check of the ID slightly to check if the first two letters of the ID start with "FL". There was an existing check like this already, but it only looked to see if the ID was literally "LL" or "WL". These are the IDs of a user's liked videos playlist and watch later playlist. Since normal playlists always start with "PL", I further modified it to automatically classify an ID as a playlist if it starts with "PL" as well.

How to use this:
Drop urlparser.py in /home/src/ta/ and overwrite the existing file.
