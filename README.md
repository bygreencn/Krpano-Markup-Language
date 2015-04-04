#Krpano Markup Language

Package inclides 
* Syntax definition of [krpano](http://krpano.com) panoramic viewer settings(KML) made for [SublimeText 3](http://www.sublimetext.com/3);
* May Thunderstorm color theme for ST optimized to highlight KML code;
* Python Script to remove comments from src.

##Contents

* Installation
* Features
* Modifying

## Installation ##

1. Clone or download this repo into ST User packages folder (Packages -> Browse Packages, then enter User folder);
2. Restart ST if required.

## Features ##

**I.**	Syntax definition is based on [official krpano documentation](http://krpano.com/docu/xml/#top), [plugin](http://krpano.com/plugins/) docs and is intended to recognize all structural entities(e.g. elements, properties or keywords) of KML.

Current list of recognized entities includes:
* Operators (( ) [ ] . , ; == === != !== < > <= >= ! AND OR LT GT LE GE);
* Instruction words (see [Programming logic/Flow control](http://krpano.com/docu/actions/#actionsreference) section of krpano docs);
* Basic functions (all other pre-defined functions);
* [Global Variables](http://krpano.com/docu/actions/#globalvarsreference);
* Named constants;
* Pre-defined [elements](http://krpano.com/docu/xml);
* Pre-defined element properties;
* Action arguments;
* Hex numbers prefixed by 0x or #;
* Decimal numbers including % values;
* Comments following // until the end of the line**(1)**;
* XML tags.

**1. Since comments are not supported niether in actions nor in event handlers they should be removed from source code before execution.**

**II.**	May Thunderstorm is user-defined color theme for ST3 based on [Seti dark color scheme](https://github.com/jesseweed/seti-ui) so it supports any other language.

**III.**	removeComments.py script removes single-line comments from KML source. This operation is required for correct code exec.

At one call comments from one file are removed.

Usage:
	`python script_dir/remove_comments.py src_dir src_file output_dir1 output_dir2`

## Modifying ##
 
See [Syntax Definitions](http://docs.sublimetext.info/en/latest/extensibility/syntaxdefs.html) chapter of ST unofficial manual,
use the same process to modify color scheme.