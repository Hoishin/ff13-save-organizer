# xiii-save-manager

Organize your FF13 practice save files and load into the game in order.

## Features

- [x] Organize save files and sort by chapter and file names
- [ ] Profile, allowing you to switch between different sets of saves

## Install

### Executable

1. Download executable from releases
1. Open Command Prompt or PowerShell to run the executable
   ```
   .\xiii-save-manager-x64.exe
   ```

### npm

1. Install with npm
   ```
   npm install -g xiii-save-manager
   ```
1. Run the command
   ```
   xiii-save-manager
   ```

## Usage

When you run for the first time, It will create `C:\Users\{USERNAME}\ff13-saves` folder with 13 folders for each chapter.

Put your practice saves into each folder. Next time you run the command, the saves will be copied to FF13 save files folder, sorted with chapter and file names.

**EXISTING SAVE FILES IN FF13'S SAVE FOLDER WILL BE OVERWRITTEN. BACKUP IF YOU NEED.**

You don't have to put saves into all folders. If a chapter folder is empty, it will simply be ignored.

### Put saves of all chapters

```
xiii-save-manager.exe
```

or

```
xiii-save-manager.exe all
```

### Put saves of specific chapters

Only Chapter 5

```
xiii-save-manager.exe 5
```

Chapter 12 and 13

```
xiii-save-manager.exe 12 13
```

## Under the hood

In-game save file list sorts them with `mtime`, the timestamp of when the save file was modified. This script uses npm package `utime` to modify that after copying save files.