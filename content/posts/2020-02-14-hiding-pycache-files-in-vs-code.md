---
template: post
title: Hiding Pycache Files in VS Code
slug: hiding-pycache-files-in-vscode
draft: false
date: 2020-02-14T12:36:19.816Z
description: >-
  If you've been working on Python projects in VS Code, you will notice that
  __pycache__ folders appear within your project directory and they result in a
  lot of visual clutter. This post will walk you through getting a little bit
  more zen back into your editor by freeing up visual real-estate so you don't
  need to look at it ever again!
category: Python
tags:
  - python
  - vscode
---
If you've been working on Python projects in VS Code, you will notice that \_\_pycache\_\_ folders appear within your project directory and they result in a lot of visual clutter. This post will walk you through getting a little bit more zen back into your editor by freeing up visual real-estate so you don't need to look at it ever again!

## Open Settings UI

In VS Code, open your settings via one of the following methods:

* Code > Preferences > Settings
* Cmd+Shift+P > Preferences > Open User Settings

Search for `files.exclude`

![](/media/vscode_files_exclude.png "UI Settings in VS Code")

Click on Add Pattern and type in ```**/__pycache__``` in the Exclude Pattern box and click OK.

## Open Settings (JSON)
If you'd prefer to edit a JSON file, open your preferences by entering Cmd+Shift+P > Preferences: Open Settings (JSON).

Find the entry for "files.exclude" and add the following entry:  
```**/__pycache__": true```

At the end, your settings should look like this:
```javascript
"files.exclude": {
        "**/__pycache__": true
    }
```

