# pushall.sh

This is a very very simple bash script that I use to simplify my git workflow. Normally when you use git on the
command line, you end up typing out the same three commands over and over-
`git add .`
`git commit -m ""`
`git push <branch>`

With `pushall.sh`, you would simply write
`bin/pushall.sh <commit message> <branch>`

This is by no means a perfect solution, as it removes a lot of the functionality that git provides like
adding specific files at a time. But, since most of the time I'm using git for classes or small projects,
it is a fine substitution to replace all three lines.

### Installation

The easiest way I have found to install the script is to write it into a .sh file and then run
`install script.sh ~/bin`
This will give it the correct exec permissions off the bat. There are ways to go crazy with this command, but this
is the method that works for me.

### Use

Right now I use the command by ./'ing it with it's relative directory path. So, if I am in ~/project/folder, I
would call `~/bin/pushall.sh <commit message> <branch>`
