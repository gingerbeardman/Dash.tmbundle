Dash.tmbundle
=============

This bundle lets you to launch [Dash](http://kapeli.com/dash/) from [TextMate](http://macromates.com) with automatic keyword lookup.

Created by Matt Sephton, [http://www.gingerbeardman.com](http://www.gingerbeardman.com)

## Features
Launches Dash to lookup current word.

_Current word is either the current selection, or the word in which the cursor is currently located._

## Options

You can add the Dash lookup to new languages by adding their scopes using the TextMate bundle editor.  
By default the command is enabled for PHP and JavaScript.

### Internals

The code that does the hard work is as follows:

	if grep <<<${TM_CURRENT_WORD:-!} -Esq '[a-zA-Z0-9_]+' 
	then
		open 'dash://'$TM_CURRENT_WORD
	fi

### Requirements
- TextMate [http://macromates.com](http://macromates.com)
- Dash [http://kapeli.com/dash/](http://kapeli.com/dash/)

### License
Dash.tmbundle is made available under a [Creative Commons Attribution-Share Alike 3.0 Unported License](http://creativecommons.org/licenses/by-sa/3.0).

### Changelog

**2012-07-16**  
- Initial public release  
