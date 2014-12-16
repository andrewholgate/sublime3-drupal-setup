# Sublime3 Drupal Development Setup

# 1. Install Sublime3 Text

Download and install [Sublime3](http://www.sublimetext.com/3) for your operating system.

# 2. Install Sublime3 Package Manager

The Package Manager allows for the easy installation of Sublime3 packages from [Package Control](https://sublime.wbond.net/) (the Sublime package manager).

- In order to easily install these 3rd party packages, you will first need to navigate to the [Package Control installer](https://sublime.wbond.net/installation#st3) and **copy** the code underneath the Sublime3 tab, which looks like:

```
import urllib.request,os,hashlib; h = '7183a2d3e96f11eeadd761d777e62404' + 'e330c659d4bb41d3bdf022e94cab3cd0'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

- In Sublime3, open the menu `View > Show Console` and a console will open at the bottom. **Paste** the code which you copied in the previous step and press enter. Sublime3 will then install the Package Control manager for you.

## Using the Package Manager

You can now quickly and easily install new Sublime3 packages by:

1. Open the Command Palette using `Ctrl/Cmd + Shift + p` - a small dialog box will appear at the top of the screen.

1. Start typing in the word `install` and the command `Package Control: Install Package` will appear. Hit enter or click on it.

1. After  few second the dialog box will show a list of all the packages available from the online Package Control. When you start to type the name of the package you want, it will autocomplete for you. Once highlighted, press enter and it will install the package for use in Sublime3.

# 3. Install Sublime3 Packages

Below is a non-exhaustive list of Sublime3 packages I use regularly for Drupal development.
Read the descriptions of each one for their exact usage.

## Drupal Specific Packages

- [Drupal](https://sublime.wbond.net/packages/Drupal)
- [Goto Drupal API](https://sublime.wbond.net/packages/Goto%20Drupal%20API)

## Theme Package

- [Theme - Flatland](https://sublime.wbond.net/packages/Theme%20-%20Flatland)

## Debugging Package

- [Xdebug Client](https://sublime.wbond.net/packages/Xdebug%20Client)

## Coding Standards and Helpers Packages

- [DocBlockr](https://sublime.wbond.net/packages/DocBlockr)
- [Auto Semi-Colon](https://sublime.wbond.net/packages/Auto%20Semi-Colon)
- [BracketHighlighter](https://sublime.wbond.net/packages/BracketHighlighter)
- [SublimeCodeIntel](https://sublime.wbond.net/packages/SublimeCodeIntel)
- [TrailingSpaces](https://sublime.wbond.net/packages/TrailingSpaces)
- [Trimmer](https://sublime.wbond.net/packages/Trimmer)
- [CSScomb](https://sublime.wbond.net/packages/CSScomb)
- [SublimeLinter](https://sublime.wbond.net/packages/SublimeLinter)
  - [SublimeLinter-php](https://sublime.wbond.net/packages/SublimeLinter-php)
  - [SublimeLinter-jshint](https://sublime.wbond.net/packages/SublimeLinter-jshint)
  - [SublimeLinter-json](https://sublime.wbond.net/packages/SublimeLinter-json)
- [SublimeLinter-csslint](https://sublime.wbond.net/packages/SublimeLinter-csslint)
- [Emmet](https://sublime.wbond.net/packages/Emmet)

## Other Packages

- [GitGutter](https://sublime.wbond.net/packages/GitGutter) (disable when using XDebug)
- [SideBarEnhancements](https://sublime.wbond.net/packages/SideBarEnhancements)
- [FileDiffs](https://sublime.wbond.net/packages/FileDiffs)

# 4. Drupal formatting

Configure Sublime3 formatting with common Drupal settings, such as 2 spaces for indents, an 80 character right boarder, etc:

Open the menu `Preferences > Settings - User` and **paste** the following and **Save**.

```
{
  "bold_folder_labels": true,
  "caret_style": "wide",
  "color_scheme": "Packages/Theme - Flatland/Flatland Dark.tmTheme",
  "default_line_ending": "unix",
  "draw_white_space": "all",
  "ensure_newline_at_eof_on_save": true,
  "fade_fold_buttons": false,
  "fallback_encoding": "UTF-8",
  "find_selected_text": true,
  "font_options":
  [
    "subpixel_antialias"
  ],
  "font_size": 12.0,
  "highlight_line": true,
  "line_padding_bottom": 1,
  "open_files_in_new_window": false,
  "rulers":
  [
    80
  ],
  "ignored_packages":
   [
    "Vintage"
  ],
  "shift_tab_unindent": true,
  "soda_classic_tabs": true,
  "tab_size": 2,
  "theme": "Flatland Dark.sublime-theme",
  "translate_tabs_to_spaces": true,
  "trim_automatic_white_space": true,
  "trim_trailing_white_space_on_save": true,
  "use_tab_stops": true,
  "word_separators": "./\\()\"'-:,.;<>~!@#%^&*|+=[]{}`~?"
}
```

If you want to set these formating rules on a project or languuage basis, read the [settings documentation](http://www.sublimetext.com/docs/3/settings.html).


View HTML version at: http://andrewholgate.github.io/sublime3-drupal-setup/
