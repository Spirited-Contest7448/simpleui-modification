# Simple UI Modified — KOReader Plugin

![Image Alt]([image_url](https://github.com/Spirited-Contest7448/simpleui-modification/blob/main/UI%20Screenshot.png?raw=true)) 

> Tested on **Kindle Paperwhite 5 (2021)**  
> **KOReader:** v2026.03-81-g41c9e02b5 (2026-05-02)  
> **Simple UI:** 1.4.1

## About

This is a personal modification of the Simple UI plugin for KOReader, shared purely because people asked for it. **This is not meant to be a customisable or maintained plugin** — it is my personal setup, posted here due to allegations of gatekeeping. 😄 Use it as-is, or as a reference to make your own changes.

## What's Changed

- **Home screen recent books** displayed as a 3×2 grid with large portrait covers
- **Page indicator circles** shown below the grid when there are multiple pages (up to 18 books / 3 pages of 6)
- **Kindle-style book thumbnail** in the bottom bar (home screen only), tapping it opens the last read book
- **"Recent Books" title** font size locked so it no longer changes between launches
- **Home/Library labels** in the bottom bar displayed at larger font size

## ⚠️ Known Limitation

**Page navigation on the home screen is currently disabled.** The page indicator circles will show which page you are on, but swiping or tapping to go to the next page of recent books is not functional. This feature was disabled due to instability. Only the first 6 most recent books are shown. This may be fixed in a future update.

## Customisation

This plugin is **not designed to be customisable** and no support will be provided for modifications. That said, if you want to tweak the number of books shown on the home screen, you can edit the following values in `koreader/plugins/simpleui.koplugin/desktop_modules/module_recent.lua`:

```lua
local COLS      = 3   -- number of columns
local ROWS      = 2   -- number of rows
local MAX_BOOKS = 18  -- maximum books to fetch
```

Changing these values will also automatically resize the covers to fit the new grid — more books means smaller covers, fewer books means larger covers. For example, `COLS = 3` and `ROWS = 3` will show 9 books with smaller covers. You are on your own from here! 😄

## Installation

1. Download the ZIP file.
2. Connect your Kindle to your computer via USB and open the `koreader/plugins/` folder.
3. **Save a backup** of the existing `simpleui.koplugin` folder to your PC.
4. Delete the `simpleui.koplugin` folder from your Kindle.
5. Extract the ZIP file and paste the folder into the `koreader/plugins/` folder.
6. Rename the folder from `simpleui_modified` to `simpleui.koplugin`.
7. Safely eject your Kindle.
8. Open KOReader.

## ⚠️ Disclaimer

This plugin modification may not work for everyone. If KOReader crashes or behaves unexpectedly after installing, replace the new `simpleui.koplugin` folder with the backup you saved in Step 3 and everything will return to normal.
