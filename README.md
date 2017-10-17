## Purpose

This fork is to keep [huyng/bashmarks](https://github.com/huyng/bashmarks "bashmarks") synchronized with [bachya/bashmarks](https://github.com/bachya/bashmarks). Bachya/bashmarks adds several enhancements, most importantly allowing a prefix to be set for bashmark shell commands - eg upstream will conflict with the shell alias "l" in Ubuntu, so we can now prefix the bashmarks command as "bl".

## Install

1. git clone git://github.com/huyng/bashmarks.git
2. make install
3. add optional [command prefix](#command-prefix)
4. source **~/.local/bin/bashmarks.sh** from within your **~.bash\_profile** or **~/.bashrc** file

## Command Prefix

Because the aliases that Bashmarks uses might already be in use on your system, Bashmarks allows you
to specify a "command prefix":

```bash
export BASHMARKS_PREFIX="bm"
```

If this is specified, the prefix must be used before any Bashmarks command; if it is not specified,
the aliases can be used as-is.
=======
2. cd bashmarks
3. make install
4. source **~/.local/bin/bashmarks.sh** from within your **~.bash\_profile** or **~/.bashrc** file

## Shell Commands

    <command_prefix>s <bookmark_name> - Saves the current directory as "bookmark_name"
    <command_prefix>g <bookmark_name> - Goes (cd) to the directory associated with "bookmark_name"
    <command_prefix>p <bookmark_name> - Prints the directory associated with "bookmark_name"
    <command_prefix>d <bookmark_name> - Deletes the bookmark
    <command_prefix>l                 - Lists all available bookmarks
    
## Example Usage

    $ cd /var/www/
    $ <command_prefix>s webfolder
    $ cd /usr/local/lib/
    $ <command_prefix>s locallib
    $ <command_prefix>l
    $ <command_prefix>g web<tab>
    $ <command_prefix>g webfolder

## Storage
    
All of your directory bookmarks are saved in a file called ".sdirs" in your HOME directory.
