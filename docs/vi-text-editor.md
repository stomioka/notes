# How to use vi text editor

Good resource: [Colorado State University](https://www.cs.colostate.edu/helpdocs/vi.html)

# To start, save, close

* to start vim
`$ vi` or `$vi sometext.txt`

* to save, go to command line and
`:w` or `:w sometext.txt`

* to overwrite
`:w!`

* to close vim
`:q`

* to force close vim
`:q!`

* save and close vim
`:wq!`

# To move the cursor

* move down one line
`j` or <return>

* move up
`k` or <up-arrow>

* move left/right
`h`/`l` or <left-arrow>/<right-arrow>

* move to the top line
`gg`

* move to the last line
`G`

* move to the last of the line
`$`

* move to the first of the line
`^`

* move to the next word
`w`


# editing
* edit after cursor
`a`

* edit bedore cursor
`i`

* edit from the start if the line
<shift>+i

* add a new line below
`o`

* copy the line
`yy`

* paste the line before the cursor
`P`

* paste the line after the cursor
`p`

* delete the line
`dd`

* delete a character
`d`

* search a word after moving the cursor on the search word
`#`
type `n` to go to the next hit
type`N` to go to the previous hit

* replace a character A to caracter B in lines 10 to 20
g -> replace when 'A' appears multiple times in a line
c -> check each replace
`s:10,20/A/B/gc`
