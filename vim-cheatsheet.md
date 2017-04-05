My Vim Cheatsheet :wink:
===
Description | command | Further explication
--- | --- | ---
Last Edit |	`‘.`	| apostrophe, period
Suspend Vim | `CTRL Z` |	In Vim
Return to Vim |	`fg` | In terminal (To restart post suspension)
Copy all text |	`:%y+`	| Tells vim to yank all text on the page the ‘+’ copies it to the system clipboard
Select all text |	`ggVG` |	Goes to the top then visual then jumps to the bottom
Page up | 	<C-B>	This moves the page up (by a page) |
Page down |	<C-W>	This moves the page down (by a page) natively this command is <C-F> |
~ |	Toggle  case of the character under the cursor, or all visually-selected characters. |
3~		Toggle | case of the next three characters. |
g~3w		Toggle | case of the next three words. |
g~iw		Toggle | case of the current word (inner word – cursor anywhere in word). |
g~$		Toggle | case of all characters to end of line. |
g~~		Toggle | case of the current line (same as V~). |
U		Uppercase | the visually-selected text. First press v or V then move to select text. If you don't select text, pressing U will undo all changes to the current line. |
gUU		Change | the current line to uppercase (same as VU). |
gUiw		Change | current word to uppercase. |
u		Lowercase | the visually-selected text. If you don't select text, pressing u will undo the last change. |
guu		Change | the current line to lowercase (same as Vu). |
) | 		Jump forward one sentence. |
( | 		Jump backward one sentence. |
} | 		Jump forward one paragraph. |
{ | 		Jump backward one paragraph. |
Just before a character |	`t<char>` |	find a character forward in a line and move un(t)il it (one character before)
:e. 	| Open integrated file explorer	 |
:Sex	| Split  window and open integrated file explorer	 |
"Scroll Upwards"|	`<Ctrl-Y>` |	Scrolls upwards without moving the cursor till page end
High| `H` |	Jumps to top of the page (approx)
Middle | `M`	| Jumps to the middle of the page (approx)
Low	 | `L`	|Jumps  to the bottom of the page (approx) 
Find a character |	`f<char>` |	(f)ind a character forward in a line and move to it
Backwards find |	`F<char>` | (f)ind a character backward in a line and move to it
Backward just before a character	| `T<char>`	| find a character backward in a line and move un(t)il it
Repeat f or t command |	`;`	| repeat last f, t, F, or T command
Repeat f or t command  backwards |`,`|	repeat last f, t, F, or T command, but in opposite direction
`:echo @%	def/my.txt`	| directory/name of file (relative to the current working directory of /abc) |
Close splits |	`<C-W>q`	| This command closes splits one at a time
Save Vim session |`:mksession[!][session name]`|	this command saves open windows and tabs the ! option overwrites existing session and session name can be left blank and will be Session.vim (the session is a vimscript)
Save and close all |	`:wqa`	| Save and quit all
Close vim and all tabs |	`:qa`	| Close all tabs and program
Retrace your movements backwards	|`<C-O>	` |
Retrace your movements backwards	|`<C-I>	` |
paste text in insert mode	 |`<C-R>0	` |
Paste text in insert mode (with sorted indentation) |	`<C-R><C-P>0` |	
delete back one character (backspace)	|`<C-h`>|	
delete back one word	|`<C-w>`|	
delete back to start of line - in insert mode	|`<C-u>` | 	
delete forward to end of line - in insert mode	|`<C-k> 	` |
Scroll downwards	|`<Ctrl-E>`	Scrolls downwards without moving the cursor till page end |
Open  file under cursor	|`gf`|	 open file name under cursor 
Move up and down the page (post search)	| `C-u, C-d` |	move (u)p or (d)own
Move to next instance |	`*` |	go to next instance of word at cursor |
Setting Marks	|`m .. [char]` |	Press M to initialise a mark and the character will be the trigger for the mark |
Using Marks	|``[char] `|	To use a mark use backtick with the character set as the mark
lower case and upper case marks | ```a  … `A``|	a lower case mark (26 can be set) will move you to a point within a buffer/file however an upper case mark will move you between buffers |
Single quote mark	|`‘[char]` |	Hitting a single quote then mark will move you to the beginning of the line where the mark was set |
Mapping	|:map <key> “motion” |	maps a key to a motion |
mode mapping	| `vmap - visual mode, nmap - normal mode, imap - insert mode `|   	Mapping based on the current mode user is in BEWARE - this kind of mapping can lead to recursive mapping especially if there is future unexpected conflict with plugins|
non-recursive mapping	| `inormap, vnoremap, nnoremap` |	These mappings do not take other mappings into account e.g if x is mapped to dd and dd mapped to U a non recursive mapping will stop x from performing U’s function
reselect text	|`gv` | 	Reselect a previously selection portion of text
Replace a word	|`:%s/word/replacement/g` |	Replaces a word searched for and all its instances with the replacement. use a c flag after the g and you will be prompted for each replacement
Scroll down the page	| Ctrl E |	Scrolls down the page, cursor doesn’t move with this
Scroll up the page	| `Ctrl Y` |	Scrolls up the page as above
Minimize all windows/ splits except current	| `:on`	| This command minimises all splits it is short for `:only` has same effect as <C-W> <C-O>
Append at the end	| `A`	| Starts the append command at the end of a line
Insert at the beginning	| `I`	| Starts insert command at the beginning of a line
Change the following |	`C` |	Changes everything following the cursor puts you in insert mode
Delete the following |	`D` |	deletes everything to the end of the line
Delete inside (matching symbol) |	`di`| deletes inside quotes di( parentheses "	the di command represents delete ‘inside’ a particular type of matching symbol
Change/delete all of  word	| `caw / daw` |	changes/deletes an entire word regardless of cursor position in the word
Delete all including parens	| `da{ or da(` | 	Delete everything inside parens including the parens
Yank or change all |	`ya{ or ya( or ca{ or ca (`	| Yank or change everything between parens
Move horizontal window to vertically 	|`Ctrl-w t Ctrl-w H`|	Ctrl-w H moves the current window to full-height at far left
Move Vertical window to horizontally |	`Ctrl-w t Ctrl-w K` |	Ctrl-w t makes the first (topleft) window current  Ctrl-w K   moves the current window to full-width at the very top
Move to beginning of visually highlighted text	| `o`	 | Press o to move to the beginning of visually highlighted text and o to move back to the end
Select a line visually	| `Shift-v or V` |	This selects a whole line regardless of cursor position 
Blockwise selection	| `Ctrl-v` | 	This selects vertically a block of visually highlighted text
Refresh/Reload a file already open in vim	| `:edit` | (no arguments)	
Go to the last place edited	| `g;` |	Moves to the last part of a document that was changed
Compare two files in vim using diff	| :vimdiff [file1][file2]	|
:browse |`e`|	Graphical file explorer	
Open command-line window	| `ctrl-F` |	Opens a command line vim window
In cmd mode - move to beginning	| `ctrl-B` |	cursor to beginning of command-line
In cmd mode - move to end	|`ctrl-E` |	Move cursor to end of command-line
In cmd mode - delete word under cursor	| `ctrl-W` |	delete the word before the cursor
In cmd mode - remove between cursor and beginning	|`ctrl-U` |	remove all characters between the cursor position and the beginning of the line
Add a file’s contents into another	| `:read [desired_file]` |	Places all the contents of a file into the currently opened buffer
Deletes a lines content but not the line	| `S`	| NB: this keeps the line only deletes the text
Delete everything beyond the cursor |	`D` |	
Changes everything before the cursor |	`C`	 |
Multiline insertion	|`<C-V>I`|	"Use block wise selection to highlight where to insert text then I inserts across all select line NB “i” is used here to select specific objects within the visually selected area"
Write and quit|	`:x or :wq`|	Saves file and quits vim
Finds the word under the cursor |	`* #, g* g#` 	 | find word under cursor (forwards/backwards), append g to find the word backwards
`:echo expand('%:t')	my.txt`	|name of file ('tail')|
`:echo expand('%:p')	/abc/def/my.txt`	|full path|
`:echo expand('%:p:h')	/abc/def`	|	directory containing file ('head')|
`:set timeoutlen`	|	Can be used to set duration of timeout for the leader key |
`:bufdo! bw`	|	deletes all buffers except those with unwritten changes |
`:bufdo! bw`	|	deletes all buffers, no error on any unwritten changes |
`/search … N` |	`N` |	search backwards once search pattern has been input
``/search … c`|	`c` |	Accept search result at cursor position |
`:bw` |        		deletes the current buffer, errors if there are unwritten changes |
`:bw!` | 		deletes the current buffer, no error if unwritten changes |
`:bufdo  bw` |		deletes all buffers, stops at first error (unwritten changes) |
