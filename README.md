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

## Moving quickly

## Moving the cursor

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

## Quick 'on the fly' calculations

* Ctrl+r = 8 * 2 will result in '16' (the calculation result) into the current
  cursor position.
