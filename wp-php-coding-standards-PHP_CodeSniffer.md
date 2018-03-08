# WordPress Coding Standards for PHP_CodeSniffer

## Overview
This project is a collection of `PHP_CodeSniffer` rules (sniffs) to validate code developed for WordPress. It ensures code quality and adherence to coding conventions, especially the official [WordPress Coding Standards](https://make.wordpress.org/core/handbook/best-practices/coding-standards/).

## Installation

1. Clone `PHP_CodeSniffer` repository:
 ```bash
git clone https://github.com/squizlabs/PHP_CodeSniffer.git phpcs
```

2. Clone WordPress standards repository:
 ```bash
git clone -b master https://github.com/WordPress-Coding-Standards/WordPress-Coding-Standards.git wpcs
```

3. Add path of `wpcs` to `PHP_CodeSniffer` configuration:
 ```bash
phpcs --config-set installed_paths /path/to/wpcs
```

4. Add the `/path/to/your/folder/phpcs/scripts` directory to your `PATH` environment variable via your `.bashrc` or `~/.profile` file.

 Open your `.bashrc` or `.profile` file and input:
 ```bash
export PATH=$PATH:/path/to/your/folder/phpcs/scripts
```

5. Restart your computer

 To check if phpcs work, open command line and type: `phpcs -i` and then you should see `WordPress-Core` listed

## To summarize:
```bash
cd ~/projects
git clone https://github.com/squizlabs/PHP_CodeSniffer.git phpcs
git clone -b master https://github.com/WordPress-Coding-Standards/WordPress-Coding-Standards.git wpcs
cd phpcs
./scripts/phpcs --config-set installed_paths ../wpcs
```

## How to use
### Command line

Run the `phpcs` command line tool on a given file or directory:

```bash
phpcs --standard=WordPress /path/to/your/file.php
```
Will result in following output:

```bash
--------------------------------------------------------------------------------
FOUND 13 ERROR(S) AFFECTING 7 LINE(S)
--------------------------------------------------------------------------------
  1 | ERROR | End of line character is invalid; expected "\n" but found "\r\n"
 22 | ERROR | No space after opening parenthesis of function  prohibited
 22 | ERROR | No space before closing parenthesis of function  prohibited
 26 | ERROR | No space before closing parenthesis of function  prohibited
 31 | ERROR | No space after opening parenthesis of function  prohibited
 31 | ERROR | No space before closing parenthesis of function  prohibited
 31 | ERROR | No space after opening parenthesis of function  prohibited
 31 | ERROR | No space before closing parenthesis of function  prohibited
 34 | ERROR | No space after opening parenthesis of function  prohibited
 34 | ERROR | No space before closing parenthesis of function  prohibited
 55 | ERROR | Detected usage of a non-validated input variable: $_SERVER
 55 | ERROR | Detected usage of a non-sanitized input variable: $_SERVER
 70 | ERROR | String "Create a Configuration File" does not require double
    |       | quotes; use single quotes instead
--------------------------------------------------------------------------------
```

### Edit rules set:
#### Set rule to use space indent:
* Open file `ruleset.xml` in `wpcs/Wordpress-Core/` folder
* Find and replace `Generic.WhiteSpace.DisallowSpaceIndent` into `Generic.WhiteSpace.DisallowTabIndent`

### Editors Integration
* [Sublime Text 3](https://github.com/EvolableAsiaDevelopment/eva-operation-rule/blob/master/php-coding-standards/sublimetext-Integration.md)
* [Netbeans 8](https://github.com/EvolableAsiaDevelopment/eva-operation-rule/blob/master/php-coding-standards/netbeans-integration.md)
