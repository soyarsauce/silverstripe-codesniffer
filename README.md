# SilverStripe Codesniffer ruleset

This is a proposed ruleset for SilverStripe projects.

It tries to follow the official guidelines from
http://doc.silverstripe.org/framework/en/trunk/misc/coding-conventions.

This relies on the PHPCodesniffer being installed

## General Installation

1) First install PHPCodesniffer, check for it's existens via:

     phpcs --version

If it's not installed, the easiest way to install is via PEAR. Instructions
here: http://pear.php.net/package/PHP_CodeSniffer/download

2) Checkout this project somewhere on your hardrive

    git clone git://github.com/stojg/silverstripe-codesniffer.git SilverStripe

**NOTE:** It is critical that the base directory for this standard is named
"SilverStripe", otherwise the PHPCodesniffer autoloader will fail.

## Running the codesniffer

    phpcs --standard=silverstripe-codesniffer/ --tab-width=4  path/to/your/code

NOTE: Beware, running this on a whole silverstripe installation takes to long to
 be worth it. Use it on your mysite module or target specific directories.
 
## Install for Mac OS X

After you have installed PHP Codesniffer via pear, you should have a pear folder in your home directory, example:

     /Users/stig/pear
     
git clone this repository into the PHP Codesniffer standards directory:

     git clone git://github.com/stojg/silverstripe-codesniffer.git /Users/slindqvist/pear/share/pear/PHP/CodeSniffer/Standards/SilverStripe

If you are primary developing SilverStripe projects, you can set a couple of PHP CS settings as default:

     phpcs --config-set default_standard SilverStripe
     phpcs --config-set report_width 120
     phpcs --config-set encoding utf-8
     
With this setup you only need run phpcs like this:

     phpcs cms

## Contribution

Feel free to help me clear up the ruleset and remove / add missing rules and
sniffs. Best way is to see what can be used is to read the sourcecode of the PHPCodesniffer.

