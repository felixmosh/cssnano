# 4.0.0-rc.0

* Breaking: Drops support for Node 0.12, we now require at least Node 4.
* Breaking: Update PostCSS to 6.0.0.
* Breaking: Removes the browsers option, as it has been superseded by using
  Browserslist to supply a list of browsers; we recommend using the config file
  as the same values will be propagated to other cssnano plugins which have the
  same functionality. See https://github.com/ai/browserslist#config-file
  for more details.
* Breaking: Removes the `silent` option & logger; now stylehacks will add the
  warnings to `Result#messages`. If you would like logging this can be handled
  in your PostCSS runner.
* Breaking: Removes the CLI from stylehacks. We recommend using a PostCSS
  runner instead as it's easier to add stylehacks into an existing setup rather
  than using a separate command.

# 2.3.2

* Resolves an issue where stylehacks would crash on CSS mixins.

# 2.3.1

* Upgraded postcss-selector-parser to `v2.0.0`.
* Fixed an issue where stylehacks was not removing `*zoom: 1` from rules
  generated by other PostCSS plugins.

# 2.3.0

* Each warning now contains more information about the hack; what identifier
  it targets, what the hack is, and the browsers that it affects. E.g:
  
  ```js
  {
      browsers: [ 'ie 6', 'ie 5.5' ],
      identifier: 'selector',
      hack: '* html h1'
  }
  ```

# 2.2.0

* Added `value\9` hack.

# 2.1.0

* Added `html ~ /**/ body .selector` hack.
* Added a method to detect if a PostCSS node has any hacks.

# 2.0.0

* Added `body:empty` & `html:first-child` hacks.
* Upgraded to PostCSS 5.

# 1.0.0

* Initial release.
