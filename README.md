# This is a custom variant for use with Kabaji's pugs. 
Not much differs from the original, other than I have made it a bit nicer visually and integrated Bootstrap CSS. 

This one can be seen at: https://pugs.kabajiow.com

This will have a few extra collaborators, and have custom stuff even more unique to pugs. 

## Summary of changes made

Some of the main changes I made include: 
  * Integrated BootStrap CSS 
    * This is because BootStrap is generally very responsive. 
    * While it's not perfect here (on mobile devices), [it DID get rid of of the lack of uniform text.](https://imgur.com/a/UHgTkGc) 
    * This is included via their public CDN - details [here](https://getbootstrap.com/docs/4.5/getting-started/introduction/#css)
    * I did not include any of the JS - it's not needed, I only care about the CSS. 
  * Why did I use BootStrap? 
    * It's responsive, easy to modify, and adds some consistency to the text. 
    * It also allowed me to convert the page to a 'dark' theme easily. 
  * Added a [Navbar](https://getbootstrap.com/docs/4.5/components/navbar/) to the top
  * Added some `<head>` tags for a new title, a profile, a favicon, etc. for embeds. 
  * Formatted the positioning of the 'add player' line so it's more uniform
  * Added a lot of div's to various regions with classes such as... 
    * `<nav class="navbar navbar-expand-md navbar-dark bg-dark">`
    * Notice the "bg-dark" above - this was used widely throughout (**bg-dark** is the darker background, **bg-secondary** is the lighter grey)
    * I also added various classes to the input buttons to change their appearance, such as...
    `<input value="Fill teams" class="big-btn text-light bg-secondary" type="button" onclick="fill_teams();" title=` 
    * Notice the "**text-light** and **bg-secondary** - this darkens the button, and makes the text a light color which is nicer to read. 
  * Moved all of the pre-existing JavaScript files (which essentially ensure this entire page runs smoothly) into a folder called scripts, and moved the stylesheet into a folder called 'css'

Overall, this was already great - I just did some tidying up to make it look cleaner.
Props to [adminimusRU](https://github.com/adminimusRU/OWcustomBalancer) as this was phenomenal as I dove further in. 

# Overwatch custom game balancer
Tool for balancing teams in Overwatch custom games.

[Live version on GitHub Pages](https://adminimusru.github.io/OWcustomBalancer/index.html)

## Features:
  * Advanced auto balancing algorithm:
    * Balancing teams by average SR and player's classes/roles;
    * Adjustable priority of balancing factors (SR and classes);
    * Tweakable average SR calculation depending on player's main class to reflect different gameplay impact;
    * Separation of similar one-trick ponies;
    * Tweakable player's SR calculation for classic balancing mode without class restrictions;
  * Balancing with role lock:
    * Adjustable role slots count;
    * Aims to put players to theim main role slot;
    * Adjustable balance factors priority;
  * Seamless switching between 'role lock' mode and classic (no restrictions) mode;
  * Supports separate SR per role (since Season 18);
  * Automatic calculation of team's average SR for manual balancing;
  * New players are added by BattleTag, all stats (current competitive SR, level, most played heroes and roles/classes) are automatically acquired via [OWAPI](https://github.com/SunDwarf/OWAPI);
  * Lobby used to store any amount of players (limited only by browser's storage size);
  * Player list import and export in JSON and CSV formats;
  * Team composition export in text, HTML and image formats;
  * Quick search for players in lobby by name or BattleTag;
  * Player sorting by name, SR or class (only for classic mode);
  * All added players and settings automatically saved in browser storage;
  * Multiple ways to move players between lobby and teams:
    * Drag & drop;
    * Double click (auto move to empty slot);
  * Adjustable team size and role slots (3x3, 6x6 or any custom size);
  * Player nickname, SR and class can be edited manually (right click on player);
  * Editable team names;
  * Stats can be updated for all players in one click or for specific player only;
    * Options for update only selected fields and exclude manually edited fields;
  * Outdated stats automatically updated on player transfer from lobby;
  * Region selection for stats (EU, US, KR).
