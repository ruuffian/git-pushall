# pushall.sh

This is a very very simple bash script that I use to simplify my git workflow. Normally when you use git on the
command line, you end up typing out the same three commands over and over-

>git add .
>
>git commit -m ""
>
>git push <branch>

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

If you install with the linux `install` command, you can run pushall the same way you would run any other linux command
like ls or cd- just type pushall into your command line with the correct args and it should work! I am working on some sort of 
argument validation or tab-autocompletion, so I'm not 100% on anything more complicated than this. That's the beauty of shell scripts though-
you can always make them more complicated!
  
### Requirements
  
This requires the pushall.sh file to have execution priviliges, as well as git cli working and installed. Beyond that, there aren't any requirements that I can 
  think of!
