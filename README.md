# vim-cheatsheet

This cheatsheet describes the Vim commands which I find most useful. It doesn't
describe the absolute basics or anything that's particularly advanced but should
be helpful to relative novices which are looking for tips to improve their
productivity.

Please get in touch if anything doesn't make sense.

## Change/Delete 'inner' X

This series of commands allow you to delete or change the a construct and -
having done so - to 'repeat' or 'undo' them.

[c|d]i[w|p|t|"|(|{]

For example:

* d i w 'delete inner word' deletes the word the cursor is on
* c i w 'change inner word' deletes the word and places you in Insert Mode

Having done either of these you can repeat the change at other places in the
document. This also extends to paragraphs, tags (for XML), quotes, parentheses
and brackets.

Note: using W will allow you to change something like a dot separated class
name.

## Copying and moving text

### Copying with :t
* `:29t.` will **copy line 29** to just below the current text (note the
  '.')
* `:t29` will copy the current line to just below line 29

### Moving with :m
* Having made a visual selection `:m26` will move the selection to after line 26

## Moving quickly

### Moving the cursor

Repeated keystrokes are considered an antipattern in Vim. Here are a few ways to
avoid that:

* H M L move to the top, center or bottom of the current view
* 9[h|j|k|l] will move nine lines in the chosen direction
* 9[w|e|b] moves that number of words in the chosen direction
* ^ moves to the first non-blank character on the screen
* * finds the next occurence of the word under the cursor

### Moving the viewport

* Ctrl+[d|u] page the viewport down/up
* Ctrl+[e|y] moves the viewport
* z[z|b|t] moves the viewport so that your current line is at the
  middle/bottom/top of the screen

## Search

Good search features are:

* Having performed a search, hit 'n' to find the next occurence.
* Hitting '*' will find the next occurence of the current word.
  Similarly, hittiing '#' will find the previous.

### Replacing

For replacement I use:

* `:%s/<pattern>/<replacement>/g` - to replace all occurencences of an
  item across all lines. **Note: without the 'g' it'll only do the
first instance on all lines**.
* `5,40s/<pattern>/<replacement>/g` - will replace across the stated
  lines.

## Using tabs

Tabs can be extremely useful when working with multiple files simultaneously.
Here are a few tips for tabs, all of which are ':' commands:

* vim -p file_one.txt, file_two.txt will open the corresponding files within
  tabs. Good for startup.
* Texplore will open file explorer within a new tab
* :tabn [file] will open a new tab (containing the file, if one is passed or an
  empty buffer if not)
* :tabo closes all but the current tab
* gt moves to the next tab, gT to the previous
* :tabdo will run a command (such as search/replace) over all open tabs

## Interacting with the shell
Two very quick ways of interacting with the shell are:

* `:shell` will drop you into a full shell. You can then return to Vim
  by exiting this shell. 
* `:!` allows you to run a single shell command. 

## Quick 'on the fly' calculations

* Ctrl+r = 8 * 2 will result in '16' (the calculation result) into the current
  cursor position.

## Sorting

The `:sort` command provides an easy means of sorting
