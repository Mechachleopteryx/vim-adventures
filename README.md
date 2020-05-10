# vim-adventures
solutions to puzzles in Vim Adventures

---

### Readme
[Vim Adventures](http://vim-adventures.com/) is an excellent educational game by Doron Linder.  It focuses on teaching many popular commands and motions used in the [Vim](http://www.vim.org/) text editor.  Here are a few disclaimers: 
- My solutions may not be the only way, and may not even be the optimal way to solve the puzzles.
- I strongly suggest you attempt all levels on your own before turning to the following spoilers.

---

### Levels
#### Level 8
- last puzzle: 
   - start on first twin brother, `j  #  E  #  n  n  ^  k  $  *  j  j`, end on second brother

#### Level 9
- puzzle to the right: 
   - start on 'N' `$  j  j  j` end on 'd', get key
   - to go back, start on 'd' `gg`
- use key to enter house and get ability to use all numbers
- puzzle below the house (with 11 key presses):
   - start on 'n', which is numbered with a red '1'
   - you should visit the blocks in numerical order
   - `4j` → `b` → `2k` → `3w` → `4$` → `Tu`, you are now at the space on the other side
   - the key has appeared at the beginning of this puzzle, lets go back to get it
   - starting at the space, `5G` → `to` → `4k` 
   - now we have the key and can go back again to the bottom side of this puzzle, using the original way we came
- puzzle down and to the right of the last puzzle (with 8 key presses):
   - start on the 'f', which is numbered with a red '1', and we will again go in numerical order
   - `fi` → `3*` → `Fu` → `2*`
   - we are now at the other side on the 's' of 'sum', follow the path down to the '.' on the morse code looking puzzle
- morse code puzzle (spells out 'VIM ADVENTURES' in morse code):
   - `3e` gets directly to the other side
   - go down to lolcat sounding puzzle
- lolcat puzzle (16 key presses)
   - starting on 'W', `3x  ~  j  5~  5j  d4j  fC  2rG`
   - the key appears at the beginning of the puzzle, `6k` to go back up to get it
   - go back up through the morse code puzzle, `3e  k  5f.`
   - starting on 's' of 'sum', go back through this puzzle, `2G`
   - go left to '.' of next puzzle
- puzzle left of pink haired girl in bush (4 key presses)
   - starting on '.', `16b` (probably not the best answer to this puzzle)
   - go up to puzzle with a whole lot of numbers (actually just one number, Pi, to a whole lot of decimal places)
- Pi number puzzle (7 key presses)
   - start on '8', `9G  2f8  4k`, end on broken '5' tile
   - key appears on last '8', get there with `11G  6l  4j  3l`, we now have 3 keys
   - and back to the start of the puzzle with `3h`
   - go down to previous puzzle on 'k'
- puzzle below Pi puzzle (4 key presses)
   - start on 'k' of 'keep', `3$` to get to '.' on right side
   - `l h` to exit and re-enter puzzle from right side
   - `b Fa` to end on the 'a' above the locked gate
   - go down, unlock gate, and go to next puzzle
- deleting puzzle
   - go to start of 'not so ' → `d2w`
   - go to start of 'e22' → `3x`
   - go to start of '(C) Writes serverd ''s' → `d3W x`
   - go to start of 'XOOOO XOOOOO O' → `d2fX`
   - go to start of 'word1 w2 word1 w2 ''1' → `d4W x`
   - go to start of `bye bye` → `d2fe`
   - grab the new key (have 3 keys again)
   - go down and use all keys to open three locked gates to end of level

#### Level 10
- paste puzzle
   - go down and grab the 'p' command
   - delete a word with the red box around it, starting with cursor on first letter of that word
      - 'you' → `dw`
      - 'delet' → `5x`
      - 'real' → `4x`
   - paste those deleted words from the buffer, to where the corresponding purple bubbles show
      - 'P' for pasting before cursor, 'p' for pasting after cursor
   - grab the key after you pasted the correct word for each purple bubble
   - move to the 't' and use `x` to save it to the register for the next puzzle
   - go down and open locked gate
   - go to the right
- t puzzle
   - "Betty bought a bit of butter"
   - paste that 't' using `p` in all the spots that it indicates
   - `l 2""p 2e p 2e pte te 2p`
   - go left and down to the line delete puzzle below the house
- line delete puzzle below the house (7 key presses)
![The wheels on the bus.](https://github.com/Mechachleopteryx/vim-adventures/blob/master/the%20wheels%20on%20the%20bus.png)
   - start on 'd' of 'round', `j  dj  k  P  G  P`
   - grab the '"' register specification
   - go up to the house and save the 't' character into another register (such as "a) `"ax`
   - go down, right, and up to the 't and x puzzle' above the 't puzzle'
- t and x puzzle (7 key presses)
   - start and red boxed 'x'
   - `"x  gg  $  "ap` (the `"ap` pastes from the "a register, if that is where you saved 't' to)
   - a key has appeared, `3j  2Fl` to get it
   - go down, right, and down to the 'tweedle beetle puzzle'
- tweedle beetle puzzle (98 key presses)
   - start on 3rd 'e' of 'beetles' → `3j 2b "adw "bdw  b  "Bdt (space) j "Adw "Adw k "aP j "bP`
   - a small brown key appears, grab it
   - go back to the house at the beginning and use the small brown key on the chest
   - the chest gives you the 'y' yank operator
   - go back to the 'tweedle beetle puzzle' and head down to the 'one ring puzzle'
- one ring puzzle
   - go to start of 'One ring to ' → `3yw` to yank the text
   - paste where the two purple bubbles tell you to, using 'p' or 'P'
   - key appears, grab it (now you have 2)
   - go down to 'Hip, Hip, Hooray! puzzle'
- Hip, Hip, Hooray! puzzle
   - delete the two red boxed lines using `dd` on each
   - move to the 'Hip, Hip, Hooray!' line and yank it using `yy`
   - paste it where the purple bubbles are → `2P  3j  3p`
   - key appears, grab it (you now have 3)
   - go all the way back to the house at the beginning, and go down to the 'Delete me! puzzle'
- Delete me! puzzle (7 key presses)
   - start on 't' of 'Delete' → `G  dd  dd  dd`
   - go down to '99 bottles puzzle'
- 99 bottles puzzle (15 key presses)
   - check `:reg` to see which registers you will need to use for pasting the text from
   - start on 'h' of 'the' → `"0P  j  "0p  j  p  j  "2p`
   - go down to next, and last puzzle
- last puzzle
   - check `:reg` to see which text you have saved to registers
   - you need the following lines of text saved to registers:
      - 'Betty rules'
      - 'tweedle beetle'
      - 'on the wall'
      - 'One Ring'
   - go back to the previous puzzles and save each to a different register using yank
      - I saved each, in order, from registers a-d, starting on the first character of each phrase:
         - 'Betty rules' → `"ayw` for 'Betty ' + `"Aye` for 'rule' + `"Ay$` for 's' (on the last 's' of 'darkness', because it was the last character on the line)
         - 'tweedle beetle' → `"b2ye` for 'tweedle beetle'
         - 'on the wall' → `"c3ye` for 'on the wall'
         - 'One Ring' → `"d2ye` for 'One Ring'
   - go back to this puzzle and past the phrases in the right spot, using the right registers
      - for me, starting on the first space → `"aP  6l  "bP  l  "cp  $  "dp`
   - a new island appears, follow the path left and up and unlock the 3 gates to the end of the level

#### Level 11
- go down to miracle puzzle
- miracle puzzle (15 key presses)
   - yank 'you' with `ye`
   - leave puzzle and re-enter on 'r' of 'rush' → `P  b  ~  3w  yw  j  w  P  rs`
   - grab 'c' change operator
   - go down to change puzzle
- change puzzle (44 key presses)
   - start on 'C' of 'Ctrl+1,' → `3CEsc<Esc>  j  CInsert mode<Esc>  G  w  cwreturn to<Esc>  2w  c2wmode<Esc>`
   - go down to second change puzzle
- second change puzzle
   - edit each of the following red boxes, starting on the first letter of each box:
      - 'terrible ' → `dw`
      - 'deleting' → `cwediting<Esc>`
      - '!' → `r?`
      - 'ctrl' → `cwBackspace<Esc>`
      - 'Shift' → `cwDelete<Esc>`
      - last line → `ccto fix it.<Esc>`
   - grab the 's' substitute command
   - go back to the start of the level (at the top) and go right to the Gandalf puzzle
- Gandalf puzzle (8 key presses)
   - start on 'G' of 'Grey.' → `* CWhite<Esc>`
   - go right to another editing puzzle
- editing puzzle
   - edit each of the following red boxes, starting on the first letter of each box:
      - 'i' → `x`
      - 'it' → `2x`
      - 'vegetarian dinosaurs,' → `Slocal fisherman,<Esc>`
      - 'fl' → `2sn<Esc>`
      - 'volcanic lava!' → `Swaters...<Esc>`
   - `:ls` to view buffers, we are going to the ground → `:b1`
   - go up to first ground puzzle
- first ground puzzle
   - edit each of the following red boxes, starting on the first letter of each box:
      - 'hat' → `3x`
      - 'p' → `rs`
      - 'i' → `swa<Esc>`
      - 'cookies' → `cwchocolates<Esc>`
      - 'always' → `cwnever`
      - 't' → `rw`
      - 'o nuts' → `c2wet<Esc>`
   - grab the blue key
   - go right, and down to second ground puzzle
- second ground puzzle (20 key presses)
   - start on the '8' → `w  s15<Esc>  w  cw16<Esc>  3l  x  w  4C42<Esc>`  
   - grab the small brown key
   - `:ls` to view buffers, we are going to the sky → `:b2`
   - use blue key to open the blue door
   - use the small brown key to open the chest, get the 'i' insert command
   - go left to beginning of level, and then all the way down to the 'Watson puzzle'
- Watson puzzle (6 key presses)
   - `IElem<Esc>`
   - go right to next sky insert puzzle
- sky insert puzzle (33 key presses)
   - start on 'Y' of 'You've' → `W  igot<space><Esc>  j  Iyourself<space><Esc>  G  iWell<Esc>  k  l  iI<space><Esc>`
   - grab the 'a' append command
   - `:ls` to view buffers, we are going to the ground → `:b1`
   - go up to the Hakuna Matata puzzle
- Hakuna Matata puzzle
   - start on 'H' of 'Hakuna' → `Y  gg  P  j  p  6l  k  awonderful<Esc>  Ta  2j  ino<Esc>  h  2j  ano<Esc>  0  iIt<Esc>  h  2j  iIt<Esc>  $  aphilosophy<Esc>
   - grab the blue key
   - `:ls` to view buffers, we are going to the sky → `:b2`
   - open blue door
   - grab the 'o' open command
   - go back all the way left and up a bit and left to the 'D'oh' puzzle
- D'oh puzzle (4 key presses)
   - `5A!<Esc>`
   - go right to the big edit puzzle
- big edit puzzle
   - edit each of the following red boxes, starting on the first letter of each box:
      - 'mally' → `ce instance,<Esc>`
      - 'e' → `~`
      - 'was far less smart' → `Swas more intelligent<Esc>`
      - 'lousy' → `cwgood<Esc>`
   - fill in what the purple bubbles tell you to, using `a` and `i` and `o`
   - `:ls` to view buffers, we are going to the ground → `:b1`
   - go up to 'beat it puzzle'
- beat it puzzle (20 key presses)
   - start on 'N' of 'No' → `4OBeat it<Esc>  gg  ~  IJust <Esc>`
   - go down to puzzle below arrow island
- puzzle below arrow island (33 key presses)
   - start on first line → `OYou mean<Esc>  j  oall I had<Esc>  G  Oclick my<Esc>`
   - go across the bridge to arrow island
- arrow island 
   - start at 'O' of 'Open' → `cw:e<Esc>  w  cWundeground<Esc>`
   - grab the red key
   - type `:e underground`
   - open red gate, go down to underground puzzle
- underground puzzle (20 key presses)
   - start on 'o' of 'You' → `w  cwSHALL<Esc>  l  p  4l  cw!<Esc>  3h  p`
   - talk to the princess to finish the level

#### Level 12
- puzzle with d, j, and 5W bugs
   - kill the three bugs
      - d → `dd` when it is in the same line as you
      - j → `yj` when it is below you
      - 5W → `d5W` when you are within 5 WORDS away
   - get '( )' motions for navigating sentences
- puzzle with gg, G, (, ), *, and # bugs
   - kill the 6 bugs
      - gg → `dgg` when it is anywhere above you
      - G → `dG` when it is anywhere below you
      - ( → `d(` when it is within the previous sentence
      - ) → `d)` when it is within the next sentence
      - * → `d*` when it is anywhere above you
      - # → `d#` when it is anywhere above you
   - get the '[{, [(, ]), and ]}' motions for finding unmatched braces and parenthesis
- puzzle with t and ^ bugs
   - kill the 2 bugs
      - t → `dt!` when it is to the right of you on the bottom line of it's puzzle
      - ^ → `d^` when it is to the left of you on same line
   - get '{ }' motions for navigating paragraphs
- puzzle with {, }, T, F, and $ bugs
   - kill the 5 bugs
      - } → `d}` when it is forward within the same paragraph as you, you move to end of paragraph
      - { → `d{` when it is backward within the same paragraph as you
      - T → `dTT` when you are on the top line of it's puzzle, and it is to your left
      - F → get to right side of puzzle, and `dF<character bug is on>`
      - $ → `d$` when it is to the right of the cursor, on the same line
   - get small brown key
   - go right and down to paragraph puzzle
- paragraph puzzle
   - start on '*' → `}` to jump paragraph to the space, and `}` again to kill the bug
   - `2$  ]}` to kill the ']}' bug
   - kill 3 and F bugs → `dFp` and `d3B` work nicely if you are on the end of the top line
   - kill the k and l bugs → `dk` works if you are on the last '}', and `d<some number>l` 
   - chest appears, open it to get 'ia' text objects
   - back to beginning and down and to the left to numbered puzzle
- numbered puzzle (8 key presses)
   - `)` → `2)` → `(` → `2)` → `)`
   - go down to '7' → `])`
   - go down to next bug puzzle
- bug puzzle
   - kill bugs:
      - 2[ → `d2[{`
      - 3] → `d3]}`
   - grab key
   - go way back, up and right, and open door with new key
   - go left to text object puzzle
- text object puzzle
   - kill bugs:
      - a( → `da(` within a () block
      - i( → `di(` within a () block
      - a[ → `da[` within it's [] block
      - ap → `dap`
      - 2a} → `d2a}`
      - a{ → `da{`
   - change text, start at first character:
      - '[0,1,2,3]' → `ca[endl<Esc>`
      - '(i+3)/(j-23)' → `c2i(i+1)*(j+1)<Esc>`
   - grab the red key
   - go up and to the right to the hello world puzzle
- hello word puzzle 
   - kill bugs:
      - a → from top `d3ap` will delete the bug because it is within the next three paragraphs
      - ) → from top `d4)`
      - i( → `G` to get to the bottom, then `4k` to get within the '( )' pair, then `di(`
      - % → `d%`
   - go back to top with `gg`, time to edit
   - `W  2j  ci<head<Esc>  j  c2a[<script><Esc>  4j  ci{<Space><Space>alert('Hello World!');<Esc>`
   - `G` to get the blue key
   - go back to near the beginning, and open blue door
   - go up to yoda puzzle
- yoda puzzle
   - kill bugs:
      - three a" bugs → `gg` to top of text, `da"` on each line that a bug is on
      - i" → `di"` on same line as bug
   - edit text → `gg  ci"No!<Esc>  4G  ci'do not.<Esc>`
   - grab the second red key
   - go open the first red key gate on the right
   - go down to right red gate puzzle
- right red key puzzle
   - use `i` and `a` to add in the words requested by the purple bubbles
      - starting on 'I' of 'In' → `fh  3j  "ayl  3k  "Ayw  2j  P  k  p  b  j  b  j  P  3w  j  "cy2aw  5j  yiw  5w  P  3h  6j  "cp  3e  "cp`
      - grab the '.' repeat command
      - go back and open the left red door, and head down to the left red key puzzle
- left red key puzzle
   - kill bugs while standing at start of puzzle on 'r' of 'her':
      - s → `das`
      - i → `dis`
   - edit text → `dap` while on 'r' of 'her'
   - go down to function puzzle
- function puzzle (23 key presses)
   - start on 'u' of 'function' → `%  di(  B  2j  ciwisOver<Esc>  2j  .  3j  .`
   - grab the blue key
   - move down to the fizz buzz puzzle
- fizz buzz puzzle (42 key presses)
   - `$  cwBuzz<Esc>  6w  .  2b  cwFizz<Esc>  7b  .  4w  .  7w  .  3w  cwFizzBuzz<Esc>`
   - go left to little indians puzzle
- little indians puzzle (53 key presses)
   - `6B  *  ciwIndians<Esc>  n  .  2n  .  n  3.  n  .  2n  .  n  c5iwIndian boy<Esc>  n  .  as<Esc>`
   - go down, open blue gate
   - talk to princess to finish level, and move on to level 14 (not 13)

#### Level 14
- all motions are gone!
- `yip` to get 'H' high motion
- `H` and use `zb` to get the 'L' low motion
- `L` and use `zt` repeatedly to scroll down and get the '1-9' counts back
- `:47<Enter>  6L` to get the 'nu' and 'nonu' boolean options
- `:set nu` to turn line numbers on
- use a count + `H`, with the help of line numbers, to go up and get the 'M' middle motion
- `:reg` to view the registers, and find out that the next directions are in the ground buffer
   - `:ls` to view buffers → `:b1` to go to ground to view hints for the lorem buffer
   - `:ls` to view buffers → `:b4` to go back to the lorem buffer
- hints from ground buffer, for lorem buffer, lead to:
   1. `:41<Enter>` to uncover the '|' pipe motion in the bush
   2. `:33<Enter>  39|` to get the '/ ?' search motion
   3. `:11<Enter>  47|` to get the '`' mark motion
   4. `:52<Enter>  4?pro` which leads to the 'pro' on line 37, `68|` is the space right before the 'pro', which has a portal (we'll return to this later) 
- `:43<Enter>  10|` to get to the blinking white cursor (Mr. White)
   - talk to Mr. White to learn about marks
   - learn that we had a plan to kill Big Bug, before we lost our memory
- `:4<Enter>  55|` to get to Mr. Blue
   - learn how to teleport to global marks (`` `<global mark name> ``, eg: `` `L ``)
   - learn Mr. Pink couldn't control himself and almost changed colour (interesting), and that's why the plan to kill Big Bug failed
- `:50<Enter>  64|` to get to Mr. Pink
   - learn how to list marks (`:marks`) and how to delete them (`:delm`)
   - continue to not forgive Mr. Pink, until he loses his temper and turns into Mr. Red
   - talk to Mr. Red to learn about Big Bug and how to destroy him (text in the sky tells where to place marks in the underground)
- `:ls` to view buffers → `:b2` to go to sky buffer
- `` `W `` to go to the W mark puzzle
- W mark puzzle
   - `:4<Enter>  13|  d18aw` → `:1<Enter>  9|  d/clever<Enter>`
   - `:2<Enter>  5|` to grab 'CTRL-R' redo command
   - go to H mark puzzle
- H mark puzzle (13 key presses)
   - `:delm!  :4<Enter>  30|`
   - `?'` to grab the single quote jump to mark line motion
   - go to the A mark puzzle by using `'A` (that is the single quote, not backtick)
- A mark puzzle (7 key presses)
   - `d'A` to kill bugs on top line, and `.` to repeat command → kill all bugs
   - `2/m<Enter>` to get the 'm' set mark command
   - go to the D mark puzzle
- D mark puzzle (29 key presses)
   - `:delm<Space>Dthe<Enter>  2|  mo  ?<Space>o<Enter>  mM  ?<Enter>  my  ?<Enter>  me`
   - `:7  7|` to grab the yellow star
   - lets take that star to the yellow star portal that we found in the Lorem buffer:
      - `:b4` to get to the Lorem buffer
      - `:37  68|` to get to the star portal
      - it teleports us to the B mark puzzle
- B mark puzzle
   - `mB  16|  mg  :2  mi  14|  mu`
   - a chest appears on the x, but we don't have the key yet
   - `:reg<Enter>` and notice the message on the "y register:
      - go to `` `W `` and then go to `` `Y ``, but don't skip the scrolling
      - we can see the hint 'Toadstool (Peach is also interesting...)'
      - go to the P mark puzzle
- P mark puzzle
   - `:marks` to view the marks and their associated text
   - remember our hint from the WY mark scrolling → Toadstool, Peach → lets view these words as marks:
      - `:marks Toadstool<Enter>` → this shows the marks in alphabetical order, and reveals a message → The power of undo will beat Big Bug
      - the brown key is also revealed, get it with `:5<Enter>`
      - `:marks Peach<Enter>` → also reveals a message → The cursors are NOT friends!
      - lets go back to the B mark and open the brown chest → `` `B  9|`` to get the 'u' command
      - all previous motions and commands are now restored!
      - go to the U mark puzzle
- U mark puzzle 
   - `CTRL-R` → the words 'Uganda', 'Bram', and 'Charity' are to remember
   - `:ls` to view buffers → `:b3` to go to underground buffer and start the underground mark puzzle
- underground mark puzzle
   - `:9<Enter>  mB` to set B mark, `31|  mg to set g mark`
   - `:2  mi` to set i mark
   - `:17  mu` to set u mark
   - time to fight Big Bug and his three minions (formerly cursors)!
- Big Bug fight
   - search for 'Uganda', 'Bram', and 'Charity' to kill the smaller bugs (those are their hidden names)
      - eg: `?Uganda<Enter>` or `/Uganda<Enter>`  
      - you can repeat searches in the underground buffer with `/<Enter>` and `?<Enter>`
      - big bug moves fast so using repeated searches is very helpful
      - moving between the corners with gg and G$ will give you the most time to run the search commands before big bug gets to you 
      - when you kill one, it won't come back, so keep going back to the underground buffer until you kill all three, then focus on Big Bug
   - to hurt Big Bug you must use undo (`u`) and redo (`CTRL-R`), which will cause a lightning strike where edits were made
      - type `99u` and `99<CTRL-R>` to do lots of damage at once
      - if you die, Big Bug regains health, so you must be quick and use motions like `gg`, `G`, `0`, and `$` to dodge around
      - you can spam `{` and `}` to go from corner to corner
      - this will force him to cross edited text when he scrapes along the top and bottom of the screen for easy damage
      - take Big Bug's health to zero, and he will die
   - Congratulations!  `<CTRL-R>` repeatedly to redo all the changes, and then the final cutscene will happen
- THE END!
   

