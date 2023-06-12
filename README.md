## PLEASE NOTE

This fork is only to fix an issue with the URL parser (home/src/ta/urlparser.py) and allow downloading of the auto-generated "Favorites" playlist on older youtube accounts.

Currently the script does not identify these playlists as playlists because they are a shorter length ID.
To get around this, I modified the check of the ID slightly to check if the first two letters of the ID start with "FL". There was an existing check like this already, but it only looked to see if the ID was literally "LL" or "WL". These are the IDs of a user's liked videos playlist and watch later playlist.

The check's current method of determining whether an ID is a playlist is by the length of the ID. This is a bit backwards to me, as normal playlist IDs always start with "PL". So in theory this url parser script could be modified further to skip the length check if the ID starts with "PL".
