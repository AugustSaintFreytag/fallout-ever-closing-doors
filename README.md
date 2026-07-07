# Saint's Ever-Closing Doors

A mod for Fallout: New Vegas / Tale of Two Wastelands that adds auto-closing logic for all doors in the game. Written in NVSE, lightweight, ESPLess.

## About

Tired of traversing Rivet City and being blocked by every single NPC leaving every single room door open on their way to get breakfast at Gary's Galley? Let doors be closed forevermore.

- All doors opened by NPCs will be auto-closed after a time delay.
- The time to close is tracked separately for each door.
- Only doors that were previously interacted with get closed.
- Doors only get closed if the player is far enough away.

## Configuration

Mod behavior can be customized with the included config file. You can change the time delay, tick interval, minimum distance, and more.

Use the `Doors.ini` keywords file to blacklist doors that should not be closed. This should include doors exclusively used for scripted sections and generally uncloseable/unopenable doors.

## Notes

Playing with this mod adds a risk of doors getting closed that are meant to be permanently open to the player. 

By default, the mod will only auto-close doors that either the player or an NPC have previously opened. This checks activation but also if the door's state actually changed after the interaction — the player can activate a non-interactible door, the activation will register, but it will not open or close. Activated doors that do not open will not be tracked.

Should you still find a locked door that is meant to be open (e.g. the bulk doors leading to the Project Purity chamber), you can open the console, click on it, and type `SetOpenState 1`. If you know the door's base id, you may also add it to `Doors.ini`.

## License

This mod was created by Saint for free use by the Fallout mod community under the MIT license. It may be shared, modified, or redistributed as part of mod packs with basic attribution.