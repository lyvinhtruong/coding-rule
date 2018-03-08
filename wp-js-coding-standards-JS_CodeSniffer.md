# WordPress Coding Standards for JSCodeSniffer

## Overview
`JSCodeSniffer` is a `node.js` application that checks JavaScript code style consistency according to a provided coding style, just like `phpcs`. One can define a custom coding style by using described below JSON notation or use one of predefined standards.

Reference document: https://github.com/dsheiko/jscodesniffer

## Installation

1. Install NodeJS:
 ```bash
sudo apt-get update
sudo apt-get install nodejs
```

- There are some other ways to install NodeJS in Ubuntu below:

  http://www.hostingadvice.com/how-to/install-nodejs-ubuntu-14-04/

2. Clone `JSCodeSniffer` repository:
 ```bash
git clone https://github.com/dsheiko/jscodesniffer.git
```

## How to use
### Command line

```bash
cd /path/to/your/project/
node /path/to/your/jscodesniffer/jscs.js your-js-file.js --standard=Jquery --report-full
```
Will result in following output:

```bash
 JsCodeSniffer 2.2.2 (https://github.com/dsheiko/jscodesniffer) 

 DETAILED REPORT

 FILE: /home/truongnn/projects/eva-corp/public_html/wp-content/themes/eva2015/js/common.js violates Jquery standard 
------------------------------------------------------------------------------------
 FOUND 213 ERROR(S)
+-----------------------------------------------------------------------------------
 LINE  | COLUMN   | MESSAGE 
+-----------------------------------------------------------------------------------
 64    | 0        | LineSpacing: There must be no line trailing spaces; 4 found 
 69    | 0        | LineSpacing: There must be no line trailing spaces; one found 
 9     | 0        | LineLength: There must be maximum 80 characters of line length; 
       |          | 85 found 
 17    | 0        | LineLength: There must be maximum 80 characters of line length; 
       |          | 82 found 
 18    | 0        | LineLength: There must be maximum 80 characters of line length; 
       |          | 96 found 
 19    | 0        | LineLength: There must be maximum 80 characters of line length; 
       |          | 90 found 
 106   | 0        | LineLength: There must be maximum 80 characters of line length; 
       |          | 88 found 
 9     | 22       | QuoteConventions: Single quotes not allowed for wrapping string 
       |          | literals 
 16    | 22       | QuoteConventions: Single quotes not allowed for wrapping string 
       |          | literals 
 17    | 26       | QuoteConventions: Single quotes not allowed for wrapping string 
       |          | literals 
 24    | 6        | QuoteConventions: Single quotes not allowed for wrapping string 
--------------------------------------------------------------------------------
```

### Usage:
 ```bash
jscs <path> <path>..
<path> - filename or dir to sniff
[--standard=<Standard>] - apply specified standard (Idiomatic, Jquery)
[--report-full] - full report with source codes
[--report-summary] - summary report
[--report=xml] - printing an XML report
[--report=checkstyle] - printing Jenkins-friendly checkstyle report
[--report-file=filePath] - write the report to the specified file path
[--highlight=0] - disable colors on reports
[--mode=silent] - suppress output if no violations found
[--reportWidth=84] - How many columns wide screen reports should be printed
```

### Edit rules set:
#### Set rule to use space indent:
Open file `jscodesniffer/standard/Jquery.js`

Find:
```bash
"Indentation": {
			"allowOnlyTabs": true,
			"allowOnlySpaces": false,
			"ignoreBlockComments": true
		},
```

Replace:
```bash
"Indentation": {
			"allowOnlyTabs": false,
			"allowOnlySpaces": true,
			"ignoreBlockComments": true
		},
```
