# pushall

This is a very very simple bash script that I use to simplify my git workflow. Normally when you use git on the
command line, you end up typing out the same three commands over and over-

>git add .
>
>git commit -m ""
>
>git push <branch>

With `pushall`, you would simply write

`pushall <commit message> <branch>`

This is by no means a perfect solution, as it removes a lot of the functionality that git provides like
adding specific files at a time. But, since most of the time I'm using git for classes or small projects,
it is a fine substitution to replace all three lines.

### Installation

The easiest way I have found to install the script is to write it into a .sh file and then run

`install pushall.sh ~/bin`

This will give it the correct exec permissions off the bat. There are ways to go crazy with this command, but this
is the method that works for me. I prefer to remove the .sh extension once I am ready to install, so that I can call it with just `pushall` rather than `pushall.sh`.
Either way, file extensions dont matter to linux so you can call it whatever you want.

### Use

If you install with the linux `install` command, you can run pushall the same way you would run any other linux command
like ls or cd- just type pushall into your command line with the correct args and it should work! I did a little bit of research and implemented some very basic 
argument validation. Right now the script takes 1 or 2 arguments, and changes behavior based on those inputs.
  
### Requirements
  
This requires the pushall.sh file to have execution priviliges, as well as git cli working and installed. Beyond that, there aren't any installation requirements that I can 
think of! Do keep in mind, since this script uses && to sequentially execute the git commands, it will execute them synchronously. This means that if one of them fails,
the ones before it are still executed. So, if you commit your changes and then try to use pushall, it will fail at the commit step (nothing to commit) and not execute the push command.
  

### Argument Validation

The argument validation is here to make sure the remote repo does not become out-of-sync with the local repo. It basically just fails if you input <1 or >2 arguments,
since you need a commit message but not necessarily a branch to push to (if you have defualt pushing behavior setup correctly. 

Note: If you are writing your own shell script, it can be helpful to name it with the .sh file extension up until you install it. This way, while writing you get syntax highlithing from text editors like vim.
