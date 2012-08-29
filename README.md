Twig Gettext Extractor
======================

The Twig Gettext Extractor is [Poedit](http://www.poedit.net/download.php)
friendly tool which extracts translations from twig templates.

Installation
------------

The recommended way to install Twig Gettext Extractor is [through 
composer](http://getcomposer.org). Just create a `composer.json` file and
run the `composer install` command to install it:

    {
        "minimum-stability": "dev",
        "require": {
            "umpirsky/twig-gettext-extractor": "1.0.*"
        }
    }

Setup
-----

By default, POEdit does not have the ability to parse Twig templates.
This can be resolved by adding an additional parser (Edit > Preferences > Parsers)
with the following options:

- Language: `Twig`
- List of extensions: `*.twig`
- Invocation:
    - Parser command: `<project>/vendor/bin/twig-gettext-extractor --sort-output --force-po -o %o %C %K -L PHP --files %F`
    - An item in keyword list: `-k%k`
    - An item in input file list: `%f`
    - Source code charset: `--from-code=%c`

<img src="http://i.imgur.com/f9px2.png" />

