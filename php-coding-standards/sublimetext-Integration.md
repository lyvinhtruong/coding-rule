### Integrating PHPCS with Sublime Text 3
#### sublime-phpcs package
 Install the sublime-phpcs package, then use the "Switch coding standard" command in the Command Palette to switch between coding standards.
#### SublimeLinter-phpcs
 sublime-phpcs is insanely powerful, but if you'd prefer automatic linting, [SublimeLinter-phpcs](https://github.com/SublimeLinter/SublimeLinter-phpcs/) can do that.
 * Install PHP Sniffer and Wordpress Coding Standards Checkers from [this instruction](https://github.com/truonglv-eva/coding-rule/blob/master/wp-php-coding-standards-PHP_CodeSniffer.md).
 * Use [Package Control](https://packagecontrol.io/) to search for and install [SublimeLinter](http://www.sublimelinter.com/) then [SublimeLinter-phpcs](https://github.com/SublimeLinter/SublimeLinter-phpcs/).
 * From the command palette, select `Preferences -> Package Settings -> SublimeLinter -> Settings - User` and change `user.linters.phpcs.standard` to the phpcs standard to `WordPress`.

 ![Preferences -> Package Settings -> SublimeLinter -> Settings - User](https://github.com/truonglv-eva/coding-rule/blob/master/images/sublime-php-coding-integration-user-settings.jpg?raw=true)

 * You may need to restart Sublime for these settings to take effect. Error messages appear in the bottom of the editor.
 * Open the file you want to check, right click, choose `SublimeLinter -> Toggle Linter...`, turn `phpcs` to `enabled`
