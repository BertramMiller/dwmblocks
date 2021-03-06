# dwmblocks
Modular status bar for dwm written in c.
# modifying blocks
The statusbar is made from text output from commandline programs.
Blocks are added and removed by editing the blocks.h header file.
# Luke's bulid
I have dwmblocks read my preexisting scripts [here in my dotfiles repo](https://github.com/LukeSmithxyz/voidrice/tree/master/.local/bin/statusbar).
So if you want my build out of the box, download those and put them in your `$PATH`.
I do this to avoid redundancy in LARBS, both i3 and dwm use the same statusbar scripts.
# signalling changes
For example, the audio module has the update signal 10 by default.
Thus, running `pkill -RTMIN+10 dwmblocks` will update it.
# clickable modules
Like i3blocks, this build allows you to build in additional actions into your scripts in response to click events.
See the above linked scripts for examples of this using the `$BLOCK_BUTTON` variable.

For this feature to work, you need the appropriate patch in dwm as well. See [here](https://gist.github.com/danbyl/54f7c1d57fc6507242a95b71c3d8fdea).
Credit for those patches goes to Daniel Bylinka (daniel.bylinka@gmail.com).
