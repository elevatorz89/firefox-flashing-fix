# firefox-flashing-fix
Prevent firefox from blinding you when opening certain browser extensions in dark mode.
This page was originally made to target NightTab's flashing bug upon opening a new tab, but it works for any addon.

## Setup
1. Go to `about:config` and set `toolkit.legacyUserProfileCustomizations.stylesheets` to true. This will allow you to load the style sheet.
2. Go to `about:profiles` and open the root directory of the profile currently in use.
3. Add the `chrome` folder from this repository to the profile folder.
4. Open the userContent.css file in a text editor.
5. Open `about:addons`, click on the settings gear, and click "Debug Addons".
6. Copy and replace `EXTENSION_UUID_HERE` with the targeted extension's Internal UUID.
7. Add an extra CSS rule if you have multiple extensions to target, or simply remove the  `EXTENSION_UUID_HERE/` from the first line of the CSS rule. Remember to remove the trailing slash as included in the code block.
8. Restart firefox.
