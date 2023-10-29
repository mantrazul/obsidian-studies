
#### Basic Commands

BASH stands for Bourne-Again SHell

That blank screen or window with a prompt and blinking cursor is the command line interface (CLI), where you’re able to enter commands that your computer will run for you. While there’s no need for you to reenact the scene above, working with the command line is a critical skill for you to learn as a developer. The command line is like our base of operations, from which we can launch other programs and interact with them. It has a syntax of its own to learn, but since you’ll be entering the same commands dozens of times, you’ll quickly pick up the commands you need most.

`whoami`
`man bash` - man is for manual, you can do this with most commands
`nano [file]` - text editor to open

When we say, ‘`nano` is a text editor’ we really do mean ‘text’. It can only work with plain character data, not tables, images, or any other human-friendly media. We use it in examples because it is one of the least complex text editors. However, because of this trait, it may not be powerful enough or flexible enough for the work you need to do after this workshop. On Unix systems (such as Linux and macOS), many programmers use [Emacs](https://www.gnu.org/software/emacs/) or [Vim](https://www.vim.org/) (both of which require more time to learn), or a graphical editor such as [Gedit](https://projects.gnome.org/gedit/) or [VScode](https://code.visualstudio.com/). On Windows, you may wish to use [Notepad++](https://notepad-plus-plus.org/). Windows also has a built-in editor called `notepad` that can be run from the command line in the same way as `nano` for the purposes of this lesson.

>[!important]
	>There is not substitute for `vim` the venerable VIM. 
	>You could also use Emacs for particularly large editing tasks.
	
`ls [path]` and `ls -l` (in particular, learn what every column in `ls -l` means), `less`, `head`, `tail` and `tail -f` (or even better, `less +F`), `ln` and `ln -s` (learn the differences and advantages of hard versus soft links), `chown`, `chmod`, `du` (for a quick summary of disk usage: `du -hs *`). For filesystem management, `df`, `mount`, `fdisk`, `mkfs`, `lsblk`. Learn what an inode is (`ls -i` or `df -i`).

`cd [path]` - goes to home directory
`cd -` - goes back from the current folder
`pwd` - print working directory
`touch` / `echo`- creates a file
`mkdir` - creates a directory
`cp [old] [new]` copies a file.
`mkdir [path]` creates a new directory.
`mv [old] [new]` moves (renames) a file or directory.
`rm [path]` removes (deletes) a file.
`*` matches zero or more characters in a filename, so `*.txt` matches all files ending in `.txt`.
`?` matches any single character in a filename, so `?.txt` matches `a.txt` but not `any.txt`.
`.` on its own means ‘the current directory’; `..` means ‘the directory above the current one’.
`man ascii` - ascii table!!

Access files relative to your home directory with the `~` prefix (e.g. `~/.bashrc`). In `sh` scripts refer to the home directory as `$HOME`.
