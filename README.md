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

 
