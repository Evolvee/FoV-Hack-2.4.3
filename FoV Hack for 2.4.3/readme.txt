World of Warcraft The Burning Crusade client 2.4.3 FoV changing hack

Originally written by para_ at http://www.ownedcore.com/forums/world-of-warcraft/world-of-warcraft-bots-programs/wow-memory-editing/396751-fov-wow-2.html#post2718340
Modified for TBC by xarthasskrillexx

USAGE:
	fov.exe [desired fov]

Example:
	fov.exe 1.925

If desired fov is empty or invalid, you will be prompted for it by the program.

For a fov value very similar to WotLK and later on a 16:9 monitor, use 1.925. On a 16:10 monitor try 1.7325.
Default value in TBC is about 1.57

The change should persist through instance portals etc., but will reset if you /reloadui
or log out to change characters.

You'll probably want to run the program by making a shortcut to it for your convenience.
This way you can easily set the fov with a single doubleclick, until someone comes up with a tool
that makes the process more automatic.

To make a shortcut to change fov in Windows, right-click on fov.exe and pick "Create shortcut".
Then right-click on the shortcut and pick "Properties". In the Properties window, in the "Target" box,
after fov.exe add a spacebar and then your desired fov. For example:
	D:\Documents\wowfovhack\realrelease\fov.exe 1.925
Then hit ok, and now every time you launch this shortcut your WoW fov will be changed.

The program has to be run as administrator, or else it will not work.
Unfortunately, there's no easy way around this that I know of.








technical details:
Camera pointer in TBC is a double pointer. The first pointer is at 0xC6ECCC and has an offset of 0x732C.
The second pointer points to the camera memory block, and the offset to Fov from there is 0x40.
Fov is a float value.

further reading:
http://web.archive.org/web/20090212111448/http://www.madx.dk/wowdev/wiki/index.php?title=Camera
http://www.deathsoft.com/forum/index.php/topic/6957-cheat-engine-memory-offsets/