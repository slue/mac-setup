# Atom Editor

Atom is in some ways preferable to sublime, mostly because of its sidebar styling for git files.

### Install packages

* platform-ide-terminal
* merge-conflicts
* minimap
* atom-beautify
* file-icons
* git-plus
* highlight-line
* git-history \(needs fixed typo [see here](https://github.com/jakesankey/git-history/pull/40/files)\)

### Settings

Increase Lineheight: Add to stylesheet

```
.editor { line-height: 1.5 }
```

### keymap.cson

Add the following to keycap.cson

```
'body':
  'alt-cmd-j': 'pane:show-previous-item'
  'alt-cmd-k': 'pane:show-next-item'
```



