# RubyMine Atom Sublime Text (RMAST)

I love me some RubyMine. But I didn't want to give up the great key bindings from Atom and Sublime Text. So I started looking for resources that could help me bridge the three editors. This RMAST ("R Mast ") repo is the result.    

With this repo...  
  
- I added the best Atom and Sublime Text 3 (ST3) key bindings to the RubyMine (RM) key map. 
- I made a cheatsheet to help drill them into my head

## Why

- RubyMine is great. But being able to jump to ST3 or Atom is very handy and avoids letting one editor "lock you in"
- ST3 is the "industry leader" with nice key mappings and multiple cursor option. Atom has followed the ST3 lead with most key bindings.
- I wanted to practice on one keymap that works well on all three editors. And I needed a cheat-sheet to help me practice the most useful editor key bindings.  

## Notes

- `/` is used in the chart below to separate similar commands, it is not meant to be typed
- Where conflicts occurred when adding a new binding, the default RubyMine key binding was removed to prevent future errors & unintended actions
-  Some of the key mappings - such as the RubyMine editor pane management command 'Split Vertically' - are not a direct mapping of ST3 or Atom. But they are the closest RM comes to the same intent (in my opinion)

---

## Search & Navigation

| **RM Keymapping** | **RM Action Name** | **Re-map?** | **Standard RM?** | **Notes** |
| --- | --- | --- | --- | --- |
| ⇧\*2  (Double Shift) | 'Search Everywhere' |   | X | Similar to combination of ST3 ⌘⇧P + ⌘P |
| ⌘⇧P | 'Find Action' | X |   | Mimic ST3: "Command  Palette" |
| ⌘P | 'File' | X |   | Mimic ST3: "Goto Anything" |
| ⌘E | 'Recent Files' |   | X | Search recent files, better than the default "switcher" |
| ⌘⇧F | 'Find in Path' |   | X | Find in project |
| ⌘⇧V | 'Paste from History' |   | X | Search & paste from clipboard history |
| ⌘B | 'Declaration' |   | X | Go to declaration of method |
| ⌘Y | 'Quick Definition' |   | X | "Peek" quickly at declaration definition with pop-up |
| ⌥- Enter | 'Show Intention Actions' |   | X | Show the "lightbulb" options ("intention actions") |
| ⌥⌘T | 'Surround With' |   | X | Surround a block of code. Ex. "If…Then…Else" |

## Tool Windows

| **RM Keymapping** | **RM Action Name** | **Re-map?** | **Standard RM?** | **Notes** |
| --- | --- | --- | --- | --- |
| ⌘\` | View > 'Tool Buttons' | X |  | Adds toggles for "Tool Windows" tool bar on screen edges |
| ⌘8  | Other > 'Database' | X |  | Adds toggle for "Database" tool window |
| ⌘0  | Other > 'Terminal' | X |  | Adds toggle for "Terminal" tool window |

## Tabs & Panels

| **RM Keymapping** | **RM Action Name** | **Re-map?** | **Standard RM?** | **Notes** |
| --- | --- | --- | --- | --- |
| ⌘⌃← / → | 'Select Next/Previous Tab' | X |   | Mimic Chrome; 2 modifiers = cycle between tabs in current column ("splitters" in RM terms) |
| ⌘⌥⌃↑ | 'Split Vertically' Editor Tabs | X |   | Personal choice - All 3 modifiers= add/drop/change columns ("splitters" in RM terms) |
| ⌘⌥⌃↓ |  'Unsplit' Editor Tabs | X |   | '' |
| ⌘⌥⌃←/→ | 'Move to Opposite Group' | X |   | Personal Choice - Moves the tab to a different column ("splitters" in RM terms) |
| ⌥Tab | 'Goto to Next Splitter' |   | X | Switches cursor focus between columns ("splitters" in RM terms) - ST3 binging of ⌘K or ⌘← / → was unreliable for me due to other Mac bindings; Atom has no standard key mapping |

## Edit Lines / Text

| **RM Keymapping** | **RM Action Name** | **Re-map?** | **Standard RM?** | **Notes** |
| --- | --- | --- | --- | --- |
| ⌘] / [ | 'Indent' / 'Unindent Line or Selection' | X |   | Mimic ST3 |
| ⌃⌘↑ / ↓ | 'Move Line Up/Down' | X |   | Mimic ST3 |
| ⇧⌘D | 'Duplicate Line' | X |   | Mimic ST3 |
| ⌃⇧K | 'Delete Line' | X |   | Mimic ST3 |
| ⌘J | 'Join Lines | X |   | Mimic ST3 - brings up the line below & adds to end of current line |
| ⌥⌘L | 'Reformat  Code' |   | X | 'Reformats' or 'prettfies' code based on syntax settings: aligns hashes, brackets etc. |

## Selections & Multi-Cursor

| **RM Keymapping** | **RM Action Name** | **Re-map?** | **Standard RM?** | **Notes** |
| --- | --- | --- | --- | --- |
| ⌘D | 'Add selection for next occurrence' | X |   | Mimic ST3 |
| ⌃⌘G | 'Select all occurrences' | X |   | Mimic ST3 |
| ⌘L | 'Select Line at Caret' | X |   | Mimic ST3 |
| ⌃⇧↑ / ↓ | 'Clone Caret Above' / 'Below' | X |   | Mimic ST3 |
| ⌘ Left Click | 'Add or Remove Caret' w/ mouse | X |   | Mimic ST3 |

---

## Setup
### Requirements
[RubyMine](https://www.jetbrains.com/ruby/)

### Importing Settings (Installing Keymaps)
1. Download the .jar folder 
	- Or...if you want to know exactly what you are downloading - download all other individual folders EXCEPT for the .jar folder. Then zip them & turn them into your own .jar folder (see "notes on .jar files" below).
2. Go to File > Import Settings and specify the directory where the `rubymine_atom_sublimetext_RMAST.jar` lives. 
3. Click on "Keymaps" and click `OK`.
4. Restart RubyMine
5. Go to Preferences > Keymap > Keymaps and select the new keymap `RMAST`

### Exporting Settings
1. RubyMine > File > Export Settings...
2. You can just chose "Keymaps" for the export, or select all
3. RubyMine will export a .jar file filled with your setttings

### Notes on .jar files
I'm not an expert in Java, but here's what I've learned

Mac:  
- You can safely turn `.jar` files into `.zip` files (and back again) just by changing the file extension  
- This allows you to examine the contents of the `.jar` file

## Contributing
If you have a new keybinding you think might fit the spirit of this repo:  
1. Submit your proposed key binding as an "Issue"  
2. If I like the binding I'll add it and post a new settings file  
3. If not, feel free to fork, modify and set-up your own keymap!  

### Questions, Feedback  
Please post questions or feedback in an [Issue](https://github.com/ckib16/rubymine_atom_sublimetext_RMAST/issues).

---

## Other RubyMine Stuff
### Disable Case Sensitivity
- RubyMine uses first letter case sensitivity per default. This means that if you type e, Exception won't be offered as a viable completion. This is why I disable case sensitivity completion.    
    - `Editor > General > Code Completion > Case Sensitive completion : NONE`  
	- [http://saqibrazaq.com/RubyMine-basic-configuration/](http://saqibrazaq.com/RubyMine-basic-configuration/)

### Theme changes: RM's Monokai theme w/ Darkula background
- Changed comments to gray
- Changed editor gutter to gray
- Changed font size to 14
- Changed line height to 1.2
- This is included in the settings above under `Colors` named `Monokai - RMAST`

### Helpful Plugins

| Plugin |  Description |
| --- | --- |
| Markdown |  markdown support and preview pane |
| Wrap to Column | forces soft wraps at column width, doesn't apply to text already there, just new text & when text is reformatted |
| Railways |  shows quick rake routes display as a side panel |
| Dash | ⌘⇧D for Dash documentation |

---
## About Me
* [Page](http://chriskibble.net)
* [Github](https://github.com/ckib16)

Inspired by [@leopku](https://github.com/leopku/rubymine-keymap-sublime)
