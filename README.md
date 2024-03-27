# Copy and set a user profile for gnome terminal 

I wanted to keep this somewhere in case i need to reference it in the future.  Included is the line of code to copy the current profile (on the current pc). Once you have this file you can use the other included line of code to set that profile onto a new machine.
The profile you grab can either be sent online, stored on a drive, or uploaded on git - then applied to any terminal you wish!

## Copy The Original Profile 
*copy the gnome-terminal profiles from original machine*

    $ dconf dump /org/gnome/terminal/legacy/profiles:/ > gnome-terminal-profiles.dconf

## Save.... Safely?

Store your files in a way it can be accessed in another location. flash-drives or git works really well for this! I personally recommend git so you can always have your desired terminal at quick access.

## Get Ready

You want to get the file on the new machine. Open the terminal from the location of the saved profile. (this can be done by right clicking and selecting open in terminal if you are not comfortable moving around via the command line. Once in position, fire off this next line!

## Set The New Profile
*set the gnome-terminal profiles on new machine*

    $ dconf load /org/gnome/terminal/legacy/profiles:/ < gnome-terminal-profiles.dconf

## Enjoy

You are done. Enjoy setting up a personal area so your friends are always jelly.... or share it... your choice
