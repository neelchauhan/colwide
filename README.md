# colwide

**colwide** is a [Perl](http://www.perl.org/) script which displays a specified number of a character (default: `#`) on the screen. This may sound useless, but can compliment [tmux](http://tmux.sourceforge.net/) or [GNU screen](http://www.gnu.org/software/screen/).

## Features

And misfeatures!

*   Requires **NO** Perl modules!
*   Ability to print a specified amount of characters if specified as an argument
*   Does not have the ability to change the default hash character (`#`) with an argument
*   Ability to change default values, such as:
*   Default character by changing `$char`
*   Default number of printed characters by changing `$defwidth`
*   Licensed under the Simplified BSD License
*   Has no mechanism to detect terminal size

## Usage

In these usage examples, I assume the following:

*   **colwide** means the script's official name, whereas `colwide` is the filename of the script.
*   `colwide` is downloaded to a location in your shell's `$PATH`.
*   The file in your `$PATH` is called `colwide`.
*   The execute bit (`+x`) is set on the file `colwide`
*   `$char` is set to `#` (default)
*   `$defwidth` is set to `80` (default)

Short usage info: `colwide [**charno**]`, where `**charno**` is the number of characters outputted. Leave blank for the default of 80 characters.

If you run `colwide` with no arguments, and haven't changed `$char` or `$defwidth`, you get 80 hash (`#`) symbols printed to the screen. The output of `colwide` without any arguments is shown below:

	neel@megan:~ % colwide
	################################################################################
	neel@megan:~ % 

If you specify a number as an argument, you override `$defwidth` and get the amount of hash (`#`) symbols you specified. Let's say we run `colwide 40`:

	neel@megan:~ % colwide 40
	########################################
	neel@megan:~ % 

Here, `colwide` has outputted a specified amount of hash (`#`) symbols onto your screen, where in this case, it is 40.

If you specify more characters to `colwide` than the width of your terminal, the characters will overflow, as shown in this example:

	neel@megan:~ % colwide 120
	################################################################################
	########################################
	neel@megan:~ % 

That's really it for the usage information. I don't really have anything else to add here.

## Download

You can download **colwide** from the [neelc.org](http://download.neelc.org/pub/colwide/0.01/) or by cloning this GitHub repository.

If you use [FreeBSD](http://www.freebsd.org/) user (like me!), you also have the option to download **colwide** by install the FreeBSD port [misc/colwide](http://www.freshports.org/misc/colwide).
